# Abstract machine

An abstract machine is a theoretical model of a computer that specifies how inputs become outputs through step-by-step rules, independent of any real hardware. Like a mathematical function, it takes input, applies defined operations, and produces output. It is called a "machine" because it executes programs one step at a time, and "abstract" because it omits hardware details such as voltages, timing, and circuitry.

Abstract machines serve two purposes. In the theory of computation, they support thought experiments about what can be computed and how hard it is to compute, giving rise to computational complexity theory through models like finite state machines, Mealy machines, pushdown automata, and Turing machines. In practical computing, they give compilers a precise, portable target, letting one high-level language run on many real machines through a common intermediate layer.

## Determinism

Abstract machines are classified by whether their behaviour is fixed for a given input. A deterministic abstract machine always produces the same output from the same starting state and input. A non-deterministic abstract machine can follow different paths on different runs of the same input, potentially producing different outputs. Non-determinism is a modelling tool, useful for analysing problems where the best deterministic algorithm is unknown or expensive, even though real hardware is essentially deterministic.

## Turing machines

A Turing machine is a foundational abstract machine. It operates on a tape of symbols of any length, with a pointer that reads and modifies the current symbol. A minimal Turing machine with the single command "convert symbol to 1 then move right" transforms any tape into a string of 1s. Standard Turing machines are deterministic; non-deterministic variants are studied for complexity analysis, where they define a set of possible behaviours rather than racing copies of the machine.

## Implementation

The same abstract machine can be realised three ways. In hardware, physical memory, logic circuits, and buses implement the machine directly; a CPU is a concrete realisation of an abstract machine, and once built it is hard to change. In software, a program in another language simulates the machine's data structures and algorithms; when paired with an interpreter, this is called a virtual machine. In firmware, microcode sits between hardware and software, implementing machine instructions without new circuitry. Software is the most flexible form because the simulating program is easy to change.

## Programming language implementation

For a program to run, it must be expressed in the constructs of a programming language. Most language-oriented abstract machines share a program store holding the instructions and a state that usually includes a stack and registers. A stack is a memory unit whose address register, the stack pointer, always refers to the top item. An instruction pointer marks the next instruction; after each step the interpreter advances the pointer and repeats. This fetch-decode-execute cycle is the machine's execution loop.

An abstract machine for a specific language is the collection of data structures and algorithms that can store and run programs in that language. It bridges high-level languages and real hardware with an intermediate step whose instructions are tailored to the source language, for example object access in object-oriented languages or backtracking in logic languages.

## Paradigm-specific machines

Different paradigms produced different machines. Imperative-language machines include Algol Object Code (1964), Forth (1970), the P4-machine (1976), and the UCSD P-machine (1977); the Java Virtual Machine (late 1990s) later made the intermediate-language approach widely practical. Object-oriented machines are typically stack-based, with special field and method access instructions and implicit memory management through a garbage collector, as in Smalltalk-80 (1980), Self (1989), and Java (1994). String-processing machines behind Snobol4 and ML/I gave faster execution and machine independence. Functional-language machines split between strict evaluation, as in the SECD machine (1964) and Cardelli's Functional Abstract Machine (1983), and lazy evaluation, as in the G-machine (1984), Krivine machine (1985), and Three Instruction Machine (1986). The Warren Abstract Machine (1983) became the de facto Prolog target, with unification and backtracking instructions matching Prolog's Horn-clause search.

## Structure

A generic abstract machine has two parts: a memory for programs and data, and an interpreter that executes the stored instructions. The interpreter's work falls into four categories. Primitive-data operations handle values like integers and strings, with arithmetic done in a single step. Sequence-control operations change the next-instruction pointer, enabling jumps and conditional execution. Data-transfer operations move operands between memory and interpreter. Memory-management operations allocate and reclaim storage, since data and programs can persist indefinitely or be freed dynamically.

## Hierarchies

Abstract machines are often stacked. At the bottom sits a physical computer built from electronic devices, with a possible microprogrammed firmware layer above. The operating system then presents an abstract machine with higher-level primitives such as files. On top of this host machine, a high-level language can run through an intermediary machine like the JVM, and application layers, such as a "web machine" for HTTP and HTML or a web-service layer for business protocols, can sit above. Each level uses the level below and adds new functionality, so a programmer at the top works only with the abstractions of the highest relevant machine, while lower layers translate those abstractions into physical behaviour.
