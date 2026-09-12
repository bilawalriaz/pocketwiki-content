# Parameter (computer programming)

In most programming languages, a **parameter** is a named variable declared in a function's definition, and an **argument** is the value supplied at the call site. The terms are often used interchangeably, but parameters belong to the function and arguments belong to the call. A parameter is unbound in the definition; an argument can be a literal, a variable, or a more complex expression.

A function's **signature** lists its parameters. Each call evaluates the argument expressions and binds the results to the corresponding parameters before the body runs. In `def add(x: int, y: int) -> int`, `x` and `y` are parameters; in `add(2, 3)` the arguments are the literals `2` and `3`, and in `add(a + 1, b + 2)` they are the expressions `a + 1` and `b + 2`. A mismatch in number, order, or type between argument list and parameter list is a common source of runtime errors.

## Evaluation strategies

The mechanism for binding arguments to parameters is the language's **evaluation strategy**, and it controls what a function can do to its inputs.

- **Call by value**: the parameter becomes a fresh local variable initialised with a copy of the argument. The function cannot modify the caller's variable.
- **Call by reference**: the parameter is an alias for the argument, which must itself be a variable. Assignments to the parameter change the caller's variable.

So `f(2)` and `a = 2; f(a)` are equivalent under call by value. Under call by reference only the second passes an alias. C and C++ are call by value, but passing a pointer or reference (itself a value that designates another variable) produces call-by-reference behaviour.

## DatatypesIn **strongly typed** languages each parameter's type is declared. Languages with **type inference** deduce the type from context. **Dynamically typed** languages defer type checking until the call runs. **Weakly typed** languages do little type checking and rely on the programmer. Some languages use `void` to mark a parameterless function; in type theory such a function takes the empty parameter list of type `unit`.

## Default, variadic, and named parameters

Ada, C++, Python, Ruby, Common Lisp, Fortran 90, Clojure, and PowerShell let a parameter carry a **default argument** that the caller may omit. Default arguments are a restricted form of a variadic parameter list. Some languages accept a **variable-length argument list**, where one parameter collects any number of extras (PowerShell's `$args`, iterated by the function). Ada and PowerShell support **named parameters**, where the caller writes the parameter name alongside the value, allowing reordering and omission.

## Multiple parameters in functional languages

In lambda calculus every function takes exactly one argument. A function of several arguments is modelled as a function that takes the first argument and returns a function that takes the rest. This transformation is **currying**, the surface syntax of ML and Haskell. Function application is left-associative, so `f x y` means `(f x) y`.

## Output and input/output parameters

Most parameters are **input parameters**. An **output parameter** carries a result back to the caller; an **input/output parameter** does both. The three modes are denoted `in`, `out`, and `inout`.

- `in`: any value or initialised variable; the function must not assign to it.
- `out`: an assignable variable; its prior value is inaccessible and the function must assign to it.
- `inout`: an initialised, assignable variable; the function may read and write it.

Output parameters let a function return more than one value. In C, `f(x, &width, &height)` writes through the addresses of `width` and `height`. C#'s `Int32.TryParse(s, out result)` returns a Boolean and stores the parsed integer in `result`. Ada 83 forbade reading an output parameter even after assignment; Ada 95 relaxed this so the same variable can serve without an auxiliary accumulator.

These **parameter modes** are a form of denotational semantics: they describe programmer intent rather than the underlying mechanism. A compiler may implement `in` by reference or `out` by copying back. PL/SQL passes `OUT` and `IN OUT` by value by default and copies the result back, but accepts `NOCOPY` to pass by reference. Syntactically, modes are flagged in the declaration, such as `void Fn(out int x)` in C#. Output parameters conventionally appear last.

Output parameters hinder readability. They force a side effect into the signature, blur the line with `inout`, and break **function composition**, since the result lives in a pre-declared variable rather than an expression: a chain `g(y, f(x))` must become separate statements with intermediates, unless the function also returns the output. Modern style prefers tuples, nullable types, exceptions, or tagged unions for multiple or optional results. In object-oriented code, mutating an object passed by reference (**call by sharing**) usually replaces `inout` parameters.

## Alternative convention in Eiffel

Eiffel reassigns the terms. `argument` refers exclusively to a routine's inputs, while `parameter` refers exclusively to **generic type parameters** on classes. `HASH_TABLE[G, K -> HASHABLE]` is instantiated as `HASH_TABLE[STRING, STRING]`, where `STRING` is the actual generic parameter substituted for the formal `G` and `K`.
