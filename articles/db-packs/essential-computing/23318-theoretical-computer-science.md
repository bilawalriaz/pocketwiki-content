# Theoretical computer science

Theoretical computer science (TCS) is the subfield of computer science and mathematics devoted to the abstract and mathematical foundations of computation, distinguished from applied computing by an emphasis on mathematical technique and rigor. The ACM's Special Interest Group on Algorithms and Computation Theory (SIGACT) catalogs its scope as algorithms, data structures, computational complexity, parallel and distributed computation, probabilistic and quantum computation, automata theory, information theory, cryptography, program semantics and verification, algorithmic game theory, machine learning, computational biology, computational economics, computational geometry, and computational number theory and algebra. The boundaries are not crisp, but the unifying impulse is to model what can and cannot be computed, and at what cost.

## Origins

TCS grew out of mathematics and mathematical logic, becoming an independent discipline in the twentieth century. In 1931, Kurt Gödel proved his incompleteness theorem, establishing fundamental limits on what formal systems can prove or disprove. In 1948, Claude Shannon founded information theory with his mathematical theory of communication, putting data compression and reliable transmission on a quantitative footing. In the same decade, Donald Hebb introduced a mathematical model of learning in the brain, which seeded neural networks and parallel distributed processing. In 1971, Stephen Cook, and independently Leonid Levin, proved that practically relevant problems can be NP-complete, a landmark that organized modern computational complexity theory. Other pioneers include Alonzo Church, Alan Turing, Stephen Cole Kleene, John von Neumann, and Noam Chomsky.

## Major branches

Algorithms lie at the discipline's core: an algorithm is a finite list of well-defined instructions for calculating a function, proceeding from an initial state through successive states to produce an output and terminate. Some algorithms incorporate random input and are called randomized.

Automata theory studies abstract machines and the problems they can solve; the name comes from the Greek for "self-acting." Coding theory studies the properties of codes used for data compression, cryptography, error correction, and network coding.

Computational complexity theory classifies computational problems by inherent difficulty, using models of computation to quantify the resources, typically time and storage, needed to solve them. Other measures include communication (communication complexity), gates (circuit complexity), and processors (parallel computing). Its practical purpose is to determine what computers can and cannot do.

Computational geometry develops geometric algorithms, driven originally by computer graphics and computer-aided design, with applications in robotics, geographic information systems, integrated circuit design, computer-aided engineering, and computer vision. Computational learning theory analyzes supervised learning, where an algorithm induces a classifier from labeled samples and aims to minimize mistakes on unseen data. Computational number theory, also called algorithmic number theory, studies algorithms for number-theoretic computations; its best-known problem is integer factorization.

Cryptography designs protocols for secure communication against adversaries, addressing confidentiality, data integrity, authentication, and non-repudiation. Modern cryptography relies on computational hardness assumptions (often integer factorization), so schemes are hard to break in practice though breakable in principle; these are called computationally secure. Information-theoretically secure schemes such as the one-time pad cannot be broken even with unlimited computing power, but are harder to implement.

Data structures organize data for efficient use, and choosing the right one is often the key to designing efficient algorithms. Distributed computing studies systems whose components, located on networked computers, coordinate by passing messages; three defining characteristics are concurrency of components, lack of a global clock, and independent failure of components. Examples span service-oriented architectures, massively multiplayer online games, peer-to-peer applications, and blockchains such as Bitcoin.

Information theory quantifies information and finds fundamental limits on compressing, storing, and communicating data. It sits at the intersection of mathematics, statistics, computer science, physics, neurobiology, and electrical engineering, with applications including ZIP files, MP3 and JPEG compression, channel coding for DSL, the Voyager missions, compact discs, mobile telephony, the Internet, and the analysis of black holes. Formal methods apply logic, formal languages, automata theory, program semantics, and type systems to specify and verify software and hardware, motivated by the expectation that mathematical analysis yields more reliable designs.

Machine learning constructs algorithms that build models from inputs and use them to predict or decide, rather than follow explicit rules. It overlaps with artificial intelligence and optimization, and is applied where rule-based programming is infeasible, including spam filtering, optical character recognition, search engines, and computer vision.

Natural computing uses nature as inspiration, substrate, and subject, encompassing artificial neural networks, evolutionary algorithms, swarm intelligence, artificial immune systems, DNA computing, and quantum computing. The Zuse-Fredkin thesis, from the 1960s, proposes that the entire universe is a cellular automaton updating its own rules.

Parallel computing performs many calculations simultaneously, divided into bit-level, instruction-level, data, and task parallelism. Because power consumption now prevents further increases in clock speed, parallelism, especially multi-core processors, has become the dominant paradigm in computer architecture. Amdahl's law bounds the possible speed-up from parallelization, and concurrency introduces new classes of bugs such as race conditions.

Programming language theory designs, implements, and classifies programming languages and their features. Program semantics gives a rigorous mathematical account of what programs mean. Symbolic computation manipulates mathematical expressions exactly rather than approximating them numerically, forming the basis of computer algebra systems.

Quantum computation uses quantum-mechanical phenomena such as superposition and entanglement to manipulate qubits, which can exist in superpositions of states; the quantum Turing machine is the standard theoretical model. Yuri Manin introduced the field in 1980, and Richard Feynman developed it further in 1982.

Very-large-scale integration (VLSI), dating to the 1970s, combines thousands of transistors on a single chip, enabling the microprocessor and the integration of CPU, ROM, RAM, and glue logic onto one device.

## Outlook

Modern TCS continues to expand into interdisciplinary territory. The same underlying ideas, including automata, logic, complexity, randomness, and approximation, now reach into biology, economics, physics, and cryptography. The central open questions, such as whether P equals NP, remain unresolved and continue to organize research priorities across the field.
