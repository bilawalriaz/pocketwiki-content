# Recursion (computer science)

In computer science, recursion solves a problem by depending on solutions to smaller instances of the same problem. The mechanism is a function that calls itself from within its own code. Most programming languages support recursion; some functional languages, such as Clojure, rely solely on recursion for repetition and have been proved Turing complete.

## How a recursive function is built

Every recursive function has two parts that mirror a proof by mathematical induction:

- **Base case.** One or more inputs the function answers directly, with no further recursion. These are the smallest inputs and provide the stopping condition. Without a correct base case, recursion never ends and produces infinite recursion, which in practice exhausts the call stack (the memory region a runtime uses to track active function calls) and causes a stack overflow. For factorial, `0! = 1` is the base case.
- **Recursive case.** A rule that breaks the current input into a smaller sub-problem of the same form, with each step shrinking the input toward a base case. For factorial: `n! = n · (n−1)!` for `n > 0`. The recursive call is the inductive step: assume the function works for the smaller instance, then extend that result to the current input.

The factorial trace shows the shape: `4! = 4·3! = 4·(3·2!) = 4·(3·(2·1!)) = 24`.

## Recursive data

Recursion also defines data whose size is not fixed in advance. An inductive (constructive) definition says how to build values. A linked list is either empty or a head string followed by another list; the self-reference lets lists grow to any finite length. Binary trees use two self-references (left and right), so operations like search and traversal naturally need two recursive calls per node. Programming-language grammars (Backus–Naur form) follow the same pattern, allowing expressions such as `(5 * ((3 * 6) + 8))`.

A coinductive definition instead specifies how to *observe* values, and is used for data that may be infinite, such as a stream defined by `head(s)` (a string) and `tail(s)` (another stream). Corecursion computes successive pieces of such objects in lazy languages, where evaluation is deferred until a value is needed.

## Kinds of recursion

**Direct and indirect.** Direct recursion is a function calling itself. Indirect (mutual) recursion is a cycle through other functions: if `f` calls `g` and `g` calls `f`, both recurse on each other.

**Single vs. multiple.** Single recursion makes one self-reference per call (list traversal, factorial) and is usually replaceable by a loop running in linear time and constant space. Multiple recursion makes more than one (tree traversal, naïve Fibonacci, divide-and-conquer algorithms such as quicksort and merge sort) and may need exponential time and space. Fibonacci is computed by passing two successive values rather than making two separate recursive calls.

**Structural vs. generative.** Structural recursion feeds each recursive call a strictly smaller piece of the same data, so termination follows from the data definition and covers nearly all tree and list traversals. Generative recursion invents new data at each step (quicksort, binary search, Newton's method, fractals), so termination depends on an external condition such as approximation error rather than on shrinking input.

**Tail recursion.** A call is in tail position when it is the last operation the function performs, so the caller has no deferred work. With tail-call optimization, a tail-recursive function such as the Euclidean gcd runs in constant stack space and behaves like a loop. Factorial, whose call is wrapped in a multiplication, is not tail-recursive.

## Recursion versus iteration

Recursion and iteration are equally expressive: any recursive function can be rewritten as a loop with an explicit stack, and any loop can be expressed recursively. In imperative languages, iteration is usually faster because it avoids call overhead and stack growth; naive recursive programs can run several orders of magnitude slower, and unbounded recursion can overflow the stack, which is why Python caps recursion depth. In functional languages, tail-call optimization makes recursion nearly free.

A factorial comparison shows the translation directly:

```
recursive(n): if n == 0 return 1 else return n * recursive(n−1)
iterative(n): x = 1; for i = 1 to n: x = x * i; return x
```

Tree traversal, divide-and-conquer sorts, and the Ackermann function are inherently multiply recursive but can be implemented iteratively with an explicit stack, at the cost of extra programmer effort and complexity.

## Implementation refinements

A **wrapper function** sits in front of the real recursive worker, validating parameters, allocating state such as a depth counter or memoization cache (a table that stores previously computed results so they are not recomputed), or catching errors. **Short-circuiting the base case** checks the base case *before* the recursive call, which matters when base cases are frequent, as with null pointers in a binary tree, where it can halve the number of calls. **Hybrid algorithms** keep recursion for large input and switch to a non-recursive algorithm such as insertion sort once the data is small; merge sort and Timsort are standard examples.

## Cost and limits

A naive recursive program pays both time (function-call overhead) and space (a call-stack frame per active call) for every level of nesting. Tail-call optimization removes the space cost but only where the language guarantees it; in C, Java, and Python a recursive program that should be iterative can still overflow the stack. A recursive program with no reachable base case recurses without bound until the stack is exhausted, and if tail-call optimization is active the recursion is rewritten into a true infinite loop that never terminates.

The earliest practical recursion in programming appeared in the late 1950s and early 1960s, after Church, Gödel, Kleene, and Turing developed the theory of computability (what can in principle be solved by mechanical computation). John McCarthy made recursion central to LISP in 1960, and the ALGOL 60 report that same year let procedures call themselves for the first time in a mainstream imperative language.

Source: adapted from "Recursion (computer science)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Recursion_%28computer_science%29
