# Cohesion (computer science)

In computer programming, **cohesion** is the degree to which the elements inside a module belong together. The term usually describes a single class, measuring either how strongly its methods and data serve one unifying purpose, or how strongly its methods and data relate to each other. Cohesion is an ordinal quality, so modules are described as having "high" or "low" cohesion rather than a precise number.

## Why it matters

High cohesion is associated with robustness, reliability, reusability, and understandability. Low cohesion makes code hard to maintain, test, reuse, or read. High cohesion also tends to correlate with loose **coupling** (the degree of interdependence between modules), and the two are routinely treated as complementary goals.

The metrics of coupling and cohesion were introduced by Larry Constantine in the late 1960s as part of **Structured Design**, an approach to organising programs so that maintenance and modification cost less. They appeared in Stevens, Myers & Constantine (1974) and Yourdon & Constantine (1979), after which the two terms became standard vocabulary in software engineering.

## What high cohesion looks like

In object-oriented programming, a class has high cohesion when its methods are similar in many aspects and the functionalities accessed through them have much in common. Methods should carry out a small number of related activities over related data, not coarsely grained or unrelated sets. Placing related methods in the same file or sub-directory reinforces the grouping.

The practical benefits are reduced module complexity (fewer, more focused operations), easier maintenance (a logical change touches fewer modules, and a change in one module rarely forces changes in others), and better reusability (developers can find the component they need among the cohesive set of operations it provides).

In principle, a module achieves perfect cohesion by being a single atomic element, such as one function. In practice this is rarely useful: a single element is either too complicated to express a real task or too narrow and therefore tightly coupled to other modules. Cohesion is therefore balanced against both internal complexity and coupling.

## Types of cohesion

Cohesion is qualitative. Source code is examined against a rubric and assigned to one of seven categories, from worst to best:

| Type | What groups the parts | Example |
|---|---|---|
| **Coincidental** (worst) | Nothing meaningful; parts grouped arbitrarily | A "Utilities" class that mixes unrelated helpers |
| **Logical** | Parts categorised as the same kind of thing, but different in nature | All mouse and keyboard input routines in one module; MVC folders bundling models, views, and controllers |
| **Temporal** | Parts run at the same moment in program execution | An exception handler that closes files, writes a log, and notifies the user in one call |
| **Procedural** | Parts must run in a fixed sequence | A function that checks file permissions and then opens the file |
| **Communicational** (also "informational") | Parts operate on the same data | A module that reads, validates, and writes the same record |
| **Sequential** | The output of one part is the input of the next, assembly-line style | A function that reads data from a file and then processes it |
| **Functional** (best) | All parts contribute to a single well-defined task | Lexical analysis of an XML string; an arithmetic module exposing only `+` and `*` |

The ranks do not form a steady progression. Studies by Constantine, Edward Yourdon, and Steve McConnell indicate that the first two types (coincidental and logical) are inferior, communicational and sequential are very good, and functional is superior.

A module approaches perfect, or atomic, cohesion when it cannot be reduced further without losing its task, for example a single function `r(x) = 2x + 1 + 3x + 2` written as one expression. The source presents this as an extreme of functional cohesion rather than a separate category.
