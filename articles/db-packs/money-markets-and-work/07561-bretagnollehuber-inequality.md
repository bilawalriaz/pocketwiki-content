# Bretagnolle–Huber inequality

In information theory, the Bretagnolle–Huber inequality bounds the total variation distance between two probability distributions $P$ and $Q$ using their Kullback–Leibler (KL) divergence. It serves as an alternative to Pinsker's inequality: once the KL divergence exceeds about 2, Pinsker's bound exceeds 1 and becomes vacuous, while the Bretagnolle–Huber bound stays at or below 1 and so remains informative. The bound is a standard tool in statistics and machine learning for proving information-theoretic lower bounds based on hypothesis testing. The Bretagnolle–Huber–Carol inequality is a separate concentration bound for multinomial random variables.

## Definitions

Let $P$ and $Q$ be probability distributions on a measurable space $(\mathcal{X}, \mathcal{F})$. The **total variation distance** is

$$d_{\mathrm{TV}}(P, Q) = \sup_{A \in \mathcal{F}} |P(A) - Q(A)|,$$

the largest gap between the two probabilities on any event. It lies in $[0, 1]$, with $0$ when the distributions agree and $1$ when they are concentrated on disjoint events.

The **Kullback–Leibler divergence** measures the expected log-ratio:

$$D_{\mathrm{KL}}(P \parallel Q) = \int_{\mathcal{X}} \log \frac{dP}{dQ}\, dP,$$

where $dP/dQ$ is the Radon–Nikodym derivative. The integral is finite only when $P \ll Q$ (absolute continuity of $P$ with respect to $Q$), and is $+\infty$ otherwise.

## The bound

For any two distributions $P, Q$:

$$d_{\mathrm{TV}}(P, Q) \le \sqrt{1 - \exp(-D_{\mathrm{KL}}(P \parallel Q))} \le 1 - \tfrac{1}{2}\exp(-D_{\mathrm{KL}}(P \parallel Q)).$$

Both sides are concave and bounded by 1 as a function of the KL divergence, so the bound is never vacuous, unlike Pinsker's. At $D_{\mathrm{KL}} = 0$ both sides equal $0$; as the divergence grows they rise monotonically toward $1$.

A per-event corollary follows from the right inequality. For any event $A$ with complement $\bar{A} = \Omega \setminus A$:

$$P(A) + Q(\bar{A}) \ge \tfrac{1}{2}\exp(-D_{\mathrm{KL}}(P \parallel Q)).$$

This says $A$ cannot be rare under $P$ while its complement is rare under $Q$ by more than a factor controlled by the divergence.

## Proof sketch

Following Tsybakov, the argument links total variation to KL through the Bhattacharyya coefficient $\rho = \int \sqrt{PQ}$.

**Step 1.** Using $d_{\mathrm{TV}}(P, Q) = 1 - \int \min(P, Q)$,

$$1 - d_{\mathrm{TV}}(P, Q)^2 = \int \min(P, Q) \int \max(P, Q) \ge \left(\int \sqrt{\min(P, Q)\max(P, Q)}\right)^2 = \rho^2,$$

by Cauchy–Schwarz, since $\min \cdot \max = PQ$.

**Step 2.** Jensen's inequality controls the coefficient by the KL divergence:

$$\rho^2 = \exp\!\left(2 \log \mathbb{E}_P\!\left[\sqrt{Q/P}\right]\right) \ge \exp\!\left(\mathbb{E}_P\!\left[-\log(P/Q)\right]\right) = \exp(-D_{\mathrm{KL}}(P \parallel Q)).$$

Chaining the two steps yields the main bound.

## Application: distinguishing coin biases

Given a fair coin ($p_1 = 1/2$) and an $\varepsilon$-biased coin ($p_2 = 1/2 + \varepsilon$), how many flips $n$ are needed to tell them apart with error at most $\delta$?

The KL divergence between the two Bernoulli distributions is $\tfrac{1}{2}\log(1/(1 - 4\varepsilon^2))$, so the joint divergence after $n$ independent flips is $n$ times that. A successful test requires the squared total variation between the joint distributions to reach at least $(1 - 2\delta)^2$. Applying the bound and rearranging gives

$$n \ge \frac{1}{2\varepsilon^2} \log\!\left(\frac{1}{2\delta}\right).$$

The same machinery, Bretagnolle–Huber plus a hypothesis-testing argument, gives a minimax regret lower bound for $k$-armed bandits.

## History

Jean Bretagnolle and Catherine Huber proved the inequality in 1979 in the proceedings of the Strasbourg Probability Seminar. Tsybakov's textbook republishes it as an early, less general version of Assouad's lemma, and a 2014 extension of Fano's inequality yields a constant improvement.

Source: adapted from "Bretagnolle–Huber inequality" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Bretagnolle%E2%80%93Huber_inequality
