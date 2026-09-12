# Computer science

Computer science is the study of computation, information, and automation, combining theoretical work (algorithms, the theory of what can and cannot be computed) with applied work (hardware and software design). Its central question is which problems can be automated, and at what cost.

## Origins and emergence as a discipline

Algorithms and fixed-task devices like the abacus existed in antiquity. Wilhelm Schickard built the first working mechanical calculator in 1623. Gottfried Leibniz demonstrated the Stepped Reckoner in 1673 and documented binary numbers. Charles Babbage designed the automatic Difference Engine (1822) and the programmable Analytical Engine (1834), which used Jacquard loom punch cards for programmability. Ada Lovelace's 1843 notes on the Analytical Engine contain the first published algorithm intended for a machine.

The 1940s shifted computation to electronic machines (Atanasoff–Berry, ENIAC), and the word "computer" moved from human operators to machines. Columbia offered one of the first credit courses in 1946, Cambridge launched the first computer science degree in 1953, and Purdue formed the first US department in 1962. The 1956 Dartmouth Conference established artificial intelligence as a cross-disciplinary field.

## Name, scope, and neighbouring disciplines

The name "computer science" appeared in a 1959 *Communications of the ACM* article by Louis Fein; George Forsythe championed it. Because much of the field does not study physical computers, alternatives arose: *computing science* emphasises process over machine, Peter Naur's *datalogy* (1969, Copenhagen) focuses on data, and *data science* is now a separate multi-disciplinary field. European terms such as *informatique*, *Informatik*, and *informatica* derive from "automatic information." Edsger Dijkstra observed that computer science is no more about computers than astronomy is about telescopes.

Hardware design belongs to computer engineering; commercial deployment belongs to information technology. The relationship with software engineering is contested: David Parnas separates computer science as the study of general computation from software engineering as the design of specific computations for practical goals.

## Theoretical foundations

Theoretical computer science is mathematical and abstract, motivated by practical computation.

*Theory of computation* asks what can be automated. *Computability theory* studies which problems a Turing machine (an abstract symbol-manipulating device) can solve. *Computational complexity theory* classifies problems by the time and memory they require. The P = NP? problem, asking whether every problem whose solution can be quickly verified can also be quickly solved, is unsolved and is a Millennium Prize Problem.

*Information and coding theory*, founded by Claude Shannon, quantifies information and sets fundamental limits on compression, storage, and communication. Coding theory designs codes for compression, error detection and correction, cryptography, and network coding.

*Programming language theory and formal methods* apply mathematics (logic, formal languages, automata theory, program semantics, type systems) to specify, analyse, and verify software and hardware, raising reliability for safety-critical systems at high cost.

## Three foundational insights

Philosopher Bill Rapaport identifies three insights that underpin all computation:

1. *Binary representation* (Leibniz, Boole, Turing, Shannon). Any computable problem's information can be encoded in two distinguishable states: 0/1, on/off, magnetised/demagnetised.
2. *Minimal instruction set* (Turing). Any algorithm can be expressed using only five basic operations: move left, move right, read symbol, print 0, print 1.
3. *Structured composition* (Böhm and Jacopini). Three rules combine instructions into complex programs: *sequence* (do this, then that), *selection* (IF…THEN…ELSE), and *repetition* (WHILE…DO), further simplifiable using `goto`.

## Applied computer science

**Computer graphics and visualisation** synthesise digital visual content, linking to computer vision, image processing, and computational geometry, and are heavily used in special effects and games.

**Image and sound processing** handle multimedia via signals, underpinning medical imaging and speech synthesis. An open problem is the lower bound on fast Fourier transform complexity, the minimum number of operations any algorithm that converts signals between time and frequency representations must use.

**Computational science, finance, and engineering** build mathematical models and simulations for fluid dynamics, circuits, and social or biological systems, enabling design optimisation in aircraft and integrated circuits via tools such as SPICE.

**Human–computer interaction (HCI)** studies the design and use of computer systems through human–interface analysis, with subfields linking emotion, social behaviour, and brain activity to computing.

**Software engineering** applies engineering practices to design, implement, test, and maintain software, addressing technical debt, systems engineering, and development processes.

**Artificial intelligence (AI)** synthesises goal-oriented processes such as problem-solving, decision-making, learning, and adaptation, originating in cybernetics and the 1956 Dartmouth Conference. Although popularly linked to robotics, its main application is embedded computational understanding in software. Alan Turing's 1940s question "Can computers think?" remains effectively unanswered; the Turing test is a behavioural benchmark, not a proof of cognition.

## Computer systems

**Computer architecture and microarchitecture** define the conceptual design and operational structure of a computer system, focusing on CPU internals and memory access; the term traces to IBM researchers Lyle Johnson and Frederick Brooks in 1959.

**Concurrent, parallel, and distributed computing** address simultaneous computations. Distributed systems connect multiple computers across a network with private memory, exchanging information to reach common goals. Formal models include Petri nets (graph-based descriptions of concurrent processes), process calculi, and parallel random-access machines.

**Computer networks** study network construction and behaviour, addressing performance, resilience, security, scalability, cost, and services.

**Computer security and cryptography** protect information from unauthorised access, disruption, or modification while preserving usability. Modern cryptography studies distributed computations under adversarial attack, covering symmetric and asymmetric encryption, digital signatures, hash functions, key-agreement protocols, blockchain, zero-knowledge proofs, and garbled circuits.

**Databases and data mining** organise, store, and retrieve large datasets via management systems and query languages, and discover patterns in those datasets.

## Programming paradigms

*Functional* languages treat computation as mathematical function evaluation and avoid mutable state. *Imperative* languages use statements that change program state. *Object-oriented* languages organise code around objects that bundle data (fields) and behaviour (methods), allowing objects to interact and modify their own data. *Service-oriented* architectures use services as work units for integrated applications. Most modern languages support multiple paradigms, so the distinction is often stylistic.

## Disciplinary debates

Whether computer science is a science, mathematics, or engineering discipline is unresolved. Allen Newell and Herbert Simon (1975) called it empirical, since each new machine is an experiment posing a question to nature. Dijkstra and Hoare treated programs as mathematical entities amenable to deductive reasoning. Engineering-oriented proponents note that reliability is tested like bridges or aircraft, though critics argue engineering creates phenomena rather than discovering laws. Three competing paradigm classifications, Wegner's science/technology/mathematics, Denning's theory/abstraction/design, and Eden's rationalist/technocratic/scientific, reflect this lack of consensus. Conferences, not journals, remain the primary prestige venue for research because the field's rapid pace demands fast review and distribution.
