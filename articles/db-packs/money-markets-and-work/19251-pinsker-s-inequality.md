# Pinsker's inequality

Pinsker's inequality bounds a geometric notion of distance between probability distributions using an information-theoretic one. It converts the Kullback–Leibler divergence (the expected log-ratio under $P$, measuring how surprised you would be if you expected $Q$ but the world was governed by $P$) into an upper bound on the total variation distance (the largest probability gap any single event can exhibit between $P$ and $Q$). Distributions that are close in KL-divergence cannot differ much on any test.

## Formal statement

Let $P$ and $Q$ be probability distributions on a measurable space $(X, \Sigma)$. Then

$$\delta(P,Q) \le \sqrt{\tfrac{1}{2}\,D_{\mathrm{KL}}(P \parallel Q)},$$

where $\delta(P,Q) = \sup\bigl\{|P(A) - Q(A)| : A \in \Sigma\bigr\}$ is the total variation distance, and

$$D_{\mathrm{KL}}(P \parallel Q) = \mathbb{E}_P\!\left[\log \tfrac{\mathrm{d}P}{\mathrm{d}Q}\right] = \int_X \left(\log \tfrac{\mathrm{d}P}{\mathrm{d}Q}\right)\mathrm{d}P$$

is the Kullback–Leibler divergence in nats (natural-log units). On a finite set $X$,

$$D_{\mathrm{KL}}(P \parallel Q) = \sum_{i \in X} \left(\log \tfrac{P(i)}{Q(i)}\right) P(i).$$

The bound is tight up to constant factors. In terms of the total variation norm $\|P - Q\|$ of the signed measure $P - Q$, the inequality picks up a factor of two,

$$\|P - Q\| \le \sqrt{2\,D_{\mathrm{KL}}(P \parallel Q)},$$

which is the same inequality written differently.

## Alternative form and the choice of logarithm

The numerical value of $D_{\mathrm{KL}}$ depends on the logarithm's base. Using $\ln$ gives nats; using $\log_2$ gives bits. Writing $D$ for the bit-based version, $D(P \parallel Q) = D_{\mathrm{KL}}(P \parallel Q)/\ln 2$. With $V(p,q) = \sum_{x \in X}|p(x) - q(x)|$ the non-normalized variation distance on a finite alphabet,

$$D(P \parallel Q) \ge \frac{1}{2 \ln 2}\,V(p,q)^2,$$

or equivalently $\sqrt{D_{\mathrm{KL}}(P \parallel Q)/2} \ge V(p,q)/2$. Convergence in KL-divergence therefore implies convergence in variation distance, but not the reverse.

A short proof by John Pollard starts from $r(x) = P(x)/Q(x) - 1 \ge -1$ and uses the elementary bound $(1+u)\log(1+u) - u \ge \tfrac{1}{2}\tfrac{u^2}{1+u/3}$ together with Titu's lemma (Sedrakyan's inequality) to obtain $D_{\mathrm{KL}}(P \parallel Q) \ge \tfrac{1}{2} V(p,q)^2$.

The same conclusion follows by partitioning the sample space. First verify the Bernoulli case $D(P \parallel Q) \ge \tfrac{1}{2\ln 2}\|P - Q\|_1^2$ directly. Then let $A = \{x : p(x) \ge q(x)\}$ and collapse each distribution to a two-point distribution that records total mass on $A$. KL-divergence decomposes as $D(P \parallel Q) = D(P(Z) \parallel Q(Z)) + D(P \parallel Q \mid Z)$, and the conditional term is nonnegative, so the general inequality reduces to the Bernoulli case.

## Limitations and the inverse direction

Pinsker's inequality is one-directional: the reverse fails. For every $\varepsilon > 0$ there exist $P_\varepsilon, Q$ with $\delta(P_\varepsilon, Q) \le \varepsilon$ yet $D_{\mathrm{KL}}(P_\varepsilon \parallel Q) = \infty$. On the two-point space $\{0,1\}$ take $Q(0) = 0$, $Q(1) = 1$ and $P_\varepsilon(0) = \varepsilon$, $P_\varepsilon(1) = 1 - \varepsilon$: variation distance is $2\varepsilon$, but $P_\varepsilon$ assigns positive mass to $\{0\}$ that $Q$ makes impossible, sending the KL-divergence to infinity.

On finite spaces a partial inverse does hold. Let $\alpha_Q = \min\{Q(x) : Q(x) > 0\}$. Then for any $P$ absolutely continuous with respect to $Q$,

$$\tfrac{1}{2}\,D_{\mathrm{KL}}(P \parallel Q) \le \frac{1}{\alpha_Q}\,\delta(P,Q)^2,$$

so when $Q$ has full support ($Q(x) > 0$ everywhere), the two quantities are equivalent up to constants:

$$\delta(P,Q)^2 \;\le\; \tfrac{1}{2}\,D_{\mathrm{KL}}(P \parallel Q) \;\le\; \frac{1}{\alpha_Q}\,\delta(P,Q)^2.$$

When $D_{\mathrm{KL}}(P \parallel Q) > 2$, Pinsker's bound becomes vacuous, since total variation distance is at most 1. The complementary Bretagnolle–Huber inequality covers that regime:

$$\delta(P,Q) \le \sqrt{1 - e^{-D_{\mathrm{KL}}(P \parallel Q)}},$$

which stays informative up to $\delta = 1$.

## History

Pinsker first proved the inequality with a larger constant. The form stated here was proved independently by Solomon Kullback, Imre Csiszár, and J. H. B. Kemperman.

Source: adapted from "Pinsker's inequality" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Pinsker%27s_inequality
