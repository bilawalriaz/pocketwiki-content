# Limit (mathematics)

## Overview
A limit is the value that a function or sequence approaches as its argument or index approaches some value. Limits are the foundational tool of calculus and mathematical analysis, used to rigorously define continuity, derivatives, and integrals. The concept extends beyond real numbers to abstract spaces like metric and topological spaces, and connects to category theory via direct and inverse limits.

## Timeline
- **c. 300 BC** — Euclid's *Elements* (Proposition X.1) establishes the method of exhaustion, an early form of limit reasoning
- **1647** — Grégoire de Saint-Vincent gives the first definition of the limit (terminus) of a geometric series in *Opus Geometricum*
- **1687** — Isaac Newton states a clear definition of limits in the *Scholium to Principia*, describing them as values approached so closely that their difference is less than any given quantity
- **1817** — Bernard Bolzano develops the epsilon-delta technique for defining continuous functions, though his work remains unknown until decades after his death
- **1821** — Augustin-Louis Cauchy formalizes the (ε, δ)-definition of the limit of a function
- **1905** — John Gaston Leathem invents the modern notation of placing the arrow below the limit symbol
- **1908** — G. H. Hardy popularizes the modern limit notation in *A Course of Pure Mathematics*

## Body

### Notation and Intuition
The limit of a function is written as $\lim_{x \to c} f(x) = L$, meaning $f(x)$ can be made arbitrarily close to $L$ by choosing $x$ sufficiently close to $c$. This is read as "the limit of $f$ of $x$ as $x$ approaches $c$ equals $L$." Alternative notations include $f(x) \to L$ as $x \to c$, or $f(x) \xrightarrow{x \to c} L$.

### Limits of Sequences
A sequence of real numbers $\{a_n\}_{n \in \mathbb{N}}$ converges to a limit $L$ if, for every positive real number $\epsilon$, there exists a positive integer $N$ such that every term $a_n$ with $n > N$ is within distance $\epsilon$ of $L$. This is written as $\lim_{n \to \infty} a_n = L$. If no such $L$ exists, the sequence is divergent. A sequence tends to infinity ($\lim_{n \to \infty} a_n = \infty$) if, for any real $M$, there exists $N$ such that $a_n > M$ for all $n > N$.

### Limits in Abstract Spaces
The concept of limits generalizes to metric spaces, where a sequence $\{a_n\}$ in a metric space $M$ with distance function $d$ converges to $a \in M$ if, for every $\varepsilon > 0$, there exists $N$ such that $d(a, a_n) < \varepsilon$ for all $n > N$. In topological spaces, the limit of a sequence is a point $a$ such that, for every open neighborhood $U$ of $a$, there exists $N$ such that $a_n \in U$ for all $n > N$. In topological spaces, limits may not be unique unless the space is Hausdorff.

### Limits of Functions
The (ε, δ)-definition states that $\lim_{x \to c} f(x) = L$ means: for every $\varepsilon > 0$, there exists $\delta > 0$ such that $0 < |x - c| < \delta$ implies $|f(x) - L| < \varepsilon$. The inequality $0 < |x - c|$ excludes $c$ itself from consideration, though some authors omit this, effectively requiring $f$ to be continuous at $c$. An equivalent sequential definition states that $\lim_{x \to c} f(x) = L$ if, for every sequence $x_n \to c$, the image sequence $f(x_n) \to L$.

### One-Sided Limits and Infinity
One-sided limits consider approach from below ($x \to c^-$) or above ($x \to c^+$). If these differ, the two-sided limit does not exist. Functions can also tend to infinity in the domain ($\lim_{x \to +\infty} f(x) = L$) or in the value ($\lim_{x \to c} f(x) = \infty$). The former means that for every $\varepsilon > 0$, there exists $M > 0$ such that $x > M$ implies $|f(x) - L| < \varepsilon$. The latter means that for every $M > 0$, there exists $\delta > 0$ such that $0 < |x - c| < \delta$ implies $|f(x)| > M$.

### Nonstandard Analysis
In nonstandard analysis, the limit of a sequence $(a_n)$ is expressed as the standard part of $a_H$, where $H$ is an infinite hypernatural index: $\lim_{n \to \infty} a_n = \text{st}(a_H)$. The standard part function rounds each finite hyperreal to the nearest real number, formalizing the intuition that terms are "very close" to the limit for "very large" indices.

### Limit Sets
The limit set of a sequence in a topological space is the set of all limit points of convergent subsequences. For oscillatory sequences like $a_n = (-1)^n$, the limit set is $\{-1, +1\}$. In dynamical systems, the limit set of a trajectory $\gamma(t)$ consists of all points that are limits of $\gamma(t_n)$ for sequences of increasing times $t_n$.

### Applications in Analysis
Limits define key concepts: infinite series $\sum_{n=1}^{\infty} a_n$ are defined as limits of partial sums $s_n = \sum_{i=1}^{n} a_i$. A series is absolutely convergent if $\sum |a_n|$ converges, and conditionally convergent otherwise. The Riemann series theorem shows that conditionally convergent series can be rearranged to converge to any real number or $\pm \infty$. Power series $f(z) = \sum_{n=0}^{\infty} c_n z^n$ converge within a circle whose radius is the radius of convergence. Continuity at a point $c$ means $\lim_{x \to c} f(x) = f(c)$, or equivalently, $f(x_n) \to f(c)$ for every sequence $x_n \to c$. The derivative is defined as $\lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$.

### Properties and Convergence
For convergent sequences, the sum, product, and inverse (when nonzero) of limits equal the limits of the respective operations. A sequence is Cauchy if, for every $\varepsilon > 0$, there exists $N$ such that $|a_m - a_n| < \varepsilon$ for all $m, n > N$. In complete metric spaces (like $\mathbb{R}$), every Cauchy sequence converges. The order of convergence quantifies how fast a sequence approaches its limit: if $\lim_{n \to \infty} \frac{|a_{n+1} - a|}{|a_n - a|^\alpha} = \lambda$, then $a_n$ converges with order $\alpha$ and asymptotic error constant $\lambda$.

## Terms
- **Limit**: The value that a function or sequence approaches as the argument or index approaches some value
- **ε-δ definition**: The formal definition of a limit using arbitrary positive error bounds (ε) and corresponding proximity thresholds (δ)
- **Convergent sequence**: A sequence that approaches a specific limit as the index tends to infinity
- **Cauchy sequence**: A sequence where terms become arbitrarily close to each other as the index increases
- **Complete metric space**: A metric space in which every Cauchy sequence converges
- **Pointwise convergence**: A sequence of functions converges pointwise if, for each $x$, the sequence of values $f_n(x)$ converges
- **Uniform convergence**: A stronger form of convergence where the rate of convergence is uniform across all points in the domain
- **One-sided limit**: A limit approached from only one direction (left or right)
- **Limit point**: A point that is the limit of some convergent subsequence
- **Order of convergence**: A measure of how quickly a sequence approaches its limit, characterized by constants $\alpha$ and $\lambda$

## Debates and Open Questions
The historical development of limits involved significant debate over rigor. Newton's intuitive understanding was later formalized by Bolzano and Cauchy using the ε-δ technique, but Bolzano's work remained unknown for decades. The question of whether limits should exclude the point itself (the $0 < |x - c|$ condition) remains a matter of convention among authors. In computability theory, some limits have undecidable moduli of convergence, meaning the rate at which they converge cannot be algorithmically determined. The distinction between pointwise and uniform convergence remains a subtle area where different notions of convergence on function spaces can yield different results, particularly regarding the preservation of properties like continuity.