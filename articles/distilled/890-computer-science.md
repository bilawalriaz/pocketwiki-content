# Computer science

## Overview
Computer science is the study of computation, information, and automation, spanning theoretical disciplines (algorithms, theory of computation) and applied disciplines (hardware/software design). Its fundamental concern is determining what can and cannot be automated. The field emerged from early mechanical calculators and theoretical work by mathematicians like Leibniz, Babbage, and Turing, becoming a distinct academic discipline in the 1950s–1960s. It intersects with mathematics, engineering, and natural sciences, while its subfields—such as artificial intelligence, cryptography, and human–computer interaction—address both abstract computational limits and practical system implementation.

## Timeline
- **1623** — Wilhelm Schickard constructs the first working mechanical calculator.
- **1673** — Gottfried Leibniz demonstrates the Stepped Reckoner, a digital mechanical calculator; documents binary number system.
- **1822** — Charles Babbage begins design of the Difference Engine, leading to the programmable Analytical Engine (1834).
- **1843** — Ada Lovelace publishes the first algorithm tailored for computer implementation (Bernoulli numbers for the Analytical Engine).
- **1885** — Herman Hollerith invents the punched-card tabulator for statistical processing; company later becomes IBM.
- **1937** — Howard Aiken and IBM complete the ASCC/Harvard Mark I, a giant programmable calculator based on Babbage’s principles.
- **1940s** — Machines like the Atanasoff–Berry computer and ENIAC shift the term "computer" from human operators to electronic machines.
- **1946** — Columbia University offers one of the first academic-credit courses in computer science.
- **1953** — University of Cambridge launches the world’s first computer science degree program (Cambridge Diploma in Computer Science).
- **1956** — Dartmouth Conference establishes artificial intelligence as a cross-disciplinary field.
- **1962** — Purdue University forms the first computer science department in the United States.
- **1969** — University of Copenhagen founds the Department of Datalogy, the first institution to use Peter Naur’s proposed term.

## Body

### History and Foundations
The conceptual roots of computer science predate digital computers. Antiquity saw algorithms and devices like the abacus for fixed numerical tasks. In 1623, Wilhelm Schickard built the first working mechanical calculator. Gottfried Leibniz’s 1673 Stepped Reckoner and documentation of the binary system positioned him as a pivotal early figure. The 19th century brought industrial calculation: Thomas de Colmar’s reliable arithmometer (1820) and Charles Babbage’s designs for the automatic Difference Engine (1822) and the programmable Analytical Engine (1834), which adopted Jacquard loom punch cards for infinite programmability. Ada Lovelace’s 1843 notes on the Analytical Engine contained the first published algorithm for a machine. Herman Hollerith’s tabulator (1885) automated census data via punch cards, founding the lineage of IBM. Percy Ludgate (1909) and Leonardo Torres Quevedo (1914, 1920) independently advanced electromechanical designs, the latter introducing floating-point arithmetic. Howard Aiken’s Harvard Mark I (1937), built with IBM, realized Babbage’s vision using punch cards and a central processing unit.

The 1940s transitioned computation to electronic machines (Atanasoff–Berry, ENIAC), broadening the field beyond mathematical calculation to general computation. IBM’s Watson Laboratory at Columbia (1945) catalyzed academic recognition; Columbia offered credit courses by 1946. Computer science solidified as a discipline in the 1950s–60s: Cambridge started the first degree (1953), Purdue the first US department (1962). The 1956 Dartmouth Conference launched artificial intelligence as a cross-disciplinary endeavor drawing on mathematics, logic, engineering, and neurophysiology.

### Etymology, Scope, and Relationship to Other Disciplines
The term "computer science" appeared in a 1959 *Communications of the ACM* article by Louis Fein, arguing for a graduate school analogous to Harvard Business School; George Forsythe championed the name. Because much of the field does not study physical computers, alternatives arose: *computing science* (emphasizing process over machine), *datalogy* (Peter Naur, 1969, University of Copenhagen, focusing on data treatment), and *data science* (now a distinct multi-disciplinary field). European terminology often derives from "automatic information" (e.g., *informatique*, *Informatik*, *informatica*). A folkloric quote attributed to Edsger Dijkstra states: "computer science is no more about computers than astronomy is about telescopes."

