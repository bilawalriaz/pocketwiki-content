# Dynamic programming language

A dynamic programming language defers decisions about variables, method calls, and data types until the program is running, rather than fixing them at compile time. In a static language, the compiler locks in each variable's type and the shape of every method call before the program starts; a dynamic language postpones that work and decides what to do based on the values it encounters at runtime. A single variable can first hold an integer and later hold a string with no type declaration in between, and a function can be replaced, extended, or created while the program is executing.

The earliest language in this family is Lisp (McCarthy, 1965), which has shaped the design of dynamic languages since. Widely used dynamic languages include JavaScript, Python, Ruby, PHP, Lua, and Perl, alongside Common Lisp, Smalltalk, Elixir, Groovy, Julia, and R.

## Capabilities that shift work into the running program

Dynamic behaviour shows up in five recurring capabilities. Each one moves work a static language performs at compile time into the running program.

- **Eval and runtime code generation.** An `eval` function takes a string or an abstract syntax tree (a tree representation of parsed source code) and executes it, returning the value if the code is an expression. Erik Meijer and Peter Drayton warn that `eval` is often misused to imitate higher-order functions (functions that accept or return other functions) or to perform deserialisation (reconstructing data from a stored form), when a more direct construct would do.
- **Object and type alteration.** Classes, inheritance, and method tables can be rewritten while the program runs. A new slot (a named field on an object) can be added to an existing class so that previously created instances gain the field without being rebuilt, and a method on those instances can be replaced with a new version that the existing objects immediately see.
- **Type inference.** Because the type system is dynamic, the runtime continually infers types from the values it handles, recalculating as values change and atomic operations are performed.
- **Implicit memory allocation.** Static languages often require the developer to declare memory sizes in advance or to manipulate pointers (raw memory addresses) explicitly; dynamic languages allocate and reallocate as the program's operations demand it, consistent with their ability to alter object layout at runtime.
- **Reflection.** Programs can inspect their own types and metadata at runtime. In Lisp, reflection goes further and can analyse and modify the program's code treated as data, working with S-expressions (Lisp's parenthesised syntax for both code and data) directly.

A small number of dynamic languages add **macros** on top of these. Unlike C or C++ macros, which only do textual substitution before compilation, macros in dynamic languages combine code introspection (examining classes, functions, and keywords) with `eval`. They reach into the compiler, interpreter, or virtual machine and can define new language-like constructs, optimise code, or modify the syntax of the language itself. Assembly, C, C++, early Java, and Fortran sit outside this dynamic category.

## A worked example in Common Lisp

Common Lisp and its Common Lisp Object System (CLOS) make the moving parts visible. A lambda expression (an anonymous function written inline) is stored in a variable, compiled into a function called `best-guess`, and called with the input 10.3 to produce 265.225. The source code in the variable is then rewritten to take the square root instead, the function is recompiled, and the next call with the same input returns 16.28573. The call site never changed; only the function it was bound to did, an instance of late binding (resolving the actual code to run at the moment of the call rather than earlier).

Next, an existing object is altered by changing its class. A `person` class is defined with a `name` slot, an instance called Eva Luator is created, and a custom print method is installed. The `person` class is then redefined to add an `age` slot, the print method is replaced, and the original instance immediately reflects the change, displaying the new slot and using the new print routine without being reconstructed.

Behaviour can also be assembled from multiple methods at call time. A `person` class with a simple print method gains a new superclass, `id-mixin`, which contributes its own `:after` print method. A mixin is a small class designed to be combined with others to add behaviour. When the instance is displayed, the runtime combines an `:around` method, the primary method, and the `:after` method into a single effective method that prints the name followed by the ID. The combination is chosen from the actual class of the argument at the moment of the call, not at compile time.

These capabilities trade compile-time guarantees for runtime flexibility. Type errors, missing methods, and memory layout decisions surface during execution rather than before it, so mistakes that a static compiler would catch are deferred to testing or to the running program.
