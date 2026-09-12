# Kullback's inequality

In information theory and statistics, Kullback's inequality is a lower bound on the Kullback–Leibler divergence between two probability distributions, expressed through the large deviations rate function of one of them. A *large deviations rate function* is a convex function that quantifies how quickly the probability of rare events decays. *Kullback–Leibler divergence* $D_{KL}(P \parallel Q)$ measures the information lost when $Q$ is used to approximate $P$. The bound reads

$$D_{KL}(P \parallel Q) \;\geq\; \Psi_Q^{*}\!\bigl(\mu_1'(P)\bigr),$$

where $P$ and $Q$ are probability distributions on the real line with $P$ *absolutely continuous* with respect to $Q$ (every event assigned zero probability by $Q$ is also assigned zero probability by $P$, written $P \ll Q$), and whose first moments exist. The term $\mu_1'(P)$ is the first moment (mean) of $P$, and $\Psi_Q^{*}$ is the *rate function*, defined as the *convex conjugate* of the *cumulant-generating function* $\Psi_Q$ of $Q$. The convex conjugate of a function $f$ is $\sup_x \{x y - f(x)\}$, and the cumulant-generating function is $\Psi_Q(\theta) = \log M_Q(\theta)$, where $M_Q(\theta) = \int e^{\theta x}\, Q(dx)$ is the *moment-generating function* of $Q$. The Cramér–Rao bound, a classical lower bound on the variance of unbiased estimators, follows as a corollary.

## Proof

Let $P$ and $Q$ be probability measures on $\mathbb{R}$ with $P \ll Q$ and existing first moments. Construct the *natural exponential family* of $Q$,

$$Q_\theta(A) \;=\; \frac{1}{M_Q(\theta)} \int_A e^{\theta x}\, Q(dx),$$

which tilts $Q$ by the exponential weight $e^{\theta x}$, with $Q_0 = Q$. A direct calculation gives the decomposition

$$D_{KL}(P \parallel Q) \;=\; D_{KL}(P \parallel Q_\theta) \;+\; \int_{\mathrm{supp}\,P} \!\log \frac{dQ_\theta}{dQ}\, dP.$$

By *Gibbs' inequality*, $D_{KL}(P \parallel Q_\theta) \geq 0$, so dropping that term yields

$$D_{KL}(P \parallel Q) \;\geq\; \int_{\mathrm{supp}\,P} \!\log \frac{e^{\theta x}}{M_Q(\theta)}\, P(dx) \;=\; \mu_1'(P)\,\theta \;-\; \Psi_Q(\theta),$$

valid for every real $\theta$ where $M_Q(\theta) < \infty$. Taking the supremum over $\theta$ realises the convex conjugate and produces the stated inequality

$$D_{KL}(P \parallel Q) \;\geq\; \sup_{\theta} \bigl\{\mu_1'(P)\,\theta - \Psi_Q(\theta)\bigr\} \;=\; \Psi_Q^{*}\!\bigl(\mu_1'(P)\bigr).$$

## Corollary: the Cramér–Rao bound

Let $X_\theta$ be a family of distributions on $\mathbb{R}$ indexed by a real parameter $\theta$, satisfying standard regularity conditions. Divide Kullback's inequality by $h^2$ and let $h \to 0$:

$$\lim_{h \to 0} \frac{D_{KL}(X_{\theta+h} \parallel X_\theta)}{h^2} \;\geq\; \lim_{h \to 0} \frac{\Psi_\theta^{*}(\mu_{\theta+h})}{h^2}.$$

The left side expands, via a Taylor series for $\log(1-t)$, to $\tfrac{1}{2}\, \mathcal{I}_X(\theta)$, where $\mathcal{I}_X(\theta)$ is the *Fisher information*, a measure of how much information an observation carries about $\theta$. On the right side, the supremum is attained at a value $\tau$ where $\Psi_\theta'(\tau) = \mu_{\theta+h}$. Using $\Psi_\theta'(0) = \mu_\theta$ and a second-order expansion around the optimum gives

$$\lim_{h \to 0} \frac{\Psi_\theta^{*}(\mu_{\theta+h})}{h^2} \;=\; \frac{1}{2\,\mathrm{Var}(X_\theta)} \left(\frac{d\mu_\theta}{d\theta}\right)^{\!2}.$$

Combining both sides,

$$\frac{1}{2}\, \mathcal{I}_X(\theta) \;\geq\; \frac{1}{2\,\mathrm{Var}(X_\theta)} \left(\frac{d\mu_\theta}{d\theta}\right)^{\!2},$$

which rearranges to the Cramér–Rao bound

$$\mathrm{Var}(X_\theta) \;\geq\; \frac{(d\mu_\theta / d\theta)^2}{\mathcal{I}_X(\theta)}.$$
