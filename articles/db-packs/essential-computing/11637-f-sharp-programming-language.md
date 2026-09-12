# F Sharp (programming language)

F# is a strongly typed, multi-paradigm programming language that combines functional, imperative, and object-oriented styles. It runs on the .NET runtime, and its compiler can also target JavaScript and GPU code. The language was created at Microsoft Research by Don Syme, first released in 2005, and is now developed by Microsoft and the F# Software Foundation under the MIT license. It descends from the ML family of languages, and its core is largely compatible with OCaml, a functional language from the same family.

F# files use the extensions `.fs`, `.fsi`, `.fsx`, and `.fsscript`. It is supported in Visual Studio and JetBrains Rider, with editor plugins for VS Code, Vim, and Emacs.

## Core Design

F# is functional-first: functional style is the default, but imperative and object-oriented features are available when needed. Its type system is static, strong, and inferred. The compiler deduces types from how values are used, so type annotations are optional in most code.

In F#, everything is an expression. `if`, `try`, and loops all produce a value rather than acting as standalone statements. A block with no useful return value has the type `unit`, F#'s equivalent of "nothing." Values are bound to names with the `let` keyword, and bindings are immutable by default; opting into mutation requires `let mutable`.

Functions are first-class values. They can be stored, passed as arguments, returned from other functions, and composed with the `>>` and `<<` operators. F# also supports currying, where a function that takes several arguments can be treated as a chain of single-argument functions. Anonymous functions (lambdas) capture surrounding variables, forming closures.

Three built-in type forms structure functional data:

- A **record** has named fields, like `{ Name = "AB"; Age = 42 }`.
- A **tuple** is a fixed-position grouping, written `(A, B, C)`.
- A **discriminated union** is a tagged variant where each case carries its own data, similar to a tagged enum with payloads.

Two more types model the absence or failure of a value: `option` distinguishes `Some x` from `None`, and `Result` distinguishes `Ok value` from `Error reason`. Lists are immutable singly-linked lists, written `[1; 2; 3]` or built with the `cons` operator `head :: tail`.

Pattern matching decomposes values and dispatches control flow based on shape. It is used with records, tuples, and discriminated unions, and it can be extended with active patterns, custom rules that match values in ways the built-in forms cannot.

Computation expressions provide a unified syntax for chaining operations that share a structure, such as sequences, asynchronous workflows, and queries. The same shape handles lists (`[ ... ]`), arrays (`[| ... |]`), and on-demand sequences (`seq { ... }`).

## Imperative and Object-Oriented Features

F# includes `for` and `while` loops, arrays, and hash tables, all usable alongside the functional core. For object-oriented programming it offers classes, structs, interfaces, enums, and delegates, with dot-notation, type tests (`x :? string`), and named or optional arguments. F# objects interoperate with C# and other .NET languages because both compile to the same runtime.

## Asynchronous and Parallel Programming

Asynchronous workflows, written `async { ... }`, let the runtime continue other work while waiting for I/O. The `let!` keyword suspends until a result is available, but does not block a thread. Since version 6.0, F# also supports .NET `Task` objects through `task { ... }` expressions. Parallel execution uses `Async.Parallel` and `Array.Parallel`, or direct access to the .NET thread pool.

## Units of Measure

A distinctive F# feature: numeric values can be tagged with dimensional units such as meters, seconds, or kilograms. The compiler then verifies that arithmetic is dimensionally consistent, so adding a length to a time becomes a compile error. Units are erased before runtime and exist only for static checking.

## Metaprogramming

Quotations represent F# code as data, an abstract syntax tree other code can inspect or transform. They are used to compile F# to JavaScript or GPU code. Type providers, introduced in version 3.0, let external components supply types to the compiler on demand, giving strongly typed access to external sources such as databases and web APIs.

## Agent Programming

F# supports a lightweight actor model through `MailboxProcessor`. Each agent is an asynchronous message loop that owns its state and communicates only by passing messages, avoiding shared mutable state and locks.

## Tools and Ecosystem

F# is supported in Visual Studio, JetBrains Rider, VS Code (via Ionide), Vim, and Emacs, and runs on Windows, Linux, and macOS. Common application areas include web development with the SAFE Stack, mobile apps through Xamarin, quantitative finance, machine learning, and REPL scripting. Notable open-source projects include Fable, an F#-to-JavaScript transpiler, Paket for package management, FAKE for build automation, and Giraffe and Suave for web servers. F# also includes an ML compatibility mode that compiles a subset of OCaml.
