# Limit (mathematics)

A limit is the value a function or sequence approaches as its argument or index draws near a target. Limits are the foundation of calculus and analysis: they rigorously define continuity, derivatives, and integrals, and they extend beyond real numbers to metric and topological spaces.

## Core idea

The limit of $f(x)$ as $x$ approaches $c$ is written

$$\lim_{x \to c} f(x) = L,$$

meaning $f(x)$ can be made as close to $L$ as desired by choosing $x$ close enough to $c$. A sequence $\{a_n\}$ converges to $L$ if later terms cluster around $L$. If no such $L$ exists, the sequence is divergent.

## The ε-δ definition

For functions: for every $\varepsilon > 0$ there exists a $\delta > 0$ such that

$$0 < |x - c| < \delta \quad \text{implies} \quad |f(x) - L| < \varepsilon.$$

Here $\varepsilon$ bounds the allowed error in the output and $\delta$ bounds the required closeness of the input. The strict inequality $0 < |x - c|$ excludes the point $c$ itself; omitting it effectively requires $f$ to be continuous at $c$.

An equivalent sequential form: $\lim_{x \to c} f(x) = L$ iff $f(x_n) \to L$ for every sequence $x_n \to c$ with $x_n \neq c$. For sequences themselves, $N$ replaces $\delta$: for every $\varepsilon > 0$ there exists an integer $N$ such that $n > N$ implies $|a_n - L| < \varepsilon$.

## One-sided limits and infinity

Approach from below ($x \to c^-$) or above ($x \to c^+$) gives one-sided limits; if they disagree, the two-sided limit does not exist. Limits may involve $\pm\infty$. For example, $\lim_{x \to +\infty} f(x) = L$ means: for every $\varepsilon > 0$ there exists $M$ with $x > M \Rightarrow |f(x) - L| < \varepsilon$. And $\lim_{x \to c} f(x) = \infty$ means: for every $M$ there exists $\delta$ with $0 < |x - c| < \delta \Rightarrow |f(x)| > M$. A sequence tends to infinity if every real bound is eventually exceeded.

## Limits in abstract spaces

In a metric space with distance $d$, $\{a_n\}$ converges to $a$ if $d(a, a_n) < \varepsilon$ for all sufficiently large $n$. In a general topological space, every open neighbourhood of $a$ must contain all but finitely many $a_n$. Uniqueness of limits can fail in non-Hausdorff spaces.

## Applications in analysis

Limits define the central objects of the subject. Continuity at $c$ means $\lim_{x \to c} f(x) = f(c)$. The derivative is $f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$. An infinite series $\sum a_n$ is defined as the limit of its partial sums $s_n = \sum_{i=1}^{n} a_i$. Absolute convergence means $\sum |a_n|$ also converges; conditional convergence does not, and the Riemann series theorem shows such a series can be rearranged to converge to any prescribed real, or to diverge to $\pm\infty$. Power series $f(z) = \sum c_n z^n$ converge inside a circle whose radius is set by the coefficients.

## Cauchy sequences and completeness

A sequence is Cauchy if its terms become arbitrarily close to each other: for every $\varepsilon > 0$ there exists $N$ such that $|a_m - a_n| < \varepsilon$ for all $m, n > N$. In a complete metric space such as $\mathbb{R}$, every Cauchy sequence converges; this is the property that makes calculus work on the real line. The order of convergence measures speed: if $\lim_{n \to \infty} |a_{n+1} - a| / |a_n - a|^{\alpha} = \lambda$, then $a_n$ converges with order $\alpha$ and asymptotic error constant $\lambda$, with larger $\alpha$ generally meaning faster convergence.

## Limit sets and nonstandard analysis

The limit set of a sequence is the collection of all points that are limits of convergent subsequences; for $a_n = (-1)^n$ it is $\{-1, +1\}$. Nonstandard analysis recasts convergence using hyperreal numbers: $\lim_{n \to \infty} a_n = \mathrm{st}(a_H)$, where $H$ is an infinite hypernatural index and $\mathrm{st}$ rounds each finite hyperreal to the nearest real.

## Historical landmarks

Euclid's *Elements* (c. 300 BC) used the method of exhaustion, an early limit ancestor. Grégoire de Saint-Vincent gave the first explicit limit of a geometric series in 1647; Newton described limits in the 1687 *Principia*; Bolzano developed ε-δ in 1817 (unrecognised for decades); Cauchy formalised the modern definition in 1821; Leathem introduced the arrow under the limit symbol in 1905; Hardy popularised it in 1908. Two conventions persist on whether $0 < |x - c|$ is required, and in computability theory some limits have moduli of convergence that are undecidable.
