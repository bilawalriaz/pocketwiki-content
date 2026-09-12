# Series (mathematics)

## Overview

A series is the sum of infinitely many terms arranged in order, formally defined as the limit of its partial sums. Series are foundational in calculus and mathematical analysis, with applications across physics, computer science, statistics, and finance. Their study evolved from ancient paradoxes about infinity to rigorous 19th-century frameworks involving limits, convergence, and topological structures.

## Timeline

- **c. 250 BCE**: Archimedes uses infinite series in quadrature of the parabola
- **1350 CE**: Kerala school studies series expansions for trigonometric functions
- **1360**: Nicole Oresme proves divergence of the harmonic series
- **1668**: James Gregory introduces convergence/divergence terminology
- **1715**: Brook Taylor provides general method for Taylor series
- **1812**: Gauss publishes convergence criteria for hypergeometric series
- **1821**: Cauchy insists on strict convergence tests; develops power series theory
- **1826**: Abel corrects Cauchy's conclusions on binomial series
- **1829**: Dirichlet handles Fourier series convergence scientifically
- **1854**: Riemann improves Dirichlet's trigonometric series treatment
- **1889**: Pringsheim presents most complete general convergence theory

## Body

### Definition and Basic Concepts

A series is an infinite sum $a_0 + a_1 + a_2 + \cdots$ or $\sum_{k=0}^{\infty} a_k$, where terms come from a sequence of numbers, functions, matrices, or other addable objects. The nth partial sum $s_n = \sum_{k=0}^{n} a_k$ represents the finite sum of the first $n+1$ terms. A series converges if the sequence of partial sums approaches a limit; otherwise it diverges. The sum of a convergent series equals $\lim_{n\to\infty} s_n$.

### Convergence and Divergence

The nth-term test states that if $\lim_{n\to\infty} a_n \neq 0$, the series diverges. For non-negative term series, convergence is equivalent to bounded partial sums. Key convergence tests include: direct comparison (bounding by known convergent series), limit comparison, ratio test (comparing successive term ratios to geometric series), root test, and integral test (comparing to improper integrals).

### Absolute and Conditional Convergence

A series converges absolutely if $\sum |a_n|$ converges. Absolute convergence implies convergence and allows arbitrary rearrangement without changing the sum. Series that converge but not absolutely are conditionally convergent. The Riemann series theorem states that any conditionally convergent real series can be rearranged to converge to any real number or diverge. The alternating harmonic series $\sum (-1)^{n+1}/n = \ln 2$ exemplifies this, converging conditionally while $\sum 1/n$ diverges.

### Operations on Series

Series form algebraic structures: addition is termwise $(a_k + b_k)$, scalar multiplication is termwise $(ca_k)$, and multiplication uses the Cauchy product $c_k = \sum_{j=0}^{k} a_j b_{k-j}$. These operations make convergent series a vector space, and absolutely convergent series a commutative ring (or algebra with scalar multiplication).

### Special Series Types

Geometric series $\sum ar^n$ converge to $a/(1-r)$ when $|r|<1$. Telescoping series $\sum (b_n - b_{n+1})$ converge to $b_1 - L$ when $b_n \to L$. Arithmetico-geometric series combine arithmetic and geometric progressions. Dirichlet series $\sum a_n/n^s$ connect to analytic number theory via the Riemann zeta function.

### Function Series

Power series $\sum a_n(x-c)^n$ converge within a radius of convergence, uniformly on compact subsets. Taylor series represent functions as power series. Formal power series treat the sum symbolically without convergence concerns, useful in combinatorics. Laurent series allow negative exponents, converging in annuli. Trigonometric series, especially Fourier series, expand functions in sine/cosine terms.

### Summation Methods for Divergent Series

Generalized summation methods extend classical sums to divergent series: Cesàro summation averages partial sums, Abel summation uses analytic continuation, and Borel summation applies analytic techniques. The Silverman-Toeplitz theorem characterizes matrix summation methods.

### Advanced Topics

Series generalize to arbitrary index sets $I$, requiring topological structures for convergence. In Banach spaces, absolute convergence implies unconditional convergence, but not conversely in infinite dimensions. Well-ordered sums use transfinite recursion for ordinal-indexed series.

## Terms

- **Partial sum**: $s_n = \sum_{k=0}^{n} a_k$, the finite sum of first $n+1$ terms
- **Convergent series**: Series whose partial sums approach a finite limit
- **Divergent series**: Series whose partial sums do not approach a limit
- **Absolute convergence**: Series where $\sum |a_n|$ converges
- **Conditional convergence**: Series convergent but not absolutely convergent
- **Cauchy product**: Multiplication rule $c_k = \sum_{j=0}^{k} a_j b_{k-j}$
- **Radius of convergence**: Distance from center where power series converges
- **Unconditional convergence**: Series converging regardless of term rearrangement
- **Truncation error**: Difference $s - s_n = \sum_{k=n+1}^{\infty} a_k$

## Debates and Open Questions

The convergence of the Flint Hills series $\sum_{n=1}^{\infty} \frac{1}{n^3 \sin^2 n}$ remains unknown, depending on how well π can be approximated by rational numbers. The numerators of continued fraction convergents of π (1, 3, 22, 333, 355, 103993, ...) determine where terms contribute most to this sum. Whether spatial motion is infinitely divisible remains debated in physics, with quantum gravity theories suggesting spacetime quantization at the Planck scale.