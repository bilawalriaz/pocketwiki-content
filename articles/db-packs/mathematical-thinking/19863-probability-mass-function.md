# Probability mass function

A probability mass function (PMF) gives the probability that a discrete random variable $X$ takes a specific value. A variable is discrete when it jumps between isolated, countable outcomes, so asking "what is the chance that $X$ equals exactly this number?" makes sense. Formally,

$$p_X(x) = P(X = x), \qquad -\infty < x < \infty,$$

with $p$ taking values in $[0, 1]$. The value of $x$ with the largest probability is called the *mode*. A PMF characterises the discrete distribution, in the same way a PDF characterises a continuous one.

## Two rules

Every PMF satisfies:

1. **Non-negativity:** $p_X(x) \geq 0$ for every $x$.
2. **Unit total:** $\displaystyle \sum_{x} p_X(x) = 1$.

Probability behaves like physical mass: it cannot be negative, and the total amount is conserved across all possible outcomes. For any $x$ outside the values $X$ can actually take, $p_X(x) = 0$. Because the support of a discrete variable is countable, the PMF is nonzero at only countably many points and is zero elsewhere, which makes it discontinuous.

## PMF versus PDF

A PMF returns a probability directly. A continuous probability density function (PDF) does not; it must be integrated over an interval to give a probability. For a continuous variable, $P(X = x) = 0$ at every single point, even though those points can still occur. For a discrete variable, $P(X = x) = 1$ means the event is certain, and $P(X = x) = 0$ means it is impossible, so points are the only setting where a single value carries genuine probability mass.

## Common finite examples

**Bernoulli, Ber(p).** A single trial with two outcomes, encoded as 1 and 0:

$$p_X(x) = \begin{cases} p & \text{if } x = 1, \\ 1-p & \text{if } x = 0. \end{cases}$$

A fair coin toss with "tails" = 0 and "heads" = 1 gives $p_X(0) = p_X(1) = 1/2$ and $p_X(x) = 0$ otherwise.

**Binomial.** Number of successes in $n$ independent trials with success probability $p$:

$$p_X(k) = \binom{n}{k} p^{k} (1-p)^{n-k}, \qquad k = 0, 1, \dots, n.$$

Rolling a fair die three times and asking the probability of exactly one 6 has $n = 3$, $p = 1/6$.

**Geometric.** Number of independent trials needed for the first success, with success probability $p$:

$$p_X(k) = (1-p)^{k-1} p, \qquad k = 1, 2, 3, \dots$$

Tossing a fair coin until the first heads illustrates it: $p = 1/2$, and $k$ counts tosses.

A fair die is itself a PMF, with each face in $\{1, 2, 3, 4, 5, 6\}$ receiving probability $1/6$.

## Infinite example

A PMF can have countably many outcomes. The distribution

$$\Pr(X = i) = \frac{1}{2^{i}}, \qquad i = 1, 2, 3, \dots$$

places $1/2$ on 1, $1/4$ on 2, $1/8$ on 3, and so on. The geometric series $1/2 + 1/4 + 1/8 + \cdots$ sums to 1, so the unit-total rule still holds.

## Joint PMFs

For two or more discrete variables $X_1, X_2, \dots$, a joint PMF assigns a probability to every combination of values:

$$p(x_1, x_2, \dots) = P(X_1 = x_1, X_2 = x_2, \dots),$$

and must satisfy non-negativity and unit-sum across the whole joint grid. The categorical distribution extends Bernoulli to two or more unordered categories in a single trial, and the multinomial extends the binomial to several categories across $n$ trials, listing a probability for every joint outcome.

## Measure-theoretic view

A PMF can be defined rigorously as the Radon–Nikodym derivative of the distribution of $X$ with respect to the counting measure, so for any value $b$ in the image of $X$,

$$P(X = b) = \int_{\{b\}} f\, d\mu = f(b).$$

This guarantees that the PMF recovers each single-point probability and that the unit-total rule holds across all singletons in the support of $X$.

Source: adapted from "Probability mass function" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Probability_mass_function
