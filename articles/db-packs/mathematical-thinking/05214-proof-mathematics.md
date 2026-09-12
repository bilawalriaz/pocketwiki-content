# Proof (mathematics)

A proof is a deductive argument that shows the assumptions of a statement logically force its conclusion. Unlike evidence from many cases or a plausible pattern, a proof covers every possible case and yields logical certainty, not mere reasonable expectation. An unproved statement believed true is called a conjecture, or a hypothesis when it serves as an assumption for other work.

The core engine of a proof is deductive logic: each step follows necessarily from prior steps and the rules of inference. In practice, proofs mix mathematical symbols with natural language in what is called rigorous informal logic. A formal proof, written entirely in symbolic form, is a sequence of formulas in a formal language in which each formula is a logical consequence of the preceding ones, and the field of proof theory studies these structures. Mathematicians trust that an accepted informal proof could in principle be rewritten as a formal one, even though this is rarely done outside automated proof assistants.

## The axiomatic method

Every proof ultimately rests on axioms, basic assumptions treated as self-evidently true, and undefined terms that the axioms describe. From this starting point, theorems are derived by deductive logic. The axiomatic method was introduced by Euclid around 300 BCE in the *Elements*, which remained standard reading for educated people in the West until the mid-20th century. Besides geometry, the *Elements* proves that √2 is irrational and that there are infinitely many prime numbers. Earlier Greek mathematicians, including Thales (624–546 BCE) and Hippocrates of Chios (c. 470–410 BCE), gave some of the first known geometric proofs. In the 10th century, Al-Hashimi extended these techniques to purely numerical algebra, and Al-Karaji introduced an inductive proof for arithmetic progressions that helped establish the binomial theorem and properties of Pascal's triangle. Modern proof theory no longer requires that axioms be true in any intuitive sense, only that the symbolic deduction rules are followed, which is what allows parallel axiomatic systems such as Euclidean and non-Euclidean geometry to coexist.

## Common proof methods

Direct proof chains the conclusion to axioms, definitions, and earlier theorems. To prove the sum of two even integers is even, write *x = 2a* and *y = 2b*, so *x + y = 2(a + b)*, which is even by definition.

Proof by mathematical induction is deduction, not empirical induction. It proves a base case *P(1)*, then proves the induction rule that *P(n)* implies *P(n+1)*; repeated application covers every natural number. A variant, infinite descent, is used in the classic proof that √2 is irrational.

Proof by contraposition establishes "if *p* then *q*" by proving the equivalent "if not *q* then not *p*." To show that an even square forces an even base, assume *x* is odd, note that the product of two odd numbers is odd, so *x²* is odd, contradicting evenness.

Proof by contradiction (reductio ad absurdum) assumes the statement is false and derives a contradiction. To prove √2 is irrational, suppose √2 = *a/b* in lowest terms; squaring gives *2b² = a²*, so *a* is even, writing *a = 2c* leads to *b² = 2c²*, so *b* is also even. Both even contradicts the lowest-terms assumption, so √2 cannot be rational.

Proof by construction exhibits a specific object with the required property, as Joseph Liouville did to show transcendental numbers exist; the same idea yields a counterexample when a universal claim is false.

Proof by exhaustion checks every case in a finite partition. The first proof of the four color theorem used 1,936 cases, most checked by computer, which made it controversial.

A probabilistic proof uses probability to show some candidate must have a property, without identifying which one, provided the probability of success is positive. The Collatz conjecture shows how far probabilistic or empirical evidence falls short of proof.

A combinatorial proof equates two expressions for the same counted set, often via a bijection or double counting.

A nonconstructive proof shows that an object with a property must exist without finding one. A standard example shows there exist irrationals *a* and *b* with *aᵇ* rational: either √2^√2 is rational (done) or it is irrational, in which case *a = √2^√2* and *b = √2* give *aᵇ = 2*, rational, with no need to know which case holds.

## Computer-assisted proofs

The first proof of the four color theorem relied on a computer to check its 1,936 cases, breaking the long-standing assumption that any proof could be verified by a competent human reader. Such proofs are met with caution because of possible program or runtime errors, though redundancy, self-checks, and multiple independent implementations can reduce the risk, and human-checked proofs carry their own risk of hidden fallacies.

## Undecidable statements

Gödel's first incompleteness theorem shows that any sufficiently expressive axiom system contains statements that can be neither proved nor disproved within it. The parallel postulate is neither provable nor refutable from the remaining Euclidean axioms, and many statements are undecidable in Zermelo–Fraenkel set theory with the axiom of choice.

Proofs are routinely marked with the abbreviation Q.E.D. (Latin for "that which was to be demonstrated"), a tombstone symbol □, or the Unicode end-of-proof character ∎ (U+220E), named the Halmos after Paul Halmos, who popularised it.
