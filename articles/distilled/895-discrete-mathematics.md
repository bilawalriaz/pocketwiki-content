# Discrete mathematics

## Overview
Discrete mathematics studies mathematical structures that are fundamentally discrete—having a bijection with natural numbers—rather than continuous. It encompasses countable sets (finite or countably infinite) such as integers, graphs, and logical statements, excluding continuous topics like real numbers and calculus. The field expanded rapidly in the late twentieth century due to digital computers, which operate in discrete steps and store data in discrete bits, making discrete mathematics foundational to computer science, cryptography, and algorithm design. While focused on discrete objects, the field frequently employs analytic methods from continuous mathematics.

## Timeline
- **1852** — Four color theorem first stated in graph theory.
- **1900** — David Hilbert presents list of open problems, including consistency of arithmetic (2nd) and solvability of Diophantine equations (10th).
- **1931** — Kurt Gödel proves second incompleteness theorem, showing arithmetic cannot prove its own consistency.
- **1936** — Alan Turing publishes *On Computable Numbers*, laying groundwork for theoretical computer science.
- **1940s** — World War II codebreaking at Bletchley Park drives advances in cryptography and the first programmable digital electronic computer.
- **1970** — Yuri Matiyasevich proves Hilbert's tenth problem unsolvable (no general algorithm for Diophantine equations).
- **1976** — Kenneth Appel and Wolfgang Haken prove the four color theorem using substantial computer assistance.
- **1980s** — Discrete mathematics enters university curricula as a computer science support course.
- **Late 20th century** — Public-key cryptography developed; ACM and MAA standardize curriculum to develop mathematical maturity.
- **2000** — Clay Mathematics Institute offers $1 million prize for solution to P = NP problem. |

## Body

### Definition and Scope
Discrete mathematics deals with countable sets—finite sets or those with the cardinality of the natural numbers. There is no single exact definition of the field. It studies integers, graphs, and logical statements, excluding continuous mathematics such as real numbers, calculus, and Euclidean geometry. The term "finite mathematics" sometimes refers to the subfield dealing with finite sets, particularly areas relevant to business. Although the main objects are discrete, analytic methods from continuous mathematics are often employed.

### Theoretical Computer Science
This area draws heavily on graph theory and mathematical logic. It includes the study of algorithms and data structures. **Computability** (what can be computed in principle) has close ties to logic; **complexity** studies the time, space, and other resources required for computations. **Automata theory** and **formal language theory** relate to computability. **Petri nets** and **process algebras** model computer systems. Discrete mathematics analyzes VLSI electronic circuits. **Computational geometry** applies algorithms to geometrical problems; **computer image analysis** applies them to image representations. Theoretical computer science also includes continuous computational topics.

### Information Theory
Information theory quantifies information. **Coding theory** designs efficient, reliable data transmission and storage methods. The field also includes continuous topics such as analog signals, analog coding, and analog encryption.

### Logic
Logic studies valid reasoning, inference, consistency, soundness, and completeness. Logical formulas and proofs are discrete structures; proofs form finite trees or directed acyclic graphs. Truth values usually form a finite set (typically true/false), though continuous-valued logics exist (e.g., fuzzy logic). The study of mathematical proof underpins automated theorem proving and formal verification of software. Infinite proof trees are studied in infinitary logic.

### Set Theory
Set theory studies collections of objects. In discrete mathematics, the focus is on countable sets (including finite sets). The field began with Georg Cantor's work distinguishing different infinite sets, motivated by trigonometric series. Further development of infinite set theory (descriptive set theory) uses continuous mathematics and lies outside discrete mathematics' scope.

### Combinatorics
Combinatorics studies how discrete structures combine or arrange. **Enumerative combinatorics** counts combinatorial objects (e.g., the twelvefold way for permutations, combinations, partitions). **Analytic combinatorics** uses complex analysis and probability for asymptotic formulae. **Topological combinatorics** applies topology. **Design theory** studies combinatorial designs (subsets with intersection properties). **Partition theory** studies integer partitions, related to q-series and orthogonal polynomials. **Order theory** studies partially ordered sets.

### Graph Theory
Graph theory studies graphs and networks—prime objects in discrete mathematics. Often considered part of combinatorics, it is now a distinct subject. Graphs model relations and dynamics in physical, biological, and social systems. In computer science, they represent communication networks, data organization, and computational flow. In mathematics, they apply to geometry and topology (e.g., knot theory). **Algebraic graph theory** links to group theory; **topological graph theory** links to topology. Continuous graphs exist but most research is discrete.

