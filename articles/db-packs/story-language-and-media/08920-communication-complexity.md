# Communication complexity

Communication complexity studies the minimum number of bits two parties, traditionally called Alice and Bob, must exchange to compute a function f(x,y) when Alice holds an n-bit string x and Bob holds an n-bit string y, with each knowing only their own input. The worst-case communication complexity D(f) is the smallest number of bits any agreed-upon protocol must exchange on the hardest input pair.

The trivial upper bound is D(f) ≤ n: Bob can simply send all n of his bits and Alice computes the answer. The interesting question is when clever protocols can drive communication far below n, and when no protocol can. Unlike computational complexity, communication complexity ignores how much Alice or Bob compute locally and asks only how much they must say to each other. The same framework extends to more than two parties.

## The communication matrix and rectangles

A useful picture replaces f with a 2^n × 2^n matrix A whose (x,y) entry is f(x,y). Both parties know the whole matrix in advance, but neither knows which row or column holds their own input. Communication gradually narrows the candidate region to the correct entry. After k bits have been exchanged on a transcript h, the set of input pairs (x,y) consistent with that transcript forms a combinatorial rectangle R = M × N, meaning M ⊆ X and N ⊆ Y. Rectangles are the key combinatorial object: a deterministic protocol partitions the matrix into rectangles, one per possible transcript.

## Lower bound for equality

The equality function EQ(x,y) outputs 1 if x = y and 0 otherwise. Any deterministic protocol needs exactly n bits: if two different inputs (x,x) and (x',x') on the diagonal produced the same transcript h, then by the rectangle property the pair (x,x') would also lie in that rectangle, so EQ(x,x') would have to be 1, contradicting x ≠ x'. This argument is the fooling set technique.

With a shared random string z of length n, Alice and Bob can instead solve EQ in O(log n) bits. Alice sends the single bit b = z·x, where · is the dot product computed mod 2 over the binary field GF(2) (bits 0 and 1 with addition mod 2). If x = y, then z·x = z·y and Bob accepts with probability 1. If x ≠ y, the two strings differ in some positions; cancelling the positions where they agree reduces the problem to whether a fresh random bit string z' has an even number of 1s when dotted with the all-1s vector, which happens with probability exactly 1/2. Repeating the test with fresh z drives the error to any desired level.

## Public versus private randomness

Allowing both parties to share a public random string is convenient. Any public-coin protocol can be simulated by a private-coin protocol with only O(log n) extra bits: fix a set of 100n candidate random strings beforehand, let Alice and Bob agree on one by index, and run the original protocol with that string. A Hoeffding-tail bound shows that with positive probability some such set reproduces the original protocol's success probability within 0.1 for every input pair (x,y), so the private-coin simulation has error probability at most 0.2 on every (x,y).

## Other variants

Yao's minimax principle connects randomized complexity to distributional complexity: the randomized cost of f equals the maximum over all input distributions μ of the cheapest deterministic protocol that errs on at most 1/3 of inputs drawn from μ. This lets one prove randomized lower bounds by designing a hard distribution; Razborov used this method to show that the disjointness function requires Ω(n) bits.

Information complexity measures, for a protocol with transcript Π on random inputs (X,Y) drawn from μ, the sum I(Π;Y|X) + I(Π;X|Y), capturing how much each party learns about the other's input. Braverman and Rao showed that the cost of solving n independent copies of f is roughly n times f's information complexity, mirroring how Shannon entropy gives amortized bit-length. Applied to set disjointness, this pins the exact randomized communication complexity at 1.4923…n bits.

Three quantum models exist: exchanging qubits over an optical channel, sharing unlimited prior entanglement, or combining both. Quantum correlations and the broader almost-quantum class are provably non-collapsing, meaning they do not let one bit of classical communication solve every Boolean function, while hypothetical devices called PR-boxes would collapse communication complexity to O(1).

The unbounded-error model accepts protocols whose answer correlates nontrivially with the truth, with success probability strictly above 1/2. Even here, Forster showed that inner product requires Ω(n) bits, and Alon, Frankl, and Rödl showed the same holds for almost every Boolean function.

## Lifting and the log-rank conjecture

Lifting translates a simple complexity measure into a stronger one by composing a hard function f with a small gadget g. Raz and McKenzie proved that a decision tree of depth Δ for f yields a protocol of cost Δ·D(g) for the composed function f∘g, and this is tight using the indexing gadget, where Alice's input picks one bit of Bob's much longer string. The technique separates the monotone NC hierarchy and has since been extended to randomized protocols, monotone circuits, proof complexity, and quantum settings.

A central open question is the log-rank conjecture: D(f) is polynomially related to log rank(M_f). For randomized protocols the analogous Log-Approximate-Rank Conjecture was refuted in 2019 by Chattopadhyay, Mande, and Sherif, so approximate rank is not the right yardstick for randomized communication complexity even on problems as simple as equality.

Source: adapted from "Communication complexity" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Communication_complexity
