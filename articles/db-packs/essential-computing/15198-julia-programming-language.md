# Julia (programming language)

Julia is a high-level, dynamic, general-purpose programming language designed to be as easy to write as Python and as fast as C. Work began in 2009 by Jeff Bezanson, Stefan Karpinski, Viral B. Shah, and Alan Edelman to solve the "two-language problem" in scientific computing, where prototypes are written in a slow high-level language and then rewritten in a fast low-level one. The project launched publicly on 14 February 2012; version 1.0 shipped on 8 August 2018, and syntax has been backward-compatible since.

## How it works

The speed comes from just-in-time (JIT) compilation through the LLVM compiler toolchain, which compiles source to optimized machine code the first time a function runs, so later calls run at near-C speed. Parallel and distributed computing, coroutines (lightweight green threads), and a tracing garbage collector are built in.

The defining design choice is multiple dispatch. In most object-oriented languages, a method is chosen from the type of one special argument (the receiver, or `self`). In Julia, the method is chosen from the types of *all* arguments and their combinations. Every concrete type is a subtype of `Any`, the top of the type hierarchy, and composition replaces inheritance. The type system is dynamic, inferred, optional, parametric (types can take other types as parameters), and strong. Types document code and drive dispatch, so optional annotations let the compiler emit faster machine code without forcing declarations.

Functions stand alone rather than living inside classes, and built-in operators like `+` are themselves generic functions that user code can extend for new number types. The `Unitful.jl` package extends this to physical units, letting expressions carry meters, kilograms, and seconds with full type checking.

## Ecosystem and tooling

A built-in package manager installs and tracks dependencies from a central registry, with federated registries also supported. Packages typically ship as source on GitHub. Notebooks such as Pluto.jl, Jupyter, and (since 2025) Google Colab run Julia interactively, and Quarto weaves Julia with Python, R, and JavaScript in one document. The official read–eval–print loop (REPL) supports tab completion, searchable history, shell access (`;`), and help mode (`?`). Julia source files use the `.jl` extension.

Julia interoperates with C and Fortran directly, and with C++, Python, R, Rust, Java, JavaScript, MATLAB, and C# through packages. It compiles to standalone executables with `PackageCompiler.jl` and (since 1.12) `JuliaC.jl`; a stricter static subset is available through `StaticCompiler.jl`.

## Language lineage

Julia borrows Lisp-like macros from Scheme and Common Lisp, including homoiconic macros that operate on abstract syntax trees, and adopts the syntax style of MATLAB, with infix operators, array literals, and mathematical notation. Its multiple-dispatch model echoes CLOS, Dylan, and Fortress:

| Language | Type system | Generic functions | Parametric types |
|----------|-------------|-------------------|------------------|
| Julia | Dynamic | Default | Yes |
| Common Lisp | Dynamic | Opt-in | Yes (no dispatch) |
| Dylan | Dynamic | Default | Partial (no dispatch) |
| Fortress | Static | Default | Yes |

## Use and adoption

Julia runs on Linux, macOS, Windows 10+, and FreeBSD, with tiered support for ARM Linux, Apple Silicon, RISC-V, and GPU backends including NVIDIA CUDA, Apple Metal, Intel oneAPI, and AMD ROCm. Multi-threading is native.

Adoption spans universities (MIT, Stanford, UC Berkeley, Technical University of Munich, Ferdowsi University of Mashhad, University of Cape Town) and major organizations: NASA for spacecraft dynamics and cosmology, CERN for LHCb data analysis, the Federal Reserve Bank of New York and Bank of Canada for macroeconomic modeling, the U.S. Air Force Research Laboratory for autonomous drone flight, and pharmaceutical firms including Moderna, Pfizer, and AstraZeneca for drug development. BlackRock applies it to financial time series, and ASML uses it for hard real-time machine control. Julia code has flown in space on a Raspberry Pi Compute Module 4 aboard the Waratah Seed-1 cubesat, running a GPS receiver payload.
