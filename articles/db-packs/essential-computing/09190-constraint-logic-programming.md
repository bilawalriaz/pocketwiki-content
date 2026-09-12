# Constraint logic programming

Constraint logic programming (CLP) extends logic programming by allowing constraints, such as `X > 0` or `X + Y = 3`, to appear directly inside the body of clauses. A clause like `A(X,Y) :- X + Y > 0, B(X), C(Y)` says that `A(X,Y)` holds when `X+Y` is greater than zero and both `B(X)` and `C(Y)` are provable. Logic programming supplies the search; constraint solving supplies the arithmetic and relational reasoning.

## The constraint store

A CLP interpreter evaluates a goal by maintaining a pair `<G, S>`, where `G` is the current goal (literals still to prove, possibly with constraints) and `S` is the constraint store, the set of constraints assumed satisfiable so far. The interpreter works like a standard logic-programming interpreter, but constraints encountered during evaluation are moved into `S` instead of being proved like literals. After each addition, `S` is checked and simplified. If `S` becomes unsatisfiable, the interpreter backtracks to the most recent choice and tries an alternative clause. Execution succeeds when `G` is empty and `S` is satisfiable; the result is `S` itself, which can include loose constraints like `X > 2` that bound a variable without fixing it.

When a literal `L(t1,...,tn)` is matched against a clause head `L(t1',...,tn')`, the interpreter first renames the clause to a fresh variant using new variables, then replaces the literal with the equalities `t1=t1', ..., tn=tn'` followed by the variant's body. If the head's predicate has no matching clause, evaluation fails for that branch.

Satisfiability of `S` may be checked using an incomplete algorithm that simplifies the store into an equivalent, easier-to-solve form. Such a checker can sometimes prove unsatisfiability of an unsatisfiable store, but not always, which is why an extra search step is often needed.

A small example makes the flow concrete. Given:

```
B(X,1) :- X < 0.
B(X,Y) :- X = 1, Y > 0.
A(X,Y) :- X > 0, B(X,Y).
```

Evaluating `A(X,1)` adds `X > 0` to `S` and tries `B(X,1)`. The first clause of `B` adds `X < 0`, making `S` unsatisfiable, so the interpreter backtracks. The second clause adds `X = 1` and `Y > 0`, satisfied by `Y = 1`. Execution halts with `X = 1, Y = 1`.

## Kinds of constraints

CLP is parametric in the constraint domain. Three main families are used.

**Tree terms.** Terms are variables, constants, and function symbols. The only constraints are equalities and disequalities, solved by unification. When `S` contains only tree equalities, it behaves exactly like a Prolog substitution, so this setting emulates ordinary logic programming.

**Real numbers.** Terms are arithmetic expressions over reals. Constraints include equalities and inequalities between expressions, handled by methods such as variable elimination for polynomial equations. A variable that appears in a real expression is restricted to numeric values and cannot later take a structured term.

**Finite domains.** Each variable has a domain, often a range of integers, written `X :: [1..5]`. Adding constraints triggers constraint propagation, which enforces a local consistency condition (arc, hyper-arc, or bound consistency) and may shrink variable domains. A domain that becomes empty signals inconsistency. A domain that collapses to a single value fixes the variable. The current domain of a variable can be inspected using a built-in like `dom(X, D)`.

If a variable is asked to be both a real number and a tree term, `S` becomes unsatisfiable.

## Labeling and search

Local consistency is cheap but incomplete. It may leave `S` looking satisfiable when it is not, or leave a variable's domain large when the true solution is a single value. A labeling literal, written `labeling([X,Y,...])`, forces the interpreter to search the listed variables' domains, trying each value and backtracking on failure. Used over all relevant variables, it checks full satisfiability; used over a subset, it enumerates solutions.

The standard pattern for solving a constraint satisfaction problem is:

```
solve(X) :- constraints(X), labeling(X).
constraints(X) :- (all constraints of the CSP).
```

The interpreter first accumulates every constraint in `S`, then labels. Searching later, with more constraints already known, prunes the search space far more effectively than labeling early.

## Program reformulation

Three rewritings reliably speed CLP programs.

1. Put `labeling` after the constraints. `A(X) :- X > 0, labeling(X)` is far better than `A(X) :- labeling(X), X > 0`, because the second form may try values like `X = -1` that the first eliminates without search.
2. Put constraints before recursive literals. `A(X) :- X > 0, B(X)` can backtrack before evaluating `B`; `A(X) :- B(X), X > 0` wastes work evaluating `B` first.
3. Add redundant constraints known to hold. If `B(X)` always yields a positive value, writing `A(X) :- X > 0, B(X)` makes `S` inconsistent immediately for negative inputs.

## Constraint handling rules

Constraint handling rules (CHR) let the programmer define how `S` is rewritten. An equivalence rule `A(X) <=> B(X) | C(X)` says: when `B(X)` is entailed, replace `A(X)` with `C(X)`. An implication rule `A(X) ==> B(X) | C(X)` says: when `A(X)` is in `S` and `B(X)` is entailed, add `C(X)` without removing the original. Equivalences simplify; implications add new constraints that may trigger further propagation or expose inconsistency.

## Bottom-up evaluation

The default CLP strategy is top-down and depth-first from the goal. A bottom-up strategy instead starts from the facts and repeatedly applies clauses to derive new facts. Adding a fact already in the derived set has no effect, so cycles in the program do not cause infinite loops, the way they can under top-down evaluation. Bottom-up terminates whenever the consequence set reaches a fixed point, which makes it preferable when computing all consequences of a program rather than proving a single goal.

## Concurrent CLP

Concurrent constraint logic programming models processes as goal evaluations that run together. Clauses carry guards, constraints whose satisfaction controls whether a clause is applicable. Unlike non-concurrent CLP, which tries every matching clause, the concurrent interpreter commits to a single choice and never revisits it. A goal may therefore be unprovable in isolation while the whole evaluation still succeeds, because the concurrent semantics models ongoing computation rather than one-shot search.

## History and implementations

CLP was introduced by Jaffar and Lassez in 1987, generalising the observation that Prolog II's term equations were a specific constraint language. The first implementations were Prolog III, CLP(R), and CHIP. Subsequent systems include B-Prolog, BNR Prolog, Ciao, ECLiPSe, GNU Prolog, and SWI-Prolog. CLP has been applied to automated scheduling, type inference, civil and mechanical engineering, digital circuit verification, air traffic control, and finance.
