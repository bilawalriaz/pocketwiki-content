# E (mathematical constant)

## Overview
The number **e** (≈ 2.71828) is a fundamental mathematical constant serving as the base of the natural logarithm and the natural exponential function. It is unique in that the function *eˣ* is its own derivative and integral, making it the natural choice for calculus involving rates of change. Discovered by Jacob Bernoulli in 1683 while studying compound interest, it was later analyzed extensively by Leonhard Euler, who introduced the symbol *e*. The constant is both **irrational** (cannot be a ratio of integers) and **transcendental** (not a root of any non-zero polynomial with rational coefficients). It appears pervasively across mathematics, linking the five fundamental constants 0, 1, π, *i*, and *e* in Euler's identity (*eⁱᵖ + 1 = 0*).

## Timeline
- **1618** — First calculations involving *e* (natural logarithms) published in an appendix to John Napier's work on logarithms; likely computed by William Oughtred.
- **1661** — Christiaan Huygens computes the base-10 logarithm of *e* geometrically but does not recognize *e* as a distinct constant.
- **1683** — Jacob Bernoulli discovers the constant explicitly as the limit of *(1 + 1/n)ⁿ* while solving the problem of continuous compound interest.
- **1690–1691** — Gottfried Leibniz uses the letter *b* to denote the constant in letters to Huygens.
- **1727–1728** — Leonhard Euler begins using the letter *e* for the constant in unpublished work and a letter to Christian Goldbach.
- **1736** — First printed appearance of the symbol *e* in Euler's *Mechanica*.
- **1737** — Euler proves *e* is the sum of the infinite series *∑ 1/n!* and demonstrates its irrationality via continued fractions.
- **1873** — Charles Hermite proves *e* is transcendental (first such proof for a non-constructed number).
- **2023 Dec 24** — Jordan Ranous computes a record 35 trillion digits of *e*.

## Body

### Definitions and Characterizations
The number *e* admits several equivalent definitions. It is the limit of the compound interest expression: **limₙ→∞ (1 + 1/n)ⁿ**. It is the sum of the infinite series of reciprocal factorials: **e = ∑ₙ₌₀^∞ 1/n! = 1 + 1 + 1/2! + 1/3! + ...**. It is the unique positive number *a* such that the derivative of *aˣ* at *x=0* is 1, or equivalently, the base for which **d/dx eˣ = eˣ**. It is the value of the natural exponential function at 1: **e = exp(1)**, where *exp* is the unique function equal to its own derivative with *exp(0)=1*. Finally, it is defined by the integral **∫₁ᵉ (1/x) dx = 1**, making it the base of the natural logarithm *ln(x)*.

### History
The constant emerged implicitly in 1618 in a table of natural logarithms appended to Napier's work, though the concept of a logarithmic base did not yet exist. Christiaan Huygens later calculated log₁₀(*e*) without identifying the base itself. Jacob Bernoulli isolated the constant in 1683 by investigating the limit of compounding interest as intervals approach infinity. Leibniz denoted it *b* in correspondence (1690–91). Euler adopted *e* in 1727–28 (reason unknown) and established its modern notation in *Mechanica* (1736). Euler proved the series representation and irrationality; Hermite proved transcendence in 1873.

### Applications

**Compound Interest**
Bernoulli's original problem: $1 at 100% annual interest compounded *n* times yields $(1 + 1/n)ⁿ$. As *n* increases (annual → monthly → daily), the value approaches *e* ($2.71828...). Continuous compounding yields *eᴿᵗ* for principal $1, rate *R*, time *t*.

