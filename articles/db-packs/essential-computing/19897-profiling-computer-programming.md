# Profiling (computer programming)

In software engineering, profiling (also called program profiling or software profiling) is a form of dynamic program analysis that measures how a running program uses resources such as time, memory, or specific instructions, and records the frequency and duration of function calls. The output most often drives program optimization, specifically performance engineering.

A profiler is the tool that performs these measurements. It works by instrumenting either the program source code or its compiled binary, meaning it inserts extra instructions or hooks that record what the program is doing while it runs. Common collection techniques include hardware interrupts, code instrumentation, instruction set simulation, operating system hooks, and performance counters.

## Output formats

A profiler produces one of three kinds of output. A statistical summary of the events observed, called a profile, is usually shown annotated next to the source statements where events occur, so the data size scales with the code size of the program. A stream of recorded events, called a trace, preserves timing relationships, which matters for parallel programs where waiting on messages or synchronization depends on the order of events; because trace size scales with the program's instruction path length, traces are usually started and stopped at chosen points. An ongoing interaction with a hypervisor, the layer that controls the virtual machine running the program, allows the trace to be toggled at any point and shows live metrics for the executing program.

## Uses

Profilers identify performance bottlenecks by making long-running code obvious at the scale of a method, a module, or a whole program. Results can be ingested by a compiler to perform profile-guided optimization, where the compiler uses real runtime data to decide how to optimize. Profilers also feed into application performance management systems that aggregate profiling data across distributed transactions.

## Profiler types by output

A flat profiler computes average call times without breaking them down by callee or context. A call-graph profiler extends this by showing call times, frequencies, and the call chains that reach each callee. An input-sensitive profiler adds another dimension by relating performance to features of the input workload, such as input size or values, and produces charts that show how an application scales as input changes.

## Profiler types by collection method

Event-based profilers interrupt program execution to collect information. The interrupts limit timing resolution, so results should be read with that in mind. Examples include JVMTI (the JVM Tools Interface) for Java, which provides hooks for events such as calls and class loads; the .NET Profiling API, which lets an agent attach to the CLR and rewrite bytecode; and Python's `sys.setprofile`, which traps call, return, and exception events.

Statistical profilers work by sampling. A sampling profiler probes the target program's call stack at regular intervals using operating system interrupts. Sampling gives only a statistical approximation and is less numerically precise, but it lets the program run at near full speed. Because it is less intrusive, sampling avoids disturbing memory caches and instruction pipelines, and it can expose problems that other methods would hide. Some processors include dedicated hardware, such as the PCSAMPLE register on certain ARM Cortex-M3 and MIPS cores, that samples the program counter with no detectable overhead.

## Instrumentation

Instrumentation is the general technique of adding instructions to a target program so it records information about itself. Instrumenting a program can change its behavior and distort measurements, a class of bugs sometimes called heisenbugs. The effect depends on what is being collected: counting each procedure call is cheaper than counting each statement.

Instrumentation can be applied at several levels: manual (a programmer adds timing code or counts events explicitly), automatic source level (a tool rewrites the source code according to an instrumentation policy), intermediate language (instrumentation inserted into assembly or decompiled bytecode, supporting multiple source languages), binary translation (a tool adds instrumentation to a compiled executable), runtime instrumentation (the code is instrumented just before execution), runtime injection (a lighter approach that rewrites code at runtime to jump into helper functions), and interpreter instrumentation (bytecode, control table, or JIT interpreters expose performance metrics as each statement runs because the interpreter controls execution completely).

## History

Profiler-driven analysis on Unix began in 1973 with `prof`, which listed each function and its share of execution time. In 1982, `gprof` extended this to a complete call graph analysis. In 1994, Amitabh Srivastava and Alan Eustace at Digital Equipment Corporation published ATOM, which converts a program into its own profiler by inserting analysis code at compile time, the canonical example of instrumentation. Performance-analysis tools existed on IBM/360 and IBM/370 systems from the early 1970s based on timer interrupts that detected hot spots, an early form of sampling.
