# Frame (linear algebra)

A **frame** is a set of vectors in an inner product space that spans the space but may be linearly dependent. Where a basis forces each vector to have a unique expansion, a frame permits redundancy: the same vector can be built from many different combinations of frame elements. The redundancy buys stability, which is why frames are used in signal processing, wavelets, error correction, and filter banks.

## The motivating problem

Given a vector space V over a field F and a set {**e**_k} ⊂ V, the goal is to express any **v** ∈ V as a linear combination **v** = ∑ c_k **e**_k. Three cases arise:

1. If {**e**_k} does not span V, some vectors cannot be represented at all.
2. If {**e**_k} spans V and is linearly independent, it is a basis and the coefficients c_k are unique.
3. If {**e**_k} spans V but is linearly dependent, representation is possible but not unique.

The naive fix (delete vectors until the set becomes a basis) is risky: arbitrary deletions may destroy the spanning property, the selection is impractical for large or infinite sets, and the extra vectors are often useful. A frame handles case 3 directly by accepting the redundancy.

## Definition

Let V be an inner product space and {**e**_k}ₖ∈ℕ a sequence of vectors in V. The set is a **frame** if there exist constants 0 < A ≤ B < ∞ such that

A‖**v**‖² ≤ ∑_k |⟨**v**, **e**_k⟩|² ≤ B‖**v**‖², ∀**v** ∈ V.

The inner product ⟨**v**, **e**_k⟩ is a scalar measuring the projection of **v** onto **e**_k. The left inequality guarantees that no nonzero vector can be orthogonal to all frame vectors, so the frame spans V. The right inequality guarantees that the frame coefficients do not blow up. The constants A and B are the **frame bounds**; their ratio reflects how much redundancy exists.

A frame is **overcomplete** (or redundant) when it is not a Riesz basis. A frame of K ≥ N normalized vectors in an N-dimensional space satisfies A ≤ K/N ≤ B. When the frame is a Riesz basis (linearly independent), the bounds collapse to A ≤ 1 ≤ B.

Spanning V does not make a set a frame. Consider V = ℝ² with vectors (1,0), (0,1), (0,1/√2), (0,1/√3), …. This set spans ℝ², yet ∑ |⟨e_k, (0,1)⟩|² = 1 + 1/2 + 1/3 + ··· = ∞, so no finite upper bound B exists.

## The three core operators

**Analysis operator.** T : V → ℓ² sends **v** to the sequence of frame coefficients c_k = ⟨**v**, **e**_k⟩. The frame condition rewrites as A‖**v**‖² ≤ ‖T**v**‖² ≤ B‖**v**‖².

**Synthesis operator.** The adjoint T* : ℓ² → V rebuilds vectors from coefficient sequences: {c_k} ↦ ∑ c_k **e**_k.

**Frame operator.** S = T*T maps V to itself, S**v** = ∑ ⟨**v**, **e**_k⟩ **e**_k, and satisfies A‖**v**‖² ≤ ⟨S**v**, **v**⟩ ≤ B‖**v**‖². S is positive definite, bounded, and self-adjoint, so its inverse S⁻¹ exists. The optimal bounds A and B are the infimum and supremum of the spectrum of S; in finite dimensions they are the smallest and largest eigenvalues (equivalently, singular values of T).

## Dual frames

Because a frame is redundant, many coefficient sequences produce the same **v**. A practical reconstruction uses the **canonical dual frame** **ẽ**_k = S⁻¹**e**_k, which satisfies

**v** = ∑ ⟨**v**, **e**_k⟩ **ẽ**_k = ∑ ⟨**v**, **ẽ**_k⟩ **e**_k.

The proof: S⁻¹ applied to S**v** = ∑ ⟨**v**, **e**_k⟩ **e**_k returns **v** = ∑ ⟨**v**, **e**_k⟩ S⁻¹**e**_k. Canonical duality is reciprocal, so the canonical dual of {**ẽ**_k} is {**e**_k}. For an overcomplete frame there exist other dual frames {**g**_k} ≠ {**ẽ**_k}, and overcompleteness is exactly what makes this freedom possible.

When V is a subspace of a Hilbert space H and {**e**_k} does not depend on f ∈ H, the dual uses the restriction T_V. The orthogonal projection of f onto V is P_V f = ∑ ⟨f, **e**_k⟩ **ẽ**_k, which is the closest element of V to f.

## Special frames

| Type | Condition | Property |
|---|---|---|
| Tight frame | A = B | Reconstruction without dual: **v** = (1/A) ∑ ⟨**v**, **e**_k⟩ **e**_k |
| Parseval frame | A = B = 1 | Every orthonormal basis is Parseval; not all Parseval frames are bases |
| Equal-norm frame | ‖**e**_k‖ = c for all k | All frame vectors have equal length |
| Unit-norm frame | ‖**e**_k‖ = 1 | Special case of equal-norm |
| Equiangular frame | \|⟨**e**_i, **e**_j⟩\| = c for i ≠ j | All pairwise angles equal; every orthonormal basis is equiangular |
| Exact frame | No proper subset still spans V | A basis is a minimally spanning exact frame |

The union of k disjoint orthonormal bases is an overcomplete tight frame with bounds A = B = k.

## Non-harmonic Fourier series

On L²(−π, π), the exponentials {e^{ikx}}ₖ∈ℤ form a tight frame with bounds A = B = 2π. The key question is stability under perturbation: when does {e^{iλ_k x}} remain a basis or a frame after the frequencies λ_k are shifted away from the integers?

**Kadec's 1/4-theorem.** If |λ_k − k| ≤ L < 1/4 for all k, then {e^{iλ_k x}} satisfies the Paley–Wiener criterion and forms a Riesz basis for L²(−π, π), giving every function a unique non-harmonic Fourier series f(x) = ∑ c_k e^{iλ_k x} with ∑ |c_k|² < ∞. The same condition, applied to perturbations {μ_k} instead of integers, turns the system into a frame with explicit bounds.

## Frame projectors and noise mitigation

Redundancy lets a frame suppress noise in its coefficients. Given noisy coefficients **a** ∈ ℓ²(ℕ), the orthogonal projection onto the image of T is P**a** = T T̃* **a** = ∑_p **a**_p ⟨**ẽ**_p, **e**_k⟩. A sequence is a clean set of frame coefficients exactly when P**a** = **a**. The projection turns ℓ² and im(T) into reproducing kernel Hilbert spaces with kernel M_{k,p} = ⟨S⁻¹**e**_p, **e**_k⟩.

## Beyond discrete frames

A **semi-frame** satisfies only one of the two frame inequalities; a **Bessel sequence** satisfies only the upper bound. A **fusion frame** replaces a single subspace with a family {W_i, w_i} of weighted closed subspaces and demands A‖f‖² ≤ ∑ w_i² ‖P_{W_i} f‖² ≤ B‖f‖². A **continuous frame** generalizes the discrete index set to a locally compact space X with a Borel measure μ, replacing the sum by an integral ∫_X |⟨f, f_x⟩|² dμ(x); the analysis, synthesis, and frame operators all extend with integrals in place of sums, and a **framed POVM** carries the same inequality structure into operator-valued measures.
