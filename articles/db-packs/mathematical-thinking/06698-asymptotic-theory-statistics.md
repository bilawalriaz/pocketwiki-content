# Asymptotic theory (statistics)

Asymptotic theory, also called large sample theory, is a framework for assessing estimators and statistical tests by examining what happens as the sample size n grows without bound (n → ∞). The limit results are typically approximately valid for large finite samples too, and they often give qualitative understanding that numerical methods cannot.

A convergence mode is the rule used to declare that a sequence of random quantities settles on a limit. Converges in probability means the chance of being far from the limit shrinks to zero; converges almost surely means the sequence eventually stays within any chosen neighbourhood of the limit.

## The standard setup and its variants

The standard approach assumes one keeps drawing observations, so n → ∞. The prototype result is the weak law of large numbers: for IID (independent and identically distributed) random variables X₁, X₂, … with population mean E[Xᵢ], the sample average X̄ₙ converges in probability to E[Xᵢ] as n → ∞.

Some models require modified limits:

- **Panel data.** One dimension stays fixed while the other grows, e.g. T constant and N → ∞.
- **Local asymptotic normality.** The true parameter drifts with n as θₙ = θ + h/√n, used to study estimator regularity.
- **Local alternatives.** Tests are evaluated against alternatives close to the null, with H₁: θ = θ₀ + h/√n, a setup common in unit root tests.
- **Expanding parameter space.** The dimension of Θₙ grows slowly with n, allowing more structural effects to be modelled.
- **Kernel methods.** Bandwidth h is an extra parameter, typically chosen so h → 0 with h ∝ n^(−1/5).

## Point estimators: the key properties

For a sequence of estimators (θ̂ₙ), the standard properties are:

- **Weak consistency.** θ̂ₙ converges in probability to the true parameter θ₀.
- **Strong consistency.** θ̂ₙ converges almost surely to θ₀, a strictly stronger statement.
- **aₙ-consistency.** The error shrinks at rate 1/aₙ, written Oₚ(1/aₙ).
- **Asymptotic distribution.** Constants (aₙ) and (bₙ) and a non-degenerate distribution μ exist such that bₙ(θ̂ₙ − aₙ) converges in distribution to μ. When μ = N(0, V), the estimator is asymptotically normal with asymptotic variance V. Most authors fix aₙ = θ₀ and bₙ = √n.
- **Unbiased in the limit.** lim E[θ̂ₙ] = θ₀, also called approximately unbiased.
- **Asymptotic efficiency.** Asymptotically normal with V equal to the inverse Fisher information I(θ₀)⁻¹, attaining the Cramér–Rao bound.

Limiting variance, σ², is defined by lim τₙ Var(θ̂ₙ) = σ², usually with τₙ = n; it coincides with the asymptotic variance for asymptotically unbiased estimators.

## How the properties relate

These conditions form a chain of implications. Asymptotic normality implies consistency (by Slutsky's theorem), consistency implies asymptotic unbiasedness, and asymptotic unbiasedness together with uniform integrability of (θ̂ₙ) implies unbiasedness in the limit. Uniform integrability is automatic when the second moments are uniformly bounded, e.g. sup E[|θ̂ₙ|²] < ∞.

In the univariate case, an asymptotically unbiased estimator with asymptotic variance τ² satisfies τ² ≤ σ², where σ² is the limiting variance. Equality holds precisely when the normalised sequence bₙ(θ̂ₙ − θ₀) is uniformly integrable, a condition that often holds in practice.

## Theorems that deliver these properties

Given IID observations X₁, X₂, … from P_θ, the following results are the main tools:

- **Strong law of large numbers.** For sample-mean estimators θ̂ₙ = (1/n)∑f(Xᵢ) with E[|f(X₁)|] < ∞, θ̂ₙ converges almost surely to E[f(X₁)], giving strong consistency when θ = E[f(X₁)].
- **Continuous mapping theorem.** If θ = f(τ) for a continuous f and τ̂ₙ is consistent for τ, then f(τ̂ₙ) is consistent for θ.
- **Central limit theorem (CLT).** Under E[|f(X₁)|²] < ∞, the same sample-mean estimator is asymptotically normal: √n (θ̂ₙ − μ)/σ →d N(0, 1), where μ = E[f(X₁)] and σ² = Var(f(X₁)).
- **Fisher–Tippet–Gnedenko theorem.** For estimators of the form max_{i=1,…,n} f(Xᵢ), after suitable centring and scaling the asymptotic distribution is a generalised extreme value distribution.
- **Delta method.** If θ = f(τ) with ∇f(τ) ≠ 0 and τ̂ₙ is asymptotically normal for τ with variance V, then f(τ̂ₙ) is asymptotically normal for θ with variance ∇f(τ)ᵀ V ∇f(τ).
