# Statement (computer science)

In a programming language, a **statement** is the smallest syntactic unit that tells the computer to do something. A program is a sequence of one or more statements, and a statement may contain smaller pieces called **expressions**, which are the fragments that produce a value (a number, a string, or a decision such as "is x bigger than 3").

Many languages, including Ada, Algol 60, C, Java, and Pascal, draw a sharp line between **declarations** and statements. A declaration introduces a name and its type ("this variable x will hold integers"); a statement is an action performed on that data. In C, `int x;` is a declaration, while `x = x + 1;` is a statement.

Statements fall into two structural families. **Simple** statements cannot contain other statements: assignment, subroutine call, `goto`, `return`, and program-terminating commands like `exit`. **Compound** statements contain other statements, allowing nested groups and conditional or repeated execution.

Compound statements come in a few familiar shapes. A **grouping** turns a sequence of statements into one unit, written `begin ... end` in Pascal, `{ ... }` in C and Java. A **counted loop** repeats a body a fixed number of times: `for (i = 1; i <= limit; i += 1) ...` in C, `for i in 1..limit loop ... end loop;` in Ada. A **while loop** tests a condition before each iteration, a **repeat-until loop** tests after, and C and Ada allow a test in the middle. An **if** chooses between branches, and a **case or switch** picks one of many. **Exception handling** wraps a block in constructs such as Java's `try / catch / finally` or Python's `try / except / else / finally`, separating the normal path from the recovery path.

In theory, one looping construct and one choice construct are enough, because the others can be expressed with tests, jumps, and labels. In practice, the special cases stay because they read more clearly and can compile to faster code.

The visible form of a statement, its spelling, is **syntax**. Algol 60 introduced **Backus–Naur form (BNF)**, a notation that uses recursion to express repetition; it became the standard way to define language grammar. Fortran was originally described in English prose, then moved to a BNF variant from Fortran 90 onward. Cobol used a two-dimensional metalanguage, and Pascal published both syntax diagrams and BNF. The meaning of a statement is **semantics**, which is harder to pin down; standards documents typically give English prose and examples, which can be ambiguous. A while loop, for instance, can be defined by translating it into simpler tests, jumps, and labels.

A second axis separates statements from **expressions**. Expressions always produce a value; statements do not. In C, `x = y + 1` is an expression that sets x and also evaluates to the same value, but `x = y + 1;` with the trailing semicolon is a statement whose value is discarded. A bare expression followed by `;` is a legal statement whose only effect is whatever the expression does. In Python, assignment is a statement rather than an expression, so `=` is a separator, not an operator.

Most languages also decide whether a word like `if` or `while` is a **reserved keyword** that cannot be used as a variable name. C reserves about 30 such words; COBOL reserves around 400. Fortran and PL/I historically did not, producing famously confusing code such as `IF IF = THEN THEN` and, because Fortran ignored spaces before Fortran 95, the typo `DO 10 I = 1.5` turned a loop into an assignment to a variable named `DO10I`. To avoid this, Algol 60 and Algol 68 used **stropping**, a special marker around keywords; later languages simply forbid reuse as identifiers.

Most languages ship with a fixed set of statements defined by the language designer, though **extensible languages** have been built that let programmers define new statements.

Source: adapted from "Statement (computer science)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Statement_%28computer_science%29
