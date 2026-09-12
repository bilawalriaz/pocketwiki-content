# Probability theory

Probability theory is the branch of mathematics that puts chance on a rigorous footing. It treats any random experiment as a set of possible outcomes, assigns each subset of those outcomes a number between 0 and 1, and requires those numbers to follow a small set of axioms. This axiomatic framing, completed in 1933 by Andrey Kolmogorov by combining Richard von Mises's notion of a sample space with measure theory, is the accepted foundation of the modern subject, though alternatives such as Bruno de Finetti's finite additivity exist.

## The basic objects

The set of all possible outcomes of an experiment is the **sample space**, written Ω. Any subset of Ω is an **event**: a collection of outcomes that may or may not occur. For a fair six-sided die, Ω = {1,2,3,4,5,6}, and "rolling an odd number" is the event {1,3,5}.

A **probability measure** assigns a number P(E) to each event E, obeying three rules: 0 ≤ P(E) ≤ 1; P(Ω) = 1, so the whole sample space is certain; and for any collection of mutually exclusive events (those sharing no outcomes, such as {1,6}, {3}, and {2,4}), the probability that at least one occurs equals the sum of their individual probabilities. So P({1,3,5}) = 3/6 = 1/2, and P({1,2,3,4,6}) = 5/6.

A **random variable** is a function from outcomes to numbers. Flipping a coin has outcomes "heads" and "tails", neither of which is a number, so a random variable X is defined by X(heads) = 0 and X(tails) = 1.

## Discrete and continuous distributions

A **probability distribution** describes how probability is spread across the values of a random variable.

**Discrete case.** The sample space is finite or countable. Each value x has a probability mass function f(x) satisfying 0 ≤ f(x) ≤ 1 and Σ f(x) = 1 over all x. The probability of an event E is then P(E) = Σ f(x) for x in E. The classical "favourable cases over total cases" rule is the special case where every elementary outcome is equiprobable: rolling an even number gives 3/6 = 1/2.

**Continuous case.** Outcomes lie on the real line or an interval, and individual points carry probability zero. Instead, a **cumulative distribution function** F(x) = P(X ≤ x) captures everything: it is non-decreasing, right-continuous, starts at 0 as x → −∞, and reaches 1 as x → ∞. When F is absolutely continuous (has no jumps), its derivative f(x) = dF/dx is a **probability density**, and P(X ∈ E) = ∫_E f(x) dx. Probability is now the area under a curve, not the height of a bar.

Some distributions fit neither mould. The Cantor distribution assigns no positive probability to any single point yet has no density. A variable that is 0 with probability 1/2 and otherwise normal can be handled using the Dirac delta function, a generalised spike that integrates to 1. Both are handled cleanly once probability is defined as a measure on a **σ-algebra** (a collection of subsets closed under complements and countable unions), the measure-theoretic treatment that unifies discrete, continuous, and exotic cases in a single framework.

## Convergence of random variables

Probability theory needs precise notions of what it means for a sequence X₁, X₂, … to "approach" a limit X, because ordinary numerical limits are not enough when randomness is involved. Three notions are standard, listed from weakest to strongest:

- **Convergence in distribution** (weak convergence): the cumulative distribution functions of the Xₙ converge to that of X wherever the latter is continuous.
- **Convergence in probability**: for every ε > 0, P(|Xₙ − X| ≥ ε) → 0 as n → ∞.
- **Almost sure convergence** (strong convergence): P(lim Xₙ = X) = 1.

Strong convergence implies convergence in probability, which implies convergence in distribution; the reverses do not always hold.

## Two landmark theorems

**Law of large numbers (LLN).** Toss a fair coin many times and the proportion of heads settles near 1/2; the more tosses, the closer it gets. The LLN formalises this: if X₁, X₂, … are independent and identically distributed with finite mean μ, then the sample average X̄ₙ = (1/n)Σ Xₖ converges to μ. The weak law says convergence in probability; the strong law says almost sure convergence. The LLN is not built into the axioms; it is derived from them, which is why it links abstract probabilities to observed frequencies.

**Central limit theorem (CLT).** Take any independent, identically distributed random variables with finite mean μ and variance σ² > 0, regardless of their original distribution. Standardise their sum by subtracting nμ and dividing by σ√n, and the resulting distribution approaches the standard normal. This explains why the bell curve appears so often in nature: averages of many small, independent effects look Gaussian even when the underlying variables do not. For distributions with heavy tails the convergence can be very slow, and a generalised version of the theorem is used instead.

## Where the theory reaches

Probability theory underpins statistics, so it shapes any activity that reasons from data. The same machinery describes complex systems known only partially, from statistical mechanics to sequential estimation. Twentieth-century physics revealed that phenomena at atomic scales are themselves probabilistic, though quantum mechanics relies on a different interpretation of probability than the Kolmogorov axioms. The subject's roots lie in Gerolamo Cardano's sixteenth-century analysis of games of chance, the problem of points solved by Pierre de Fermat and Blaise Pascal in the seventeenth century, Christiaan Huygens's 1657 treatise, and Pierre Laplace's classical definition in the nineteenth century.
