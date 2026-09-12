# Natural number

## Overview
Natural numbers are the basic counting numbers (0, 1, 2, 3, ...) possibly excluding 0, used for counting and ordering. They form the foundation for all other number systems and are central to arithmetic, number theory, and combinatorics. Their formal definition involves either the Peano axioms or set-theoretic constructions, with ongoing debate about whether 0 is included.

## Timeline
- **c. 1484** — Nicolas Chuquet uses "progression naturelle"
- **1763** — First known use of "natural number" in English
- **1860s** — Hermann Grassmann proposes recursive definition
- **1881** — Charles Sanders Peirce first axiomatizes natural-number arithmetic
- **1888** — Richard Dedekind proposes axiomatization
- **1889** — Giuseppe Peano publishes simplified axioms
- **1978** — ISO 31-11 formalizes inclusion of 0

## Body

### Intuitive Concept
Natural numbers arise naturally through counting and ordering. Two key aspects are cardinality (size of a collection) and ordinality (position in a sequence). Cardinality is established via one-to-one correspondence between collections, while ordinality uses well-ordered sets where each element has a clear successor. The natural numbers form the simplest infinite well-ordered set with order type ω.

### Terminology and Notation
The term "natural numbers" has two common definitions: {0, 1, 2, ...} or {1, 2, 3, ...}. To resolve ambiguity, positive integers (starting at 1) and non-negative integers (including 0) are used. The set is denoted ℕ, with subscripts like ℕ₀ or ℕ₁ clarifying inclusion of 0. "Whole numbers" sometimes refers to natural numbers including 0, but can also mean all integers.

### Formal Definitions
Formal definitions build on intuitive understanding using mathematical logic. Two standard approaches are the Peano axioms and set theory. The Peano axioms define natural numbers through five statements: 0 is natural, every number has a successor, 0 is not a successor, successors are unique, and mathematical induction holds. Set theory defines each number as a set, with the von Neumann construction defining 0 as the empty set and each successor as S(a) = a ∪ {a}.

### Properties
Natural numbers support addition and multiplication, defined recursively via the successor function. Addition makes ℕ a commutative monoid with identity 0, while multiplication makes ℕ* a free commutative monoid with identity 1. The structure (ℕ, +, ×) forms a semiring (rig) since it lacks additive inverses. Natural numbers are well-ordered, meaning every non-empty subset has a least element. Division is handled via Euclidean division: for any a, b with b ≠ 0, there exist unique q, r such that a = b×q + r and r < b.

### History
Originally, natural numbers were simply "numbers." The need to distinguish them arose as negative, rational, and irrational numbers were discovered. Formal construction efforts in 19th-century Europe addressed foundational questions. Poincaré emphasized finite application of axioms, while Kronecker believed "God made the integers." Constructivists like Grassmann showed natural numbers result from recursive definitions. Frege's class-based definition led to paradoxes, prompting the shift to defining each number as a specific set.

## Terms
- **Cardinal number**: A number describing the size of a collection
- **Ordinal number**: A number describing position in an ordered sequence
- **Successor function**: A function S(n) that gives the next natural number after n
- **Well-ordered set**: A set where every non-empty subset has a least element
- **Peano axioms**: Five axioms defining natural numbers through succession and induction
- **Von Neumann ordinals**: Set-theoretic construction where each number is the set of all smaller numbers
- **Semiring (rig)**: Algebraic structure like a ring but without additive inverses
- **Euclidean division**: Division with remainder producing unique quotient and remainder

## Debates and Open Questions
The primary debate concerns whether 0 is a natural number. Early authors mostly excluded 0, but inclusion gained acceptance in the 1960s, formalized by ISO standards. Another foundational question involves the equivalence of different formal definitions—Peano arithmetic and set theory are consistent but differ in philosophical implications. Additionally, some theorems (like Goodstein's theorem) are provable in ZFC set theory but not in Peano arithmetic, highlighting limitations in formal systems.

Source: adapted from "Natural number" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Natural_number
