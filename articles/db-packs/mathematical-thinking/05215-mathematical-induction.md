# Mathematical induction

Mathematical induction is a technique for proving that a statement P(n) is true for every natural number n. Instead of checking P(0), P(1), P(2), and so on one at a time, induction uses two ingredients to cover all cases at once.

## The two-step structure

Every standard proof by induction has two parts.

The **base case** establishes P at a starting value, usually n = 0 or n = 1, with no assumptions about other cases.

The **induction step** shows that whenever P holds for some arbitrary natural number k, it also holds for k + 1. The assumption that P(k) is true is called the **induction hypothesis**, and it is treated as a given fact while the proof of P(k + 1) is constructed. The base case need not start at 0; it can start at any fixed n = N, in which case induction proves P(n) for every n ≥ N.

A useful image is climbing a ladder. Proving that the first rung is reachable is the base case, and proving that from any rung the next one is reachable is the induction step; together they make the whole ladder climbable.

## Why the two steps suffice

Applying the induction step at k = 0 gives P(0) → P(1); combined with the base case this yields P(1). The step at k = 1 then gives P(2), and so on. Although infinitely many cases are covered, the proof itself is a finite chain of deductive reasoning about the symbol n. The result is a rigorous proof, not a probabilistic one, which is why mathematical induction differs from the philosophical use of "induction," where examining many cases yields only a probable generalisation.

## A worked example

To prove the formula for the sum of the first n + 1 natural numbers,

$$0 + 1 + 2 + \cdots + n = \frac{n(n+1)}{2},$$

one proceeds as follows.

Base case (n = 0): the left side is 0 and the right side is 0·1/2 = 0.

Induction step: assume the formula holds for some arbitrary k ≥ 0, so

$$0 + 1 + \cdots + k = \frac{k(k+1)}{2}.$$

Adding (k + 1) to both sides gives

$$0 + 1 + \cdots + k + (k+1) = \frac{k(k+1)}{2} + (k+1) = \frac{k(k+1) + 2(k+1)}{2} = \frac{(k+1)(k+2)}{2},$$

which is the formula with n replaced by k + 1. Both parts hold, so the formula is true for every n ≥ 0.

## Common variants

**Strong (complete) induction** uses a stronger hypothesis in the step: to prove P(k + 1), one may assume P(m) for all m ≤ k. Despite the name, it proves the same class of statements as ordinary induction; any strong-induction proof can be rewritten as an ordinary one by rephrasing the hypothesis. Strong induction is needed when proving P(k + 1) genuinely uses earlier cases other than k, as in the proof that every integer greater than 1 is a product of primes: a composite m = n₁n₂ splits into two strictly smaller factors, each of which the hypothesis already covers.

**Infinite descent**, used by Fermat, is induction running backwards to prove a negation. If some property held of a natural number, it would also hold of a strictly smaller one, which is impossible because the natural numbers have no infinite descending chain. This is equivalent to an ordinary induction proof applied to the negated statement.

**Multiple counters** extend induction to statements P(n, m) by nesting: prove a base case and step in n, with each step containing its own base case and step in m.

## A classical pitfall

The induction step must work for every value of n, including the smallest one for which it is invoked. A famous "proof" that all horses are the same color fails for exactly this reason: the step assumes two overlapping sets of n horses, but at n = 1 the supposed overlap is empty, so the argument breaks at the very case it is meant to cover.

## Formal statement

In second-order logic, the induction principle is the axiom

$$\forall P \bigl(P(0) \land \forall k\,(P(k) \rightarrow P(k+1)) \rightarrow \forall n\, P(n)\bigr),$$

which is one of the Peano axioms for the natural numbers. The remaining Peano axioms state that 0 is a natural number, every natural number has a successor, the successor function is injective, and 0 is not itself a successor. In first-order arithmetic the principle must be stated as a separate axiom for each predicate, because the first-order language cannot quantify over properties; in ZFC set theory the principle is a theorem, since the natural numbers are defined from the axiom of infinity and the axiom schema of specification.

## Generalisation to well-founded sets

Replacing the natural numbers by any **well-founded** set, meaning an ordered set with no infinite descending chain, gives **transfinite induction**: to prove P(n) for every element of such a set, it suffices to show that P(m) for all m < n implies P(n). The case of a minimal element is vacuous, the case of an immediate predecessor reduces to ordinary induction, and the remaining limit-ordinal case uses the hypothesis for all smaller elements.
