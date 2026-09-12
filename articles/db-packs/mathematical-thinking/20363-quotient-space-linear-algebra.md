# Quotient space (linear algebra)

Let V be a vector space over a field K, and let U be a subspace of V. The quotient space V/U is V with the entire subspace U collapsed to zero. Two vectors become indistinguishable when they differ by an element of U, so V/U captures what remains of V once U has been erased. An affine subspace of V is a translate of a subspace by a fixed vector; a parallel translate of U means a set of the form v + U.

## Construction

Define an equivalence relation on V by x ~ y if and only if x − y ∈ U. The equivalence class (coset) of a vector v is

[v] = {w : v − w ∈ U} = {v + u : u ∈ U},

also written v + U. V/U is the set of these classes. Addition and scalar multiplication are defined class-wise:

α[x] = [αx],  [x] + [y] = [x + y].

These operations are well-defined, meaning they do not depend on which representative of each class is chosen, and turn V/U into a vector space over K in which U itself becomes the zero class [0]. The map v ↦ [v] is the quotient map from V onto V/U. Geometrically, V/U is the set of all affine subspaces of V parallel to U, since every coset v + U is such a parallel translate.

## Examples

Take the Cartesian plane X = ℝ² and a line Y through the origin. The quotient X/Y is the set of all lines in ℝ² parallel to Y. Points on the same parallel line differ by a vector in Y, so they form one equivalence class; points on different parallels belong to different classes.

A second example: ℝⁿ modulo the subspace spanned by the first m standard basis vectors. That subspace consists of all n-tuples whose last n − m entries are zero. Two ℝⁿ vectors are equivalent exactly when their last n − m coordinates agree, so ℝⁿ / ℝᵐ ≅ ℝⁿ⁻ᵐ.

A functional example: let 𝒫₃(ℝ) be the space of cubic polynomials and let U = ⟨x²⟩. Two polynomials are equivalent when they differ by a multiple of x². The coset of x³ − 2x + 3 is {x³ + ax² − 2x + 3 : a ∈ ℝ}.

## Dimension and codimension

For finite-dimensional V, dim(V) = dim(U) + dim(V/U). Equivalently, the codimension of U in V, defined as dim(V/U), equals dim(V) − dim(U).

The map v ↦ [v] is an epimorphism, an onto linear map, from V onto V/U; its kernel is precisely U. This is encoded in the short exact sequence

0 → U → V → V/U → 0.

When V = U ⊕ W is an internal direct sum, where U and W are independent subspaces whose vectors add to give all of V, the quotient V/U is naturally isomorphic to the complement W.

## The first isomorphism theorem

For a linear operator T : V → W, the kernel ker(T) = {x : Tx = 0} is a subspace of V. The first isomorphism theorem states that the induced map

T̄ : V / ker(T) → im(T), T̄([v]) = T(v)

is well-defined and an isomorphism. In finite dimensions this gives the rank–nullity theorem: dim(V) = nullity(T) + rank(T). The cokernel of T is the quotient W / im(T).

## Quotients of Banach and Hilbert spaces

If X is a Banach space, a complete normed vector space, and M is a closed subspace, X/M inherits a Banach space structure with norm ‖[x]‖_{X/M} = inf_{m ∈ M} ‖x − m‖_X. A concrete instance: C[0,1], the continuous real-valued functions on [0,1] with the sup norm, modulo the closed subspace M = {f : f(0) = 0} is isomorphic to ℝ, because two functions are equivalent exactly when they share the value at 0. If X is a Hilbert space, then X/M is isomorphic to the orthogonal complement of M.

Source: adapted from "Quotient space (linear algebra)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Quotient_space_%28linear_algebra%29
