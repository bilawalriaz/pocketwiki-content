# Boolean algebra

Boolean algebra is the algebra of two values, true and false, usually written 1 and 0. Where elementary algebra uses numbers and arithmetic operators, Boolean algebra uses truth values and three logical operators: AND (∧, conjunction), OR (∨, disjunction), and NOT (¬, negation). The values do not behave like the integers 0 and 1, where 1 + 1 = 2. They behave like elements of the two-element field GF(2), where 1 + 1 = 0. Identifying AND with multiplication and OR with addition modulo 2 makes every Boolean expression an arithmetic expression in disguise, though XOR and ordinary OR differ in Boolean contexts.

## Operations

The three basic operations are defined by the rule that AND returns 1 only when both inputs are 1, OR returns 0 only when both inputs are 0, and NOT flips 0 and 1. A truth table makes this explicit:

| x | y | x ∧ y | x ∨ y | ¬x |
|---|---|-------|-------|-----|
| 0 | 0 | 0 | 0 | 1 |
| 0 | 1 | 0 | 1 | 1 |
| 1 | 0 | 0 | 1 | 0 |
| 1 | 1 | 1 | 1 | 0 |

Only two of the three are needed, because De Morgan's laws let you express each in terms of the other plus negation: x ∧ y = ¬(¬x ∨ ¬y) and x ∨ y = ¬(¬x ∧ ¬y). Useful secondary operations include implication x → y = ¬x ∨ y, equivalence x ≡ y, and XOR x ⊕ y, which is true exactly when its inputs differ and equals arithmetic addition modulo 2.

## Laws

A Boolean law is an identity that holds for all assignments of truth values to its variables. Boolean algebra shares many laws with ordinary algebra: associativity, commutativity, and distributivity of ∧ over ∨. It also has laws ordinary algebra lacks, because values can only be 0 or 1: x ∨ 1 = 1, x ∧ 0 = 0, idempotence x ∨ x = x and x ∧ x = x, and the two absorption laws x ∧ (x ∨ y) = x and x ∨ (x ∧ y) = x. Negation is captured by the complement laws x ∧ ¬x = 0 and x ∨ ¬x = 1, from which double negation ¬¬x = x and De Morgan's laws follow.

The monotone laws plus the two complement laws form a complete axiomatization. Every other Boolean identity is derivable from these, and every structure satisfying them is a Boolean algebra. Finitely many equations suffice, and a single equation using only the Sheffer stroke (NAND) can axiomatize the whole theory.

## Duality

Every Boolean operation pairs with a dual obtained by swapping 0 ↔ 1 and ∧ ↔ ∨ simultaneously. The duality principle says that if an identity holds, so does the identity formed by replacing every operator and constant with its dual, because interchanging both pairs leaves the structure indistinguishable. Complement is self-dual.

## Boolean algebras as structures

A concrete Boolean algebra is a collection of subsets of some set X closed under union, intersection, and complement. The power set of X is the standard example. An abstract Boolean algebra is any set with ∧, ∨, and ¬ operations satisfying the Boolean laws; its elements need not be sets. M. H. Stone proved in 1936 that every abstract Boolean algebra is isomorphic to some field of sets, so the two notions coincide. Because of this, the laws satisfied by all Boolean algebras are exactly the laws satisfied by the two-element algebra {0, 1}. The nondegenerate case, where 0 ≠ 1, is the one used in practice.

## Applications

George Boole introduced Boolean algebra in *The Mathematical Analysis of Logic* (1847) and developed it further in *An Investigation of the Laws of Thought* (1854). In 1937 Claude Shannon formally established the equivalence between Boolean algebra and switching circuits, founding switching algebra, so the two terms are often used interchangeably.

Every modern computer is built from two-valued Boolean circuits. Bits are stored as voltages, magnetic orientations, or holes, and combined by AND, OR, and NOT gates. Programmers encounter Boolean operations whenever they combine conditions, mask bits, or work with low-level registers, since a 32- or 64-bit register is a 32- or 64-element Boolean algebra. Efficient implementation of Boolean functions is a core problem in VLSI design, addressed with reduced ordered binary decision diagrams.

Beyond hardware, Boolean algebra underlies classical propositional logic: every Boolean term translates to a propositional formula, and every tautology corresponds to a Boolean equation equal to 1. Set theory interprets Boolean operations as union, intersection, and complement on subsets. Solid modeling systems combine shapes with set operations, and raster graphics use the 256-element free Boolean algebra on three generators, packaged as a single raster-operation byte, to combine source, destination, and mask pixels per bit. Search engines expose the same AND, OR, and NOT through query syntax, while statistical and fuzzy extensions replace {0, 1} with the unit interval [0, 1], where AND becomes multiplication and NOT becomes 1 − x.

Source: adapted from "Boolean algebra" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Boolean_algebra
