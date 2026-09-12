# Consensus (computer science)

In any distributed system, separate processes must sometimes agree on a single value even though some of them may crash, lie, or delay their messages. That agreement problem is called **consensus**, and it sits underneath almost every reliable distributed service: committing a database transaction in order, replicating a state machine, broadcasting a message atomically, keeping clocks in sync, balancing load, coordinating robots, and maintaining a blockchain.

## The problem

Each process starts with a candidate value. After exchanging messages, every non-faulty process must output the same value, and that value must be one that some process actually proposed. A protocol that can do this when up to `t` of `n` processes fail is called **t-resilient**. To rule out the trivial solution where every process just outputs 1, the output is required to be the input of some process. Once a process has decided, that decision is final.

Three properties define a correct consensus protocol:

- **Termination** — every correct process eventually decides.
- **Agreement** — all correct processes decide the same value.
- **Integrity** — if all correct processes proposed the same value `v`, then any correct process must decide `v`.

A separate condition called **validity** appears in some literature: a message sent by a correct process is eventually delivered to its intended receivers. Performance is measured by the number of communication rounds (running time) and the total message traffic (message complexity).

## What "faulty" can mean

A process can fail in two ways. A **crash failure** simply stops it. A **Byzantine failure** is worse: the process may send conflicting information to different peers, sleep for a long time, or behave maliciously under an adversary's control. Protocols that tolerate Byzantine failures must therefore be resilient against every possible misbehaviour, and Byzantine-tolerant consensus has to strengthen the integrity rule so that the decided value must come from a correct process, not from a faulty one.

## Channels, models, and synchrony

Whether messages carry proof of origin matters. In the **oral** model, receivers only know the immediate sender. In the **written** model, every message is digitally signed, so a receiver can trace its full history. Written-message protocols tolerate many more failures than oral-message ones.

In **synchronous** systems, communication proceeds in lockstep rounds: every message sent in round `r` is received before round `r+1` begins. In **asynchronous** systems, no such bound exists, and messages may be arbitrarily delayed. The 1985 **FLP impossibility result**, proved by Fischer, Lynch, and Paterson, showed that in a fully asynchronous system where even one process may crash, no deterministic algorithm can always reach consensus in bounded time. Randomized algorithms can circumvent FLP by achieving both safety and liveness with overwhelming probability, and in practice consensus is reached; the result only rules out a worst-case deterministic guarantee.

## A solvable example: the Phase King algorithm

For synchronous systems with Byzantine failures, the Phase King algorithm (Garay and Berman) reaches consensus whenever `n > 4f`, where `f` is the number of Byzantine processes. It runs for `f+1` phases of two rounds each. In the first round, every process broadcasts its current preferred value and tallies the majority. In the second round, the process whose id matches the phase number acts as the **king** and broadcasts the majority it observed, breaking ties. A process adopts that majority if its count exceeded `n/2 + f`; otherwise it adopts the king's value. After `f+1` phases, all correct processes converge on the same output.

## How many processes can a shared object convince?

When processes coordinate through shared memory rather than messages, each concurrent object has a **consensus number**: the maximum number of processes that can reach consensus using only that object in a wait-free way. Atomic read/write registers have consensus number 1, so they cannot solve consensus for even two processes. Test-and-set, swap, fetch-and-add, and wait-free queues or stacks reach consensus number 2. Compare-and-swap, load-link/store-conditional, and a few others have consensus number ∞, meaning they are **universal** and can implement any other concurrent object. This ordering is known as Herlihy's hierarchy.

## Permissioned and permissionless systems

Traditional consensus algorithms such as **Paxos** and **Raft** assume a fixed, authenticated membership, elect a leader to make progress, and tolerate only crashes. They are pervasive in cloud and distributed systems. Open networks face a different obstacle: without a known membership, an attacker can create countless fake identities, a **Sybil attack**, and overwhelm the fault threshold. Permissionless protocols block this by making participation costly. **Bitcoin** introduced proof of work, where miners burn computation solving cryptographic puzzles and the first to solve one appends the next block. Successive systems use **proof of stake** (locked-up currency), **proof of space** (committed disk storage), **proof of authority** (vetted identities), and similar schemes. **Proof of personhood** aims to give each real human exactly one vote regardless of wealth.

## Where consensus shows up

Google's Chubby lock service builds high availability on a Paxos-backed replicated log, so a small set of files representing locks survives failures. Many peer-to-peer real-time strategy games run a lockstep protocol in which every action is broadcast with a hash of the new game state; if hashes disagree, players in the minority are desynced and removed. In control theory, **MSR-type** algorithms reach agreement among UAVs and other multi-agent systems under noise and faults. The solvable thresholds differ sharply across these settings: `n > 3f` for classical oral Byzantine protocols, `n > f+1` when signatures are available, and no deterministic solution in fully asynchronous systems with even one crash.
