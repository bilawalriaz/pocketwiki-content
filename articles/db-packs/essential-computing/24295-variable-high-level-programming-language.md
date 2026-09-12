# Variable (high-level programming language)

A variable is a symbolic name paired with a storage location that holds a value. The name and the storage are separate: the name lets a programmer refer to the value, the storage holds the actual bits in memory. A compiler or interpreter maintains the link, and most languages let the stored value change during program execution.

In BASIC, Python, and Ruby the model is closer to "a name associated with a value," with memory handled transparently by the runtime. In C and Java the model is closer to a typed container at a fixed location. Both describe the same idea: a name bound to a value that can be read or replaced.

## How variables differ from mathematical variables

A programming variable is a concrete, mutable holder of data, not an abstract symbol in an equation. Its value is read, written, and reassigned, and it can be locked to a single value for its whole lifetime, in which case it behaves like a constant. Programming variables tend to have long, descriptive names such as `total_count` or `user_name`, while mathematical variables usually have terse one- or two-character names.

## Identifiers, aliasing, and binding

A variable can have more than one identifier pointing to it, a situation called aliasing. If two names refer to the same storage, writing through one changes what the other reads. If `total_count` and `r` both identify the same variable, setting `r` to 2009 causes `total_count` to read 2009 instead of its earlier 1956. With one identifier, that identifier is the variable's name; with several, each is one of its names.

At run time the identifier in source code is bound to a value, and that binding can change as the program executes. The compiler translates the symbolic names a programmer writes into the actual memory addresses the machine uses.

## Scope and extent

Scope is where in the source text a name is visible; it is a property of the name, decided by program structure. Extent, also called lifetime, is the period of execution during which a binding to a value or memory location remains valid; it is a property of the storage, decided at run time.

With lexical scope a name is visible only inside a particular function or block, and resolution happens at compile time. With dynamic scope resolution happens at run time against a binding stack that depends on control flow. Variables confined to a function are local; variables reachable from anywhere are global.

Scope and extent can drift apart. A variable whose scope begins before its extent is uninitialized and typically holds an arbitrary value if read, similar to a wild pointer. A variable whose extent ends before its scope becomes a dangling pointer. A variable whose extent outlasts its scope can cause a memory leak if the language lacks garbage collection, because the memory can no longer be freed through any accessible name.

## Typing

In statically typed languages such as C, C++, Java, and C#, each variable carries a type that restricts which values it may hold, so an integer variable cannot store text. In dynamically typed languages such as Python, a variable has no fixed type; the type is inferred from the current value and can change as the value changes. Common Lisp supports both: a variable has a compile-time type (defaulting to `T`, the universal supertype) and each value carries a runtime type that can be inspected.

Static typing lets parametric polymorphism be resolved at compile time, which differs from the run-time dispatch in object-oriented virtual functions, where the implementation is chosen by the runtime type of the value rather than the declared type of the variable.

## Parameters

Function parameters are themselves variables. In `def add_two(x: int) -> int: return x + 2`, `x` is a parameter that receives a value when the function is called; the 5 passed in is the argument supplying that value. Parameters usually have local scope, so this `x` is visible only inside `add_two`, though other functions can declare their own `x`.

## Memory allocation

How variables are stored varies by language and implementation. Local variables whose extent is a single function call are usually placed on the call stack, a per-function region of memory that is reclaimed automatically when the function returns. More generally, a variable's name is bound to the address of a contiguous block of bytes, and operations on the variable manipulate that block.

Values that are large or of unknown size at compile time are usually stored indirectly: the variable holds a reference, and the value itself lives in a pool of memory called the heap. In garbage-collected languages such as C#, Java, Python, Go, and Lisp, the runtime reclaims heap objects automatically once no variable can reach them. In languages without garbage collection, such as C, the programmer must allocate and free heap memory explicitly; forgetting to free causes a memory leak that gradually exhausts available memory.

## Naming

Programming variables usually take multi-character descriptive names such as `COST` or `total`. Single letters, most commonly `i`, `j`, `k`, are reserved for auxiliary roles like array indices. Most languages forbid starting a name with a digit, forbid whitespace inside names, and allow only letters, digits, and the underscore; some languages attach sigils, symbols such as `$` or `@`, to mark a name's type or scope. Case sensitivity varies: most modern languages treat `count` and `Count` as different names, while some older ones do not.

Names exist for human readers. At the machine-code level no name is used, so any legal name works for the computer. Descriptive names make code easier to review, which is why most teams adopt a style guide for naming.

## Lifetime classification

Variables can be grouped by when their storage is bound and released:

- Static: bound to a memory cell before execution begins and keeps that cell until the program terminates, like static variables in C and C++.
- Stack-dynamic: bound when the declaration is executed and released when the procedure returns, like local variables in C functions and Java methods.
- Explicit heap-dynamic: allocated and freed by explicit run-time instructions, like C++ objects created with `new` and destroyed with `delete`, and all objects in Java.
- Implicit heap-dynamic: bound to heap storage only on assignment, with allocation and release on each reassignment, like variables in JavaScript and PHP, and all variables in APL.

Source: adapted from "Variable (high-level programming language)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Variable_%28high-level_programming_language%29
