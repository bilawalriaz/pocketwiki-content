# Number

A number is a mathematical object used to count, measure, and label. It is distinct from the word or symbol used to write it: "eleven" and "11" name the same number. Writing happens through numerals arranged in a numeral system, almost always today the Hindu–Arabic decimal system, whose power comes from place value and a working zero.

## How the concept grew

Humans first recorded numbers as tally marks on bone, possibly as early as 40,000 years ago. Tallying can record counts but cannot express place value, so it could not compactly represent large numbers. The breakthrough was positional notation, where a digit's position sets its value. Mesopotamia developed a base-60 (sexagesimal) positional system around 3400 BC, the earliest unambiguous numerals; Egypt used an early base-10 system by 3100 BC; and India produced the modern decimal place-value system, including a true zero as a number, by around AD 500. Brahmagupta's *Brāhmasphuṭasiddhānta* (AD 628) is the first text to treat zero as a number on equal footing with others and to lay out rules for arithmetic with it, including the undefined case of division by zero. By the late 14th century Hindu–Arabic numerals had replaced Roman numerals across Europe.

The idea of "number" itself expanded with each problem mathematicians met. To allow debts and subtraction to always work, negative numbers were introduced; recognized in China by 100–50 BC (red and black counting rods), used by Brahmagupta for the quadratic formula, but resisted in Europe until the 17th century, where Descartes called them "false" and Chuquet "absurd." To measure lengths like √2, irrationals were accepted; Hippasus, a Pythagorean, first proved √2 irrational, and the Babylonians had already approximated it to six decimal places. To make analysis rigorous, real numbers were given formal definitions only in the late 19th century by Weierstrass, Heine, Dedekind, Cantor, and Méray. To solve every polynomial, complex numbers, of the form a + bi with i² = −1, were forced on mathematicians by 16th-century cubic and quartic formulas; Descartes labeled them "imaginary" in 1637, and acceptance arrived with Wessel's geometric interpretation in 1799 and Euler's formula e^{iπ} + 1 = 0, which ties e, i, π, 1, and 0 into one identity.

Infinity sits alongside this history but is not itself a number. Aristotle separated *actual* from *potential* infinity, and Cantor's 19th-century set theory introduced transfinite cardinals and ordinals that let mathematicians compare the sizes of infinite sets. Robinson's 1960s hyperreal numbers made infinitesimals mathematically rigorous.

## The standard hierarchy

Modern number systems nest, each enlarging the last to close a gap:

ℕ ⊂ ℤ ⊂ ℚ ⊂ ℝ ⊂ ℂ.

- **Natural numbers (ℕ):** the counting numbers. Whether 0 belongs is a convention (ℕ₀ vs ℕ₁). They can be built formally from set theory or Peano arithmetic, a system that defines each natural as zero or a successor of zero.
- **Integers (ℤ):** naturals plus their negatives, written as a + (−a). They form a ring, a structure where addition and multiplication behave predictably; the Z comes from German *Zahl*.
- **Rationals (ℚ):** fractions m/n with integer numerator and nonzero integer denominator. In decimal form, rationals are exactly the eventually repeating decimals.
- **Reals (ℝ):** every point on the continuous number line, including irrationals such as √2, e ≈ 2.71828, and π. The reals have the *least upper bound* property: any nonempty set bounded above has a smallest upper bound. Every complete ordered field, meaning a number line with no gaps that supports arithmetic and ordering, is isomorphic to ℝ, so there is essentially one such structure.
- **Complex numbers (ℂ):** a + bi, where i² = −1. They form an algebraically closed field, a system in which every polynomial factors completely, but they cannot be ordered in a way that respects arithmetic, so "less than" does not apply. They are essential to quantum mechanics and widespread across physics and engineering.

## Two ideas that recur

**Algebraic vs. transcendental.** A real or complex number is *algebraic* if it solves some polynomial with integer coefficients (so every rational is algebraic). A *transcendental* number is not algebraic: it solves no such polynomial. Liouville established that transcendental numbers exist (1844–1851), Hermite proved e transcendental (1873), and Lindemann proved π transcendental (1882). Cantor later showed that almost all reals are transcendental, even though explicit examples are rare.

**Primes.** A prime is a natural number greater than 1 that is not the product of two smaller positive integers. Euclid proved primes are infinite and that every integer factors uniquely into primes (the fundamental theorem of arithmetic). Primes now underpin cryptography, hashing, and error-detection codes. Legendre conjectured the prime number theorem, the density of primes near N is about 1 / ln N, which Hadamard and de la Vallée-Poussin proved in 1896. Goldbach's conjecture (every even number above 2 is a sum of two primes) and the Riemann hypothesis (a statement about the zeros of ζ(s) that controls prime distribution) remain unproven.

## Extensions beyond ℂ

Several constructions enlarge the rationals or reals in different directions:

- **p-adic numbers** extend leftward infinitely in a prime base p and contain ℚ, but they are not a subfield of ℂ. They are useful in number theory.
- **Quaternions, octonions, sedenions** come from the Cayley–Dickson construction. Quaternions (used for 3D rotations) are non-commutative: ab ≠ ba in general. Octonions are also non-associative. Each step loses one algebraic property.
- **Constructible numbers** are those reachable from 0 and 1 with straightedge and compass; a regular n-gon is constructible exactly when n is a product of a power of 2 and distinct Fermat primes.
- **Computable numbers** are those whose digits some algorithm can produce. Equality of two computable numbers is undecidable in general, and almost all reals are non-computable.
- **Transfinite, hyperreal, superreal, and surreal numbers** add infinities and infinitesimals while remaining fields, used in set theory and nonstandard analysis.

## Mental model

A number is whatever a recognized system treats as one, and the systems grew by closing gaps: ℕ cannot represent debts, so ℤ is added; ℤ cannot represent √2, so ℝ is added; ℝ cannot factor every polynomial, so ℂ is added. Each enlargement keeps the previous one inside it. Everything else, primes, transcendentals, p-adics, quaternions, is a specialized structure layered on this single, expanding idea.

Source: adapted from "Number" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Number
