# Low-level programming language

A low-level programming language provides little or no abstraction from a computer's instruction set architecture, memory, and physical hardware. Its commands map closely to the processor's instructions, so the programmer sees and controls memory addresses and machine operations directly. Because the gap between the language and the CPU is small, these languages are described as "close to the hardware," and they give full control over memory and machine code at the cost of portability and safety.

## Machine code

Machine code, the first-generation programming language, is raw bits the CPU stores and interprets according to its instruction set architecture. Each instruction typically moves data between registers (small named storage slots inside the processor) and memory, performs arithmetic or Boolean operations, compares values, or alters control flow through branching and jumping. Programmers almost never write machine code by hand; they use assembly or a higher-level language, and they read machine code mainly while inspecting core dumps and debugging.

## Assembly language

Assembly language, a second-generation language, adds a thin layer of readability on top of machine code by replacing binary opcodes (numeric codes the CPU recognises) with short mnemonics and by giving symbolic names to memory addresses. It has little formal semantics: it is mostly a direct mapping from human-readable symbols to opcodes, addresses, constants, and strings. One line of assembly commonly represents one machine instruction, and an assembler turns this text into object files that can be linked or loaded on their own; most assemblers also offer macros to repeat common instruction sequences. Because every architecture has its own instruction set, assembly programs written and optimised for one CPU family do not run on another, so they are non-portable.

## Languages between assembly and high-level code

A family of so-called machine-oriented, mid-level, half-way, or quarter-way languages occupied the territory between pure assembly and later high-level languages. Examples tied to specific machines include MOL940 for the SDS 940, MOL-360, PL360, and PL/S for the IBM System/360 line, ESPOL and NEWP for the Burroughs Large Systems, PL-11 for the PDP-11 series, PL516 for the DDP-516, and PS440 for the Telefunken TR 440.

## C and the boundary case

The C language is a third-generation language whose classification is genuinely contested. Its syntax is platform-independent rather than tied to one machine, but it exposes pointers, manual memory management, and arithmetic on those pointers, so the programmer still deals with concerns a higher-level language would hide. Other languages sometimes classed above C can also touch hardware directly, and C code can itself encode abstractions that hide those details. C is therefore higher level than assembly, especially syntactically, yet lower level than many languages in some respects. C is not architecture-independent, but its standard library provides "an interface to system-dependent objects that is itself relatively system independent," which makes cross-platform code possible even when technically challenging.

## A worked comparison: Fibonacci

The same algorithm to compute the nth Fibonacci number appears at three levels. In x86-64 machine code, each line is a hexadecimal encoding of one CPU instruction, such as `89 f8`, `85 ff`, and `74 26`, with no symbolic names. In x86-64 assembly using Intel syntax, the registers rax, rcx, rsi, and rdi are named and manipulated directly. Arguments arrive in rdi and results are returned in rax because of the System V application binary interface (ABI) for x86-64; assembly itself imposes no standard for passing or returning values, since that convention is supplied by an ABI rather than the language.

The same algorithm in C omits all of that. The parameter `n` and the locals `f_nminus2`, `f_nminus1`, and `f_n` carry no specific storage location; the compiler chooses one according to the target's calling convention (a fixed rule for how arguments and return values are placed in registers or on the stack). The `return` statement specifies the value but not the mechanism, so a C compiler for x86-64 typically places the result in rax, as the assembly example does, while a compiler for another architecture uses its own convention. Those abstractions are exactly why the C version compiles for any supported architecture without modification, whereas the assembly version runs only on x86-64.

## Reaching down from a higher-level language

Several high-level languages, including PL/S, BLISS, BCPL, extended ALGOL, NEWP, and C, expose a path to lower-level code. One common mechanism is inline assembly, where assembly instructions are embedded directly in the higher-level source. Many of these languages also accept architecture-dependent compiler optimisation directives that nudge how the compiler uses the target processor. A short GCC snippet illustrates the pattern: variables `src` and `dst` are declared in C, and an `asm` block moves `src` into `dst` and adds one, then `printf` prints the result.

Source: adapted from "Low-level programming language" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Low-level_programming_language
