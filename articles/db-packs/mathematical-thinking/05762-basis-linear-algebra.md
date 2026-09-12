# Basis (linear algebra)

A **basis** of a vector space *V* is a set of vectors that is both *linearly independent* (no vector in the set is a combination of the others) and a *spanning set* (every vector in *V* is a finite linear combination of vectors from the set). Independence makes each expansion unique, so the scalars in that combination, called **coordinates** with respect to the basis, are well defined.

A vector space has many bases, but every basis has the same number of elements. That number is the **dimension** of the space. A space with a finite basis is *finite-dimensional*.

## Definition

Let *V* be a vector space over a field *F* (typically the real numbers ℝ or complex numbers ℂ). A subset *B* ⊆ *V* is a basis when it satisfies two conditions:

1. **Linear independence.** For any finite subset {v₁, …, vₘ} of *B* and any scalars c₁, …, cₘ in *F*, c₁v₁ + ⋯ + cₘvₘ = 0 forces every cᵢ = 0.
2. **Spanning.** Every v ∈ *V* can be written v = a₁v₁ + ⋯ + aₙvₙ for some aᵢ ∈ *F* and vᵢ ∈ *B*.

Together these give a unique expansion, so the coordinates aᵢ are well defined. An **ordered basis** is a basis with an imposed order on its vectors; order matters when comparing coordinates across bases or discussing orientation.

## Examplesℝ², the space of ordered pairs of real numbers, has standard basis e₁ = (1, 0) and e₂ = (0, 1). Any vector (a, b) decomposes uniquely as a·e₁ + b·e₂. Any other linearly independent pair, such as (1, 1) and (−1, 2), is also a basis.

More generally, *F*ⁿ (the space of *n*-tuples over a field *F*) has standard basis e₁, …, eₙ, where eᵢ has a 1 in position *i* and 0 elsewhere.

The space *F*[*X*] of polynomials in one variable with coefficients in *F* has the infinite **monomial basis** {1, *X*, *X*², …}, showing that polynomial spaces can be infinite-dimensional. Bernstein or Chebyshev polynomial sequences also form bases, provided each degree appears exactly once.

## Properties

Most finite-dimensional properties follow from the **Steinitz exchange lemma**: given a finite spanning set *S* and a linearly independent set *L* with *n* elements, one can swap *n* elements of *S* for the elements of *L* and keep a spanning set of the same size. In infinite dimensions, the corresponding results need the axiom of choice.

For any vector space *V* over a field *F*:

- Every spanning set contains a basis, and every linearly independent set extends to one.
- *V* always has a basis (take *L* = ∅ in the extension property).
- All bases of *V* have the same cardinality, the **dimension** of *V*.
- A spanning set is a basis iff it is *minimal*; a linearly independent set is a basis iff it is *maximal*.

If dim *V* = *n*, then any *n*-element subset is a basis iff it is linearly independent, and likewise iff it spans *V*. One check suffices.

## Coordinates

Fix an ordered basis B = (b₁, …, bₙ) of *V*. The map φ : *F*ⁿ → *V*, (λ₁, …, λₙ) ↦ λ₁b₁ + ⋯ + λₙbₙ is a linear isomorphism from *F*ⁿ (the **coordinate space**) onto *V*. The *n*-tuple φ⁻¹(v) is the **coordinate vector** of v. Every ordered basis of *V* is the image of the standard basis of *F*ⁿ under such an isomorphism, and choosing an ordered basis is equivalent to choosing a linear isomorphism *F*ⁿ → *V*. An ordered basis used with a chosen origin is also called a *frame*.

## Change of basis

Let B_old = (v₁, …, vₙ) and B_new = (w₁, …, wₙ) be two ordered bases. Express the new basis in the old: w_j = Σᵢ aᵢⱼ vᵢ. If x has coordinates X in B_old and Y in B_new, then

xᵢ = Σⱼ aᵢⱼ yⱼ,

or in matrix form, **X = AY**, where *A* = (aᵢⱼ). The formula follows from writing x in both bases and matching coefficients using uniqueness of expansion in B_old.

## Related notions

**Free modules.** Replacing the field by a ring gives a *module*. A basis of a module is again an independent generating set, but not every module has one; a module with a basis is called *free*. A module over ℤ is an abelian group, so a free module over ℤ is a *free abelian group*.

**Infinite-dimensional analysis.** The basis defined here is sometimes called a **Hamel basis** in infinite-dimensional spaces over ℝ or ℂ, to distinguish it from notions that allow infinite combinations. In a Banach space (a complete normed vector space), the Baire category theorem forces every Hamel basis to be uncountable, so analysts prefer Schauder or orthogonal bases. The Fourier basis {1} ∪ {sin(*nx*), cos(*nx*)} spans the square-integrable functions on [0, 2π] only as an infinite combination, not as a Hamel basis of that space.

**Geometry.** An *affine basis* of an *n*-dimensional affine space is *n* + 1 points in general position; a *projective basis* of an *n*-dimensional projective space is *n* + 2 points in general position; a *convex basis* of a polytope is its vertices; a *cone basis* is one point per edge of a polygonal cone.

**Random bases.** In ℝⁿ with a continuous distribution, *n* independent random vectors are linearly independent with probability one, because dependent vectors have determinant zero and the zero set of a nonzero polynomial has measure zero. In high dimensions, independent random vectors are nearly orthogonal with high probability, and the number of such vectors grows exponentially with *n* (a *measure concentration* phenomenon).

## Existence

Every vector space has a basis, but the general proof uses the **axiom of choice** (equivalently, Zorn's lemma). Let *X* be the set of all linearly independent subsets of *V*, partially ordered by inclusion. Every totally ordered subfamily has an upper bound, namely its union. By Zorn's lemma, a maximal independent set exists; it must span *V*, because any non-spanned vector could be added to form a larger independent set, contradicting maximality. The converse also holds: a basis existing for every vector space implies the axiom of choice.

Source: adapted from "Basis (linear algebra)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Basis_%28linear_algebra%29