Computer hardware design falls under computer engineering; commercial system deployment under information technology/systems. Computer science intersects heavily with mathematics (logic, category theory, algebra), influenced by Gödel, Turing, von Neumann, Church, and Kleene. The relationship with software engineering is contentious: David Parnas distinguishes computer science as studying general computation properties, while software engineering designs specific computations for practical goals. Academic departments vary by mathematical vs. engineering emphasis, affecting funding and curriculum alignment.

### Philosophy: Epistemology and Paradigms
Whether computer science is a science, mathematics, or engineering discipline is debated. Allen Newell and Herbert Simon (1975) called it an empirical discipline: each new machine is an experiment posing a question to nature. Proponents of the engineering view note reliability is tested like bridges or planes; critics argue engineering observes the possible, not the existent, and creates phenomena rather than discovering laws. The mathematical view treats programs as physical realizations of mathematical entities, amenable to deductive reasoning (Dijkstra, Hoare).

Three paradigm classifications exist: Peter Wegner proposes science, technology, mathematics; Peter Denning’s group proposes theory, abstraction (modeling), design; Amnon Eden describes the rationalist (mathematical/deductive), technocratic (engineering/software), and scientific (empirical/natural science, e.g., AI) paradigms. The field focuses on design, specification, programming, verification, implementation, and testing of human-made computing systems.

### Theoretical Computer Science
Theoretical computer science is mathematical and abstract, motivated by practical computation to understand its nature and improve methodologies.

**Theory of Computation** addresses the fundamental question: "What can be automated?" *Computability theory* examines which problems are solvable on theoretical models (e.g., Turing machines). *Computational complexity theory* studies time and space resource costs. The P = NP? problem (a Millennium Prize Problem) remains open.

**Information and Coding Theory**: Information theory (Claude Shannon) quantifies information, defining fundamental limits on data compression, storage, and communication. Coding theory studies codes (systems converting information forms) for compression, cryptography, error detection/correction, and network coding, aiming for efficient, reliable transmission.

**Data Structures and Algorithms** study common computational methods and their efficiency.

**Programming Language Theory and Formal Methods**: Programming language theory covers design, implementation, analysis, and classification of languages, intersecting mathematics, software engineering, and linguistics. Formal methods apply mathematical techniques (logic calculi, formal languages, automata theory, program semantics, type systems) to specify, develop, and verify software/hardware. They enhance reliability for high-integrity, life-critical systems but are costly, limiting industrial use to safety/security-critical contexts.

### Applied Computer Science
**Computer Graphics and Visualization** studies digital visual content synthesis and manipulation, connecting to computer vision, image processing, and computational geometry; heavily used in special effects and video games.

**Image and Sound Processing** handles multimedia information (images, sound, video) streamed via signals. This is central to *informatics* (European view: information processing algorithms independent of carrier—electrical, mechanical, biological). Applications include medical imaging and speech synthesis. An open problem: the lower bound on fast Fourier transform complexity.

**Computational Science, Finance, and Engineering** (Scientific Computing) constructs mathematical models and quantitative techniques to solve scientific problems via simulation (fluid dynamics, circuits, social/biological systems). It enables design optimization (e.g., aircraft) and circuit design (SPICE, integrated circuit software).

**Human–Computer Interaction (HCI)** researches design and use of computer systems based on human–interface interaction analysis, with subfields linking emotions, social behavior, and brain activity to computing.

**Software Engineering** applies engineering practices to design, implement, and modify software for quality, affordability, maintainability, and speed. It covers organizing/analyzing software, including testing, systems engineering, technical debt, and development processes.

**Artificial Intelligence (AI)** synthesizes goal-oriented processes: problem-solving, decision-making, adaptation, learning, communication. Originating in cybernetics and the 1956 Dartmouth Conference, it is cross-disciplinary (math, logic, semiotics, engineering, philosophy, neurophysiology). While popularly linked to robotics, its main application is embedded computational understanding in software. Alan Turing’s 1940s question "Can computers think?" remains effectively unanswered; the Turing test assesses human-like intelligence. Automation of evaluative/predictive tasks increasingly substitutes human monitoring in complex real-world domains.

### Computer Systems
**Computer Architecture and Microarchitecture** defines the conceptual design and operational structure of a computer system, focusing on CPU internal operation and memory access. The term traces to IBM researchers Lyle Johnson and Frederick Brooks (1959). Computer engineers design hardware from processors to supercomputers and embedded systems.

