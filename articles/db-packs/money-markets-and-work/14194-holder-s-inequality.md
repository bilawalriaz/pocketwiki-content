# Hölder's inequality

Hölder's inequality bounds the integral of a product |fg| by the product of the individual L^p and L^q norms of f and g. The special case p = q = 2 is the Cauchy–Schwarz inequality.

## The statement

Let (S, Σ, μ) be a measure space and let p, q ∈ [1, ∞] satisfy 1/p + 1/q = 1, with 1/∞ read as 0. For every measurable real- or complex-valued function f and g on S,

∫_S |fg| dμ ≤ (∫_S |f|^p dμ)^(1/p) · (∫_S |g|^q dμ)^(1/q).

The number q is the Hölder conjugate of p. When p = ∞, ‖f‖_∞ denotes the essential supremum of |f|. If f ∈ L^p and g ∈ L^q, the product fg lies in L^1, so the left side is finite.

Equality holds for p, q ∈ (1, ∞) with both norms finite and nonzero if and only if |f|^p and |g|^q are linearly dependent in L^1(μ): there exist α, β ≥ 0, not both zero, with α|f|^p = β|g|^q μ-almost everywhere.

## Proof via Young's inequality

Young's inequality for products says that for a, b ≥ 0 and p, q ∈ (1, ∞) with 1/p + 1/q = 1,

ab ≤ a^p/p + b^q/q,

with equality iff a^p = b^q. Substitute a = |f(s)|/‖f‖_p and b = |g(s)|/‖g‖_q, apply Young pointwise, and integrate over S. The denominators cancel and 1/p + 1/q = 1 leaves1 on the right.

## Special cases

- Counting measure on {1,…,n}: Σ|x_k y_k| ≤ (Σ|x_k|^p)^(1/p) (Σ|y_k|^q)^(1/q). The same form holds on ℕ for sequence spaces.
- Lebesgue measure on ℝ^n: ∫|fg| ≤ (∫|f|^p)^(1/p) (∫|g|^q)^(1/q).
- Probability space (Ω, 𝓕, ℙ): 𝔼[|XY|] ≤ (𝔼[|X|^p])^(1/p) (𝔼[|Y|^q])^(1/q). With p = s/r and 1 < r < s, finiteness of the s-th absolute moment implies finiteness of the r-th.

For probability measures the requirement relaxes to 1/p + 1/q ≤ 1.

## Extremal equality

For 1 ≤ p < ∞ and q the conjugate, ‖f‖_p equals the dual supremum

‖f‖_p = max { |∫ f g dμ| : g ∈ L^q, ‖g‖_q ≤ 1 }.

The maximizer is g = ‖f‖_p^(1−p) |f|^p / f on the set where f ≠ 0, and it satisfies ‖g‖_q = 1. For p = ∞ a similar representation holds under mild σ-finiteness assumptions, but the supremum need not be attained; it can fail outright on σ-fields that contain no set of finite positive measure inside an infinite-measure set.

## Consequences

Hölder proves the triangle inequality (Minkowski) in L^p: writing |f₁+f₂|^p ≤ |f₁|·|f₁+f₂|^(p−1) + |f₂|·|f₁+f₂|^(p−1) and applying Hölder to each term gives ‖f₁+f₂‖_p ≤ ‖f₁‖_p + ‖f₂‖_p.

Every f ∈ L^p defines a bounded linear functional κ_f(g) = ∫ f g dμ on L^q. The extremal equality shows ‖κ_f‖ = ‖f‖_p, so L^q is isometrically isomorphic to the dual of L^p for p ∈ [1, ∞).

## More than two functions

If p₁,…,pₙ ∈ (0, ∞] satisfy Σ 1/p_k = 1/r (with 1/∞ = 0), then

‖f₁ ··· fₙ‖_r ≤ ‖f₁‖_{p₁} ··· ‖fₙ‖_{pₙ}.

The proof applies the two-function case inductively. Two corollaries: Littlewood's inequality ‖f‖_{p_θ} ≤ ‖f‖_{p₁}^θ ‖f‖_{p₀}^{1−θ} for 1/p_θ = θ/p₁ + (1−θ)/p₀, and Lyapunov's inequality ‖f‖_p^p ≤ ‖f‖_{p₀}^{p₀(1−θ)} · ‖f‖_{p₁}^{p₁θ} for p = (1−θ)p₀ + θp₁. Both imply that if f ∈ L^{p₀} ∩ L^{p₁}, then f ∈ L^p for every p between p₀ and p₁.

## Reverse Hölder

For p ∈ (1, ∞) and g nonzero μ-almost everywhere,

∫ |fg| dμ ≥ (∫ |f|^{1/p} dμ)^p · (∫ |g|^{−1/(p−1)} dμ)^{−(p−1)},

with equality iff |f| = α|g|^{−p/(p−1)} almost everywhere. It follows from the standard inequality by writing |f|^{1/p} = |fg|^{1/p} · |g|^{−1/p}.

## Other settings

For a sub-σ-algebra 𝒢 of a probability space, the inequality holds for conditional expectations: 𝔼[|XY| | 𝒢] ≤ (𝔼[|X|^p | 𝒢])^(1/p)(𝔼[|Y|^q | 𝒢])^(1/q), ℙ-almost surely. An Aczél–Beckenbach symmetric form says that for vectors with positive entries satisfying f(i)g(i)h(i) = 1 and 1/p + 1/q + 1/r = 0, ‖f‖_p ‖g‖_q ‖h‖_r ≥ 1 when two of p, q, r are positive and ≤ 1 when two are negative; the standard inequality follows immediately.
