# Abductive logic programming

Abductive logic programming (ALP) extends ordinary logic programming with abduction, a form of inference that, given an observation, proposes hypotheses to explain it. A logic program in Prolog style proves what follows from its rules; an abductive program additionally generates values for a chosen set of predicates so that the rules, together with those values, entail the observation. The same machinery handles goals to be achieved, treating them as observations the program must explain. ALP has been applied to diagnosis, planning, natural language, and machine learning, and it gives a uniform account of default reasoning and negation as failure.

## The triple ⟨P, A, IC⟩

An abductive logic program has three parts:

- **P** is a logic program in the usual sense. Its clauses define the non-abducible predicates and describe the problem domain.
- **A** is a set of *abducible* predicates. Their truth is not fixed by the program; values for them are to be hypothesised.
- **IC** is a set of *integrity constraints*, first-order formulae that any acceptable solution must respect. In practice these are usually denials of the form `false :- A1, ..., An, not B1, ..., not Bm`, which forbids a state in which every Aᵢ holds and every Bⱼ fails to be proved.

By convention no clause in P has an abducible predicate in its head. The restriction is not a real loss, because any such clause can be rewritten so the abducible appears only in the body.

## What counts as a solution

A problem G is a conjunction of positive and negative literals, read either as an observation to be explained or as a goal to be achieved. An *abductive explanation* of G is a set Δ of ground instances of abducible predicates such that, when Δ is added to P, three conditions hold:

1. P ∪ Δ entails G.
2. P ∪ Δ entails IC.
3. P ∪ Δ is consistent.

Condition 2 is the strong reading: the integrity constraints must hold in every model of the extended program. A weaker reading, useful when P ∪ Δ has a unique model, asks only that P ∪ IC ∪ Δ be consistent, meaning some model of the extended program satisfies the constraints. In many practical settings the two readings coincide. The entailment relation itself can be given any standard logic-programming semantics, such as completion, stable, or well-founded semantics, and each choice defines a different variant of ALP.

## A small example

The wet-grass case shows the mechanism. P states: the grass is wet if it rained; the grass is wet if the sprinkler was on; the sun was shining. A contains the two abducibles `rained` and `sprinkler_on`. IC contains a single denial, `false :- rained, sun_shining`. The observation `grass_wet` has two candidate explanations, `rained` and `sprinkler_on`, both of which together with P entail the observation. The integrity constraint eliminates the first: assuming it rained while the sun was shining is forbidden, so only `sprinkler_on` survives.

## Default reasoning and negation as failure

ALP captures the default "birds fly unless abnormal". The ordinary logic-program version uses negation as failure: `canfly(X) :- bird(X), not abnormal(X)`, with a rule that makes wounded things abnormal. The ALP version replaces the negative condition with a positive abducible: `canfly(X) :- bird(X), normal(X)`, with the integrity constraint `false :- normal(X), wounded(X)`. Given the facts `bird(john)`, `bird(mary)`, and `wounded(john)`, the system can assume `normal(mary)` but cannot assume `normal(john)`, so it concludes `canfly(mary)` and not `canfly(john)`. The two encodings yield the same conclusions because in ALP assuming an abducible fails exactly when it would violate an integrity constraint, which is the same condition that triggers negation as failure in ordinary logic programs.

The correspondence runs both ways. For every abducible `p`, adding a contrary `negp` together with the pair `p :- not negp.` and `negp :- not p.` produces two stable models, one with `p` true and one with `negp` true. Answer Set Programming uses this construction as its standard generate-and-test technique for encoding abduction.

## Implementations

Most ALP systems extend the SLD-resolution model of Prolog-style logic programming; examples are ACLP, A-system, CIFF, SCIFF, ABDUAL, and ProLogICA. ALP can also be built on Answer Set Programming, with the ASP solver performing the underlying search.

Source: adapted from "Abductive logic programming" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Abductive_logic_programming