**Concurrent, Parallel, and Distributed Computing**: Concurrency allows simultaneous, potentially interacting computations. Models include Petri nets, process calculi, and parallel random access machines. Distributed systems connect multiple computers in a network with private memory, exchanging information for common goals.

**Computer Networks** studies construction and behavior of networks, addressing performance, resilience, security, scalability, cost-effectiveness, and services.

**Computer Security and Cryptography**: Security protects information from unauthorized access/disruption/modification while maintaining usability. Historical cryptography writes/deciphers secret messages. Modern cryptography scientifically studies distributed computations under attack, covering symmetric/asymmetric encryption, digital signatures, hash functions, key-agreement protocols, blockchain, zero-knowledge proofs, and garbled circuits.

**Databases and Data Mining**: Databases organize, store, and retrieve large data via management systems, models, and query languages. Data mining discovers patterns in large datasets.

### Discoveries: Three Great Insights
Philosopher Bill Rapaport identifies three foundational insights:
1.  **Binary Representation** (Leibniz, Boole, Turing, Shannon, Morse): Any computable problem’s information can be represented using only two distinguishable states (0/1, on/off, magnetized/demagnetized).
2.  **Minimal Instruction Set** (Turing): Any algorithm can be expressed using only five basic instructions: move left, move right, read symbol, print 0, print 1.
3.  **Structured Composition** (Böhm, Jacopini): Only three rules combine basic instructions into complex ones: *sequence* (do this, then that), *selection* (IF...THEN...ELSE), *repetition* (WHILE...DO). These can be further simplified using `goto`.

### Programming Paradigms
Languages support different styles:
*   **Functional**: Treats computation as mathematical function evaluation; avoids state/mutable data; declarative (expressions/declarations).
*   **Imperative**: Uses statements changing program state; commands for the computer; focuses on *how* to operate.
*   **Object-Oriented**: Based on "objects" containing data (fields/attributes) and code (methods); objects interact and modify their own data.
*   **Service-Oriented**: Uses "services" as work units for integrated business/mission-critical applications.
Many languages support multiple paradigms; distinction is often stylistic.

### Research Culture
Conferences are the primary prestige venue for computer science research, unlike most fields where journals dominate. This is attributed to the field’s rapid development requiring fast review and distribution of results.

## Terms
- ****Algorithm**** — A finite sequence of rigorous instructions for performing a computation or solving a problem.
- ****Turing Machine**** — An abstract mathematical model of computation that manipulates symbols on a tape according to rules; used to define computability.
- ****Computational Complexity Theory**** — The study of the resources (time, space) required to solve computational problems, classifying them by inherent difficulty.
- ****P = NP Problem**** — A major unsolved problem asking whether every problem whose solution can be quickly verified can also be quickly solved.
- ****Information Theory**** — The mathematical study of the quantification, storage, and communication of information, founded by Claude Shannon.
- ****Formal Methods**** — Mathematically based techniques for the specification, development, and verification of software and hardware systems.
- ****Artificial Intelligence (AI)**** — The synthesis of goal-oriented processes (problem-solving, learning, adaptation) found in humans and animals.
- ****Distributed System**** — A system of multiple networked computers with private memory that communicate to achieve a common goal.
- ****Cryptography**** — The scientific study of techniques for secure communication in the presence of adversaries; modern cryptography analyzes distributed computations under attack.
- ****Programming Paradigm**** — A style or classification of programming (e.g., functional, imperative, object-oriented) defining how computation is structured.

## Debates and Open Questions
*   **Epistemological Status**: Is computer science a natural science, a mathematical discipline, or an engineering discipline? Arguments exist for empirical experimentation (Newell/Simon), mathematical deduction (Dijkstra/Hoare), and engineering reliability testing.
*   **Paradigm Classification**: No consensus on the field's fundamental paradigms; competing frameworks include science/technology/math (Wegner), theory/abstraction/design (Denning), and rationalist/technocratic/scientific (Eden).
*   **Relationship to Software Engineering**: Whether they are distinct disciplines (Parnas: science vs. design) or overlapping practices remains contentious, complicated by vague definitions of "software engineering."
*   **P vs. NP**: The central open problem in theory of computation; resolution would define the limits of feasible computation.
*   **Machine Intelligence**: Turing’s question "Can computers think?" remains effectively unanswered; the Turing test is a behavioral benchmark, not a proof of cognition.
*   **Fast Fourier Transform Lower Bound**: The minimum computational complexity for FFT algorithms is an unsolved problem in theoretical computer science.