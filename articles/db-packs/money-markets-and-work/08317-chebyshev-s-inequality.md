# Chebyshev's inequality

Chebyshev's inequality is a bound on how far a random variable can stray from its mean. For any random variable $X$ with mean $\mu$ and standard deviation $\sigma$, the probability of being at least $k$ standard deviations from the mean is at most $1/k^2$:

$$\Pr(|X - \mu| \geq k\sigma) \leq \frac{1}{k^2}$$

Only $k > 1$ gives useful information; for $k \leq 1$ the right-hand side is at least 1, which every probability already satisfies. An equivalent form states $\Pr(|X-\mu| \geq a) \leq \sigma^2/a^2$ for any $a > 0$.

The bound holds for any distribution with finite mean and variance, regardless of shape. The price is looseness: the 68–95–99.7 rule for normal distributions gives about 95% within two standard deviations and 99.7% within three, whereas Chebyshev guarantees only 75% within two and about 88.9% within three. When the distribution is known, sharper inequalities give tighter confidence intervals: Vysochanskij–Petunin provides $4/(9k^2)$ for unimodal data, and DasGupta's bound gives $1/(3k^2)$ for normal data.

| $k$ | Min. % within $k\sigma$ | Max. % beyond |
|---|---|---|
| $\sqrt{2}$ | 50% | 50% |
| 1.5 | 55.55% | 44.44% |
| 2 | 75% | 25% |
| $2\sqrt{2}$ | 87.5% | 12.5% |
| 3 | 88.8889% | 11.1111% |
| 4 | 93.75% | 6.25% |
| 5 | 96% | 4% |

The bound is sharp: for any $k \geq 1$, a distribution placing mass $1/(2k^2)$ at $-1$, mass $1/(2k^2)$ at $+1$, and the rest at $0$ achieves equality. No improvement is possible without extra assumptions.

## Why it works

Apply Markov's inequality ($\Pr(Y \geq a) \leq \mathbb{E}[Y]/a$ for non-negative $Y$) to $Y = (X-\mu)^2$ with $a = (k\sigma)^2$. The squared deviation is at least $k^2\sigma^2$ exactly when $|X-\mu| \geq k\sigma$, and the expected squared deviation equals $\sigma^2$, so:

$$\Pr(|X-\mu| \geq k\sigma) = \Pr((X-\mu)^2 \geq k^2\sigma^2) \leq \frac{\sigma^2}{k^2\sigma^2} = \frac{1}{k^2}$$

The bound is loose in practice because the proof replaces $(X-\mu)^2$ on the tail by its minimum value $k^2\sigma^2$ and ignores the contribution from values below the threshold.

## History and naming

Irénée-Jules Bienaymé proved the result in 1853; Pafnuty Chebyshev gave a more general proof in 1867; Chebyshev's student Andrey Markov proved it again in his 1884 Ph.D. thesis. The result is sometimes called the Bienaymé–Chebyshev inequality. Some authors name Markov's inequality "Chebyshev's First Inequality" and the result above "Chebyshev's Second Inequality."

## Applications and extensions

Weak law of large numbers. Apply the inequality to the sample mean of $n$ independent draws. Its variance is $\sigma^2/n$, so the probability the sample mean deviates from $\mu$ by $k\sigma/\sqrt{n}$ is at most $1/k^2$ and shrinks to zero as $n$ grows.

Mean–median bound. Cantelli's one-sided variant gives $\Pr(X - \mu \geq k\sigma) \leq 1/(1+k^2)$. Setting $k=1$ gives $\Pr(X \geq \mu + \sigma) \leq 1/2$ and, by symmetry on the other side, $\Pr(X \leq \mu - \sigma) \leq 1/2$. Since the median $\nu$ satisfies both $\Pr(X \geq \nu) \geq 1/2$ and $\Pr(X \leq \nu) \geq 1/2$, the median must lie within one standard deviation of the mean: $|\mu - \nu| \leq \sigma$.

Multivariate form. For a vector $X$ with mean $\mu$ and covariance matrix $S$, $\Pr((X-\mu)^\top S^{-1}(X-\mu) \geq k) \leq n/k$, where $n$ is the dimension. This Mahalanobis-distance bound is sharp.

Finite samples. When only sample estimates $m$ and $s$ are available and the population moments are unknown, Saw–Yang–Mo and Kabán's distribution-free bounds replace $1/k^2$ with terms depending on sample size $N$, approaching $1/(N+1)$ when the mean is large relative to the standard deviation.

Higher moments. Applying Markov's inequality to $|X-\mathbb{E}(X)|^n$ produces tail bounds of order $1/k^n$ via the $n$-th absolute moment; for $n > 4$ these beat the $1/k^2$ rate.
