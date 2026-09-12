# Function (computer programming)

A function is a named, callable block of instructions that a program can invoke any number of times, optionally receiving inputs and returning a result. Different languages call this same thing a procedure, method, subroutine, routine, or subprogram. A function exists at several levels of abstraction: source code names it, the compiler turns it into machine code that follows the same meaning, and at run time the machine allocates a separate working area for each active call.

Functions matter because they let a programmer break a hard problem into smaller, named pieces. Each piece has a small mental footprint (low cognitive load, meaning the reader can hold it in mind without straining), can be reused across a program or across many programs, hides its internals from callers, and can be tested, replaced, or maintained on its own.

## What happens during a call

When a caller invokes a function, control jumps from the call site to the function's first instruction. The function runs sequentially except where its own logic branches. When it finishes, control returns to the instruction right after the call, and any return value becomes available to the caller. For the machine to come back, it has to remember the caller's position, called the return address, and it has to keep the function's working data separate from the caller's, so each call saves a return address together with a fresh working area.

Early machines had no single call instruction, so programmers wrote a short call sequence by hand at every call site to save the return address and jump. Designers later added a jump-to-subroutine instruction that combined both steps, and then machines moved the saved return address and working data onto a call stack: a contiguous region of memory where each active call occupies its own stack frame at the top. When the function returns, its frame is popped. Languages from ALGOL and C onward, including nearly all modern ones, rely on this call-stack mechanism, which is also what makes a function safely recursive.

## Arguments and return values

A function declares formal parameters, the named slots and types it expects. The caller supplies actual parameters, also called arguments. Languages differ in how the argument reaches the function:

- By value: the function gets a copy, so its changes cannot affect the caller.
- By reference: the function gets the address of the caller's variable and can modify it.
- By result or value-result: the caller's variable is updated on return with a value computed inside.
- By name: the argument expression is re-evaluated in the caller's context each time the parameter is used.

By value is the default in C, C++, Java, and most Algol-style languages; by reference is selectable in C++, Fortran, PL/I, Ada, and similar languages. A function either returns a value or performs an action without producing one. C and C++ use the keyword `void` to mark the no-return case; BASIC historically used different syntax such as `Sub` versus `Function`.

## Local state and side effects

A function typically owns local variables held in its stack frame and invisible to the caller. Each call gets its own fresh copy, so nested calls to the same function never interfere. A function may also read or modify things outside its frame, such as global variables, arguments received by reference, files, or devices; any such observable change is called a side effect. In strictly functional languages such as Haskell, side effects are forbidden, so the same input always yields the same output, which makes programs easier to reason about.

## Recursion

A function may call itself. Each recursive call gets a new stack frame with its own locals and return address, so the suspended call's state is preserved while the inner call runs. Recursion mirrors mathematical induction and naturally expresses divide-and-conquer algorithms. The classic example is the Fibonacci function, which calls itself for `n-1` and `n-2` and returns `n` when `n` is 0 or 1. Early Fortran could not recurse because each subroutine owned only one set of variables and one return address; the call stack changed that.

## Reentrancy, overloading, and closures

A function is reentrant if it still works correctly while another call to it is already running, which is required for safe use across threads. Overloading lets several functions share one name if their parameter types differ, so the compiler picks the right one from the argument types, as with `sqrt` defined for reals, complex numbers, and matrices. A closure is a function plus the values of some variables captured from the scope where it was created, a feature Lisp made famous and useful for callbacks and hidden state.

## Cost

Calling a function has overhead: allocating and freeing its stack frame, saving and restoring registers, copying arguments, and copying results on return. Compilers cut this cost in two main ways. Inlining replaces a call with a copy of the function's body, removing the call but enlarging the program. Delayed stacking keeps a leaf function, one that calls nothing else, entirely in registers and only touches the stack if the function itself makes another call. Whether a compiler can safely reorder or duplicate a call depends on side effects; because detecting them is undecidable in general, compilers usually assume any call might have them.

## Origins

The callable-unit idea appeared with the earliest stored-program computers. Konrad Zuse implemented a single subroutine on the Z4 in 1945 using tape, and Alan Turing in 1945 used the terms "bury" and "unbury" for calling and returning while drafting the concept of a return-address stack. Maurice Wilkes, David Wheeler, and Stanley Gill are usually credited with formalising the closed subroutine, in contrast to open subroutines, also called macros, whose body is spliced into each caller. FORTRAN II (1958) was among the first high-level languages to let users write their own subroutines; ALGOL and later procedural languages followed. Collections of reusable subroutines, originally stored as physical tapes or card decks sometimes kept in a literal library, became the first subroutine libraries.

Source: adapted from "Function (computer programming)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Function_%28computer_programming%29
