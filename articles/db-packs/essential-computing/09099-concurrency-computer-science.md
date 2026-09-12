# Concurrency (computer science)

In computer science, **concurrency** is the ability of a system to handle multiple tasks during overlapping time periods, either by running them simultaneously on separate processors or by interleaving them on a single processor through time-sharing (rapid context switching, in which the processor saves one task's state and loads another's). Tasks share resources and must coordinate, which lets modern systems improve responsiveness, throughput, and scalability in operating systems, embedded and distributed systems, parallel and high-performance computing, databases, web applications, and cloud platforms.

## Parallelism vs concurrency

**Parallelism** is simultaneous execution on multiple processing units (CPU cores). **Concurrency** is the broader property of having multiple threads of control at the program level, where a *thread of control* is an independent sequence of execution steps. A concurrent program can achieve its work through parallelism, through time-slicing on one core, or through a mix of both. A given program may therefore exhibit parallelism only, concurrency only, both at once, or neither.

## Coordination mechanisms

Several mechanisms work together. **Multi-threading and multi-processing** run multiple threads or processes that share system resources. **Synchronization** coordinates access to those shared resources. **Coordination** manages interactions between concurrent tasks. **Concurrency control** ensures data stays consistent. **Inter-process communication (IPC)** lets tasks exchange information.

## Why concurrent systems are hard

Because computations in a concurrent system can interact while running, the number of possible execution paths can be extremely large, and the outcome can be **indeterminate**: given the same inputs, the system may reach different final states depending on timing. Shared resources drive this indeterminacy, producing two classic problems: **deadlocks**, in which tasks wait on each other in a cycle, and **resource starvation**, in which a task never gets the access it needs. Designing concurrent systems centers on techniques for coordinating execution, data exchange, memory allocation, and scheduling to keep response time low and throughput high.

## Theory and models

Concurrency has been an active research field in theoretical computer science since Carl Adam Petri introduced **Petri nets** in the early 1960s. Several formalisms now exist for modeling concurrent systems. The **actor model** treats computation as independent actors that communicate by sending messages. The **process calculi** family (CCS, CSP, and the π-calculus) describes systems as collections of processes that exchange messages over channels. **Petri nets** model systems as places, transitions, and tokens. Some are used mainly for reasoning and specification; others, like the bulk synchronous parallel (BSP) model, support the full development cycle. Some rely on message passing, others on shared state.

The proliferation of models has motivated unification. Lee and Sangiovanni-Vincentelli showed a "tagged-signal" model can give a common framework for the *denotational semantics* (the formal mathematical meaning of programs) of many models, and Nielsen, Sassone, and Winskel showed category theory can do the same. In the actor model, a Concurrency Representation Theorem gives a general way to represent closed concurrent systems (those that do not receive communications from outside) as a limit of increasingly refined approximations of their possible behaviors.

**Temporal logics** support formal reasoning about concurrent systems by making assertions about sequences of states or actions. Linear temporal logic and computation tree logic reason about state sequences; action computational tree logic, Hennessy–Milner logic, and Lamport's temporal logic of actions reason about actions (state changes). Their main use is writing precise specifications for concurrent systems.

## Practice

Concurrent programming covers the languages and algorithms used to build concurrent systems. It is generally broader than parallel programming, because it can involve arbitrary, dynamic communication patterns, while parallel systems typically use a predefined, well-structured communication pattern. The base goals are correctness, performance, and robustness. Operating systems and database management systems are designed to keep running, recover from failure, and avoid unexpected termination.

Because shared resources are involved, concurrent systems usually require some form of **arbiter**, hardware or software that decides which task gets a contested resource next. Arbiters introduce **unbounded nondeterminism**: an arbiter can delay a task arbitrarily long, so the system's set of possible behaviors can be infinite. This complicates **model checking** (automated verification that a system satisfies a property by exhaustively exploring its states) by causing state-space explosion, and it can make models have infinitely many states. Some programming models, including coprocesses and deterministic concurrency, avoid this by having threads explicitly yield their timeslices, so the program, not the arbiter, decides the interleaving.

Source: adapted from "Concurrency (computer science)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Concurrency_%28computer_science%29
