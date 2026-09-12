# Absolute value (algebra)

In algebra, an **absolute value** on a field or integral domain D is a function |·| from D to the real numbers that generalises the ordinary absolute value on ℝ. It assigns a nonnegative "size" to every element and must obey four axioms, which then force a metric, a notion of limits, and a completion of D.

## The four axioms

Let D be a field or integral domain. A function |·|: D → ℝ is an absolute value when, for all x and y in D:

1. **Non-negativity.** |x| ≥ 0.
2. **Positive definiteness.** |x| = 0 if and only if x = 0.
3. **Multiplicativity.** |xy| = |x|·|y|.
4. **Triangle inequality.** |x + y| ≤ |x| + |y|.

These axioms force several consequences. From 1 = 1·1, multiplicativity gives |1| = 1, hence |−1| = 1 and |−x| = |x|. Writing a positive integer n as the sum of n copies of 1 and applying the triangle inequality repeatedly gives |n| ≤ n, where the left-hand n denotes that sum in D and the right-hand n is the ordinary real number.

The standard absolute value on ℝ and the modulus |a + bi| = √(a² + b²) on ℂ both satisfy the axioms. The square of the real absolute value does not, because it fails the triangle inequality; that is why |x|² is not itself an absolute value.

## Examples

- **Real absolute value.** On ℤ, ℚ, or ℝ, |x| = x for x ≥ 0 and |x| = −x for x < 0.
- **Complex modulus.** On ℂ, |a + bi| = √(a² + b²) for real a, b.
- **p-adic absolute value.** Fix a prime p. For any nonzero rational x, write x = pⁿ·(a/b) with a, b coprime to p, and set |x|ₚ = p⁻ⁿ; also |0|ₚ = 0. This inverts the usual intuition: a rational divisible by a high power of p is *small* under |·|ₚ.
- **Trivial absolute value.** Set |0| = 0 and |x| = 1 for x ≠ 0. Every integral domain carries this, and it is the only absolute value on a finite field, since in a finite field every nonzero element is a root of unity and has some positive power equal to 1, forcing |x| = 1.

## Archimedean and non-Archimedean

If an absolute value satisfies the stronger rule |x + y| ≤ max(|x|, |y|) for all x, y, it is called **non-Archimedean** or **ultrametric**. Otherwise it is **Archimedean**. The real and complex absolute values are Archimedean; every p-adic absolute value is non-Archimedean. The ultrametric inequality is strictly stronger than the triangle inequality, and it follows that in any ultrametric the two largest of |x|, |y|, |x + y| are equal.

## Equivalent absolute values and places

Two absolute values |·|₁ and |·|₂ on D are **equivalent** if |x|₁ < 1 if and only if |x|₂ < 1 for every x. Any two equivalent nontrivial absolute values satisfy |x|₁^e = |x|₂ for some positive exponent e. Raising an absolute value to a power between 0 and 1 always yields another absolute value, but raising it to a power greater than 1 generally does not. An equivalence class of absolute values is called a **place**. The real absolute value and each p-adic absolute value on ℚ define different places, and **Ostrowski's theorem** says these are all of them: up to equivalence, the only nontrivial absolute values on ℚ are the usual one and |·|ₚ for each prime p.

## Valuations

For any non-Archimedean absolute value and any base b > 1, define ν(x) = −log_b |x| for x ≠ 0 and ν(0) = ∞, with ∞ ordered above every real number. Then ν maps D to ℝ ∪ {∞} and satisfies ν(x) = ∞ ⇔ x = 0, ν(xy) = ν(x) + ν(y), and ν(x + y) ≥ min(ν(x), ν(y)). This ν is called a **valuation**, and is essentially the logarithm of a non-Archimedean absolute value; some authors reverse the terminology.

## Completions

An absolute value defines a distance d(x, y) = |x − y|, and therefore a notion of Cauchy sequence: (xₙ) is Cauchy if |xₘ − xₙ| → 0 as m, n grow. Cauchy sequences form a ring under pointwise operations, and the **null sequences** (those with |aₙ| → 0) form a prime ideal in this ring. The quotient is an integral domain that contains D, called the **completion** of D with respect to |·|. Taking ℚ with the p-adic absolute value gives the p-adic numbers ℚₚ, while taking ℚ with the usual absolute value gives ℝ, the same idea that fills the gaps of ℚ with limits of Cauchy sequences.

A second theorem of Ostrowski states that any field complete with respect to an Archimedean absolute value is isomorphic to ℝ or ℂ, with the absolute value equivalent to the usual one.

Source: adapted from "Absolute value (algebra)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Absolute_value_%28algebra%29
