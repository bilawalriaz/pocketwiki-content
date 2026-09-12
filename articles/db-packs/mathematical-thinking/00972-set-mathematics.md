# Set (mathematics)

A set is a collection of distinct elements, called members. The elements can be numbers, points, functions, or other sets. Mathematics does not reduce "set" to any prior concept; its behaviour is instead governed by an axiom system, most often Zermelo–Fraenkel set theory with the axiom of choice (ZFC), from which nearly every other mathematical object is constructed.

The modern theory arose in the 1870s when Georg Cantor began treating infinite sets as completed objects rather than as processes. His central discovery was that some infinities are larger than others. In 1883 he proved the real numbers outnumber the natural numbers, and he showed that a line segment has the same cardinality as the entire line. These results overturned the older view of "infinity" as a single, undifferentiated idea and made sets the universal language for algebra, topology, and analysis.

## How a set is defined

A set is determined entirely by its elements. Two sets are equal precisely when they have the same members, which is the axiom of extensionality. Sets are written either by listing members, called roster notation, as in {1, 2, 3}, or by stating a defining property, called set-builder notation, as in {x | P(x)}. The empty set, written ∅, is the unique set with no elements. A set is finite when its elements can be placed in one-to-one correspondence (a bijection) with {1, 2, …, n} for some natural number n; otherwise it is infinite. The natural numbers ℕ, integers ℤ, rationals ℚ, and real numbers ℝ are all infinite.

## Subsets and containment

A set A is a subset of B, written A ⊆ B, when every element of A is also an element of B. If A ⊆ B but A ≠ B, then A is a proper subset, written A ⊊ B. The empty set is a subset of every set, and two sets are equal exactly when each is a subset of the other.

## Basic operations

Three operations combine sets. The intersection A ∩ B contains the elements common to both; the union A ∪ B contains the elements in either; and the set difference A ∖ B contains the elements in A but not in B. The symmetric difference A Δ B contains the elements in exactly one of A or B. These operations are associative and commutative. Given a set U, its powerset 𝒫(U) is the set of all subsets of U.

## Functions and the Cartesian product

A function f: A → B assigns to each element of A a unique element of B. Its graph, the set of ordered pairs (a, f(a)), is a subset of the Cartesian product A × B, the set of all pairs (a, b) with a ∈ A and b ∈ B. The disjoint union A ⊔ B keeps track of which set each element came from, and set exponentiation Fᴱ denotes the set of all functions from E to F. An indexed family (Aᵢ)ᵢ ∈ I is a function from an index set I into the collection of sets, letting one write ⋃ᵢ Aᵢ and ⋂ᵢ Aᵢ for unions and intersections over the family.

## Cardinality

The cardinality |S| generalises "number of elements" to infinite sets. Two sets have the same cardinality when a bijection exists between them. A set is infinite exactly when it has the same cardinality as one of its proper subsets.

Cantor's diagonal argument shows that the powerset of any set S is strictly larger than S itself: |S| < |2ˢ|. No largest cardinality therefore exists. The smallest infinite cardinality is ℵ₀ (aleph-null), the size of the natural numbers. Sets of size at most ℵ₀ are countable; those of larger size are uncountable. The real numbers have cardinality 𝔠 = 2^{ℵ₀} > ℵ₀, called the continuum, and Cantor showed 𝔠 equals the cardinality of any finite-dimensional Euclidean space.

The continuum hypothesis (CH), proposed by Cantor in 1878, asserts that no set has cardinality strictly between ℵ₀ and 𝔠. In 1963 Paul Cohen proved CH is independent of ZFC, so neither CH nor its negation can be derived from the standard axioms (assuming ZFC itself is consistent).

## The paradoxes and the axioms

Cantor's work exposed contradictions, the most famous being Russell's paradox of 1899, which arose from the naive assumption that any defining property yields a set: the "set of all sets that do not contain themselves" is both a member of itself and not. To prevent such contradictions, Ernst Zermelo produced the first axiomatisation in 1908; refinements through the 1920s produced the Zermelo–Fraenkel axioms (ZF), and adding the axiom of choice gave ZFC.

## The axiom of choice

The axiom of choice (AC) states that from any family of nonempty sets, one element can be chosen from each. Equivalent formulations include: the Cartesian product of any family of nonempty sets is nonempty; every set admits a well-ordering (a total ordering in which every nonempty subset has a least element); and Zorn's lemma holds, meaning that if every chain in a partially ordered set has an upper bound, the set contains a maximal element. AC was once controversial for its non-constructive character, but it is now standard and underpins results such as the existence of a basis for every vector space and the existence of maximal ideals in rings.
