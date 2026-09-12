# Logic programming

Logic programming is a paradigm where programs are sets of logical sentences, and computation runs by applying logical reasoning to those sentences to answer questions about a stated domain. The three main language families are **Prolog**, **Answer Set Programming** (ASP), and **Datalog**.

## Facts, rules, and queries

A program is built from clauses. A **rule** has the shape `A :- B1, ..., Bn`, read declaratively as "A if B1 and … and Bn". `A` is the **head**; `B1, …, Bn` is the **body**; each `Bi` is a **literal**. When the body is empty, the rule is a **fact**, written `A.`

**Queries** use the same syntax as rule bodies, written `?- B1, ..., Bn.` The interpreter solves the query by reasoning with the clauses.

In the simplest case (**Horn clauses**), every head and body element is an atomic formula `p(t1, …, tm)`, where `p` names a relation and the `ti` are terms. Constants like `charles` name specific objects; variables like `X` start with an uppercase letter.

A small family program illustrates the loop:

```
mother_child(elizabeth, charles).
father_child(charles, william).
father_child(charles, harry).
parent_child(X, Y) :- mother_child(X, Y).
parent_child(X, Y) :- father_child(X, Y).
grandparent_child(X, Y) :- parent_child(X, Z), parent_child(Z, Y).
```

Given `?- parent_child(X, william)`, the only answer is `X = charles`. Different queries enumerate grandparents, descendants, all pairs, or simply check a pair.

## Two readings of a clause

The same clause `A :- B1, …, Bn` carries two interpretations. **Declaratively**, it is a logical statement about the domain. **Procedurally**, in the Prolog reading, it is a recipe: "to solve `A`, solve `B1`, and … and solve `Bn`", a form of goal reduction. Kowalski's equation **Algorithm = Logic + Control** captures this split: the logical representation supplies what to compute; a search strategy supplies how. Different strategies over the same logic, or different logics under the same strategy, yield different algorithms.

## Problem-solving strategies

The two main strategies are **backward reasoning** (top-down, goal reduction) and **forward reasoning** (bottom-up, deriving new facts from existing ones). With a goal and a set of matching clauses, backward reasoning builds an **and-or tree** whose root is the goal: children of a node are subgoals from one clause's body (an "and" group), and alternative clauses for the same node form an "or" group. Prolog searches this tree depth-first, last-in-first-out, and **backtracks** on failure.

Backward reasoning is usually faster, but sometimes forward wins. Computing the nth Fibonacci number by backward reduction of `fibonacci(n, Result)` re-solves overlapping subgoals and runs in roughly exponential time; forward reasoning generates 0, 1, 2, … in linear time. Prolog emulates this advantage with **tabling**: solved subgoals and their answers are cached and reused.

## Negation as failure

Most practical programs need a negative condition. Defining "sibling" requires "not the same person":

```
sibling(X, Y) :- parent_child(Z, X), parent_child(Z, Y), not (X = Y).
```

**Negation as failure** (NAF) treats `not B` as holding whenever the positive `B` fails to be proved. NAF makes logic programming a **non-monotonic logic**: adding a new fact can withdraw earlier conclusions. Keith Clark's **program completion** gave NAF a logical semantics by treating a predicate's clauses as an if-and-only-if definition.

Two model-based semantics also handle negation. The **well-founded semantics** always yields a unique three-valued minimal model; the **stable model semantics** may yield zero or several two-valued minimal models and underpins ASP. For **stratified** programs the three semantics coincide.

## The main language families

**Prolog** is Turing-complete, uses depth-first backward chaining with backtracking, and adds extra-logical features (the `cut` operator, `assert`/`retract`) that have no clean logical reading. NAF can be defined inside Prolog using `cut` and `fail`.

**Datalog** is a database query language: terms are only constants and variables, every fact is variable-free, and recursive relations (such as transitive `ancestor_descendant`) are natural to express in ways relational algebra cannot. Pure top-down execution may loop; bottom-up evaluation terminates, and top-down with tabling also terminates.

**Answer Set Programming** treats the whole program as the goal and uses stable-model semantics to generate its intended models. Ordinary clauses define a search space; **constraint clauses** of the form `:- Body.` eliminate unwanted models, a generate-and-test pattern. Most ASP solvers first **ground** the program to propositional form, then apply a SAT-style solver; some, like s(CASP), skip grounding.

Other extensions include **constraint logic programming** (CLP), which adds domain-specific constraint predicates handled by an external solver; **abductive logic programming**, where some predicates are assumable so goals can be explained or planned; **inductive logic programming**, which synthesises new rules from examples and can invent auxiliary predicates; **concurrent logic programming**, with guarded committed-choice clauses; and higher-order, linear-logic, object-oriented (F-logic, Logtalk), and transaction-logic variants.

## Relationship to functional programming

Logic programs generalise functional ones by treating functions as a special case of relations. `mother(X) = Y` becomes the relation `mother(X, Y)`. Functional nested syntax is syntactic sugar for the flat relational form, and Ciao Prolog compiles it back into ordinary Prolog.

## History

The clausal-form idea traces to Cordell Green's 1969 theorem-proving work and to Foster and Elcock's Absys. A late-1960s debate in AI between declarative and procedural representations of knowledge shaped the field: declarativists clustered at Stanford (McCarthy, Raphael, Green) and Edinburgh (Robinson, Hayes, Kowalski); proceduralists at MIT under Minsky and Papert. Carl Hewitt's **Planner** came from the procedural camp and introduced goal-reduction with pattern-directed invocation; its subset Micro-Planner powered Winograd's SHRDLU.

In 1971 Colmerauer invited Kowalski to Marseille; together they saw that clausal logic could represent formal grammars and that SL-resolution could parse. In 1972 Kowalski developed the procedural interpretation of clauses and restricted SL-resolution to **SLD resolution**. Colmerauer and Roussel used that reading to build **Prolog** in 1972. David Warren's 1977 Edinburgh Prolog compiler made the language practical and became the de facto standard.

Japan's 1980s **Fifth Generation Computer Systems** project chose logic programming, eventually concurrent logic programming, for massively parallel AI hardware. The committed-choice feature interfered with logical semantics, and the parallel hardware failed to keep up with conventional processors, so the project fell short. Meanwhile, deductive databases (prominent from a 1977 Toulouse workshop led by Gallaire and Minker), then constraint logic programming and ASP, advanced the declarative side. The Association for Logic Programming was founded in 1986.
