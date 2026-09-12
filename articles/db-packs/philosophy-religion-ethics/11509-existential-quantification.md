# Existential quantification

In predicate logic, an **existential quantification** is a statement that asserts the existence of at least one object with some property. It is written with the symbol ∃, read "there exists", "there is at least one", or "for some". The formula ∃x P(x) is true precisely when the predicate P(x) holds for at least one value of x in the **domain of discourse** — the collection of objects the variable is allowed to range over. Existential quantification is the dual of universal quantification (∀, "for all"), which instead claims the property holds for every member of the domain.

One witness is enough: to prove ∃x P(x) it suffices to exhibit a single x for which P(x) is true, even if no other x works.

## A motivating example

Consider the formal sentence "for some natural number n, n × n = 25":

∃n ∈ ℕ : n × n = 25

This is true because n = 5 is a natural number and 5 × 5 = 25. The "and so on" of an informal listing is replaced by an explicit restriction of the domain to ℕ.

If the domain is changed to the even numbers, the same predicate becomes false, because no even n satisfies n × n = 25. The domain of discourse therefore controls the truth value. Domain restrictions can also be encoded by conjunction inside the predicate: "for some positive odd n, n × n = 25" is equivalent to "for some natural number n, n is odd and n × n = 25".

## Notation

The symbol ∃ is a rotated capital "E" (Unicode U+2203 THERE EXISTS, written `\exists` in LaTeX). It first appeared in Giuseppe Peano's *Formulario mathematico* (1896); Bertrand Russell later popularised it as the existential quantifier.

## Negation

The negation of an existential is a universal over the negation of the predicate:

¬∃x ∈ X P(x) ≡ ∀x ∈ X ¬P(x)

This generalises De Morgan's laws to predicate logic. For example, "there exists a natural number x with 0 < x < 1" is false, and its negation is "for every natural number x, x is not greater than 0 and less than 1".

A common natural-language error is to confuse two distinct claims:

- ¬∃x P(x) ≡ ∀x ¬P(x) — "no x has property P" (none are)
- ¬∀x P(x) ≡ ∃x ¬P(x) — "not all x have property P" (some aren't)

"All persons are not married" asserts the first; "not all persons are married" asserts the second. The two are not equivalent.

Negation can also be written with ∄ ("there exists no"):

∄x ∈ X P(x) ≡ ¬∃x ∈ X P(x)

## Distribution and the empty domain

Unlike ∀, the existential quantifier distributes over disjunction:

∃x (P(x) ∨ Q(x)) → (∃x P(x) ∨ ∃x Q(x))

If the domain is the empty set ∅, then ∃x ∈ ∅ P(x) is false for every predicate P, because no element exists to serve as a witness.

## Rules of inference

**Existential introduction (∃I)**: from a concrete instance, infer existence.

P(a) → ∃x ∈ X P(x)

If P holds of a specific a, then there exists an x with P(x).

**Existential elimination (∃E)**: from an existence claim, reason about an arbitrary witness. Given ∃x ∈ X P(x), introduce a fresh name c for some such x, assume P(c), and derive any conclusion Q that does not mention c. The condition is that P(c) → Q must hold for all values of c in the domain; if c is a specific element rather than an arbitrary one, the step would smuggle in unjustified information about that element.

## Proving an existential

An existential claim can be proved in two ways. A **constructive proof** exhibits an explicit witness, such as n = 5 for ∃n ∈ ℕ : n × n = 25. A **nonconstructive proof** shows that a witness must exist without identifying it, for example by the pigeonhole principle or proof by contradiction. Both styles are accepted; only the witness, not the method of finding it, is required by ∃.

Source: adapted from "Existential quantification" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Existential_quantification
