# Production system (computer science)

A production system is a computer program used to build artificial intelligence. It consists of two parts: a set of behavioural rules called productions, and the mechanism that runs them. Productions are a basic form of knowledge representation used in automated planning, expert systems, and action selection.

## Structure of a production

A production has two parts. The sensory precondition, the "IF" part, tests some aspect of the current state of the world. The action, the "THEN" part, changes that state. When a precondition matches the current state, the production is said to be triggered. When its action runs, it has fired. Two further components make a production system work:

- **Working memory**, a database of facts about the current state.
- **A rule interpreter**, the mechanism that chooses and fires rules.

## How rules fire

The interpreter usually runs forward chaining: it tests each rule's left-hand side (LHS) against working memory, and when conditions match it runs the right-hand side (RHS) to add or remove facts. In a data-oriented or idealized system, every triggered rule fires in turn, and the loop stops when the user interrupts, a cycle limit is reached, a "halt" rule fires, or no LHS is true.

Real-time and expert systems often cannot fire every triggered rule, because actions take time and choices must be exclusive. Their interpreter, called an inference engine in this setting, runs two steps in a cycle: first match production rules against working memory to build the conflict set, then pick which matched rule to fire. Some systems skip the second step and fire all matches at once, but real-time and expert systems depend on a good conflict resolution strategy for both correctness and speed.

## Matching: naive versus compiled

Matching can be naive, trying each rule in order until one fits, or compiled into a network of inter-related conditions. The classic compiled approach is the Rete algorithm, designed by Charles L. Forgy in 1974 and used in the OPS family of production systems developed at Carnegie Mellon University, which culminated in OPS5 in the early 1980s. OPS5 can be viewed as a full programming language for production systems.

## Conflict resolution

The conflict set can be ordered by rule order, by assigned weights, by recency of previous firings, or by the size of the changes the RHS would make. Whichever strategy is used matters for the correctness and efficiency of the system.

## Examples

**String reversal.** Given an alphabet without `$` or `*`, the following rules reverse any input. `$` marks the left end, `*` marks the right end, and `x`, `y` match any single character.

```
P1: $$  -> *
P2: *$  -> *
P3: *x  -> x*
P4: *   -> (halt)
P5: $xy -> y$x
P6: (empty) -> $
```

Applied to `ABC`, the system walks through `$ABC -> $BC$A -> $$C$B$A -> ... -> CBA`. Rule order is critical, and the lack of control structure makes production systems difficult to design. Control structure can be added in the inference engine or in working memory.

**OPS5 style.** OPS5 stores structured records in working memory: each record has a type such as `goal`, `physical-object`, or `monkey`, with `^`-prefixed fields. Variables appear between angle brackets, and a leading `-` marks a negative condition. In a small world where a monkey can grab objects and climb on others, a rule that grabs a ceiling-hanging object might require an active `holds` goal, a light object on the ceiling at position `p`, a ladder on the floor at `p`, a monkey standing on the ladder holding nothing, and no other object on the target. Its RHS updates working memory so the same rule can no longer match, which prevents the goal from looping.

## Relationship with logic

Some textbooks describe production systems as systems of logic that reason by forward chaining. Stewart Shapiro, reviewing John Sowa's *Knowledge Representation*, and Robert Kowalski with Fariba Sadri argue this is a misrepresentation, because production actions are imperatives rather than logical conclusions and so lack a logical semantics. Their Logic Production System (LPS) combines a logic program, interpreted as the agent's beliefs, with reactive rules, interpreted as the agent's goals. In LPS a rule such as `if fire then deal_with_fire` is triggered just like a production rule, but its conclusion becomes a goal, reduced to subgoals such as `eliminate` or `escape` through the logic program, at least one of which must be executed.

## Related systems

Rule-based and production-style systems include CLIPS, JESS (a CLIPS superset for Java), JBoss Drools, ILOG rules, OpenL Tablets, Lisa, and Constraint Handling Rules. The cognitive architectures ACT-R, Soar, and OpenCog are also built on production systems. Prolog is often mentioned alongside them but uses backward chaining and a logical rather than imperative semantics.

Source: adapted from "Production system (computer science)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Production_system_%28computer_science%29
