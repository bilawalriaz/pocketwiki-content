# Paxos (computer science)

Paxos is a family of protocols that get a group of unreliable computers to agree on a single value, called *consensus*. It is the standard building block for replicating a service across machines: every replica runs the same state machine, and Paxos ensures they process the same sequence of commands, so the group stays consistent even when individual machines crash or messages are lost. Leslie Lamport first submitted the protocol in 1989 and published it in 1998, naming it after a fictional legislature on the Greek island of Paxos whose members wandered in and out but still had to pass laws.

## The safety-liveness tradeoff

The Fischer-Lynch-Paterson (FLP) result shows that no deterministic consensus protocol can guarantee progress in a purely asynchronous network when even one process may fail. A consensus protocol can have at most two of three properties: safety, liveness, and fault tolerance. Paxos chooses safety and fault tolerance. Replicas never disagree, but progress can stall under adversarial timing; the conditions that cause a stall are hard to provoke in practice.

## Assumptions and processor count

Processors run at arbitrary speed and may crash and recover if they keep stable storage. The network can delay, drop, duplicate, and reorder messages but cannot corrupt them. Processes do not lie or collude; Byzantine Paxos relaxes that assumption. To tolerate F simultaneous crashes, Paxos needs at least 2F+1 processors, because non-faulty processes must outnumber faulty ones. Reconfiguration can extend this so that arbitrarily many total failures are survivable, as long as no more than F happen at once.

## The protocol

A single decision, called an *instance*, runs in two phases. Each process plays one or more of three roles: **Proposer** (suggests values), **Acceptor** (votes on values), and **Learner** (discovers the chosen value).

**Phase 1a (Prepare).** A Proposer picks a unique number *n*, higher than any it has used before, and sends a Prepare message with *n* to a *quorum* (majority) of Acceptors.

**Phase 1b (Promise).** Each Acceptor compares *n* with every proposal number it has seen. If *n* is higher than all previous ones, the Acceptor promises to ignore any future proposal numbered ≤ *n* and replies with the highest-numbered value it has already accepted, if any. If *n* is too low, the Acceptor may ignore the message or send a negative acknowledgement (NAK).

**Phase 2a (Accept).** Once the Proposer collects Promises from a quorum, it sets the value to propose. If any Acceptor reported an already-accepted value, the Proposer must reuse the value attached to the *highest* reported proposal number, never its own choice. This rule forces any new leader to inherit whatever the cluster had previously agreed on. The Proposer then sends an Accept message carrying (*n*, *v*) to a quorum of Acceptors.

**Phase 2b (Accepted).** An Acceptor accepts the message only if it has not promised to ignore proposals numbered ≥ *n*. It registers *v* as accepted and notifies the Proposer and the Learners.

Consensus is decided once a majority of Acceptors have accepted the same proposal number. Because each number is unique and carries exactly one value, agreement on a number implies agreement on a value. Learners learn the result only after hearing from a majority, not from the first reply.

## Counter-intuitive properties

Because the protocol tracks proposal numbers, not values, three things happen that look wrong but are correct: Acceptors may accept multiple different values over time, a value can briefly hold a numerical majority and then be superseded, and Acceptors may keep accepting after a value is chosen. Once a value reaches a majority, it is final and immutable, and no future Proposer can change it. Rounds fail when Proposers race with conflicting Prepares or when a Proposer cannot gather a quorum; recovery is to start a new round with a higher proposal number.

## Multi-Paxos

Replicating a database requires a continuous stream of decisions. Running Basic Paxos for every command repeats Phase 1 unnecessarily. If the leader is stable, Multi-Paxos runs one Phase 1 and then issues Accept! messages for each new command with an incrementing instance number *I*, cutting the message delay from four steps to two. In typical deployments the three roles collapse into one server role, giving a client-server architecture familiar from replicated databases.

## Variants

**Cheap Paxos** tolerates F failures with F+1 main processors plus F auxiliary ones, reconfiguring after each failure. The auxiliaries stay idle during normal operation and can be small or shared, at the cost of halting if too many main processors fail in quick succession.

**Fast Paxos** lets the client send its proposal directly to the Acceptors, reaching a decision in two message delays. It needs 3F+1 Acceptors instead of 2F+1, and on collision the leader coordinates recovery, adding delays. **Generalized Paxos** exploits the fact that some commands commute: a read of one register and a write to another can both be accepted without conflict, so collisions are avoided. When conflicts do arise, recovery takes two extra round trips.

**Byzantine Paxos** tolerates arbitrary, malicious behaviour. Castro and Liskov add a Verify message so Acceptors cross-check each other, and Learners wait for F+1 matching replies before trusting a value. **Fast Byzantine Paxos** lets the client send directly to the Acceptors and broadcasts every Accepted message across all Acceptors and Learners so the group can detect a faulty Acceptor and re-broadcast the correct value.

## Hardware and production use

Modern datacenter networks offer remote direct memory access (RDMA), where the network card handles transport. The open-source Derecho C++ library adapts Paxos to sustain full RDMA bandwidth by streaming data asynchronously off the leader's critical path, offering both durable Paxos and vertical Paxos for in-memory replication.

Paxos runs inside Chubby, Spanner, Megastore, and Bigtable at Google; in Windows Server Failover Clustering and Bing's Autopilot at Microsoft; in IBM's SAN Volume Controller; in WANdisco's DConE, XtreemFS, Heroku's Doozerd, Ceph monitors, MariaDB Xpand, Neo4j HA, Cassandra and ScyllaDB lightweight transactions, Amazon's Elastic Container Services, and DynamoDB's leader election.

Source: adapted from "Paxos (computer science)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Paxos_%28computer_science%29
