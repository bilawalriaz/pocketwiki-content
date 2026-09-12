# Truth table

A truth table is a mathematical table that lists every combination of truth values for the inputs to a logical expression and shows the resulting output for each combination. Truth tables belong to Boolean algebra, Boolean functions, and propositional calculus. They make it possible to read off whether a propositional expression is true for all input assignments, which is the definition of logical validity.

A table has one column per input variable and a final column for the output. Each row gives one configuration of the inputs and the result for that configuration. The same information can be encoded as a truth function, a mathematical mapping from inputs to outputs, with the table as its graphical form.

## Origins

C. S. Peirce devised a truth-functional matrix in 1883, and Wittgenstein is generally credited with inventing and popularizing the truth table in his *Tractatus Logico-Philosophicus* (1918). Emil Post independently proposed a similar system in 1921.

## Basic structure

A single Boolean variable has two values, written T for true and F for false. With *n* variables there are 2^*n* input combinations, and the number of distinct Boolean functions of *n* variables is the double exponential 2^(2^*n*).

A condensed notation uses the first operand for rows and the second for columns. It is common in Boolean logic, makes the shape of a commutative operator easy to read, and reduces the row explosion in multi-valued extensions.

| Operation | Symbol | Output is true when |
|---|---|---|
| NOT | ¬p | p is false |
| AND | p ∧ q | both p and q are true |
| OR | p ∨ q | at least one of p, q is true |
| NAND | p ↑ q | NOT (p AND q) |
| NOR | p ↓ q | NOT (p OR q), also called the Peirce arrow |
| XOR | p ⊕ q | exactly one of p, q is true |
| XNOR | p ↔ q | p and q have the same value |
| IMPLIES | p → q | false only when p is true and q is false, equivalent to ¬p ∨ q |

NAND and NOR verify De Morgan's laws: ¬(p ∧ q) matches (¬p) ∨ (¬q) row by row, and ¬(p ∨ q) matches (¬p) ∧ (¬q).

## Proving equivalences

Truth tables establish logical equivalence. For the material conditional p → q, computing ¬p and ¬p ∨ q alongside p and q produces an output column identical to that of p → q, so p → q and ¬p ∨ q may be substituted for each other.

## Applications

In digital logic, truth tables specify hardware look-up tables (LUTs). An *n*-input LUT is fully described by a table of 2^*n* rows, and the output can be encoded as a single integer with one bit per row; a 32-bit integer encodes a table for up to 5 inputs. The bit index *k* is *k* = *V*₀·2⁰ + *V*₁·2¹ + ⋯ + *V*_{*n*−1}·2^{*n*−1}, where each *V*ᵢ is 1 if the *i*-th input is true and 0 otherwise. Because tables double in size with each new input, they are not practical for many inputs; binary decision diagrams and text equations are more memory efficient.

A half-adder for binary addition is a four-row table with inputs A and B, carry C, and result R, and is equivalent to modulo-2 addition and to XOR. A full-adder adds the previous carry as a third input and needs eight rows.
