# Operator (computer programming)

An operator is a programming language construct, usually written with symbols rather than letters, that performs a computation the language treats as built-in and that would be awkward or impossible to express as an ordinary function. In most languages `a + b` is an operator, not a call to `add(a, b)`, because the symbolic form is shorter, parses more naturally, and is allowed to bypass the rules that govern regular functions.

## How operators look: syntax and arity

Operators are positioned relative to their operands using a property called **fixity**: prefix (`-x`), infix (`a + b`), postfix (`x++`), and rarer forms such as circumfix (wrapping the operand) and matchfix (a pair of symbols around the operand). Most operators are **binary**, taking two operands; some are **unary**, taking one; a few are **ternary**, taking three. C's `?:` (written `a ? b : c`) is the standard ternary operator, and its dominance in that role is why programmers often say "the ternary operator" without naming a language.

The syntax of an expression depends on three properties of each operator: **arity** (how many operands), **precedence** (which binds tighter, as multiplication does before addition), and **associativity** (which way a chain of equal-precedence operators groups, usually left to right). Functions are almost always called in prefix form with parentheses, so they occupy a fixed syntactic slot rather than a position in a precedence table.

## How operators behave: semantics

Operators are not simply functions with different syntax. Their semantics can differ sharply from a normal call.

**Short-circuit evaluation.** Boolean `&&` and `||` may skip later operands if an earlier one already decides the result, an effect no straightforward function call reproduces.

**Assignment replaces rather than evaluates.** In `a = b`, the target `a` is not read; its storage is overwritten with the value of `b`.

**Name-level access.** Scope resolution (`Foo::Bar`) and member access (`a.b`) operate on identifiers and structure rather than on ordinary values.

**Compound effects in place.** C's `++a[i]` reads `a[i]` and writes back in one step. The C++ stream operator `<<` chains to thread a single object through a sequence of operations, producing fluent syntax like `cout << "Hello" << " " << "world!" << endl`.

**Ad hoc polymorphism.** A single operator can perform different actions depending on type: Java's `+` adds numbers but concatenates strings.

## Customisation: overloading and user-defined operators

Many languages let the programmer **overload** an existing operator, giving it new behaviour for new types. C++ and Fortran allow this. Fewer languages let programmers define entirely new operator symbols; Prolog, F#, OCaml, Haskell, Raku, and Smalltalk do, while C, C++, Java, and PHP keep a fixed symbol set. Some languages accept named operators instead of symbols, such as Pascal's `div`, and Fortran allows operator names of up to 31 characters enclosed in dots.

Allowing arbitrary new operators complicates the language itself. Each new symbol introduces a new arity and precedence slot, changing how the **lexer** (the phase that splits text into tokens) and the **parser** (the phase that builds the syntax tree) must process the program. When operators can be defined at runtime, the language's syntax can effectively become **Turing-complete**, meaning it can in principle express any computation. In such a case building even the parse tree can require solving the **halting problem**, the question of whether an arbitrary program will ever finish, which has no general algorithm. Perl and certain Lisp dialects cross into this territory; C deliberately does not, which is why its grammar stays tractable.

## Implicit conversion of operands

Before an operator runs, many languages silently **coerce** its operands to compatible types, and the rules vary by language. In Perl, `12 + "3.14"` yields the number `15.14`: the string is converted to a float, and the integer is widened to match. In JavaScript the same expression yields the string `"123.14"` because the integer is converted to a string and `+` falls back to concatenation. Programmers must know their language's coercion rules to predict results, since the same symbols can mean arithmetic in one language and string handling in another.

## Common operators by category

| Category | Example | Syntax |
|---|---|---|
| Arithmetic | addition | `a + b` |
| Relational | greater than | `a > b` |
| Logical | and | `a && b` |
| Assignment | simple | `a = b`, `a := b` |
| Three-way compare | "spaceship" | `a <=> b` |
| Field or scope | member, scope | `a.b`, `a::b` |
| Conditional | ternary, Elvis, null-coalesce | `a ? b : c`, `x ?: y`, `x ?? y` |
| Address, dereference (C/C++) | reference, follow pointer | `&x`, `*p` |
| Compound assignment | augmented | `+=`, `-=`, `<<=`, … |

Operator systems differ across languages along several axes: the fixities allowed (APL supports prefix and infix; Smalltalk supports only infix and postfix), whether overloading is permitted (Haskell via type classes, Eiffel not), and whether new operator symbols can be introduced (Raku yes, C no).

Source: adapted from "Operator (computer programming)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Operator_%28computer_programming%29
