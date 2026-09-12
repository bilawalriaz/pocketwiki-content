# Algebra

## Overview

Algebra is the branch of mathematics that studies algebraic structures—non-empty sets of mathematical objects (like integers) together with operations defined on them (like addition)—and the manipulation of expressions within those systems. It generalizes arithmetic by introducing variables for unspecified quantities and by extending beyond standard arithmetic operations. Algebra is foundational to modern mathematics and science: its methods are applied across geometry, topology, number theory, calculus, logic, physics, and computer science, and its historical development from solving isolated problems to a self-contained symbolic discipline marks one of the great intellectual transformations in human thought.

## Timeline

- **c. 1650 BCE** — Rhind Mathematical Papyrus (Egypt) discusses solutions to linear equations
- **c. 1650 BCE** — Babylonian clay tablets explain methods for linear and quadratic equations
- **6th c. BCE–3rd c. CE** — Greeks apply algebraic methods to geometry; Diophantus writes *Arithmetica* (3rd c. CE)
- **10th c. BCE–2nd c. CE** — Chinese *Nine Chapters on the Mathematical Art* uses matrix-like constructs
- **825 CE** — Al-Khwarizmi publishes *The Compendious Book on Calculation by Completion and Balancing*, systematizing algebra as an independent discipline
- **7th–12th c. CE** — Indian mathematicians (Brahmagupta, Mahāvīra, Bhāskara II) refine methods; Qin Jiushao (1247) develops polynomial evaluation algorithm
- **1545** — Cardano's *Ars Magna* presents general methods for cubic and quartic equations
- **16th–17th c.** — Viète and Descartes introduce symbolic notation for variables and operations
- **Early 19th c.** — Gauss proves the fundamental theorem of algebra; Ruffini and Abel show no general solution exists for degree 5+ polynomials; Galois develops Galois theory
- **Mid-19th c.–present** — Shift to abstract algebra; emergence of universal algebra (Whitehead 1898), topological algebra, homological algebra, and category theory

## Body

### Definition and etymology

Algebra is often understood as a generalization of arithmetic. Elementary algebra constitutes the first level of abstraction: like arithmetic, it restricts itself to specific types of numbers and operations, but it generalizes these by allowing variables. Abstract algebra is not limited to a particular domain and examines structures such as groups and rings. Universal algebra is still more abstract, investigating characteristics of algebraic structures in general. The term "algebra" can also refer, as a countable noun, to a specific type of algebraic structure involving a vector space with a bilinear map (e.g., a Lie algebra).

The word comes from the Arabic *al-jabr*, originally referring to surgical bonesetting. In the 9th century, al-Khwarizmi gave it a mathematical meaning in the title of his treatise, translated into Latin as *Liber Algebrae et Almucabola*. The word entered English in the 16th century from Italian, Spanish, and medieval Latin. Initially restricted to the theory of equations, its meaning broadened in the 19th century to cover diverse algebraic operations and structures.

### Elementary algebra

Elementary algebra (also called school, college, or classical algebra) is the oldest and most basic form. It relies on variables—symbols for unspecified or unknown quantities—to express general laws, such as the commutative property of multiplication (*a* × *b* = *b* × *a*). Algebraic expressions combine variables and numbers via arithmetic operations. Equations state that two expressions are equal; inequations use symbols like <, >, and ≠. Statements can be true or false depending on variable values. Identity equations are true for all values; conditional equations only for some.

The main goal is determining values for which statements are true. A key principle: whatever operation is applied to one side of an equation must be done to the other. Solving involves isolating the variable. Other techniques include simplification (e.g., 7*x* − 3*x* = 4*x* by the distributive property) and substitution. Equations can be interpreted geometrically as graphs, with variable values as coordinates.

**Polynomials.** A polynomial is an expression of terms added or subtracted, each term being a constant, a variable, or a product of constants and variables raised to positive integer powers. The degree is the maximal sum of exponents. Polynomials of degree one are linear. Factorization rewrites a polynomial as a product of factors (e.g., *x*² − 3*x* − 10 = (*x* + 2)(*x* − 5)). The quadratic formula solves second-degree equations; cubic and quartic formulas exist for degrees 3 and 4. The Abel–Ruffini theorem (19th century) proved no general solutions exist for higher degrees. The fundamental theorem of algebra asserts every univariate polynomial of positive degree with real or complex coefficients has at least one complex solution, but provides no way to compute them.

### Linear algebra

Linear algebra studies systems of linear equations—equations expressible as *a₁x₁* + *a₂x₂* + ... + *aₙxₙ* = *b*. Matrices—rectangular arrays of values—were introduced for compact notation of such systems. Under certain conditions, matrices can be added, multiplied, and inverted; all solving methods can be expressed as matrix manipulations. Methods range from substitution and elimination to Cramer's rule, Gaussian elimination, and LU decomposition. Systems are either inconsistent (no solutions) or consistent (one unique or infinite solutions).

Vector spaces and linear maps form a large part of linear algebra. A vector space is a set with addition (forming an abelian group) and scalar multiplication compatible with addition. A linear map is a function between vector spaces compatible with both operations. In finite-dimensional cases, vectors and linear maps can be represented by matrices, making the theories essentially identical. Systems of equations can be interpreted geometrically: two-variable equations represent lines (intersecting, parallel, or coincident); three-variable equations represent planes.

### Abstract algebra

Abstract algebra (also called modern algebra) studies algebraic structures generally, comparing types like groups, rings, and fields. A structure is a set (the underlying set) with one or more operations, primarily binary operations mapping two objects to another. The underlying set can contain non-numbers (e.g., geometric transformations), and operations need not be arithmetic.

