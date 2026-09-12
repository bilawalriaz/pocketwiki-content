# Big O in probability notation

The order in probability notation extends the familiar big O and little o from ordinary real sequences to sequences of random variables. Where big O in mathematics controls how fast ordinary numbers grow, $O_p$ and $o_p$ control how fast random variables grow, with closeness measured by convergence in probability rather than by the ordinary limit.

The setup is a sequence of random variables $X_n$ and a sequence of constants $a_n$, both indexed by $n$ (which need not be restricted to integer values). Writing $X_n = o_p(a_n)$ means the ratio $X_n/a_n$ shrinks to zero in probability as $n$ grows:

$$X_n = o_p(a_n) \iff \lim_{n\to\infty} P\!\left[\left|\tfrac{X_n}{a_n}\right| \ge \varepsilon\right] = 0 \quad \text{for every } \varepsilon > 0.$$

Writing $X_n = O_p(a_n)$ means the ratio is stochastically bounded: for every $\varepsilon > 0$ there exist finite $M$ and $N$ with

$$P\!\left(\left|\tfrac{X_n}{a_n}\right| > M\right) < \varepsilon \quad \text{for all } n > N.$$

## How the two definitions differ

Both definitions are stated by swapping two quantifiers over the same probability bound $P(|X_n| \ge \delta) \le \varepsilon$. The hidden variable is $\delta$, the size of the deviation you are willing to tolerate.

| Notation | Quantifier order | Meaning |
|---|---|---|
| $O_p(1)$ | $\forall \varepsilon\; \exists \delta_\varepsilon, N_\varepsilon$ | some $\delta$ works, and it may shrink with $\varepsilon$ |
| $o_p(1)$ | $\forall \varepsilon, \delta\; \exists N_{\varepsilon,\delta}$ | works for every $\delta$, no matter how small |

So $O_p$ only demands that the sequence be bounded in probability, while $o_p$ demands a bound that tightens toward zero as $n$ grows. Convergence in probability therefore implies stochastic boundedness, $o_p(1) \Rightarrow O_p(1)$, but the reverse fails: a tightly bounded sequence need not collapse to zero.

## Chebyshev's lemma for stochastic order

The standard bridge from raw variance to a stochastic order is Chebyshev's inequality, which for any random variable $X$ with mean $\mu$ and standard deviation $\sigma$ gives

$$P(|X - \mu| \le h\sigma) \ge 1 - h^{-2} \quad (h > 0).$$

Apply it to $X_n$ with mean $\mu_n$ and finite variance $\sigma_n^2$. Set $h = \eta^{-1/2}$ for any $0 < \eta < 1$:

$$P\!\left(\left|\tfrac{X_n - \mu_n}{\sigma_n}\right| < \eta^{-1/2}\right) \ge 1 - \eta \quad \text{for all } n \ge 1.$$

Choosing $K(\eta) = \eta^{-1/2}$ and $n(\eta) = 1$ matches the defining condition for stochastic boundedness, so

$$X_n - \mu_n = O_p(\sigma_n), \qquad \text{equivalently} \quad \tfrac{X_n - \mu_n}{\sigma_n} = O_p(1).$$

If, in addition, the scaled variance $a_n^{-2}\,\mathrm{var}(X_n) = \mathrm{var}(a_n^{-1}X_n)$ forms a null sequence for some real sequence $(a_n)$, Chebyshev's inequality forces $a_n^{-1}(X_n - E(X_n))$ to converge to zero in probability, giving

$$X_n - E(X_n) = o_p(a_n).$$

The single variance-to-probability step above is what turns a moment bound into a stochastic order.
