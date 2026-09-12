# Exponentiation

## Overview

Exponentiation, denoted \( b^n \), is a binary mathematical operation with a base \( b \) and an exponent \( n \). When \( n \) is a positive integer, it represents repeated multiplication of the base: \( b^n = \underbrace{b \times b \times \cdots \times b}_{n \text{ times}} \). The operation extends naturally to zero, negative, fractional, real, and complex exponents while preserving key algebraic identities. Exponentiation underpins vast areas of mathematics and science, including compound interest, population models, wave mechanics, cryptography, and computational algorithms.

---

## Timeline

- **c. 250 BCE** — Archimedes proves the law of exponents \( 10^a \cdot 10^b = 10^{a+b} \) in *The Sand Reckoner*.
- **9th century** — Al-Khwarizmi uses terms *māl* (square) and *kaʿbah* (cube) for powers.
- **15th century** — Nicolas Chuquet introduces early exponential notation (e.g., \( 12x^2 \)).
- **1544** — Michael Stifel coins the term "exponent".
- **1636** — James Hume uses modern-style notation \( A^3 \).
- **1670s** — René Descartes formalizes superscript notation in *La Géométrie*.
- **1696** — Samuel Jeake introduces the term "indices".
- **1748** — Leonhard Euler introduces variable and non-integer exponents.
- **1914** — Leonardo Torres Quevedo proposes floating-point representation.
- **1938** — Konrad Zuse implements floating-point in the Z1 computer.

---

## Body

### Definition and Basic Properties

For positive integer exponents, exponentiation is defined as repeated multiplication:  
\[
b^n = \underbrace{b \times b \times \cdots \times b}_{n \text{ times}}
\]
This leads directly to the **multiplication rule**:  
\[
b^n \cdot b^m = b^{n+m}
\]
and the **power rule**:  
\[
(b^m)^n = b^{mn}
\]
These identities form the foundation for extending exponentiation beyond positive integers.

### Extension to All Integer Exponents

To preserve the multiplication rule, exponentiation is extended to zero and negative integers:

- **Zero exponent**: For any nonzero \( b \), \( b^0 = 1 \). This ensures consistency with \( b^0 \cdot b^n = b^n \).
- **Negative exponents**: Defined as reciprocals:  
  \[
  b^{-n} = \frac{1}{b^n}
  \]
  This maintains the additive property of exponents under multiplication.

The case \( 0^0 \) remains controversial—defined as 1 in combinatorics and algebra, but often left undefined in analysis.

### Fractional and Real Exponents

Fractional exponents generalize roots:
\[
b^{n/m} = \sqrt[m]{b^n}
\]
For example, \( b^{1/2} = \sqrt{b} \), since \( (b^{1/2})^2 = b \).

For real exponents, \( b^x \) (with \( b > 0 \)) is defined via continuity or logarithms:
\[
b^x = e^{x \ln b}
\]
This preserves all exponent rules and allows smooth interpolation between rational values.

### Complex Exponents

When the base is a positive real number and the exponent is complex (\( z = x + iy \)):
\[
b^z = e^{z \ln b} = b^x (\cos(y \ln b) + i \sin(y \ln b))
\]
using **Euler’s formula** \( e^{iy} = \cos y + i \sin y \).

For complex bases, exponentiation becomes multivalued due to the periodic nature of the complex logarithm. The **principal value** uses the principal branch of the logarithm, where the argument satisfies \( -\pi < \arg(z) \leq \pi \).

### Algebraic Structures and Generalizations

Exponentiation generalizes to abstract algebraic structures like **monoids**, **groups**, **rings**, and **fields**:

- In a **group**, \( x^n \) is defined for all integers \( n \), with \( x^{-n} = (x^{-1})^n \).
- In a **ring**, elements may be **nilpotent** (\( x^n = 0 \) for some \( n \)).
- In **finite fields** (\( \mathbb{F}_q \)), Fermat's Little Theorem gives \( x^q = x \), and the **Frobenius automorphism** \( x \mapsto x^p \) plays a central role.

### Applications in Computation and Science

- **Matrix exponentiation** models discrete dynamical systems (e.g., Markov chains): \( A^n x \) gives the state after \( n \) steps.
- **Linear operators** like differentiation can be iterated: \( \left(\frac{d}{dx}\right)^n f(x) = f^{(n)}(x) \).
- **Efficient computation** uses **exponentiation by squaring**, reducing \( n-1 \) multiplications to \( O(\log n) \).
- **Set theory**: \( S^T \) denotes the set of functions from \( T \) to \( S \), and \( |S^T| = |S|^{|T|} \).
- **Category theory**: Exponentials represent function spaces; Cartesian closed categories formalize this structure.

---

## Terms

- **Base**: The number \( b \) being multiplied in \( b^n \).
- **Exponent (or power)**: The number \( n \) indicating how many times the base is used in multiplication.
- **Monoidal exponentiation**: Extending exponentiation to associative structures with identity (monoids).
- **Nilpotent element**: An element \( x \) in a ring such that \( x^n = 0 \) for some positive integer \( n \).
- **Frobenius automorphism**: The map \( x \mapsto x^p \) in a finite field of characteristic \( p \).
- **Multivalued function**: A function that assigns multiple outputs to a single input (e.g., complex roots).
- **Principal value**: A specific choice among multiple possible values (e.g., principal branch of complex logarithm).
- **Cartesian closed category**: A category where morphisms between products behave like function spaces.
- **Tetration**: Iterated exponentiation, denoted \( {}^{n}a \), forming the basis of hyperoperations.
- **Indeterminate form**: Expressions like \( 0^0 \), \( 1^\infty \), or \( \infty^0 \) whose limits depend on context.

---

## Debates and Open Questions

- **\( 0^0 \)**: Whether it should equal 1, remain undefined, or depend on context (combinatorics vs. analysis) is debated.
- **Complex exponentiation identities**: Identities like \( (b^z)^t = b^{zt} \) fail for complex numbers unless restrictions apply, raising questions about consistent definitions.
- **Minimal addition chains**: Finding the shortest sequence of multiplications to compute \( b^n \) is computationally hard; no efficient general solution exists.
- **Continuity of complex roots**: No globally continuous nth-root function exists over the entire complex plane due to branch cuts.
- **Gelfond–Schneider theorem**: While it resolves transcendence for certain cases (\( b^x \) with algebraic \( b \neq 0,1 \) and irrational algebraic \( x \)), many related questions about transcendental numbers remain open.

Source: adapted from "Exponentiation" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Exponentiation