**Group theory.** A group has one operation that is associative, has an identity element, and has inverse elements. For example, ⟨ℤ, +⟩ is a group (identity 0, inverse −*a*), but natural numbers with addition are not (lacking inverses). Key results include the fundamental theorem of finite abelian groups and the Feit–Thompson theorem, a step in the complete classification of finite simple groups—a collaborative effort taking over 10,000 journal pages, mostly published 1960–2004.

**Ring theory and field theory.** A ring has two operations like addition and multiplication: it is a commutative group under addition; multiplication is associative and distributive over addition, with an identity element (1). Multiplication need not be commutative. A field is a commutative ring with 1 ≠ 0 where every nonzero element has a multiplicative inverse. Integers do not form a field (7's inverse is 1/7, not an integer); rationals, reals, and complex numbers do. Galois theory explores the relation between field theory and group theory.

**Theories of interrelations.** Other structures include magmas, semigroups, monoids, abelian groups, modules, lattices, and algebras over a field; adding constraints turns basic structures into specialized ones (a magma becomes a semigroup if its operation is associative). Homomorphisms are functions preserving structural characteristics between structures; isomorphisms are bijective homomorphisms indicating high similarity. A subalgebra uses the same operations but a subset of the underlying set, requiring closure. Universal algebra studies structures in general, including operations with more than two inputs, and varieties (classes satisfying certain identities). Category theory examines objects and morphisms ("arrows") between them, with composition required to be associative and identity morphisms present; it provides a unifying framework in contemporary mathematics.

### History

Algebraic methods originated in ancient Babylonia, Egypt, Greece, China, and India for solving arithmetic problems with unknown quantities. The Rhind Mathematical Papyrus (c. 1650 BCE) discusses linear equations; Babylonian tablets cover completing the square. Greeks (from 6th century BCE) applied algebraic methods to geometry; Diophantus (3rd century CE) experimented with symbolic notation. It is disputed whether these were algebra proper or precursors, as they focused on specific cases rather than abstract generality.

Al-Khwarizmi (825 CE) changed this by classifying equations into six standard forms and providing systematic solution procedures, transforming algebra into a self-contained discipline. Fibonacci brought these ideas to Europe. Cardano (1545) presented cubic and quartic solutions. Viète and Descartes introduced symbolic notation in the 16th–17th centuries—some historians see this as the key turning point, considering earlier work prehistory. After failed attempts at general solutions for degree 5+, Ruffini and Abel proved none exist; Galois developed Galois theory and laid group theory's foundations. From the mid-19th century, interest shifted to abstract algebra, with contributions from Hilbert, Steinitz, Noether, and Artin. Whitehead conceived universal algebra (1898); Birkhoff expanded it from the 1930s. Topological algebra arose in the early 20th century; homological algebra in the 1940s–50s; category theory developed around the same time.

### Applications

The algebraization of mathematics applies algebraic methods to other branches. In geometry, equations describe figures (e.g., *y* = 3*x* − 7 describes a line); algebraic varieties are solutions to polynomial equation systems. Algebraic topology uses group theory to classify topological spaces (e.g., homotopy groups detect loops or holes). Algebraic number theory applies algebraic methods to integers (e.g., Fermat's Last Theorem). Algebraic logic uses Boolean algebra for propositional logic. In the sciences, algebraic methods express laws in physics, chemistry, and biology, and are used in economics, engineering, and computer science. Linear algebra is central to artificial intelligence and machine learning. Group theory is used in crystallography, quantum mechanics, Sudoku, Rubik's Cubes, and origami; coding theory and cryptology rely on abstract algebra.

### Education

Algebra education focuses on elementary algebra, usually introduced in secondary education after arithmetic mastery. It poses cognitive challenges of abstract reasoning and generalization. Tools include geometric analogies, manipulatives, "function machines," balance scales (where unknown masses represent variables), and word problems (e.g., Naomi's brother has twice her apples; together they have twelve: 2*x* + *x* = 12, so *x* = 4). At university, students take linear algebra (matrices, vector spaces, linear maps) then abstract algebra (groups, rings, fields), typically covering specific instances like rational numbers, reals, and polynomials.

## Terms

- **Algebraic structure**: A non-empty set of mathematical objects together with one or more operations defined on it.
- **Variable**: A symbol for an unspecified or unknown quantity.
- **Polynomial**: An expression of terms (constants, variables, or products) added or subtracted; its degree is the maximal sum of exponents.
- **Matrix**: A rectangular array of values used to compactly represent systems of linear equations.
- **Vector space**: A set with addition (forming an abelian group) and scalar multiplication compatible with addition.
- **Group**: A structure with one associative operation having an identity element and inverse elements.
- **Ring**: A structure with two operations (like addition and multiplication); a commutative group under addition, with associative, distributive multiplication.
- **Field**: A commutative ring with 1 ≠ 0 where every nonzero element has a multiplicative inverse.
- **Homomorphism**: A function between algebraic structures preserving structural characteristics; a bijective homomorphism is an isomorphism.
- **Category**: A collection of objects with morphisms between them, satisfying composition and identity conditions.

## Debates and open questions

It is disputed whether ancient developments (Babylonian, Egyptian, Greek, Chinese, Indian) constitute algebra proper or only precursors, since they offered solutions to specific problems without conceiving them abstractly or generally. Some historians see the 16th–17th century introduction of symbolic notation by Viète and Descartes as the key turning point, considering everything before it the "prehistory" of algebra. The fundamental theorem of algebra guarantees existence of complex solutions for polynomials but does not close the problem, as it provides no method for computing them.