### Number Theory
Number theory studies properties of integers. Applications include cryptography and cryptanalysis: modular arithmetic, Diophantine equations, congruences, prime numbers, and primality testing. **Geometry of numbers** is a discrete aspect. **Analytic number theory** uses continuous mathematics. Topics beyond discrete objects include transcendental numbers, Diophantine approximation, p-adic analysis, and function fields.

### Algebraic Structures
Discrete algebras include: **Boolean algebra** (logic gates, programming); **relational algebra** (databases); finite groups, rings, and fields (algebraic coding theory); **discrete semigroups and monoids** (formal languages). Algebraic structures also appear as continuous examples.

### Discrete Analogues of Continuous Mathematics
Many continuous concepts have discrete versions: discrete calculus, discrete Fourier transforms, discrete geometry, discrete logarithms, discrete differential geometry, discrete exterior calculus, discrete Morse theory, discrete optimization, discrete probability theory/distribution, difference equations, discrete dynamical systems, and discrete vector measures.

#### Calculus of Finite Differences, Discrete Analysis, and Discrete Calculus
A function on an integer interval is a **sequence** (finite or infinite). Sequences can be defined explicitly, by a general term formula, or implicitly by a **recurrence relation** or **difference equation**. Difference equations replace differentiation with the difference between adjacent terms; they approximate differential equations or are studied independently. Discrete transforms (for digital signals) parallel integral transforms (for analogue signals). **Time scale calculus** unifies difference and differential equations for simultaneous discrete/continuous modeling; **hybrid dynamical systems** offer another approach.

#### Discrete Geometry
Discrete and combinatorial geometry study combinatorial properties of discrete geometrical object collections. A long-standing topic is **tiling of the plane**. In algebraic geometry, curves extend to discrete geometries via spectra of polynomial rings over finite fields modeling affine spaces. Though the space has finitely many points, curves are analogues of continuous curves, with well-defined tangent spaces (Zariski tangent space) making calculus features applicable in finite settings.

#### Discrete Modelling
Discrete modelling fits discrete formulae to data, the discrete analogue of continuous modelling. A common method uses recurrence relations. **Discretization** transfers continuous models into discrete counterparts for easier calculation via approximations; **numerical analysis** is a key example.

### Challenges and Historical Drivers
Key problems have focused research. The **four color theorem** (1852) was proved in 1976 by Appel and Haken using computer assistance. Hilbert's second problem (consistency of arithmetic) was answered negatively by Gödel's second incompleteness theorem (1931). Hilbert's tenth problem (solvability of Diophantine equations) was proved unsolvable by Matiyasevich (1970). World War II codebreaking at Bletchley Park (guided by Turing) advanced cryptography and theoretical computer science. The Cold War spurred public-key cryptography. Telecommunications drove graph theory and information theory. Formal verification needs for safety-critical software drove automated theorem proving. Computational geometry enabled modern video games and CAD. Bioinformatics (tree of life) relies on theoretical computer science, graph theory, and combinatorics. The **P = NP problem** (relationship between complexity classes P and NP) remains a major open problem with a $1 million Clay Mathematics Institute prize.

## Terms
- **Countable set**: A finite set or a set with the same cardinality as the natural numbers (bijection with ℕ).
- **Discrete structure**: A mathematical object (e.g., integer, graph, logical formula) that is distinct and separable, as opposed to continuous.
- **Computability**: The study of what problems can be solved by an algorithm in principle.
- **Complexity**: The study of resources (time, space) required to solve computational problems.
- **Difference equation**: An equation relating a sequence to its differences (discrete analogue of a differential equation).
- **Recurrence relation**: An equation defining a sequence recursively, where each term is a function of preceding terms.
- **Graph**: A structure consisting of vertices (nodes) and edges (connections) modeling pairwise relations.
- **Boolean algebra**: An algebraic structure capturing logical operations (AND, OR, NOT) used in logic gates and programming.
- **Diophantine equation**: A polynomial equation where only integer solutions are sought.
- **P = NP problem**: The question of whether every problem whose solution can be quickly verified (NP) can also be quickly solved (P).

## Debates and open questions
- **P vs. NP**: Whether the complexity classes P and NP are equal; a correct proof carries a $1 million Clay Mathematics Institute prize.
- **Definition of the field**: There is no exact, universally agreed-upon definition of "discrete mathematics"; its boundaries are fluid.
- **Scope of set theory**: The extent to which infinite set theory (descriptive set theory) belongs to discrete mathematics is debated, as it heavily uses continuous mathematics.
- **Classification of graph theory**: Whether graph theory is a subfield of combinatorics or a distinct subject in its own right.
- **Continuous vs. discrete methods**: The appropriate balance and interaction between discrete objects and continuous analytic methods (e.g., in analytic combinatorics, analytic number theory, time scale calculus).

Source: adapted from "Discrete mathematics" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Discrete_mathematics
