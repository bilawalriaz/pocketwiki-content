# Domain-specific language

A **domain-specific language (DSL)** is a programming language built to solve problems in one particular application domain, rather than across many. SQL targets relational database queries, regular expressions match text patterns, HTML structures web pages, and MATLAB handles matrix mathematics. These languages trade broad applicability for expressive power and clarity within their niche.

A **general-purpose language (GPL)** like Python, C, or Java aims to handle any computational task. It is a general workbench. A DSL is more like a specialized power tool, a drill rather than a complete workshop, designed to do one class of work extremely well.

## When the boundary blurs

The line between DSLs and general-purpose languages is not sharp. A language may have specialized features for a domain yet remain broadly usable, or it may be theoretically general-purpose but in practice serve only one purpose. Perl was originally developed as a text-processing and glue language, in the same niche as AWK and shell scripts, but ended up being used as a general-purpose language. PostScript, by contrast, is **Turing-complete**, meaning it could in principle compute anything any programming language can, yet is used almost exclusively as a page description language for printers. SQL also sits in the middle: it targets one domain but is so widely used and feature-rich that many treat it as a full programming language.

DSLs tend to be more **declarative** than general-purpose languages, meaning they describe *what* should be computed rather than step-by-step *how*. QML, SQL, and XSLT are declarative; CSS is sometimes classed as one too.

## How DSLs are created

DSLs emerge in several ways. Dedicated **language workbenches** support designing them from scratch: JetBrains MPS uses **projectional editing**, where the program is represented as a tree rather than as text, allowing tables and diagrams instead of a parser. MontiCore processes an extended grammar format and generates Java components. Xtext generated a full Eclipse-based IDE alongside a parser and abstract syntax tree, though the project was archived in April 2023. Racket provides a toolchain designed for creating both DSLs and general-purpose languages. Behind these tools, **metacompilers** like the historical META II (1964) and its descendant TreeMeta (1969) generate parsers and code generators from a **metalanguage**, a language for describing other languages, a technique still common in program transformation systems.

DSLs also emerge from **metaprogramming**, from **macro systems** that expand DSL code into a host language at compile time, from **operator overloading** in languages like C++, and from Lisp-style modification of a host language's own syntax.

## External and embedded forms

DSLs come in two structural forms. An **external DSL** stands on its own with a dedicated interpreter or compiler, like TeX, AWK, or the regular expression engine inside grep. An **embedded (or internal) DSL** is implemented as a library inside a host language, borrowing that language's syntax and runtime while adding domain-specific primitives. SQLAlchemy Core is an embedded DSL for SQL written in Python, jOOQ is one in Java, and LINQ's method syntax is one in C#. Multiple embedded DSLs can coexist in a single program, and the host language's tools, like type checking and editor support, are inherited automatically.

Application-embedded DSLs live inside larger software, like spreadsheet macros or UnrealScript inside the Unreal Engine, letting users extend the host without learning its full language. Some DSLs compile to non-code outputs: Csound compiles to audio files, and the Persistence of Vision Ray Tracer (POV-Ray) language compiles to rendered graphics.

## When a DSL is worth building

A DSL pays off when the target problem recurs often enough that expressing it in a tailored language is clearer than reusing a general-purpose one, and when the language lets a specific class of problem or solution be expressed more directly than existing languages allow. This is the core of **language-oriented programming**, which treats special-purpose languages as a standard part of problem solving, and of **domain engineering**, which selects or builds a language suited to the domain at hand. In model-driven engineering, examples include the Object Constraint Language (OCL) for annotating models and Query/View/Transformation (QVT) for model transformations.

## Design tradeoffs

A well-designed DSL is **less comprehensive** than a general-purpose language, **more expressive** within its domain, and carries **minimal redundancy**, avoiding multiple ways to say the same thing. This is why DSLs can capture idioms that GPLs cannot enforce directly. A script in a spreadsheet DSL might automatically save data on close, something a general-purpose language leaves to the programmer to remember.

## Benefits and costs

The narrower scope makes DSLs faster to learn. Using the vocabulary of the domain lets experts read and validate programs directly, though in practice few domain experts actually write or modify DSL programs themselves.

The costs are real. Designing, implementing, and maintaining a language and its toolchain, including the **integrated development environment (IDE)**, is expensive. Finding and maintaining the right scope is hard, and balancing domain-specific against general-purpose constructs is harder. Similar DSLs proliferate: two insurance companies, for example, may each maintain their own incompatible version, creating fragmentation. Performance can suffer compared to hand-written general-purpose code, and the pool of expert practitioners in any one DSL is small, which raises hiring costs and makes examples harder to find. Integrating a DSL with the rest of an IT system also tends to be more difficult than integrating a general-purpose language.

Source: adapted from "Domain-specific language" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Domain-specific_language
