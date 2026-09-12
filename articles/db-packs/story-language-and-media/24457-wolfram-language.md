# Wolfram Language

The Wolfram Language is a proprietary, high-level, multi-paradigm programming language developed by Wolfram Research. It emphasizes symbolic computation, functional programming, and rule-based programming, and operates on arbitrary symbolic structures and data. It is the language that drives the Mathematica computer algebra system.

## History and naming

The language shipped with the first version of Mathematica in 1988. Its symbolic engine performs integration, differentiation, matrix manipulation, and differential-equation solving through rewrite rules. The original release also introduced the notebook model and the ability to embed sound, images, and 3D models, as documented in Theodore Gray's patent.

The language had run unnamed inside Mathematica for 25 years before Stephen Wolfram formally named it "the Wolfram Language" in June 2013, when Wolfram Research prepared a free version of the engine for Raspberry Pi and needed a public name. Bundling the proprietary language with the Raspberry Pi Foundation's recommended software drew controversy. A planned port to Intel Edison, announced after CES 2014, never shipped. In 2019 a bridge let Wolfram libraries be called from the Unity game engine. The current stable release is version 15.0.0.

## Paradigms and influence

The language supports term-rewriting, functional, procedural, and array programming. Its design draws on APL, Lisp, Pascal, C, C++, FORTRAN, Prolog, Simula, Smalltalk, and Schoonschip, and it has influenced Jupyter, Clojure, and Julia.

## Syntax

The syntax resembles the M-expression style of 1960s Lisp, with added infix operators and bracket-style function calls.

```wolfram
Print["Hello, World!"]

4 + 3                  (* = 7 *)
1 + 2 * (3 + 4)        (* = 15 *)
6 / 4                  (* = 3/2, an exact rational *)
Sin[Pi]                (* = 0 *)
N[3/2]                 (* = 1.5 *)
```

Square brackets denote function application, curly brackets denote lists (`{1, 3, 5}`), and multiplication can be elided (`1 + 2 (3 + 4)`).

The language layers "syntactic sugar" over its underlying function notation when a friendlier surface is possible: `TeXForm` and `InputForm` reformat expressions, prefix `@` and postfix `//` apply functions, an apostrophe `'` denotes a derivative, and `FullForm[1 + 2]` desugars to `Plus[1, 2]`.

Functions are defined as rewrite rules. The pattern `x_` is sugar for `Pattern[x, Blank[]]`, a placeholder for any single value, and `:=` is the delayed assignment that leaves the right side unevaluated until the function is called. A condition `/;` guards a rule:

```wolfram
F[x_] := x^0

Int[1/x_, x_Symbol] := Log[x];

Int[x_^m_, x_Symbol] :=
  x^(m + 1) / (m + 1) /; FreeQ[m, x] && NeQ[m, -1]
```

The same pattern machinery powers one-liner algorithms. A bubble-sort step is a single rule that swaps adjacent elements whenever the left one is greater:

```wolfram
sortRule := {x___, y_, z_, k___} /; y > z -> {x, z, y, k}

{9, 5, 3, 1, 2, 4} //. sortRule   (* = {1, 2, 3, 4, 5, 9} *)
```

The `//.` operator (ReplaceRepeated) keeps applying a rule until the expression stops changing, which is why the Rubi package can express hundreds of integration cases as a table of pattern rules.

## Implementations

Mathematica is the reference implementation and is closed source. Wolfram Research releases the language's parser under the MIT License, originally written in C++ and rewritten in Rust in 2023. The reference book is open access.

Third-party open-source reimplementations include Richard Fateman's MockMMA (1991, the earliest, and the target of a cease-and-desist), Mathics (Python/SymPy), Symja (Java), and expreduce (Go). They cover the core language and its computer algebra system but not the curated Wolfram knowledge base.

In 2019 Wolfram Research released the freeware Wolfram Engine as a programming library for non-commercial software, requiring signup and online license activation; the Wolfram Kernel for Jupyter lets users drive it from Jupyter notebooks via ZMQ instead of the text-only CLI.
