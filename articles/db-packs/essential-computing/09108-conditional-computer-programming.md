# Conditional (computer programming)

A conditional is a program instruction that chooses what to do next based on whether a Boolean expression (an expression that evaluates to true or false) is true or false. A *statement* form steers control flow by running one of two blocks; an *expression* form yields a value without redirecting flow. Most languages keep the two separate, while functional languages tend to express the choice as an expression with no side effects on program flow.

## The if–then–else form

The general shape, in pseudocode, is:

```
if condition then consequent else alternative end if
```

If the condition is true, `consequent` runs; otherwise `alternative` runs. The `else` part is optional, and either branch can be a single statement or a block. A stock check:

```
if stock = 0 then message = 'order new stock' else message = 'there is stock' end if
```

A chain of `else if` clauses tests conditions in order; only the first whose condition is true runs, and the rest are skipped. Only one closing `end if` is needed because `else if` is one construct, not a nested `if`. Languages spell the chain differently: `elseif` in PHP and Ada, `elsif` in Perl and Ruby, `elif` in Python and POSIX shells, `ElseIf` in Visual Basic. In the C, Java, JavaScript, and Pascal families, the same effect comes from a nested `if`, because any single statement can follow a conditional without being wrapped in a block.

The dangling-else problem arises in nested `if` written without explicit block endings. An `else` binds to the nearest preceding `if`, but ALGOL 60 did not always make that binding explicit in its syntax, so a parser could pair the `else` with the wrong `if`. Modern languages resolve this with explicit endings such as `end if` or with block enclosures such as curly braces or `BEGIN`…`END`.

## Beyond two-way branches

A *switch* (or *case*) statement performs multiway branching on a single expression: the value is compared against constant cases, control jumps to the first match, and a default branch handles no-match cases. A compiler may implement the jump table internally as a control table.

The *arithmetic if* in Fortran through Fortran 77 was an older three-way jump based on whether a numeric value was less than, equal to, or greater than zero. It was unstructured, tied to the IBM 704's three-way test-and-branch instruction, marked obsolescent in Fortran 90, and deleted in the Fortran 2018 standard, though most compilers still accept it for legacy code.

Dijkstra's Guarded Command Language, a notation for reasoning about programs, expresses conditionals as a list of `guard → statement` pairs. If any guard is true, exactly one matching statement is chosen non-deterministically; if none is true, behaviour is undefined.

In Smalltalk the conditional is not a language construct: `Boolean` is an abstract class whose subclasses `True` and `False` each implement an `ifTrue:ifFalse:` method that runs one of two closure arguments. Haskell 98 has only an `if` expression, not a statement, and the `else` branch is required because every expression must yield a value. Because Haskell is lazy, an `if` can be written as an ordinary function that evaluates only the chosen branch. In Rust, `if` is always an expression that yields the value of the executed branch (or the unit type `()` if no branch runs), and the compiler requires every branch to produce the same type, which makes `else` effectively compulsory.

Pattern matching, available in Haskell, ML, OCaml, and Wolfram Language, is a related choice construct that selects a branch by matching the structure of a value rather than by testing a Boolean. Conditional flow can also be encoded as a dictionary lookup, with keys as cases and values as handlers, in languages with associative arrays such as Python, Perl, PHP, and Objective-C.

## Conditional expressions

A conditional *expression* evaluates to a value rather than directing control flow. John McCarthy developed the idea during late-1950s work on symbolic processing and Lisp, where conditional expressions have always been fundamental. ALGOL 60 adopted the idea using English keywords rather than McCarthy's mathematical notation. In C, C++, Java, and JavaScript, the ternary operator `condition ? true-value : false-value` provides the same effect. C#, F#, and several other languages use `?:` for the same purpose. Visual Basic's `IIf` function looks like a conditional expression but evaluates both branches and discards one, so it is not a true conditional. Tcl goes further: `if` is not a keyword but a command whose arguments are passed as strings, and the command itself evaluates the condition in the caller's scope.

## History and style

Early BASIC dialects restricted `if–then–else` bodies to `goto` statements, which produced hard-to-read "spaghetti code." Structured programming, based on the Algol family including Pascal and Modula-2, replaced this with block-structured control flow, and the structured `if–then–else` became a defining element of every widely used language from C and Java to JavaScript and Visual Basic.

Source: adapted from "Conditional (computer programming)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Conditional_%28computer_programming%29
