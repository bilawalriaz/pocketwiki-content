# Dylan (programming language)

Dylan is a multi-paradigm programming language created in the early 1990s by a group led by Apple Computer. It combines functional and object-oriented programming in a single dynamic, reflective system that can also be tuned toward static, compiled performance. The name was chosen by James Joaquin as a backronym for "DYnamic LANguage"; the project was originally code-named Ralph. Dylan's main design goal is to be a dynamic language suited for commercial software, with enough structure that the compiler can see whole compilable units such as libraries.

## Lineage and syntax

Dylan descends from Scheme and Common Lisp and adds an integrated object system derived from the Common Lisp Object System (CLOS), the same object layer that influenced many later multi-dispatch designs. All values, including numbers, characters, functions, and classes, are first-class objects. Despite this Lisp heritage, Dylan uses an ALGOL-like infix syntax rather than Lisp's parenthesized prefix form, because the designers expected ALGOL-style code to feel familiar to a wider audience. The syntax was designed by Michael Kahl and is documented in the Dylan Reference Manual. A historical prefix-dialect still exists, but the modern language is infix-dylan.

## History and implementations

Apple originally targeted Dylan at the Apple Newton, but the implementation was not mature in time, and Newton shipped with a mix of C and NewtonScript. Apple ended its Dylan effort in 1995 and released a "technology release" (Apple Dylan TR1) that included an advanced IDE. Harlequin then shipped a commercial IDE for Microsoft Windows, and Carnegie Mellon University released an open-source Unix compiler called Gwydion Dylan. Both implementations are now open source; the Harlequin line is now called Open Dylan, maintained by a volunteer group called the Dylan Hackers. The current stable release is 2026.1, and the language runs on IA-32 and x86-64.

## Syntax at a glance

Dylan is not case sensitive. Identifiers use kebab case (also called lisp-case), so multi-word names are joined with hyphens, as in `point-x`. Class names are wrapped in angle brackets that are part of the identifier, so the class is written `<point>`, not `point`. Constants conventionally start with `$`, as in `$pi`. Most non-alphanumeric characters are allowed inside identifiers, provided at least one alphanumeric character is also present, and whitespace resolves any ambiguity.

A minimal class definition:

```
define class <point> (<object>)
  slot point-x;
  slot point-y;
end;
```

The slots are typed as `<object>` by default and must be set manually. A more typed version declares slot types and required initialization keywords, and a factorial function in the language uses `case`-based pattern matching with the result of a method being the last expression evaluated, so no explicit return statement is needed.

## Modules versus classes

In most object-oriented languages, the class is the unit of both encapsulation and modularity, so adding a feature to strings generally means modifying the String class itself, which forces every user of String to pay the cost. Dylan separates these concerns. A library is the unit that gets compiled together, while a module is a namespace. Classes can live across modules, a single class can have parts defined in several modules, and different programs can carry different definitions of the same class, including only what they need.

Visibility is a property of the module and interface system rather than of the source code, so a developer can build a "Development" interface that exposes everything and a "Public" interface that hides internals without rewriting the underlying definitions. Multiple interfaces can attach to the same code, so the same string-concatenation function can be reached through both a String interface and a "concat" interface that groups all concatenation functions together.

## Classes, methods, and generic functions

Dylan classes describe slots, the data each object holds, much as classes do in C++ or Java. All access to slots goes through methods, as in Smalltalk, and default getter and setter methods are generated automatically from slot names. Unlike most OO languages, Dylan does not require methods to be defined inside the class; a `<window>` definition typically lists only its storage, while the behavior lives elsewhere.

Methods belong to generic functions, and the method to run is chosen by multiple dispatch, meaning the types of all arguments participate in selection, the same model used by CLOS. A definition like `define method turn-blue (w :: <window>) ...` adds a turn-blue behavior to windows, but the method is not bound at compile time. When the program runs, the runtime builds a table of method-name and parameter details and looks methods up through that table. New functionality can therefore be added to existing classes by writing a new module that defines methods for them, without touching the original class source. Spell checking could be added to all strings by writing a `spell-check` module that defines a generic function taking a string; once compiled in, every string gains the feature. The same `to-string` example works the same way: one module collects all the `to-string` methods for every type, so a window and a string each get a printable form without cluttering their class definitions, and a new type can be added by writing a new method in that module.

## Influence

Dylan has been cited as an influence on later dynamic languages including Lasso, Python, Ruby, and Julia.

Source: adapted from "Dylan (programming language)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Dylan_%28programming_language%29
