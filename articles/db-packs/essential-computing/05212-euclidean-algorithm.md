# Euclidean algorithm

The Euclidean algorithm finds the greatest common divisor (GCD) of two integers, the largest number that divides both with no remainder. It is one of the oldest algorithms in regular use, described by Euclid around 300 BC.

## The core idea

The GCD of two numbers does not change if the larger is replaced by its difference with the smaller. Since 21 divides both 252 and 105, and 252 − 105 = 147, the GCD of 252 and 105 equals the GCD of 147 and 105. Each step shrinks the larger number, so repeating eventually makes the two equal; that common value is the GCD.

Replacing by difference is slow when one number is much larger. The practical version replaces the larger by its remainder after division by the smaller: `r(k) = r(k−2) mod r(k−1)`. The remainders strictly decrease, so the sequence must reach zero. The last nonzero remainder is the GCD.

Worked example with a = 1071, b = 462:

| Step | Equation                          | Remainder |
|------|-----------------------------------|-----------|
| 0    | 1071 = 2 × 462 + 147              | 147       |
| 1    | 462 = 3 × 147 + 21                | 21        |
| 2    | 147 = 7 × 21 + 0                  | 0         |

So gcd(1071, 462) = 21.

## Why it terminates and is correct

Two properties suffice:

1. gcd(x, 0) = x, since every divisor of x also divides 0.
2. gcd(x, y) = gcd(y, x − zy) for any integer z. If d divides x and y, then d divides x − zy; conversely, if d divides y and x − zy, then d divides (x − zy) + zy = x.

Each step leaves the GCD invariant (property 2), and the remainders strictly decrease, so the process terminates. At termination the pair is (g, 0), and property 1 gives g as the GCD.

## Bézout's identity and the extended algorithm

By reversing the steps, the GCD can be written as a linear combination of the original numbers: g = sa + tb for some integers s and t. For the example, 21 = (−2) × 252 + 5 × 105. The extended Euclidean algorithm tracks two extra sequences of coefficients while running the main algorithm, producing s and t directly. This identity underlies modular inverses and RSA cryptography.

## Applications

The algorithm supports many computations:

- Simplifying fractions by dividing numerator and denominator by their GCD.
- Modular arithmetic, including finding multiplicative inverses needed in RSA.
- Solving linear Diophantine equations ax + by = c, which has integer solutions only when gcd(a, b) divides c.
- The Chinese remainder theorem, reconstructing an integer from its remainders modulo coprime moduli.
- Continued fraction expansions, where the quotients q₀, q₁, … give a/b = [q₀; q₁, q₂, …]. For 1071/462 this yields [2; 3, 7].
- Integer factorization methods such as Pollard's rho, which repeatedly compute GCDs.
- Proving theorems in number theory, including unique prime factorization.

## Efficiency

Gabriel Lamé proved in 1844 that the number of division steps is at most five times the number of base-10 digits of the smaller input, the first result of what became computational complexity theory. The worst case occurs for consecutive Fibonacci numbers, which produce the smallest inputs requiring a given number of steps.

A key advantage is that the algorithm stays efficient on very large numbers, while factoring those same numbers is believed to be computationally hard. The security of RSA depends on this gap between easy GCD and hard factorization.

## Generalizations

In the 19th century the algorithm was extended from natural numbers to Gaussian integers and polynomials, leading Dedekind to define a Euclidean domain: any number system with a division-with-remainder operation where the same descent argument gives a GCD.

Source: adapted from "Euclidean algorithm" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Euclidean_algorithm
