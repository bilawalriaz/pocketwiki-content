# Number theory

Number theory is the branch of mathematics devoted to studying the integers {…, −2, −1, 0, 1, 2, …} and arithmetic functions built from them, especially the prime numbers. It is one of the oldest branches of mathematics, alongside geometry, and is famous for statements that are simple to state but extremely hard to prove, such as Fermat's Last Theorem. Long treated as pure mathematics with no practical use, it became foundational for public-key cryptography in the 1970s, when the difficulty of factoring large numbers became the security of systems like RSA.

## Core ideas from elementary number theory

A central object is divisibility: a divides b if b = aq for some integer q. Euclid's division algorithm reduces any pair a, b to a remainder r, and the same procedure computes the greatest common divisor (gcd) of two integers, the largest integer dividing both. Two integers are coprime when their gcd is 1.

A prime is an integer greater than 1 whose only positive divisors are 1 and itself. Euclid proved there are infinitely many primes, and the sieve of Eratosthenes lists them by crossing out multiples. The Fundamental Theorem of Arithmetic says every integer greater than 1 factors into primes uniquely up to order. For example, 120 = 2³ · 3 · 5, and no other list of primes multiplies to 120.

Modular arithmetic studies integers up to a fixed modulus n, with a ≡ b (mod n) meaning n divides a − b. Working "mod 12" reproduces clock arithmetic, so 4 + 9 = 13 ≡ 1. Fermat's little theorem states that if p is prime and a is not a multiple of p, then a^(p−1) ≡ 1 (mod p). Euler extended this using the totient function φ(n), which counts the integers up to n that are coprime to n.

The Chinese remainder theorem, recorded in the *Sunzi Suanjing* between the 3rd and 5th centuries AD, solves systems of congruences with coprime moduli at once. Euclid's algorithm and this theorem are the workhorses of computational number theory.

## Analytic number theory

Analytic number theory uses calculus and the theory of complex numbers to estimate how many integers of a given type exist. Its central object is the prime-counting function π(x), the number of primes up to x. The prime number theorem, proved in 1896, says π(x) is asymptotic to x / log x, meaning their ratio tends to 1 as x grows. A sharper approximation uses the logarithmic integral li(x).

The Riemann zeta function ζ(s) = Σ 1/nˢ ties the distribution of primes to a single analytic object. Euler showed it equals an infinite product over primes, ζ(s) = Π (1 − p^(−s))^(−1), the first direct link between the function and prime distribution. Riemann extended ζ(s) to complex values of s and conjectured that every non-trivial zero has real part 1/2, the unsolved Riemann hypothesis. Proving it would directly sharpen knowledge of how primes are spread. In 1949, Erdős and Selberg found a proof of the prime number theorem that avoids complex analysis, though calling it "elementary" understates its difficulty.

## Algebraic number theory

Algebraic number theory generalises the integers. An algebraic number is a complex number that solves a polynomial with rational coefficients, and the full set of such solutions forms a number field. The simplest example is a + b√d, a quadratic field.

The motivation was failure of unique factorisation. In ℤ(√−5), the number 6 factors as 2 · 3 and also as (1 + √−5)(1 − √−5), and the two factorisations share no common prime factors. In the late nineteenth century, Kummer, Dedekind, and Kronecker independently patched this by enlarging the notion of factor, using ideal numbers, ideals, and valuations, three complementary responses to the same problem.

Class field theory, developed between about 1900 and 1950, classifies abelian extensions of number fields, the simpler class of field extensions. The Langlands program seeks to extend this classification to non-abelian extensions.

## Diophantine geometry and approximation

Diophantine geometry asks whether polynomial equations have integer or rational solutions, treating the solutions as geometric shapes. Finiteness of rational points on an algebraic curve depends on its genus, a topological invariant of the curve. Wiles's 1995 proof of Fermat's Last Theorem, building on work linking elliptic curves to modular forms, is a major result of this approach.

Diophantine approximation studies how well a real number x can be approximated by rationals a/q. Numbers that cannot be approximated as well as any algebraic number are transcendental; this argument showed that π and e are transcendental.

## History and open questions

The earliest trace of number theory is Plimpton 322, a Babylonian clay tablet from about 1800 BC listing Pythagorean triples, integer-sided right triangles whose layout hints at a generating identity. Diophantus's 3rd-century *Arithmetica* introduced what are now called Diophantine equations, and Brahmagupta began the systematic study of Pell's equation in 628 AD. Gauss's *Disquisitiones Arithmeticae* of 1801 set the field's modern agenda by proving quadratic reciprocity, developing quadratic forms, and introducing the congruence notation a ≡ b (mod n). Dirichlet proved his theorem on primes in arithmetic progressions in 1837, founding analytic number theory, and Riemann's 1859 work on the zeta function brought complex analysis into the subject.

Major open questions include the Riemann hypothesis, Goldbach's conjecture that every even number greater than 2 is a sum of two primes, the twin prime conjecture of infinitely many prime pairs differing by 2, and the Hardy–Littlewood conjectures on prime patterns. Fast primality tests are known, but no truly fast algorithm for factoring large integers is known, a gap public-key cryptography depends on.

Source: adapted from "Number theory" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Number_theory
