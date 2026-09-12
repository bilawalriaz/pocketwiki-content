# Flag (linear algebra)

A flag in a finite-dimensional vector space V is a strictly increasing chain of subspaces starting at the zero subspace and ending at V:

{0} = V₀ ⊂ V₁ ⊂ V₂ ⊂ ⋯ ⊂ Vₖ = V,

where each Vᵢ is a proper subspace of Vᵢ₊₁. Such a chain is also called a filtration. The name comes from a picture: the zero point, a line, and a plane correspond to a nail, a staff, and a sheet of fabric.

If dim Vᵢ = dᵢ, the dimensions form a strictly increasing sequence

0 = d₀ < d₁ < d₂ < ⋯ < dₖ = n,

where n = dim V. Since the dimensions are distinct integers from 0 to n, k ≤ n. A flag is complete when dᵢ = i for every i, so the chain passes through every dimension. Any other flag is a partial flag. Every partial flag extends to a complete one by inserting the missing intermediate subspaces; a partial flag is a complete flag with some members removed.

## Adapted bases

An ordered basis (b₁, …, bₙ) of V is adapted to the flag when, for each i, the first dᵢ basis vectors span Vᵢ. Every flag admits an adapted basis, by standard linear algebra arguments. Any ordered basis of V produces a complete flag by letting Vᵢ be the span of its first i vectors. The standard flag in Kⁿ is built from the standard basis (e₁, …, eₙ), where eᵢ has a 1 in coordinate i and 0s elsewhere:

0 < ⟨e₁⟩ < ⟨e₁, e₂⟩ < ⋯ < ⟨e₁, …, eₙ⟩ = Kⁿ.

Adapted bases are rarely unique. An adapted basis is forced only in dimension 0, and in a one-dimensional vector space over F₂ (the field with two elements), where the unique nonzero vector is the only possible basis vector.

On an inner product space, a complete flag has an essentially unique orthonormal basis: unique up to multiplying each vector by a unit scalar (1, −1, i, …). One way to see this: vᵢ lies in the one-dimensional space Vᵢ₋₁⊥ ∩ Vᵢ, leaving only a choice of unit scalar. Gram–Schmidt constructs such a basis concretely.

## Stabilizers

The stabilizer of a flag is the set of invertible linear operators T on V with T(Vᵢ) = Vᵢ for every i, the operators that preserve the flag. For the standard flag on Kⁿ, the stabilizer is the group of invertible upper triangular matrices. For a general flag, with respect to an adapted basis, the stabilizer consists of block upper triangular matrices whose block sizes match the dimension jumps dᵢ − dᵢ₋₁.

For complete flags the stabilizer is a Borel subgroup of the general linear group GL(V); for partial flags it is a parabolic subgroup. The stabilizer acts simply transitively on the adapted bases of the flag, so adapted bases are not unique unless the stabilizer is trivial.

## Infinite-dimensional generalisation

In infinite-dimensional spaces, such as those of functional analysis, the flag idea extends to a subspace nest: a totally ordered (by inclusion) collection of subspaces closed under arbitrary intersections and closed linear spans. The associated operator algebras are nest algebras.

## Set-theoretic view

From the perspective of the field with one element, a set can be regarded as a vector space over that field. An ordering on a set corresponds to a maximal flag: ordering the elements 0, 1, 2, … is the same as taking the flag {0} ⊂ {0,1} ⊂ {0, 1, 2} ⊂ ⋯. This formalises several parallels between Coxeter groups and algebraic groups.

**Changes summary:** Trimmed "on its pole" and "routine" editorial; corrected the unit-scalar list to match source scope; replaced the speculative "leaves only length and phase" gloss with the source's one-dimensional intersection claim; removed the redundant "so k ≤ n" second clause; tightened the partial/complete relationship to one sentence.
