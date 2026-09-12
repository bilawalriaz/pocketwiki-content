# Jensen's inequality

Jensen's inequality, proved by Johan Jensen in 1906, captures one fact: averaging first then applying a convex function gives a smaller result than applying the function first then averaging. Convex means the graph curves upward, like $x^2$ or $e^x$. Concave functions like $\log(x)$ reverse the inequality.

The geometric idea is simple. A convex function lies below any secant line connecting two of its points. For points $x_1, x_2$ and weight $t \in [0,1]$, the point $tx_1 + (1-t)x_2$ on the secant is higher than the graph point $f(tx_1+(1-t)x_2)$. Writing the secant height as $tf(x_1) + (1-t)f(x_2)$ gives the two-point form:

$$f(tx_1 + (1-t)x_2) \leq tf(x_1) + (1-t)f(x_2)$$

with equality only when $f$ is linear between the points or $x_1 = x_2$. Induction on $n$ extends this to the finite form with weights $\lambda_i \geq 0$ summing to 1:

$$\varphi\!\left(\sum \lambda_i x_i\right) \leq \sum \lambda_i \varphi(x_i)$$

In the probabilistic form, the same idea governs expectations. For a random variable $X$ and convex $\varphi$:

$$\varphi(\mathbb{E}[X]) \leq \mathbb{E}[\varphi(X)]$$

The difference $\mathbb{E}[\varphi(X)] - \varphi(\mathbb{E}[X])$ is called the Jensen gap. Equality holds when $\varphi$ is linear on the set where $X$ essentially lives, or when $X$ is constant.

The measure-theoretic form unifies both. On a probability space $(\Omega, \mathcal{A}, \mu)$, for $\mu$-integrable $f$ and convex $\varphi$:

$$\varphi\!\left(\int_\Omega f\,d\mu\right) \leq \int_\Omega \varphi \circ f\,d\mu$$

In analysis, applying this on $[a,b]$ with Lebesgue measure gives:

$$\varphi\!\left(\frac{1}{b-a}\int_a^b f(x)\,dx\right) \leq \frac{1}{b-a}\int_a^b \varphi(f(x))\,dx$$

The proof mirrors the geometry. Because $\varphi$ is convex, at every point $x_0$ there exists a supporting line $\varphi(x) \geq ax + b$ that touches the graph at $x_0$, so $\varphi(x_0) = ax_0 + b$. Substitute $x = f(\omega)$ for each $\omega$ and integrate. Since $\mu(\Omega)=1$, the integral of the lower bound equals $a\!\int f\,d\mu + b = \varphi(\int f\,d\mu)$. The general form follows because convex combinations of point masses are weakly dense in probability measures, and convex functions are continuous.

For intuition, a convex mapping $Y=\varphi(X)$ stretches large values of $X$ and compresses small ones, so the expected $Y$ sits above $\varphi(\mathbb{E}[X])$.

Because $\log(x)$ is concave, Jensen recovers the arithmetic-geometric mean inequality: $\frac{x_1+\cdots+x_n}{n} \geq \sqrt[n]{x_1 \cdots x_n}$. Applying Jensen to $g(x)=x^{2n}$ with convexity from $g'' \geq 0$ yields $(\mathbb{E}[X])^{2n} \leq \mathbb{E}[X^{2n}]$, so finiteness of any even moment guarantees a finite mean.

Setting $\varphi(y) = -\log(y)$ and $Y = q(X)/p(X)$ for two densities gives Gibbs' inequality: the Kullback–Leibler divergence $D(p\|q) \geq 0$, with equality only when $p=q$ almost everywhere. This means coding by the true distribution minimises average message length. In statistical physics, $\varphi(x)=e^x$ gives $e^{\mathbb{E}[X]} \leq \mathbb{E}[e^X]$, the foundation for relating partition functions to free energies.

Risk aversion in economics is precisely a concave utility $u$ with $u(\mathbb{E}[x]) > \mathbb{E}[u(x)]$: a certain expected outcome beats any fair gamble with the same mean. In the Rao–Blackwell theorem, conditioning a convex-loss estimator on a sufficient statistic produces an estimator with lower expected loss.

A sharper form bounds the Jensen gap by variance. For a twice-differentiable $\varphi$,

$$\sigma^2 \inf \frac{\varphi''(x)}{2} \leq \mathbb{E}[\varphi(X)] - \varphi(\mathbb{E}[X]) \leq \sigma^2 \sup \frac{\varphi''(x)}{2}$$

so when $\varphi$ is convex, $\varphi'' \geq 0$, and the standard inequality follows.

Source: adapted from "Jensen's inequality" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Jensen%27s_inequality
