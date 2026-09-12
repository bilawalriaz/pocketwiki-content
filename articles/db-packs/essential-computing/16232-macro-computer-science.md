# Macro (computer science)

A macro is a rule that maps a given input to a replacement output. Applying the rule is called macro expansion. The input may be a sequence of characters, a sequence of lexical tokens, or a syntax tree. The name, from the Greek *makros* meaning "long" or "large", reflects the original purpose: a short token expands into a longer block of code, sparing programmers from typing repetitive sequences.

Macros first appeared in the mid-1950s in assembly language programming, where one macro instruction stood in for several underlying machine instructions, reducing source size and enforcing coding conventions. A macro compiler, a preprocessor to the assembler, replaced the macro with full assembly, which the assembler then translated to machine code. By the late 1950s, macro preprocessors had merged with assemblers into single "Macro Assemblers". In 1959, Douglas Eastwood and Douglas McIlroy of Bell Labs added conditional and recursive macros to the SAP assembler, producing Macro SAP. McIlroy's 1960 paper on macro processors was foundational for the field.

## Two broad roles

Macros serve two distinct purposes that are easy to conflate.

First, macros automate repetitive sequences of input. Keyboard and mouse macros turn a few keystrokes or clicks into a longer, automated sequence; programs that record them are called macro recorders. Application macros are recorded inside a specific program, usually through a scripting language with direct access to that program's features. Emacs, whose name abbreviates "editing macros", was originally a set of TECO macros before being rewritten in Lisp, and most of the editor still consists of macros. Vim records keystrokes into a register and replays or edits them. Visual Basic for Applications, included in Microsoft Office from Office 97 through Office 2019, replaced earlier macro languages and, because it can invoke most Windows system calls when documents open, became a common vector for "macro viruses" in the mid-to-late 1990s; current anti-virus software counteracts these attacks.

Second, and more deeply, macros extend a programming language itself. They allow new syntax, control structures, or domain-specific constructs to be defined by the programmer rather than built into the language.

## Parameterized and parameterless

A parameterless macro is a fixed substitution. In C:

```
#define PI 3.14159
```

causes every later occurrence of `PI` to be replaced with `3.14159`.

A parameterized macro accepts arguments:

```
#define pred(x) ((x)-1)
```

so `pred(y+2)` expands to `((y+2)-1)`. C preprocessor macros operate by plain textual substitution at the token level, which makes them convenient for inline expansion but also fragile, since they cannot preserve lexical structure reliably. Macros in Lisp, Scheme, and PL/I are far more powerful: they can inspect their arguments and decide what code to emit, effectively performing compile-time code generation. PL/I's macros are distinctive because the macro language is a subset of PL/I itself, so preprocessor statements run as ordinary procedural code at compile time, at the cost of a larger, slower compiler.

## Text substitution vs. syntax trees

The C preprocessor and simple assembler macros work at the lexical-token level. Syntactic macros work instead on abstract syntax trees and preserve the original program's lexical structure. They are easiest to implement in languages with a uniform parenthesized syntax such as Lisp's S-expressions, where macro invocations are unambiguous. Lisp macros transform program structure with the full language available. Syntactic macros are also found in Prolog, Erlang, Dylan, Scala, Nemerle, Rust, Elixir, Nim, Haxe, and Julia, and as third-party extensions to JavaScript and C#.

## Lisp macro history

Before Lisp had macros, it had FEXPRs, operators that received the unevaluated syntactic form of their arguments. This meta-evaluation model proved hard to reason about. In 1963, Timothy Hart proposed macros for Lisp 1.5 in AI Memo 57. Hygienic macros, introduced in the mid-1980s, keep the syntactic environments of definition and use separate so that macro authors and users need not fear inadvertent variable capture. `syntax-rules` and `syntax-case` are the standardized Scheme forms, and Racket extends the idea into a tower of evaluators that interleave expansion and parsing even in non-parenthesized languages.

## Practical uses

Macros have three primary legitimate uses. They can choose the order of evaluation, letting a programmer define a new control structure such as `if` from primitives like `cond`, or build looping and early-exit constructs on top of Scheme's continuations. They can define data sub-languages that compile directly into code, making state machines natural and efficient. They can introduce new binding constructs, the classic case being the desugaring of `let` into the application of a function to its arguments.

A less common but historically important use is the reverse direction: mapping machine instructions back into machine-independent macros. The STAGE2 Mobile Programming System used a small macro compiler called SIMCMP to translate a target instruction set into portable macros, then bootstrapped a richer compiler written in those macros. This was one of the earliest instances of compiler bootstrapping.
