# Characteristic function (probability theory)

A characteristic function is a complex-valued function that encodes a random variable's entire probability distribution. For a real-valued random variable $X$, it is defined as

$$\varphi_X(t) = \operatorname{E}[e^{itX}], \quad t \in \mathbb{R},$$

where $i$ is the imaginary unit and $t$ is a real parameter. This object is the Fourier transform (with sign-reversed exponent) of the underlying distribution, so every probability distribution corresponds to exactly one characteristic function, and vice versa. The characteristic function always exists for every real $t$, because the integral is over a finite-measure space and $e^{itX}$ is bounded. This is a key advantage over the moment-generating function $M_X(t) = \operatorname{E}[e^{tX}]$, which may fail to exist for distributions whose tails are too heavy. When both exist, $\varphi_X(-it) = M_X(t)$.

## Core properties

For any real random variable $X$, its characteristic function satisfies $\varphi_X(0) = 1$ and $|\varphi_X(t)| \le 1$ for all $t$. It is Hermitian, meaning $\varphi_X(-t) = \overline{\varphi_X(t)}$, so $\varphi$ is real-valued and even when $X$ is symmetric about the origin. It is uniformly continuous on $\mathbb{R}$. The correspondence with distributions is a bijection: two random variables share the same distribution if and only if they share the same characteristic function.

If a density $f_X$ exists, then $\varphi_X(t) = \int_{\mathbb{R}} e^{itx} f_X(x)\,dx$, the Fourier transform of $f_X$ with a sign-reversed complex exponential.

## Moments

When moments exist, the $k$-th moment of $X$ can be read directly off the derivatives of $\varphi_X$ at zero:

$$\operatorname{E}[X^k] = i^{-k}\,\varphi_X^{(k)}(0).$$

If $X \sim \mathcal{N}(\mu, \sigma^2)$, then $\varphi_X(t) = e^{i\mu t - \frac{1}{2}\sigma^2 t^2}$, and differentiating at $t = 0$ recovers $\operatorname{E}[X] = \mu$ and $\operatorname{E}[X^2] = \mu^2 + \sigma^2$, without integration by parts. The standard Cauchy distribution has $\varphi(t) = e^{-|t|}$, which is not differentiable at $t = 0$, confirming that no expectation exists.

## Sums of independent variables

The most useful computational fact is that convolution of distributions becomes multiplication in the characteristic-function domain. If $X_1, \ldots, X_n$ are independent and $S_n = \sum a_i X_i$ for constants $a_i$, then

$$\varphi_{S_n}(t) = \prod_{i=1}^n \varphi_{X_i}(a_i t).$$

In particular, $\varphi_{X+Y}(t) = \varphi_X(t)\,\varphi_Y(t)$ when $X$ and $Y$ are independent. A worked example: if $X \sim \Gamma(k_1, \theta)$ and $Y \sim \Gamma(k_2, \theta)$ are independent with the same scale parameter $\theta$, then $\varphi_X(t) = (1 - i\theta t)^{-k_1}$ and $\varphi_Y(t) = (1 - i\theta t)^{-k_2}$, so

$$\varphi_{X+Y}(t) = (1 - i\theta t)^{-(k_1+k_2)},$$

which is the characteristic function of $\Gamma(k_1 + k_2, \theta)$. More generally, the sum of independent gamma variables with a common scale parameter is again gamma, with shape parameters added. This multiplicative property is also the reason characteristic functions appear in proofs of the Central Limit Theorem and the law of large numbers.

## Inversion

Because the map $F \leftrightarrow \varphi$ is a bijection, the distribution can be recovered from the characteristic function. When $\varphi_X$ is integrable, the density exists and is given by the inverse Fourier transform:

$$f_X(x) = \frac{1}{2\pi} \int_{\mathbb{R}} e^{-itx} \varphi_X(t)\,dt.$$

For distributions without a density, the Gil-Pelaez inversion formula expresses the cumulative distribution function at any continuity point as

$$F_X(x) = \frac{1}{2} - \frac{1}{\pi}\int_0^{\infty} \frac{\operatorname{Im}[e^{-itx}\varphi_X(t)]}{t}\,dt.$$

These integral identities establish that no information is lost in passing from a distribution to its characteristic function.

## Continuity and limits

Lévy's continuity theorem says convergence in distribution is equivalent to pointwise convergence of characteristic functions to a function that is continuous at the origin. This converts distributional limit problems into pointwise limit problems, and is the workhorse behind the characteristic-function proof of the Central Limit Theorem: a triangular array of small, independent contributions has a characteristic function that converges to $e^{-\frac{1}{2}\sigma^2 t^2}$, the characteristic function of a normal distribution.

## When is a function a characteristic function?

Bochner's theorem gives the exact criterion: a function $\varphi: \mathbb{R}^n \to \mathbb{C}$ is a characteristic function if and only if it is positive definite, continuous at the origin, and satisfies $\varphi(0) = 1$. Positive definiteness is hard to check in practice, so sufficient conditions like Pólya's theorem are sometimes used: a real, even, continuous, convex-on-$t>0$ function with $\varphi(0) = 1$ and $\varphi(\infty) = 0$ is the characteristic function of a symmetric absolutely continuous distribution.

## Generalisations

The definition extends naturally. For a $k$-dimensional random vector, $\varphi_X(t) = \operatorname{E}[e^{i t^\top X}]$ with $t \in \mathbb{R}^k$; for a random matrix, the exponent uses the trace $i\operatorname{tr}(t^\top X)$; for a stochastic process $X(s)$, $\varphi_X(t) = \operatorname{E}\!\left[\exp\!\left(i\int t(s) X(s)\,ds\right)\right]$ for suitable test functions $t(s)$. The same construction generalises to random elements of any locally compact Abelian group, where characters replace the exponential.

Source: adapted from "Characteristic function (probability theory)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Characteristic_function_%28probability_theory%29
