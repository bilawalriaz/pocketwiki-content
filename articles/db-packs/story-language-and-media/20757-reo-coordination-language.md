# Reo Coordination Language

Reo is a domain-specific language for describing how independent processes exchange data. Its programs, called *connectors* or *circuits*, are drawn as labeled directed hypergraphs in which the edges carry data between the processes attached to the graph. The same formalism covers component-based software, service-oriented systems, multithreaded programs, biological models, and cryptographic protocols. Reo has formal semantics, which is what makes its circuits verifiable and compilable.

## Nodes, channels, and components

A circuit is built from nodes and channels. Components, the ordinary computations, sit outside the circuit and talk to it only through I/O operations on *boundary nodes*, the subset of nodes where they connect. A component issues a *put-request* to dispatch a data item into a node, or a *get-request* to fetch one out. Every I/O operation is blocking: the component only proceeds once the operation has actually succeeded.

Every channel connects exactly two nodes, but a node can have many channels attached, as inputs, as outputs, or as both. Nodes have fixed behaviour. When exactly one incoming channel offers data, the node copies it to every outgoing channel (a *replicator*); when several offer data, the node picks one nondeterministically (a *merger*). The node itself never stores or alters data. Channels are different: their *type* defines what they do, and they may buffer, drop, or filter data.

## Common channel types

| Type | Behaviour |
|---|---|
| Sync | Reads its input and forwards it to its output atomically. |
| LossySync | Like Sync, but drops the data if the output side is not ready. |
| Fifo⟨n⟩ | Reads its input, buffers up to *n* items, and forwards to its output when it can. |
| SyncDrain | Reads both inputs atomically and discards both. |
| Filter⟨c⟩ | Like Sync, but only forwards when the predicate *c* holds; otherwise drops. |

A textbook example is the *Alternator* circuit: two producers on the left, one consumer on the right, wired through channels that force the producers to send synchronously while the consumer receives the items in alternating order. The protocol lives in the graph, not in the producers or the consumer.

## Exogeneity and compositionality

Coordination languages are classified by *locus*. *Endogenous* languages, such as Linda, embed their primitives inside each component, so coordination code gets tangled with the computation it is supposed to govern and the cooperation model becomes implicit. Reo is *exogenous*: the primitives live in a separate circuit that sits outside the components, so the coordination protocol of an application becomes a standalone artefact that can be designed, tested, debugged, and reused on its own.

Circuits compose by joining on boundary nodes, and synchrony is preserved through composition. Gluing two circuits that each carry synchronous flow between adjacent nodes yields a joint circuit whose end-to-end flow is also synchronous. Most concurrency models, π-calculus among them, do not preserve synchrony this way, which is what makes Reo's small reusable connectors buildable into large ones.

## Semantics and tools

Several semantics coexist. The first, due to Arbab and Rutten, modelled every node as a timed data stream, an infinite sequence of data items paired with monotonically increasing real-time timestamps, and reduced channels to relations on those streams. Baier, Sirjani, Arbab, and Rutten later introduced *constraint automata*, labeled transition systems in which each transition carries a synchronisation constraint (which nodes fire together) and a data constraint (what flows on them). Constraint automata cannot directly express context-sensitive behaviour, since a LossySync, for instance, should only drop data when its output node has no pending get-request, so Clarke, Costa, and Arbab added *connector colouring* to encode that dependency. Subsequent work added timed and probabilistic variants, and Jongmans and Arbab catalogued thirty distinct semantic formalisms.

The *Extensible Coordination Tools* (ECT) are an Eclipse-based IDE that bundles a graphical editor, an animation engine for data-flow, a Reo-to-Java compiler that emits a class simulating the circuit's constraint automaton, and a translator to the mCRL2 process algebra for model checking against μ-calculus properties. Vereofy is an alternative model checker. A separate Scala implementation runs the same circuits in a distributed fashion across multiple machines.
