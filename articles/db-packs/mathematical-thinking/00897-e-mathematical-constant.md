# E (mathematical constant)

The number **e** (≈ 2.71828) is the unique positive base whose exponential function is its own derivative. Because **d/dx eˣ = eˣ**, the slope of *eˣ* at any point equals the height of the curve there. No other positive base has this property, which is why *e* is the natural language of calculus, growth, and probability.

## What e is

Several equivalent definitions converge on the same number:

- **Compound interest limit**: *e* is what *(1 + 1/n)ⁿ* approaches as compounding intervals become infinitely fine. Starting with $1 at 100% annual interest, the maximum you can earn is *e* dollars, no matter how often interest is added.
- **Reciprocal-factorial series**: *e = 1 + 1 + 1/2! + 1/3! + 1/4! + ...*
- **Derivative definition**: *e* is the unique base for which *d/dx eˣ = eˣ* and the integral from 1 to *e* of 1/x equals 1.

The function *Keˣ* is the general solution to *y' = y*. Any quantity whose rate of change equals itself grows or decays exponentially, with *K* set by the starting value and the sign of the growth rate.

## Where e comes from

Jacob Bernoulli isolated the constant in 1683 by asking what happens to compound interest as compounding becomes continuous. Huygens had already calculated its base-10 logarithm without recognising the base. Euler introduced the symbol *e* around 1727–28 (the reason is unknown) and published it in *Mechanica* in 1736. Euler proved the series representation and showed *e* is irrational. Hermite proved in 1873 that *e* is transcendental, meaning it is not the root of any polynomial with rational coefficients. As of 2023, 35 trillion digits have been computed.

## Why e is everywhere

**Growth and decay.** A quantity whose change rate is proportional to its size follows *x(t) = x₀eᵏᵗ*. The time constant *τ = 1/k* is the time to grow by a factor of *e*.

**Probability.** In *n* independent trials each with a 1/*n* chance of success, the probability of no successes is *(1 − 1/n)ⁿ*, which approaches **1/e ≈ 36.79%** as *n* grows. The same limit governs the derangement problem: the chance that no one gets their own hat back is also 1/e, and the number of derangements of *n* items is roughly *n!/e*.

**The normal distribution.** The bell curve is *φ(x) = (1/√(2π)) e^(−x²/2)*. The factor *e^(−x²/2)* shapes the tails; the constant *1/√(2π)* keeps the total area equal to 1.

**Factorials.** Stirling's formula, *n! ≈ √(2πn) (n/e)ⁿ*, uses *e* to approximate how many ways *n* distinct objects can be arranged.

**Euler's identity.** Extending *eˣ* to complex numbers via its Taylor series gives Euler's formula, *e^(ix) = cos x + i sin x*. Setting *x = π* yields *e^(iπ) + 1 = 0*, a single equation that links 0, 1, π, *i*, and *e*. The same machinery produces *cos x = (e^(ix) + e^(−ix))/2*, *sin x = (e^(ix) − e^(−ix))/(2i)*, and de Moivre's rule *(cos x + i sin x)ⁿ = cos nx + i sin nx*.

**Information theory.** Entropy for a discrete distribution is *H = −Σ pᵢ ln pᵢ*, measured in nats. The single-outcome contribution *−x ln x* is maximised at *x = 1/e*, so the most "informative" single event has probability 1/e.

**Optimisation.** The function *x^(1/x)* peaks at *x = e*, which is why the optimal number of equal pieces to break a stick of length *L* into (to maximise their product) is roughly *L/e*. Infinite towers *x^(x^(x^…))* converge only when *x* lies in *[e^(−e), e^(1/e)] ≈ [0.0660, 1.445]*.

## Key properties

- **Irrational and transcendental**: *e* is not a ratio of integers, and not a root of any rational-coefficient polynomial. Its irrationality measure is exactly 2.
- **Inequalities**: For positive *x*, *(1 + 1/x)ˣ < e < (1 + 1/x)^(x+1)*. For real *x*, *eˣ ≥ x + 1*, with equality only at *x = 0*; *e* is the only base for which this holds universally.
- **Continued fraction**: *e = [2; 1, 2, 1, 1, 4, 1, 1, 6, 1, ...]*, with even terms following the pattern *2n*.
- **Stochastic meaning**: If uniform random numbers in [0,1] are summed until the sum exceeds 1, the expected count of draws needed equals *e*.

**Micro-glossary.** A *transcendental number* is not a root of any non-zero polynomial with rational coefficients. A *natural logarithm* is the inverse of *eˣ*. A *Bernoulli trial* is an independent yes/no experiment with fixed success probability. A *derangement* is a permutation where no item stays in its original place.

## Open questions

It is conjectured that *e* is a *normal number* (digits uniformly distributed in every base), and that *e* is *not* a *period* (an integral of an algebraic function over an algebraic region), unlike π. Whether *e* and π are algebraically independent follows from Schanuel's conjecture, which remains unproven.

Source: adapted from "E (mathematical constant)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/E_%28mathematical_constant%29
