# Fundamental theorem of arithmetic

The fundamental theorem of arithmetic states that every integer greater than 1 is either prime or can be represented as a product of prime numbers, and that this representation is unique up to the order of the factors. The theorem has two parts: existence (every such integer breaks into primes) and uniqueness (the primes and their multiplicities never change).

For example, $1200 = 2^4 \cdot 3^1 \cdot 5^2$. Any other prime decomposition of 1200 contains exactly four 2s, one 3, and two 5s, in some order, and no other primes.

The "up to order" qualification matters because reordering the factors is the only freedom. The requirement that factors be prime is essential: composite factors allow non-unique decompositions. For instance, $12 = 2 \cdot 6 = 3 \cdot 4$ are two distinct factorisations using composite numbers.

The theorem also explains why 1 is not prime. If 1 were prime, then $2 = 2 \cdot 1 = 2 \cdot 1 \cdot 1 = \ldots$ would not be unique. By convention, 1 is represented as the empty product of primes.

## Proof sketch

The proof rests on **Euclid's lemma**: if a prime $p$ divides a product $ab$, then $p$ divides $a$ or $p$ divides $b$ (or both). Euclid states this as Proposition 30 in Book VII of the *Elements*.

To show existence, use strong induction on $n$. If $n$ is prime, it is its own factorisation. If $n$ is composite, write $n = ab$ with $1 < a \le b < n$; by hypothesis both $a$ and $b$ factor into primes, and concatenating their prime lists gives a factorisation of $n$.

To show uniqueness, suppose some smallest integer $n$ has two distinct prime factorisations $n = p_1 p_2 \ldots p_j = q_1 q_2 \ldots q_k$. The prime $p_1$ divides the product $q_1 q_2 \ldots q_k$, so by Euclid's lemma $p_1$ divides some $q_i$. Since both are prime, $p_1 = q_i$. Cancelling $p_1$ from both sides leaves a smaller integer with two distinct factorisations, contradicting minimality.

## Canonical form and arithmetic

The unique representation of a positive integer $n$ as
$$n = p_1^{e_1} p_2^{e_2} \cdots p_k^{e_k}$$
with primes $p_1 < p_2 < \ldots < p_k$ and positive integer exponents is called the **canonical representation** or **standard form**. Examples: $999 = 3^3 \cdot 37$, $1000 = 2^3 \cdot 5^3$, $1001 = 7 \cdot 11 \cdot 13$. Allowing exponents to be zero extends this to an infinite product over all primes; allowing negative exponents yields a canonical form for positive rationals.

This representation makes several operations simple. For two positive integers $a$ and $b$ with exponents $a_i, b_i$ for the $i$-th prime, the product $a \cdot b$ uses $a_i + b_i$, the $\gcd(a,b)$ uses $\min(a_i, b_i)$, and the $\operatorname{lcm}(a,b)$ uses $\max(a_i, b_i)$. In practice, finding the prime factorisation of a large integer is far harder than computing products, GCDs, or LCMs, so these formulas mainly illuminate structure rather than speed computation. Many arithmetic functions, both additive and multiplicative, are defined by their values on prime powers, made possible by the uniqueness of the canonical form.

## Generalisations and limitations

The theorem generalises to other algebraic structures called **unique factorization domains (UFDs)**: principal ideal domains, Euclidean domains, and polynomial rings over a field. Gauss proved in 1832 that the Gaussian integers $\mathbb{Z}[i]$ form a UFD, with units $\pm 1, \pm i$. Eisenstein proved in 1844 that the Eisenstein integers $\mathbb{Z}[\omega]$ (with $\omega$ a primitive cube root of unity) form a UFD with six units.

Unique factorisation can fail. In $\mathbb{Z}[\sqrt{-5}]$,
$$6 = 2 \cdot 3 = (1 + \sqrt{-5})(1 - \sqrt{-5}),$$
two genuinely different factorisations. Here the element 2 is **irreducible** (not factorable into smaller non-units) but not **prime** (it divides a product without dividing either factor), so Euclid's lemma fails. This failure of unique factorisation in rings of algebraic integers was the source of errors in many attempted proofs of Fermat's Last Theorem during the 358 years between Fermat's statement and Wiles's proof.

## History

Euclid's *Elements* contains the necessary ingredients: Propositions 30, 31, and 32 of Book VII, including Euclid's lemma and the fact that every composite number has a prime divisor (proved by infinite descent), and Proposition 14 of Book IX, which shows that the least common multiple of given primes is not a multiple of any other prime, though it handles only exponents equal to one. Kamāl al-Dīn al-Fārisī later stated the full theorem for the first time, and Article 16 of Gauss's *Disquisitiones Arithmeticae* (1801) gave the first proof of uniqueness.

Source: adapted from "Fundamental theorem of arithmetic" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Fundamental_theorem_of_arithmetic
