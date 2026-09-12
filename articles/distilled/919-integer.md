# Integer

## Overview
An integer is zero, a positive natural number (1, 2, 3, …), or the negation of a positive natural number (−1, −2, −3, …); the set of all integers is denoted ℤ. Integers form the smallest ring containing the natural numbers and are countably infinite, serving as the foundational number system for algebra, number theory, and computer science.

## Timeline
- **Latin origin**: *integer* means "whole" or "untouched" (from *in* + *tangere*).
- **1765**: Leonhard Euler defines integers to include both positive and negative numbers.
- **Late 19th century**: Georg Cantor introduces infinite sets and set theory; the phrase "set of integers" comes into use.
- **Early 20th century**: David Hilbert attributes the use of ℤ (from German *Zahlen*) to denote integers.
- **1947**: Nicolas Bourbaki's *Algèbre* contains the earliest known textbook use of ℤ.
- **1961**: ℤ becomes generally adopted in modern algebra texts for positive and negative integers.

## Body

### Algebraic Properties
The integers are closed under addition, multiplication, and subtraction (unlike natural numbers, which are not closed under subtraction). Under addition, ℤ forms an abelian group and, more specifically, the unique infinite cyclic group. Under multiplication, ℤ is a commutative monoid but not a group, since most integers lack multiplicative inverses. Together, addition and multiplication make ℤ a commutative ring with unity, which is an integral domain (no zero divisors) but not a field (no multiplicative inverses in general). The smallest field containing ℤ is the field of rational numbers ℚ.

Euclidean division defines division with remainder on ℤ: for any integers *a* and *b* with *b* ≠ 0, there exist unique integers *q* (quotient) and *r* (remainder) such that *a* = *q* × *b* + *r* and 0 ≤ *r* < |*b*|. This makes ℤ a Euclidean domain, implying it is a principal ideal domain and supporting the fundamental theorem of arithmetic (unique prime factorization).

### Order-Theoretic Properties
ℤ is a totally ordered set without upper or lower bounds: … < −3 < −2 < −1 < 0 < 1 < 2 < 3 < …. An integer is positive if greater than zero, negative if less than zero, and zero is neither. The ordering is compatible with addition and multiplication, making ℤ an ordered ring. ℤ is the only nontrivial totally ordered abelian group whose positive elements are well-ordered.

### Construction
**Traditional development**: Integers are constructed as the union of the natural numbers *P*, a disjoint set *P⁻* in one-to-one correspondence with *P* (via a function ψ), and {0}. Arithmetic operations are defined piecewise across positive, negative, and zero cases.

**Equivalence classes of ordered pairs**: In modern set theory, integers are constructed as equivalence classes of ordered pairs of natural numbers (a, b), where (a, b) represents *a* − *b*. The equivalence relation is (a, b) ~ (c, d) precisely when *a* + *d* = *b* + *c*. Addition, multiplication, negation, subtraction, and ordering are all defined in terms of operations on natural numbers, avoiding case distinctions. Each equivalence class has a unique representative of the form (n, 0) or (0, n), recovering the familiar notation {…, −2, −1, 0, 1, 2, …}.

**Other approaches**: In theoretical computer science, integers are constructed using algebraic terms with basic operations like zero, succ, and pred, with at least ten known constructions differing in operation count, argument types, and constructor freedom.

### Computer Science
In programming, integers are often a primitive data type, but practical computers can only represent a finite subset of ℤ. Two's complement representation distinguishes "negative" from "non-negative" rather than using three-way sign classification. Fixed-length types (int, Integer) are common in languages like C, Java, and Algol68. Variable-length representations like bignums can store any integer fitting in memory.

### Cardinality
ℤ is countably infinite, with cardinality ℵ₀ (aleph-null). A bijection exists between ℤ and ℕ, exemplified by the pairing (0,1), (1,2), (−1,3), (2,4), (−2,5), (3,6), …, (1−k, 2k−1), (k, 2k), ….

## Terms
- **Integer**: Zero, a positive natural number, or the negation of a positive natural number.
- **ℤ (Zahlen)**: The set of all integers, named after the German word for "numbers."
- **Euclidean domain**: An integral domain where Euclidean division (division with remainder) is defined.
- **Equivalence class**: A set of elements considered equivalent under a given equivalence relation.
- **Ordered ring**: A ring equipped with a total order compatible with addition and multiplication.
- **Integral domain**: A commutative ring with unity and no zero divisors.
- **Field of fractions**: The smallest field containing a given integral domain (e.g., ℚ from ℤ).
- **Countably infinite**: A set that can be put into one-to-one correspondence with the natural numbers.
- **Bignums**: Variable-length integer representations in computer science that can store arbitrarily large integers.
- **Two's complement**: A common method for representing signed integers in binary computer systems.

## Debates and Open Questions
The definition of "whole numbers" remains ambiguous: until the early 1950s, it was synonymous with integers, but the New Math movement redefined it as natural numbers excluding negatives, while "integer" includes negatives. Notation for subsets of ℤ is inconsistent across authors: ℤ⁺, ℤ₊, or ℤ> for positive integers; ℤ⁰⁺ or ℤ≥ for non-negative integers; ℤ≠ or ℤ* for non-zero integers (though ℤ* is also used for non-negative integers or {−1, 1}). Additionally, ℤₚ ambiguously denotes either integers modulo p or p-adic integers.