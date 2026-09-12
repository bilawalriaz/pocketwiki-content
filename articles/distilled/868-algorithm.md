# Algorithm

## Overview

An algorithm is a finite, well-defined sequence of steps to solve a problem or perform a computation, forming the basis of both mathematical reasoning and computer programming. Algorithms differ from heuristics, which lack guaranteed optimal outcomes. Their study spans millennia, from ancient Babylonian and Egyptian procedures to modern quantum and AI-discovered methods, and remains central to computer science, mathematics, and technology.

## Timeline

- **c. 2500 BC** — Earliest division algorithm on Sumerian clay tablet from Shuruppak
- **c. 1800–1600 BC** — Babylonian clay tablets describe algorithms for astronomical computations
- **c. 1550 BC** — Rhind Mathematical Papyrus contains Egyptian arithmetic algorithms
- **c. 300 BC** — Euclid describes the Euclidean algorithm in *Elements*
- **825 AD** — Al-Khwarizmi writes foundational texts on Hindu-Arabic computation
- **830s AD** — Al-Kindi develops first cryptanalysis algorithm (frequency analysis)
- **1835** — Electromechanical relays invented, leading to digital computing devices
- **1936–1939** — Formalizations of algorithms via Turing machines, lambda calculus, recursive functions
- **1961–1969** — SAINT, SIN, and Risch Algorithm illustrate evolution from heuristics to formal algorithms
- **2023** — AlphaDev discovers improved sorting and hashing algorithms using reinforcement learning
- **2024** — NIST finalizes post-quantum encryption standards
- **2025** — AlphaEvolve introduced for general-purpose algorithm discovery via LLMs

## Body

### Etymology and Early History

The term "algorithm" derives from the Latinized name of the 9th-century Persian polymath Muḥammad ibn Mūsā al-Khwārizmī, whose works on Hindu-Arabic numerals were translated into Latin in the 12th century. The word evolved through "algorism" in Middle English to "algorithm" by the late 15th century, influenced by the Greek *arithmos*. Ancient civilizations independently developed algorithmic procedures: Babylonian tablets encoded division and astronomical prediction methods; Egyptian papyri included arithmetic techniques; and Greek mathematicians like Euclid and Eratosthenes formalized geometric and number-theoretic algorithms.

### Formalization and Computability

The modern concept of an algorithm emerged in the early 20th century through efforts to solve Hilbert’s Entscheidungsproblem. Key formalizations included Gödel–Herbrand–Kleene recursive functions, Church’s lambda calculus, Post’s Formulation 1, and Turing’s abstract machines. These models established the theoretical limits of computation and laid the groundwork for computer science. Later, Yuri Gurevich and Yiannis Moschovakis proposed formal mathematical theories of algorithms as distinct from computable functions, emphasizing behavioral equivalence and set-theoretic foundations.

### Modern Developments and AI Integration

Traditionally, algorithm development progressed from heuristic approximations to rigorous, guaranteed solutions—exemplified by symbolic integration advancing from Slagle’s SAINT to Risch’s algorithm. However, the rise of transformer-based AI has reversed this trend, with heuristic-driven machine learning systems displacing classical algorithms in domains like recommendation engines. Recent breakthroughs include Google DeepMind’s AlphaDev (2023), which rediscovered faster sorting routines now used in LLVM, and AlphaEvolve (2025), an LLM-powered evolutionary system for automated algorithm design. Quantum algorithms and post-quantum cryptography (standardized by NIST in 2024) represent ongoing frontiers.

### Representation and Analysis

Algorithms can be expressed in natural language, pseudocode, flowcharts, or programming languages. Turing machines offer three levels of description: high-level (conceptual), implementation-level (machine behavior), and formal-level (exact state transitions). Flowcharts use standardized symbols—rectangles for sequences, diamonds for decisions—to visualize logic. Algorithmic analysis evaluates time and space complexity using Big O notation; for instance, binary search runs in O(log n) versus linear search’s O(n). While formal analysis provides asymptotic guarantees, empirical testing reveals real-world performance nuances.

### Design Paradigms and Classification

Algorithms are classified by implementation (recursive vs. iterative), execution model (serial, parallel, distributed), determinism (deterministic vs. non-deterministic), and accuracy (exact vs. approximate). Design paradigms include brute-force search, divide-and-conquer (e.g., merge sort), dynamic programming (e.g., Floyd-Warshall), greedy methods (e.g., Kruskal’s algorithm), and randomized approaches (Monte Carlo and Las Vegas algorithms). Optimization-specific categories include linear programming, integer programming, and heuristic methods like simulated annealing and genetic algorithms.

### Legal and Ethical Dimensions

In the U.S., pure mathematical algorithms are generally unpatentable under cases like *Gottschalk v. Benson*, but practical applications may qualify—as seen in *Diamond v. Diehr*, where a rubber-curing process using feedback control was deemed patentable. Patenting software remains controversial, particularly regarding data compression algorithms like Unisys’s LZW patent. Cryptographic algorithms face export restrictions, reflecting national security concerns.

## Terms

- **Algorithm**: A finite, unambiguous sequence of instructions to solve a problem or compute a function.
- **Heuristic**: A problem-solving approach without guaranteed optimal or correct results.
- **Turing Machine**: An abstract computational model defining algorithmic computation via states, symbols, and transition rules.
- **Big O Notation**: A mathematical notation describing the upper bound of an algorithm’s time or space complexity.
- **Divide-and-Conquer**: A paradigm splitting problems into smaller subproblems, solving them recursively, then combining results.
- **Dynamic Programming**: A method solving complex problems by breaking them into overlapping subproblems and caching solutions.
- **Greedy Algorithm**: An approach making locally optimal choices at each step, hoping to find a global optimum.
- **Quantum Algorithm**: An algorithm designed for quantum computers, leveraging superposition and entanglement.
- **Post-Quantum Cryptography**: Encryption methods resistant to attacks by quantum computers, standardized by NIST in 2024.
- **Abstract State Machine (ASM)**: A formal model characterizing sequential algorithms as step-by-step state transformations.

## Debates and Open Questions

Several unresolved issues persist in algorithmic theory and practice. The P versus NP problem questions whether every problem whose solution can be verified quickly can also be solved quickly—an open question with profound implications for cryptography and optimization. Whether randomized algorithms can be the fastest for certain tasks remains debated. The inversion of the traditional heuristic-to-formal progression due to AI raises questions about the future role of human-designed algorithms. Additionally, the patentability of software and AI-discovered algorithms challenges existing legal frameworks, while ethical concerns around automated decision-making and bias in heuristic systems continue to evolve.