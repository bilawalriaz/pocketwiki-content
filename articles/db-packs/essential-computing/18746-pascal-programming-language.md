# Pascal (programming language)

Pascal is an imperative, procedural programming language designed by Niklaus Wirth in 1970 as a small, efficient tool for teaching structured programming and reliable data structuring. It is named after Blaise Pascal, the 17th-century French mathematician who built one of the earliest mechanical calculators.

## Origins in the ALGOL family

Pascal descends from ALGOL 60. Wirth worked on ALGOL during the 1960s, first on the Euler language (1965, with Helmut Weber), then on ALGOL W with Tony Hoare. When the ALGOL X committee chose the more complex ALGOL 68, which proved hard to compile efficiently, Wirth left the process and refined ALGOL W into Pascal, released in 1970.

Pascal kept ALGOL's scalars, arrays, and block structure, then added strongly typed complex data: records, variants, pointers, enumerations, sets, and procedure pointers. Some constructs were inspired by Simula 67 and ALGOL 68. A distinctive feature is that a program is syntactically like a single procedure, with procedures and functions nestable to any depth, unlike C, where block structure is more restricted. Strong typing means one type cannot be converted or reinterpreted as another without an explicit conversion. Pointers must reference only dynamically created anonymous variables and must have an associated type, which eliminates many type-safety problems found in C and PL/I.

## Compiler history

The first Pascal compiler ran on the CDC 6000 mainframe in Zurich by mid-1970, after a failed attempt to write it in FORTRAN 66. It was eventually self-hosted: written in Pascal itself, so the compiler could recompile itself when ported. The GNU Pascal compiler is a notable exception, written in C.

Wirth's Pascal-P system was a porting kit built around a p-code interpreter for a virtual stack machine. Versions Pascal-P1 through P4 came from Zurich. UCSD Pascal branched from Pascal-P2, turning the interpreter into a bytecode engine that ran well on memory-limited microprocessors. UCSD Pascal was one of three operating systems available at the launch of the original IBM PC and was the basis for Apple Pascal on the Apple II (1979).

## Rise, peak, and displacement

Pascal spread through the 1970s on minicomputers and into the late 1970s on microcomputers. UCSD Pascal carried it to the Apple II, Apple Lisa, and Macintosh; parts of the original Macintosh operating system were hand-translated from Pascal source into Motorola 68000 assembly. Apollo Computer adopted Pascal as its systems programming language starting in 1980. Donald Knuth's TeX was written in WEB, a literate programming system based on DEC PDP-10 Pascal. Adobe Photoshop was written in Macintosh Programmer's Workshop Pascal. The ISO 7185 standard was published in 1983 and widely used on mainframes, minicomputers, and 16- and 32-bit IBM PCs. In the 1980s Pascal became the dominant teaching language in university programming courses.

Turbo Pascal, written by Anders Hejlsberg in highly optimized assembly for the IBM PC, became the dominant PC compiler thanks to aggressive pricing, one of the first full-screen IDEs, and compile-link-run times measured in seconds. Object Pascal extensions were added in Turbo Pascal 5.5 (1989) and evolved into Delphi on Windows. Free Pascal is the open-source cross-platform descendant, paired with the Lazarus IDE. Pascal was displaced by C in the late 1980s and early 1990s as UNIX systems spread and C++ was released.

## Language features

A Pascal program begins with the `program` keyword, declares constants, types, variables, and procedures, then has a main block bracketed by `begin` and `end`. Semicolons separate statements; a full stop ends the program; letter case is ignored.

Predefined scalar types are `integer`, `real`, `Boolean`, and `char`. Structured types include `array`, `record`, `set`, `file`, and `pointer`. Control flow uses `if`/`then`/`else`, `while`, `for`, `repeat`/`until`, and `case`. Subroutines are `procedure` and `function`, nestable to any depth.

A record groups named fields of mixed types. Variant records, defined with a `case` clause, let several fields share the same memory. Subrange types restrict a variable to a contiguous range, such as `1..10` or `'a'..'z'`. Set types, unusual for the era, model mathematical sets over small ordinal domains. A set is represented internally as a bit vector, so membership tests like `i in [0..3, 7, 9, 12..15]` compile to fast bitwise operations, often faster than the equivalent chain of comparisons.

Pointers are declared with `^` and dereferenced with `^`. The `new` procedure creates a heap variable; `dispose` frees it. Pascal forbids pointers to ordinary static or local variables, which prevents certain aliasing bugs but does not eliminate dangling pointers, since manual `dispose` is still required. Languages like Java and C# avoid dangling pointers through automatic garbage collection, though they can still leak memory. Parameters pass by value by default; prefixing a parameter with `var` passes by reference. The strict ordering of declaration sections was designed to enable efficient single-pass compilation; later dialects like Delphi relaxed this.

## Criticism and legacy

Pascal drew sharp criticism in its early years. Nico Habermann (1973) faulted the poorly defined data types and ranges. Brian Kernighan (1981, "Why Pascal is Not My Favorite Programming Language") identified the central problem: because array sizes and string lengths were part of the type, no function could accept variable-length arrays or strings, making a generic sorting library impossible. He also cited unpredictable Boolean evaluation order, weak library support, lack of static variables, and no clean way to escape the type system.

Most of these complaints were addressed by later extensions and by Extended Pascal (ISO/IEC 10206:1990), which added variable-length strings, separate compilation, short-circuit Boolean operators, modular units with initialization and finalization, and a default `otherwise` clause for `case`. On PCs, however, Borland dialects became the de facto standard, so the formal ISO language and the popular dialects diverged. Free Pascal reunites the ecosystem by supporting both ISO and Borland dialects through mode directives.

Pascal directly influenced Ada, Modula-2, Oberon, and Object Pascal, and its influence reaches Java (originally based on a UCSD Pascal model), C#, Component Pascal, Go, VHDL, and Standard ML. Its successor line lives on as Delphi and Free Pascal/Lazarus, both still used for Windows, macOS, iOS, Android, and Linux development.
