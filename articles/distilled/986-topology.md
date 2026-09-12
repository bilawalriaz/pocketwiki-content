# Topology

## Overview  
Topology is the branch of mathematics that studies properties of geometric objects preserved under continuous deformations—stretching, twisting, bending—without tearing, gluing, or closing/opening holes. It matters because many geometric and physical problems depend not on exact shape but on how objects are assembled (connectivity, holes, boundaries). The field grew from 18th-century puzzles like Euler’s Seven Bridges of Königsberg into a foundational discipline with applications in biology, computer science, physics, robotics, and data analysis.

## Timeline  
- **1736** — Euler solves the Seven Bridges of Königsberg problem, regarded as one of the first topology applications
- **1750** — On 14 November 1750, Euler wrote to a friend that he had realized the importance of the edges of a polyhedron. This led to his polyhedron formula, V − E + F = 2
- **1847** — Johann Benedict Listing introduces the term “Topologie” in *Vorstudien zur Topologie*
- **1883** — The English form "topology" was used in Listing's obituary in the journal Nature
- **1895** — Henri Poincaré publishes *Analysis Situs*, introducing homotopy and homology
- **1906** — Maurice Fréchet introduced the metric space, unifying work on function spaces of Cantor, Volterra, Arzelà, Hadamard, and Ascoli
- **1914** — Felix Hausdorff coined the term "topological space" and defined what is now called a Hausdorff space
- **1922** — Currently, a topological space is a slight generalization of Hausdorff spaces, given in 1922 by Kazimierz Kuratowski
- **2016** — David Thouless, Duncan Haldane, and Michael Kosterlitz were awarded the 2016 Nobel Prize in Physics for their work on Topological orders
- **2022** — The 2022 Abel Prize was awarded to Dennis Sullivan "for his groundbreaking contributions to topology in its broadest sense, and in particular its algebraic, geometric and dynamical aspects"

## Body  

### Motivation and Basic Concepts  
The core insight is that some geometric problems depend on connectivity rather than exact shape. Euler’s Königsberg bridge problem showed that no route crosses each bridge exactly once—a result depending only on which bridges connect which landmasses. Similarly, the hairy ball theorem states that one cannot comb hair flat on a sphere without creating a cowlick; this applies to any shape homeomorphic to a sphere. These problems rely on properties invariant under homeomorphism—deformation without cutting or gluing. Intuitively, a coffee mug and a doughnut are topologically identical because one can be continuously deformed into the other.

A **topological space** is a set X equipped with a **topology** τ—a family of subsets (open sets) satisfying three axioms: the empty set and X belong to τ; any union of open sets is open; any finite intersection of open sets is open. Closed sets are complements of open sets; a set may be open, closed, both (clopen), or neither. A **continuous function** between topological spaces is one whose inverse image of every open set is open. A **homeomorphism** is a continuous bijection with a continuous inverse; two spaces related by a homeomorphism are topologically identical.

### Subfields  
**General (point-set) topology** establishes foundational definitions—continuity, compactness, connectedness—in terms of open sets. **Metric spaces**, where distance is defined by a metric, are a key class; any metric induces a topology. **Algebraic topology** uses algebraic invariants (homotopy groups, homology, cohomology) to classify spaces up to homeomorphism or homotopy equivalence. **Differential topology** studies differentiable functions on smooth manifolds, focusing on properties requiring only a smooth structure. **Geometric topology** centers on low-dimensional manifolds (dimensions 2–4) and their interaction with geometry, including the uniformization theorem (2D) and the geometrization theorem (3D). **Pointless topology** and **Grothendieck topologies** generalize the framework to settings lacking a set of points.

### Applications  
Topology finds broad application. In **biology**, knot theory studies DNA enzyme effects, and circuit topology classifies folded proteins. In **computer science**, topological data analysis uses persistent homology to detect large-scale data structure, while domain theory formalizes programming semantics via topological spaces. In **physics**, topological quantum field theories compute invariants relevant to quantum computing and string theory (Calabi–Yau manifolds); the quantum Hall effect exemplifies topological order. In **robotics**, configuration spaces describe possible robot positions for motion planning. **Games and puzzles** exploit topological properties, and **fiber art** applies Eulerian paths to continuous joins.

## Terms  
- **Homeomorphism**: A continuous bijection with a continuous inverse; spaces related by homeomorphism are topologically equivalent.  
- **Homotopy equivalence**: A weaker equivalence where two objects both result from “squishing” a larger object.  
- **Topological space**: A set X with a topology τ (a family of open sets satisfying closure under unions and finite intersections).  
- **Open set**: A member of the topology τ; its complement is a closed set.  
- **Continuous function**: A map where the inverse image of every open set is open.  
- **Manifold**: A topological space locally homeomorphic to Euclidean space of fixed dimension n.  
- **Compactness**: A property (defined via open covers) distinguishing, e.g., a line from a circle.  
- **Connectedness**: A property distinguishing a circle from two disjoint circles.  
- **Algebraic topology**: A branch using algebraic invariants (homology, homotopy) to classify spaces.  
- **Topological invariant**: A property preserved under homeomorphisms or homotopies (e.g., dimension, compactness).

## Debates and open questions  
The source notes that some authorities regard Euler’s polyhedron formula as the first theorem signaling the birth of topology, though this characterization is debated. Additionally, the extent to which topology should be viewed as originating in the early 20th century versus having deeper historical roots (e.g., Leibniz’s *geometria situs*) remains a matter of scholarly interpretation.

Source: adapted from "Topology" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Topology
