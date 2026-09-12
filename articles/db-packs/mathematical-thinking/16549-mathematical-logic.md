# Mathematical logic

Mathematical logic studies formal logic within mathematics. It uses a fixed artificial notation and rigorous deductive rules to analyze mathematical reasoning itself, clarifying what can be proved and exposing the limits of formal systems.

A formal logical system works with formulas built from a fixed alphabet, with rules for forming, transforming, and interpreting them. Syntax governs which strings of symbols count as well-formed formulas; semantics assigns meaning through models, which are mathematical structures giving the symbols a concrete interpretation. First-order logic is the system most often used today, because it has favorable proof-theoretic properties and suits the foundations of mathematics. In first-order logic, quantifiers range over a single fixed domain and formulas are finite.

## The four main branches

The 1977 *Handbook of Mathematical Logic* divided the field into four areas: set theory, model theory, recursion theory, and proof theory together with constructive mathematics. The borders blur and techniques overlap: forcing is used in set theory, model theory, and recursion theory, and Gödel's incompleteness theorem is central to both recursion theory and proof theory.

Set theory studies abstract collections of objects. Cantor's informal theory of cardinal and ordinal numbers was formalized by Zermelo and Fraenkel into Zermelo–Fraenkel set theory (ZF), which with the axiom of choice (ZFC) is the standard foundation for modern mathematics. Model theory studies the models of formal theories, using tools such as quantifier elimination and the Löwenheim–Skolem theorem, and sits next to universal algebra and algebraic geometry. Recursion theory, also called computability theory, studies computable functions and the Turing degrees that classify uncomputable ones; it grew from the 1930s work of Church, Turing, and Gödel and was extended by Kleene and Post. Proof theory studies formal proofs as mathematical objects, using deduction systems such as Hilbert-style systems, natural deduction, and the sequent calculus developed by Gentzen.

## Logic and the foundations of mathematics

The field grew from efforts to put mathematics on a firm axiomatic footing. Peano published axioms for arithmetic in 1889 using a logic that added quantifiers to Boole's system, and Hilbert gave a complete axiomatization of geometry in 1899. Building on these, Hilbert proposed a program to prove the consistency of foundational theories by finitary analysis of proofs.

In 1931, Gödel showed that any sufficiently strong, effectively axiomatized theory of arithmetic contains true statements it cannot prove, and cannot prove its own consistency if it is consistent. These incompleteness theorems struck at Hilbert's program, though Gentzen later proved the consistency of arithmetic using finitary methods augmented by transfinite induction. Gödel had earlier proved the completeness theorem, which shows that in first-order logic every logically valid sentence is finitely provable, and from it the compactness theorem: a set of sentences has a model if and only if every finite subset does. Together with the Löwenheim–Skolem theorem, which shows first-order axioms cannot pin down infinite structures up to isomorphism, completeness and compactness explain why first-order logic dominates mathematical practice.

In set theory, two famous statements are independent of ZF. Gödel showed in 1940 that the continuum hypothesis cannot be disproved from ZFC by building the constructible universe in which it holds, and Cohen showed in 1963, using forcing, that it cannot be proved either.

## Key results in computability

Recursion theory produced foundational undecidability results. Church and Turing independently proved in 1936 that the Entscheidungsproblem has no algorithmic solution, by showing the halting problem is undecidable. Matiyasevich completed the proof in 1970 that Hilbert's tenth problem, asking for an algorithm to decide whether a polynomial equation with integer coefficients has an integer solution, is algorithmically unsolvable.

## Nonclassical logics

Beyond first-order logic, mathematicians study stronger classical systems such as second-order and infinitary logics, as well as nonclassical logics. Intuitionistic logic, developed by Heyting to capture Brouwer's intuitionism, drops the law of the excluded middle. Kleene showed that any provably total function in intuitionistic arithmetic is computable, which fails in classical Peano arithmetic. Gödel's negative translation embeds classical logic into intuitionistic logic, and modal logic has been applied to study provability and forcing. Lindström's theorem states that first-order logic is the only extension of itself that satisfies both compactness and the downward Löwenheim–Skolem theorem.

## Applications and connections

Mathematical logic has reached into physics, biology, linguistics, economics, law, and computer science. The Curry–Howard correspondence links proofs and programs through proof theory and intuitionistic logic; Fagin's theorem of 1974 characterizes the complexity class NP by existential second-order logic; and modern proof assistants draw on the formal calculi studied in the field.

Source: adapted from "Mathematical logic" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Mathematical_logic
