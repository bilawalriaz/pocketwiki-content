# Set (mathematics)

## Overview

A set is a foundational mathematical object: a collection of distinct elements (members), typically numbers, points, functions, or other sets. Because mathematics does not define "set" in terms of prior concepts, its behavior is governed by axiom systems—most notably ZFC (Zermelo–Fraenkel set theory with the axiom of choice)—from which nearly all other mathematical objects are rigorously constructed. The modern theory of sets emerged from 19th-century work on infinity by Georg Cantor, whose paradoxes and counterintuitive results (e.g., that some infinities are larger than others) triggered a foundational crisis resolved by axiomatization. Sets now permeate all of mathematics, serving as the language for defining algebraic structures, spaces, and relations.

## Timeline

- **Pre-1870s** — Infinity viewed as potential, not actual; sets not clearly distinguished from sequences
- **1870s–1880s** — Georg Cantor initiates mathematical study of infinite sets
- **1883** — Cantor proves the real numbers are uncountable
- **1899** — Russell's paradox reveals contradiction in naive set theory
- **1908** — Ernst Zermelo formulates first axiomatization of set theory
- **1920s** — Zermelo–Fraenkel axioms (ZF) refined; ZFC becomes standard
- **1963** — Paul Cohen proves the continuum hypothesis is independent of ZFC

## Body

### Historical Context and Crisis

Before the late 19th century, mathematicians largely avoided treating infinity as a completed object, viewing it instead as a process. Cantor revolutionized this by rigorously studying infinite sets, discovering that the real numbers are "more numerous" than the natural numbers, and that any line segment has the same cardinality as the entire line. These results, along with paradoxes like Russell's paradox (the contradiction arising from assuming a set of all sets), precipitated a foundational crisis. This led to the development of axiomatic set theories, with Zermelo–Fraenkel set theory (ZF, later extended with the axiom of choice to ZFC) becoming the dominant framework.

### Basic Notions and Specification

A set is defined by its elements; two sets are equal if and only if they have the same elements (axiom of extensionality). Sets can be specified by listing elements (roster notation, e.g., {1, 2, 3}) or by a defining property (set-builder notation, e.g., {x | P(x)}). The empty set ∅ is the unique set with no elements. A set is finite if its elements can be placed in bijection with {1, 2, ..., n} for some natural number n; otherwise it is infinite. The natural numbers ℕ, integers ℤ, rationals ℚ, and reals ℝ are all infinite sets.

### Subsets and Containment

A set A is a subset of B (written A ⊆ B) if every element of A is also in B. If A ⊆ B but A ≠ B, then A is a proper subset (A ⊊ B). The empty set is a subset of every set, and two sets are equal if and only if each is a subset of the other.

### Basic Operations

Standard operations produce new sets from existing ones: intersection (A ∩ B = elements in both), union (A ∪ B = elements in either), and set difference (A ∖ B = elements in A but not B). The symmetric difference A Δ B contains elements in exactly one of A or B. These operations are associative and commutative. The powerset 𝒫(U) is the set of all subsets of U; it forms a Boolean algebra under union, intersection, and complement, and a Boolean ring under symmetric difference and intersection.

### Functions and Indexed Families

A function f: A → B assigns to each element of A a unique element of B. Its graph is the set of ordered pairs (a, f(a)), a subset of the Cartesian product A × B. An indexed family (Aᵢ)ᵢ∈ᵢ is a collection of sets labeled by an index set I; it is formally a function from I to the sets. Unions and intersections over families are written ⋃ᵢ∈ᵢ Aᵢ and ⋂ᵢ∈ᵢ Aᵢ.

### External Operations

The Cartesian product A × B is the set of ordered pairs (a, b) with a ∈ A and b ∈ B. Set exponentiation Fᴱ is the set of all functions from E to F. The disjoint union A ⊔ B treats elements from A and B as distinct even if they coincide, labeling them by origin. These operations allow constructing sets whose elements lie outside previously considered sets.

### Cardinality

The cardinality |S| measures the "number of elements" in S. Two sets have the same cardinality if there exists a bijection between them. A set is infinite if and only if it has the same cardinality as one of its proper subsets. Cantor's diagonal argument proves |S| < |2ˢ| (the power set of S has strictly greater cardinality), implying no largest cardinality exists. The cardinality of ℕ is ℵ₀ (aleph-null), the smallest infinity. Sets with cardinality ≤ ℵ₀ are countable; those with cardinality > ℵ₀ are uncountable.

The cardinality of ℝ is the continuum, denoted 𝔠 = 2^{ℵ₀} > ℵ₀. Cantor showed 𝔠 equals the cardinality of the entire plane and any finite-dimensional Euclidean space. The continuum hypothesis (CH), proposed by Cantor in 1878, asserts no set has cardinality strictly between ℵ₀ and 𝔠. In 1963, Paul Cohen proved CH is independent of ZFC: neither CH nor its negation can be derived from the ZFC axioms (assuming ZFC is consistent).

### Axiom of Choice and Equivalents

The axiom of choice (AC) states that for any family of nonempty sets, one can select an element from each. Equivalent formulations include: the Cartesian product of any family of nonempty sets is nonempty; every set can be well-ordered; and Zorn's lemma (if every chain in a partially ordered set has an upper bound, then the set contains a maximal element). AC is widely accepted in mainstream mathematics and is essential for proving results like the existence of a basis for every vector space and maximal ideals in rings. Transfinite induction, a generalization of mathematical induction to well-ordered sets, is fundamental for defining ordinal and cardinal numbers.

## Terms

- **Element/Member**: An object x belonging to a set S, written x ∈ S.
- **Subset**: A set A such that every element of A is also in B (A ⊆ B).
- **Powerset**: The set 𝒫(E) of all subsets of E.
- **Cardinality**: The "size" of a set, measured by the existence of bijections with reference sets.
- **Bijection**: A one-to-one correspondence between two sets; establishes equal cardinality.
- **Countable**: A set with cardinality ≤ ℵ₀ (finite or countably infinite).
- **Uncountable**: A set with cardinality strictly greater than ℵ₀.
- **Well-order**: A total order where every nonempty subset has a least element.
- **Transfinite induction**: Generalization of mathematical induction to well-ordered sets.
- **ZFC**: Zermelo–Fraenkel set theory with the axiom of choice; the standard axiomatic foundation of mathematics.

## Debates and Open Questions

The **continuum hypothesis** (CH) remains unresolved within ZFC: Cohen's 1963 independence proof shows it cannot be proved or disproved from the standard axioms, assuming their consistency. Whether to adopt CH, its negation, or alternative axioms (such as large cardinal axioms) is a matter of ongoing philosophical and mathematical debate. The **axiom of choice** itself was historically controversial due to its non-constructive nature, though it is now widely accepted; some areas of mathematics explore what remains true without AC. The broader question of finding new axioms to settle independent statements like CH continues to drive research in set theory.

Source: adapted from "Set (mathematics)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Set_%28mathematics%29
