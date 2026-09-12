# Synchronous programming language

A synchronous programming language is a computer programming language built for reactive systems, software that must answer a fast-moving external environment (like an autopilot) within strict time bounds. Such systems are usually real-time and embedded.

## The three classes of computer systems

Synchronous languages exist because not all software behaves the same way. Computer systems fall into three broad classes:

- **Transformational systems** take inputs, process them, produce outputs, and stop. A compiler is the classic example.
- **Interactive systems** talk to their environment continuously, but at the program's own pace. A web application fits here.
- **Reactive systems** also interact continuously, but at the environment's pace. An automatic flight control system is the canonical example: the airplane pushes data in, and the software must react before a deadline.

Reactive systems are often called real-time systems and show up most often inside embedded devices.

## The synchronous abstraction

Synchronous programming, also called synchronous reactive programming (SRP), copies an idea from digital hardware. In a synchronous circuit, designers ignore how long a gate or a wire really takes. Every gate is assumed to compute instantly, every wire to transmit instantly, and a global clock ticks the whole circuit forward. At each tick the circuit reads its inputs and current memory, and instantly produces new outputs and memory values. The electrons behave as if they moved infinitely fast.

SRP brings the same idea into software. A synchronous program reacts to its environment through a sequence of **logical ticks**. Within a tick, all computation is treated as instantaneous. So when the source writes `a||b`, the language reads it as the simultaneous package "ab", not as a race between two threads. The Esterel statement `every 60 second emit minute` means exactly that the signal `minute` lines up with the 60th occurrence of `second`.

The payoff is that the program is fully deterministic: every tick produces exactly one output for a given input and memory state. That determinism makes synchronous programs amenable to formal analysis, verification, and certified code generation, and lets the same language double as a formal specification.

## Why determinism matters here

Asynchronous models on a single processor cannot promise this. The statement `a||b` can actually run as `a;b` or as `b;a`, called interleaving-based nondeterminism. That nondeterminism produces race conditions and makes formal reasoning more complex. Asynchronous formalisms still have their place, especially for distributed systems, which are intrinsically asynchronous, but they cannot give a synchronous program its tidy, one-answer-per-tick semantics.

A separate tradition, Communicating Sequential Processes (CSP), is also synchronous in the sense that processes meet at shared rendezvous points, but it allows both deterministic external choice and nondeterministic internal choice.

## Languages and history

The first synchronous languages were invented in France in the 1980s: Esterel, Lustre, and SIGNAL. Many others followed, including Argos, Atom (a Haskell-embedded DSL for hard real-time work), Averest, Blech, ChucK (synchronous reactive programming for audio), LabVIEW, LEA, PLEXIL, SOL, and SyncCharts.

Source: adapted from "Synchronous programming language" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Synchronous_programming_language
