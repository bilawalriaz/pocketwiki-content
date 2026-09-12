# Programming language

A programming language is an engineered notation for writing instructions a computer can execute. Programs must be unambiguous and complete, because a computer does exactly what it is told. Every language pairs a surface form, **syntax**, with a meaning, **semantics**, and is usually fixed by a written specification.

A program must be converted into **machine code** before the processor can run it. A **compiler** translates the whole program ahead of time, producing a fast executable. An **interpreter** translates and runs each line on the fly, which simplifies debugging but runs 10 to 100 times slower. Hybrid approaches, including **just-in-time compilation** and **bytecode** interpreters, blend the two.

## How languages are defined

Syntax is usually described with regular expressions for individual **tokens** (words, numbers, punctuation) and a **Backus–Naur form** grammar for larger structures; nearly all languages can be parsed by a **context-free** (Chomsky Type-2) grammar. The semantics split into two layers. **Static semantics** covers rules a compiler can check before running, such as declaring every identifier before use, distinct labels in a `case` statement, and most type rules. **Dynamic semantics** defines how and when constructs produce behaviour, from evaluation order to control flow, and is often written in prose, though formal semantics is an active research area.

A small Lisp-style grammar shows the pattern:

```
expression ::= atom | list
atom       ::= number | symbol
number     ::= [+-]?['0'-'9']+
symbol     ::= ['A'-'Z''a'-'z'].*
list       ::= '(' expression* ')'
```

Not every syntactically valid program is meaningful. The C fragment `complex *p = NULL; complex abs_p = sqrt(*p >> 4 + p->im);` parses correctly but operates on a null pointer, a semantic error. Some languages, notably Perl and Lisp, allow code to run during parsing, which can make the boundary between syntax and execution **undecidable**.

## A condensed history

Early computers ran **machine code** (first generation), raw bit patterns the processor executed directly. **Assembly languages** (second generation) replaced those patterns with mnemonics, easing human effort but not portability. The 1950s introduced **third-generation, high-level languages** that abstracted away hardware: Fortran in 1957 for scientific work, ALGOL in 1958–1960 as the canonical notation for algorithms, and Lisp in 1958 as the first functional language, adding recursion, dynamic memory on a **heap**, and automatic **garbage collection**. C, descended from ALGOL, balanced low-level access with portability and remains dominant in systems programming. The 1960s and 1970s added Simula's objects, ML's inferred polymorphic types, and Prolog's logic-programming paradigm.

The 1980s brought personal computers, C++ with classes and inheritance, and Ada with concurrency. The 1990s web boom produced Java for portable, secure network code and dynamically typed **scripting languages**, Python, JavaScript, PHP, and Ruby, suited to gluing components and serving web pages. After 2010, Rust, Go, Swift, Zig, and Carbon targeted the performance-critical niches C once owned, while visual languages such as Scratch and LabVIEW opened programming to non-textual workflows.

## Core features every language supplies

A **type system** defines which values and operations are legal. Integers and floating-point numbers cover numeric work; Booleans cover logic; characters and strings cover text. Composite types include arrays, lists, records, tuples, and associative maps; **pointers** carry memory addresses; **abstract data types** hide representation behind an interface. **Static typing** fixes each variable's type at compile time, catching errors early; **dynamic typing** attaches types to values, trading late error discovery for flexibility. **Strong typing** blocks implicit conversion between unrelated types; **weak typing** permits it. Compile-time type errors are far cheaper than runtime ones, and C famously omits array-bounds checks for performance.

**Concurrency** lets a program do more than one thing at a time, across multiple processors, threads, or message-passing channels. Interpreted languages such as Python and Ruby traditionally do not exploit multiple processors; compiled systems like Java and C# coordinate threads with semaphores, monitors, or message passing.

**Exception handling** recovers from runtime errors by terminating gracefully or resuming near the failure. C, prioritising speed, omits bounds checks and reports errors through return values rather than a dedicated mechanism.

## Design, paradigms, and implementation

Most widely used languages are **imperative**, built around the **von Neumann architecture** in which the same memory holds data and instructions. That pairing makes variables, assignment, and iteration natural, and favours iteration over recursion for efficiency. **Functional** languages compose nested function calls and emphasise immutability. **Logic** languages, such as Prolog, let the programmer state goals and let the interpreter choose the steps. **Object-oriented** languages layer data abstraction, inheritance, and **dynamic dispatch** on top, and most popular imperative languages now include those features.

Design balances readability, writability, and reliability against performance. **Abstraction** hides hardware detail so a programmer solves the problem, not the machine. **Expressivity** lets a small program say a lot. **Orthogonality** keeps the number of independent constructs small. Reliability improves with type checking, exception handling, and restricted **aliasing** (multiple names referring to the same memory). Most languages ship with a **standard library** of common functions. Specifications range from explicit syntactic and semantic rules (C, Standard ML, Scheme), to translator descriptions (C++, Fortran), to reference implementations (Prolog).

Thousands of languages exist; individual projects commonly use five or more. As of June 2024 the TIOBE index ranks the top five as Python, C++, C, Java, and C#, with C dominant in embedded systems and operating systems, Fortran entrenched in scientific computing, and Ada in aerospace and real-time work. Measuring popularity is inherently biased, since job adverts, book sales, lines of code, and web mentions each capture a different slice of the picture.

**Changes made**: removed the meta-conclusion ("contract between people and machines"), tightened prose throughout, fixed missing spaces ("The1950s", "After2010"), added brief glosses for prerequisites (tokens, heap, garbage collection, aliasing, dynamic dispatch), and trimmed filler while preserving the working model (definition, implementation, syntax/semantics, history arc, type systems, paradigms, design tradeoffs, popularity). Final length ~1020 words.
