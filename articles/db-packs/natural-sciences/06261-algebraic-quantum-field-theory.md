# Algebraic quantum field theory

Algebraic quantum field theory (AQFT), introduced by Rudolf Haag and Daniel Kastler in 1964 and also called the Haag–Kastler framework, applies C*-algebra theory to local quantum physics. It describes a quantum field not by a single operator on a Hilbert space but by a family of algebras, one for every region of spacetime, with the algebraic relations between them encoding physics.

## Algebras indexed by spacetime regions

A C*-algebra is an algebraic structure generalising the bounded operators on a Hilbert space. A von Neumann algebra is a C*-algebra closed in the topology defined by its Hilbert-space action. The framework assigns to every open, bounded region $O$ of Minkowski space a von Neumann algebra $\mathcal{A}(O)$ on a common Hilbert space $\mathcal{H}$. Each $\mathcal{A}(O)$ is a *local algebra*, representing all physical operations performed inside that region. The local algebras are partially ordered by inclusion: if $O_1 \subset O_2$ then $\mathcal{A}(O_1) \subset \mathcal{A}(O_2)$, a property called isotony. The *quasilocal algebra* $\mathcal{A}$ is the C*-closure of their union, representing operations in the whole spacetime.

## The Haag–Kastler axioms

Five axioms fix the physical content:

1. Causality: if $O_1$ is spacelike separated from $O_2$ (no signal at or below light speed can connect them), every operator in $\mathcal{A}(O_1)$ commutes with every operator in $\mathcal{A}(O_2)$.
2. Poincaré covariance: a strongly continuous unitary representation $U(\mathcal{P})$ of the Poincaré group on $\mathcal{H}$ exists such that $\mathcal{A}(gO) = U(g)\mathcal{A}(O)U(g)^*$ for every $g$.
3. Spectrum condition: the joint spectrum of the energy–momentum operator lies in the closed forward lightcone, so energy is non-negative.
4. Existence of a vacuum: a cyclic, Poincaré-invariant vector $\Omega \in \mathcal{H}$ exists, representing the empty state.

Isotony, the basic inclusion property, is given in the region setup above.

## Category-theoretic reformulation

The same structure is a covariant functor $\mathcal{A}$ from the category of open subsets of Minkowski space (with inclusion maps) to the category of unital C*-algebras, mapping inclusions to monomorphisms. Causal structure is encoded by requiring that the images of $\mathcal{A}$ on causally separated open sets commute, and that the map from an open set to its causal completion is an isomorphism (primitive causality). A continuous pullback of the Poincaré action encodes covariance. This formulation is the natural setting for generalisation to curved spacetimes, where no global Poincaré structure exists.

## States and representations

A state on a C*-algebra is a positive linear functional of unit norm, assigning expectation values to operators. Restricting a state on $\mathcal{A}(M)$ through the net monomorphisms gives states on each $\mathcal{A}(O)$, forming a presheaf. By the GNS construction, each state yields a Hilbert-space representation: pure states produce irreducible representations, mixed states produce reducible ones. Each equivalence class of irreducible representations is a *superselection sector*. The vacuum sector is the representation built from $\Omega$, with energy–momentum spectrum in the forward lightcone as required by the spectrum condition.

## Curved spacetimes

Because the framework ties physics to spacetime regions rather than a fixed background, it generalises to curved spacetimes. The local-algebra viewpoint supports a renormalisation procedure on curved backgrounds, and results concerning quantum fields in the presence of black holes have been obtained within it.

Source: adapted from "Algebraic quantum field theory" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Algebraic_quantum_field_theory
