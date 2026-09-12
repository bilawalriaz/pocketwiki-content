# Concurrent constraint logic programming

Concurrent constraint logic programming (CCLP) is a variant of constraint logic programming aimed at modelling concurrent processes rather than solving a constraint satisfaction problem. A program is a set of goals evaluated by an interpreter; each goal runs as a process, and processes communicate through a shared constraint store by adding constraints to it and testing whether the store entails a constraint.

Syntactically, a CCLP clause has the form

```
H :- G | B
```

`H` is the clause head, `G` is a guard, and `B` is the body. The guard `G` is a constraint that may block the clause. A fresh variant of the clause can replace a literal `A` in the goal only if the constraint store, augmented with an equation of `A` and `H`, entails `G`.

## Don't-care vs. don't-know nondeterminism

The central semantic difference from ordinary constraint logic programming is how the interpreter handles multiple applicable clauses.

- Don't-know nondeterminism: non-concurrent constraint logic programming tries every applicable clause in turn, backtracking if a choice fails, because the aim is to find a solution.
- Don't-care nondeterminism: CCLP commits to a single arbitrary applicable clause and never reconsiders it, because the aim is to model a process that makes a one-time decision.

This commitment makes guards necessary. Without a guard, the interpreter could pick a clause that later turns out to be incompatible with the rest of the computation, with no way to recover.

## Equating a goal with a clause head

A second semantic difference is in unification. Ordinary logic programming uses standard unification, which can equate an arbitrary term with another term. CCLP uses one-sided unification, which only allows equations of the form `variable = term` where the variable belongs to the clause head. This directionality reflects the idea that the calling goal supplies values to the head's variables rather than constructing new terms from them.

The precise rule for using a fresh variant `H :- G | B` to rewrite a goal `A`:

1. `A` and `H` have the same predicate.
2. The current store entails that `A` can be equated to `H` by one-sided unification.
3. The guard `G` is entailed by the store together with the equations produced in step 2. Variables in `G` but not in `H` are treated as existentially quantified.

The applicability condition can be written compactly as: the store entails that there exist values for the variables of `H` and `G` such that `H` equals `A` and `G` is entailed. In practice, entailment is often checked with an incomplete method.

## Processes, termination, and deadlocks

A third consequence is that a process in CCLP may stop without causing the whole computation to fail. If no clause is applicable to a goal, the process evaluating that goal halts, while other processes continue. This matches the behaviour expected of concurrent programs, where individual components finish while the system keeps running.

Synchronisation between processes is implemented by guards. If a goal `A` cannot be rewritten because every candidate clause has a guard the store does not yet entail, the process solving `A` blocks until other processes add enough constraints to make at least one guard hold. A deadlock occurs if all active processes become blocked simultaneously: no new constraints are produced, so no guard becomes entailed.

## Atomic tell

A syntactic extension to CCLP is the atomic tell, written

```
H :- G : D | B
```

A second guard `D` is checked for consistency with the constraint store rather than entailment. A clause of this form rewrites a goal only if `G` is entailed and `D` is consistent; both are then added to the store. Atomic tell prevents the interpreter from adding body constraints that contradict the store, which matters because commitment to a single clause means the interpreter will not backtrack out of an inconsistent choice.

## Related systems

CCLP was developed in the late 1980s by integrating principles of concurrent logic programming into constraint logic programming, with Michael J. Maher among its initiators. Its theoretical properties were later studied by researchers including Martin Rinard and Vijay A. Saraswat. Constraint handling rules use a similar syntax but target constraint simplification and solving rather than concurrent processes. Other systems that connect logic or constraint programming to concurrency include Curry, ToonTalk, Janus, and Alice.