**Probability: Bernoulli Trials and Derangements**
In a slot machine with win probability 1/*n* played *n* times, the probability of zero wins is *(1 - 1/n)ⁿ → 1/e* (≈ 36.79%) as *n→∞*. In the **derangement (hat check) problem**, the probability that no guest receives their own hat is *pₙ = ∑ₖ₌₀ⁿ (-1)ᵏ/k!*, which also approaches **1/e**. The number of derangements is *n!/e* rounded to the nearest integer.

**Exponential Growth and Decay**
Processes where the rate of change is proportional to the current quantity follow *x(t) = x₀ eᵏᵗ*. Here *k* is the growth constant; if negative, it models decay. The time constant *τ = 1/k* is the time to grow by a factor of *e*.

**Standard Normal Distribution**
The probability density function is *φ(x) = (1/√2π) e⁻ˣ²/²*. The factor *e⁻ˣ²/²* ensures the characteristic bell shape; the normalization constant *1/√2π* ensures total area = 1.

**Optimization (Steiner's Problem)**
The function *f(x) = x¹/ˣ* (or equivalently *x⁻¹ log_b x*) attains its global maximum at **x = e**. This solves the problem of breaking a stick of length *L* into *n* equal parts to maximize the product of lengths: optimal *n* is ⌊L/e⌋ or ⌈L/e⌉. This relates to the secretary problem and entropy maximization.

**Asymptotics (Stirling's Formula)**
*e* appears in the asymptotic approximation of the factorial: **n! ~ √(2πn) (n/e)ⁿ**. Consequently, *e = limₙ→∞ n / ⁿ√n!*.

### Properties

**Calculus**
*e* is the unique base simplifying calculus. For *y = aˣ*, the derivative is *aˣ limₕ→₀ (aʰ - 1)/h*. The limit equals *ln(a)*; only for *a=e* is it 1, yielding **d/dx eˣ = eˣ**. Similarly, **d/dx ln x = 1/x**. The Taylor series follows from *eˣ* being its own derivative with value 1 at 0: **eˣ = ∑ xⁿ/n!**. The function *Keˣ* is the general solution to the differential equation *y' = y*.

**Inequalities**
For all positive *x*: **(1 + 1/x)ˣ < e < (1 + 1/x)ˣ⁺¹**. For all real *x*: **eˣ ≥ x + 1**, with equality only at *x=0*. *e* is the unique base for which *aˣ ≥ x+1* holds universally.

**Exponential-like Functions**
*   *x¹/ˣ* max at *x=e*.
*   *xˣ* min at *x=1/e*.
*   Infinite tetration *xˣˣ^...* converges iff *x ∈ [e⁻ᵉ, e¹/ᵉ] ≈ [0.066, 1.445]* (Euler).

**Number Theory**
*e* is **irrational** (Euler, via infinite continued fraction) and **transcendental** (Hermite, 1873, via Lindemann–Weierstrass theorem). It was the first "natural" constant proven transcendental. Its irrationality measure *μ(e) = 2* is known exactly. Open questions: algebraic independence of *e* and *π* (implied by Schanuel's conjecture); whether *e* is **normal** (digits uniformly distributed in any base); whether *e* is a **period** (integral of algebraic function over algebraic domain)—conjectured not, unlike *π*.

**Complex Numbers**
The Taylor series converges for all complex *x*, defining *eᶻ*. Combining with series for *sin* and *cos* yields **Euler's formula: eⁱˣ = cos x + i sin x**. Setting *x=π* gives **Euler's identity: eⁱᵖ + 1 = 0**. This implies *ln(-1) = iπ* and **de Moivre's formula**: *(cos x + i sin x)ⁿ = cos nx + i sin nx*. Trigonometric functions are expressed as *cos x = (eⁱˣ + e⁻ⁱˣ)/2*, *sin x = (eⁱˣ - e⁻ⁱˣ)/(2i)*.

**Entropy**
In information theory, the entropy of a partition is *H(ξ) = -∑ p(Aᵢ) ln p(Aᵢ)*. The contribution function *f(x) = -x ln x* is maximized at **x = 1/e**. Thus, an outcome with probability **1/e ≈ 36.8%** contributes maximum entropy (measured in **nats**); more certain or rarer events contribute less.

### Representations
Beyond the limit and series, *e* has a regular **simple continued fraction**: *e = [2; 1, 2, 1, 1, 4, 1, 1, 6, 1, ..., 1, 2n, 1, ...]*. An **infinite product**: *e = (2/1)(4/3)¹/²(6·8/5·7)¹/⁴...*. **Stochastic representation**: Let *Xᵢ* be uniform [0,1] random variables; let *V = min{n : ∑ᵢ₌₁ⁿ Xᵢ > 1}*. Then **E(V) = e**.

### Computing Digits
The series *∑ 1/k!* converges rapidly. Modern computation uses **binary splitting** on the series to achieve *O(n log² n)* complexity. As of 2023, 35 trillion digits are known. In software, *e* is hard-coded (e.g., Python `math.e`), but `exp(x)` is preferred over `pow(e, x)` for numerical stability and speed.

## Terms
- ****Transcendental number**** — A real or complex number that is not a root of any non-zero polynomial with rational coefficients.
- ****Natural logarithm (ln)**** — The logarithm to base *e*; the inverse function of *eˣ*, defined by *∫₁ˣ (1/t) dt*.
- ****Compound interest**** — Interest calculated on the initial principal and also on the accumulated interest of previous periods.
- ****Bernoulli trial**** — A random experiment with exactly two outcomes ("success" and "failure") and constant probability of success.
- ****Derangement**** — A permutation of a set where no element appears in its original position (the "hat check problem").
- ****Exponential growth/decay**** — A process where the rate of change of a quantity is proportional to the quantity itself (*dx/dt = kx*).
- ****Stirling's formula**** — An asymptotic approximation for factorials: *n! ~ √(2πn) (n/e)ⁿ*.
- ****Euler's formula**** — *eⁱˣ = cos x + i sin x*, linking exponential and trigonometric functions in the complex plane.
- ****Entropy (information theory)**** — Expected information content; for a discrete distribution, *H = -∑ pᵢ ln pᵢ* (measured in nats).
- ****Continued fraction**** — An expression of a number as an integer plus a reciprocal, iteratively; *e* has the pattern *[2; 1, 2, 1, 1, 4, 1, 1, 6, ...]*.

## Debates and open questions
1.  **Algebraic independence of *e* and *π*:** It is unknown whether a non-zero polynomial with rational coefficients exists such that *P(e, π) = 0*. Schanuel's conjecture implies they are independent.
2.  **Normality of *e*:** It is conjectured but unproven that the digits of *e* are uniformly distributed in every base (i.e., *e* is a normal number).
3.  **Period status:** It is conjectured that *e* is **not** a period (an integral of an algebraic function over an algebraic domain), unlike *π*.
4.  **Reason for Euler's notation:** It is unknown why Euler chose the letter *e* (possibly "exponential," or simply the next vowel after *a* used for other constants).

Source: adapted from "E (mathematical constant)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/E_%28mathematical_constant%29
