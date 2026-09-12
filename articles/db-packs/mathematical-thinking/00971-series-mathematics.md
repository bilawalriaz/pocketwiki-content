# Series (mathematics)

A series is the sum of infinitely many terms taken in order, written $a_0 + a_1 + a_2 + \cdots$ or $\sum_{k=0}^{\infty} a_k$, where the terms come from a sequence of numbers, functions, matrices, or any objects that can be added. The series is defined as the **limit of its partial sums** $s_n = \sum_{k=0}^{n} a_k$. If those partial sums approach a finite number $L$, the series **converges** and its value is $L$; otherwise it **diverges**.

The earliest recorded use is Archimedes' quadrature of the parabola around 250 BCE. Nicole Oresme proved in 1360 that the harmonic series $\sum 1/n$ diverges. James Gregory introduced the terms "convergent" and "divergent" in 1668. In 1821 Augustin-Cauchy insisted on a strict limit-based definition, founding modern power-series theory; five years later Niels Henrik Abel corrected some of Cauchy's claims about the binomial series.

## Detecting convergence

The simplest necessary condition is the **nth-term test**: if $\lim_{n\to\infty} a_n \neq 0$, the series must diverge. For non-negative terms, convergence is equivalent to the partial sums being bounded. The standard tests reduce an unfamiliar series to one already known:

| Test | Comparison |
|---|---|
| Direct comparison | Bound $a_n$ above by a known convergent series or below by a known divergent one |
| Limit comparison | Compare the ratio $a_n/b_n$ to a known series $b_n$ |
| Ratio test | Compare $a_{n+1}/a_n$ to a geometric series |
| Root test | Compare $\sqrt[n]{a_n}$ to a geometric series |
| Integral test | Compare $\sum a_n$ to $\int f(x)\,dx$ when $a_n = f(n)$ with $f$ positive and decreasing |

The **geometric series** $\sum ar^n = a/(1-r)$ for $|r|<1$ is the workhorse behind the ratio and root tests: any series whose successive ratios stay below a fixed number less than 1 shrinks like a geometric series. A **telescoping series** $\sum (b_n - b_{n+1})$ collapses to $b_1 - L$ when $b_n \to L$.

## Absolute and conditional convergence

A series converges **absolutely** when $\sum |a_n|$ converges. Absolute convergence implies convergence and permits arbitrary rearrangement of terms. A series that converges but not absolutely is **conditionally convergent**. The alternating harmonic series $\sum (-1)^{n+1}/n = \ln 2$ is the standard example: $\sum 1/n$ diverges, yet slowly alternating the signs yields $\ln 2$.

The **Riemann series theorem** sharpens this: any conditionally convergent series of real numbers can be rearranged to converge to any prescribed real number, or to diverge entirely. Ordinary addition is only well-defined for absolutely convergent series.

## Algebra of series

Series can be added termwise, $(a_k + b_k)$, and scaled termwise, $(ca_k)$. Multiplication uses the **Cauchy product**, $c_k = \sum_{j=0}^{k} a_j b_{k-j}$. Convergent series form a vector space under these operations, and absolutely convergent series form a commutative ring, in which multiplication, like rearrangement, is well behaved.

## Series of functions

A **power series** $\sum a_n (x-c)^n$ generalises the geometric series to functions and converges inside a **radius of convergence** $R$, an interval over the reals or a disc over the complex numbers, with uniform convergence on every compact subset (a closed, bounded set) inside. A function agreeing with a power series near a point is represented by a **Taylor series**. **Formal power series** drop the convergence requirement and are used as algebraic objects in combinatorics. **Laurent series** allow finitely many negative powers of $(x-c)$ and converge in an annulus (a ring-shaped region between two concentric circles). **Fourier series** expand a function in sines and cosines, with foundations laid by Dirichlet in 1829 and Riemann in 1854.

## Summation methods for divergent series

Several **summation methods** assign finite values to series that do not converge ordinarily. **Cesàro summation** replaces a series with the limit of the running averages of its partial sums, so $1 - 1 + 1 - 1 + \cdots$ is assigned $1/2$. **Abel summation** evaluates $\sum a_n r^n$ and lets $r \to 1^-$. The **Silverman-Toeplitz theorem** characterises which matrix-based averaging methods yield results consistent with ordinary convergence.

The convergence of the **Flint Hills series** $\sum_{n=1}^{\infty} 1/(n^3 \sin^2 n)$ remains unknown, because the size of its terms depends on how well $\pi$ is approximated by rationals, with continued-fraction convergents such as 22/7, 355/113, and 103993/33102 producing large spikes.

Source: adapted from "Series (mathematics)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Series_%28mathematics%29
