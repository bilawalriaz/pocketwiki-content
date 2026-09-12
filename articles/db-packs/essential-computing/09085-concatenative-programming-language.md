# Concatenative programming language

A concatenative programming language is a point-free language in which every expression denotes a function, and placing expressions next to each other denotes function composition. Composition replaces function application as the default way to build subroutines.

## How programs look

In an applicative language, nested calls pass a value inward and outward:

```
baz(bar(foo(x)))
```

In a concatenative language, the same program is a flat sequence of functions, read left to right:

```
x foo bar baz
```

The value `x` enters, `foo` runs on it, its result feeds `bar`, whose result feeds `baz`. There are no argument parentheses because arguments are never named. Data lives on an implicit shared structure that every function reads from and writes back to. Most concatenative languages use a stack for that structure, which is why the same word "stack-based" often appears, though the language model and the implementation choice are independent.

The style is called function-level or point-free because functions are pipelines of operations rather than procedures that name the values they touch. Because the syntax is just "function followed by function," it mirrors the semantics of composition. That alignment makes concatenative programs amenable to algebraic manipulation. The trade-off is that ordinary mathematical notation, built around applying functions to variables, does not translate naturally into this shape.

## Properties

A few consequences follow from composition-as-syntax:

- **Reduction is function-to-function.** Simplifying any expression produces another function, so the step of "applying a function to an object" never appears separately.
- **Factoring.** Any subexpression can be replaced with a name bound to that subexpression. The community calls this factoring, and it is the main tool for breaking programs into named parts, playing the same role that extracting a helper function plays elsewhere.
- **Monoid structure.** Syntax and semantics together form a monoid: concatenation is the operation, the empty program is the identity, and composition is associative.
- **Linear-logic implementations.** Because data passes through the pipeline, concatenative languages map onto the linear logic idea that each value is used exactly once, so no garbage is produced.

## Implementations

Forth was the first concatenative language, though the term "concatenative" was only applied later. Joy was the first language to which the term was actually applied. Other well-known concatenative languages include dc, Factor, Onyx, PostScript, RPL, and Staapl. Experimental and discontinued examples include Enchilada, Om, and XY. Concatenative languages appear implicitly inside virtual machines as instruction sets, and PostScript is a common example: printers carry a stack-based concatenative interpreter in their firmware.

Most concatenative languages are stack-based and dynamically typed, though stack-based is an implementation choice, not a requirement. Static typing is possible, as Cat and its successor Kitten demonstrate. In practice, concatenative languages are used for embedded, desktop, and web programming, as target languages, and for research.

Source: adapted from "Concatenative programming language" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Concatenative_programming_language
