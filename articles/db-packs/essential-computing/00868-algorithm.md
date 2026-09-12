# Algorithm

An algorithm is a finite, well-defined sequence of steps that solves a problem or computes a function. Algorithms differ from heuristics, which are problem-solving shortcuts with no guarantee of an optimal or correct answer.

## Origins and the word

Algorithmic procedures predate computers. A Sumerian clay tablet from Shuruppak (c. 2500 BC) carries one of the earliest known division algorithms. Babylonian tablets (c. 1800–1600 BC) encode astronomical computations, and the Rhind Mathematical Papyrus (c. 1550 BC) records Egyptian arithmetic procedures. Euclid's *Elements* (c. 300 BC) formalizes the Euclidean algorithm, still taught for finding the greatest common divisor of two numbers.

The English word "algorithm" derives from the 9th-century Persian polymath Muḥammad ibn Mūsā al-Khwārizmī, whose treatises on Hindu-Arabic numerals were translated into Latin in the 12th century. "Algorism" became "algorithm" by the late 15th century, influenced by the Greek *arithmos* (number). In the 830s, al-Kindi developed frequency analysis, a method that breaks ciphers by exploiting how often letters appear.

## Formalization in the 20th century

Until the 1900s, algorithms were practical recipes rather than mathematical objects. David Hilbert's Entscheidungsproblem asked whether every mathematical statement could in principle be decided by a mechanical procedure. In response, four independent models emerged between 1936 and 1939: Gödel–Herbrand–Kleene recursive functions, Alonzo Church's lambda calculus, Emil Post's Formulation 1, and Alan Turing's abstract machines, now called Turing machines. All four compute the same class of functions, a result known as the Church–Turing thesis. A Turing machine models computation as a head reading and writing symbols on a tape according to transition rules, and remains the standard way to reason about what algorithms can and cannot do.

Two terms used above:

- **Recursive function**: a function defined in terms of itself, with base cases for the simplest inputs.
- **Lambda calculus**: a notation for defining and applying functions, foundational to functional programming.

## Representation and analysis

Algorithms can be written in natural language, pseudocode, flowcharts, or programming languages. Flowcharts use rectangles for sequential steps and diamonds for decisions. Turing machines themselves admit three levels of description: high-level (what the algorithm is meant to do), implementation-level (how the machine behaves), and formal-level (the exact state transitions on the tape).

The central tool for comparing algorithms is Big O notation, which describes how an algorithm's running time or memory use grows as the input size *n* grows. It is an upper bound, not an exact figure. A linear search through *n* items takes O(*n*) time in the worst case, because the target may sit at the end. Binary search, which repeatedly halves a sorted list, takes O(log *n*) time: the number of steps grows with the logarithm of *n* rather than with *n* itself. Asymptotic analysis gives worst-case guarantees; empirical benchmarking reveals constant-factor overheads and cache effects that the theory cannot predict.

## Design paradigms

Most algorithms fit a handful of recurring strategies:

- **Brute-force search**: try every candidate until one works.
- **Divide-and-conquer**: split the problem into smaller subproblems, solve each, then combine. Merge sort recursively sorts halves and merges them.
- **Dynamic programming**: solve overlapping subproblems once and store the answers. Floyd–Warshall uses this to compute shortest paths between every pair of nodes in a graph.
- **Greedy**: at each step take the locally optimal choice. Kruskal's algorithm builds a minimum spanning tree by repeatedly adding the cheapest edge that does not form a cycle.
- **Randomized**: use random choices for speed or simplicity. Monte Carlo algorithms may return a wrong answer with small probability; Las Vegas algorithms always return a correct answer but have a random running time.

Algorithms are also classified by how they run: serial, parallel, or distributed; deterministic or non-deterministic; exact or approximate.

## From heuristics to AI-discovered algorithms

Historically, algorithm design moved from rough heuristics toward rigorous, provably correct procedures. Symbolic integration illustrates the arc: James Slagle's SAINT (1961) was heuristic-driven, SIN (1968) improved on it, and Robert Risch's algorithm (1969) decides whether a function has a closed-form integral.

That progression is now partly inverted. Transformer-based AI has introduced heuristic, learned systems into domains such as recommendation engines, where classical algorithms once dominated. Google DeepMind's AlphaDev (2023) rediscovered faster sorting routines now used in LLVM's standard library. AlphaEvolve (2025) applies large language models to general-purpose algorithm discovery through evolutionary search, training software agents with reward signals. The results are typically verified empirically against hand-written baselines rather than proven correct.

## Quantum algorithms and post-quantum cryptography

Quantum algorithms exploit superposition (quantum bits representing many states at once) and entanglement (correlation between bits) to solve certain problems faster than classical machines can. Because a sufficiently large quantum computer would break widely used public-key cryptography, NIST finalized post-quantum encryption standards in 2024, public algorithms designed to resist quantum attacks.

## Open questions

The best-known open problem in algorithmic theory is P versus NP: whether every problem whose solution can be verified quickly (NP) can also be solved quickly (P). A "yes" answer would collapse the gap between checking and finding, breaking most public-key cryptography; a "no" answer would confirm that the gap is real. Other open questions include whether randomized algorithms can be strictly faster than the best deterministic ones, and how to patent AI-discovered algorithms under U.S. law, which excludes pure mathematical algorithms but permits practical applications, as in *Diamond v. Diehr* (1981).
