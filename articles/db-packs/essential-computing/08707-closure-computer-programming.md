# Closure (computer programming)

A **closure** is a function value packaged with the bindings it needs from the place where it was created. A **free variable** is a name the function uses but does not itself define, so its value must come from some enclosing scope. A closure records, for each of those names, the value or storage location the name was bound to when the closure was built. When the closure is later called, even from a different scope, those names still resolve to the original bindings rather than to anything in the new context. A plain function, by contrast, has no such captured environment.

Closures are useful in languages with **first-class functions**, languages where functions can be passed as arguments, returned from other functions, and stored in variables like numbers or strings. In such languages a function commonly outlives the call that produced it. The captured bindings have to stay alive that long, which is why implementations that support closures usually store them on the heap and reclaim them with garbage collection rather than on a stack that is unwound when the enclosing function returns.

## A minimal example

```python
def f(x):
    def g(y):
        return x + y
    return g

a = f(1)        # a is a closure
assert a(5) == 6
```

Calling `f(1)` returns the code of `g` together with a binding of the free variable `x` to `1`. The nested function definition inside `f` is not yet a closure, because `x` is unbound there; the closure exists only after `f` actually runs and supplies a value for `x`. The same closure can be written as `return lambda y: x + y`, and a closure need never be bound to a name: `f(1)(5)` works the same way. A closure is only observably different from an ordinary function when it is invoked outside the scope of the free variables; inside that scope the names resolve the same way regardless.

## Implementation and the funarg problem

In a stack-based language such as C, a function's local variables are deallocated the moment the function returns, so a returned function whose body refers to those variables would point at freed memory. This is the **funarg problem**, short for "functional argument." The standard solution is to allocate the captured variables on the heap and tie their lifetime to the lifetime of any closure that still references them, which is why almost every language with closures also uses garbage collection. C++11 lambdas and GCC nested functions are partial exceptions: they permit the pattern but leave the programmer responsible for not letting the closure escape an invalid scope, in which case invoking it produces undefined behaviour from dangling references. In D version 1, the same restriction applied to delegates, and the programmer had to allocate the captured variable on the heap explicitly. D version 2 detects which variables are referenced by an escaping closure and allocates them on the heap automatically.

## Closures as state

Because a closure's environment persists across calls, a closure can carry private state that no other code can read or modify. This is directly analogous to private fields on an object, and closures have been used to implement object systems in which each closure plays the role of an object whose captured variables are its fields. A side effect is that such a closure is no longer a pure function, because two calls with the same arguments can return different results. Multiple closures created in the same scope share one captured environment, so they can communicate by writing to and reading from those shared variables. Closures are also used in continuation-passing style to hide state, and languages such as Smalltalk build their entire standard control flow, including `if/then/else` and loops, out of objects whose methods accept closures.

## How the binding is captured

Different languages treat captured variables differently, and the choice affects correctness.

- **By reference.** The closure holds a pointer to the variable's storage location, so all closures over the same variable observe updates. ECMAScript works this way for ordinary `var` bindings, which is why a `for` loop that attaches an event handler using `var e` produces handlers that all read the final value of `e` when clicked; using `let` instead gives each iteration its own binding.
- **By value.** The closure holds a copy of the value at the time the closure was created. ML works this way, and Java's anonymous classes require captured locals to be declared `final`, which has the same effect. C++11 lets the programmer choose between `[&]` for reference capture and `[=]` for value capture.
- **As a deferred computation.** A lazy language such as Haskell can capture an expression rather than a value, so any error inside that expression, including a division by zero, only surfaces when the closure is actually invoked.
