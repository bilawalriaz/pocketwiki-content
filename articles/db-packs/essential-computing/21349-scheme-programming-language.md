# Scheme (programming language)

Scheme is a minimalist, dynamically typed dialect of the Lisp family created in the 1970s at MIT by Guy L. Steele and Gerald Jay Sussman. Its core derives from the lambda calculus, a small formal system where computation is the definition and application of named functions, and that small core expresses both functional and imperative programs. Scheme was the first Lisp dialect to use lexical scope, where a variable's binding is determined by the surrounding program text rather than by the call context, and the first to require implementations to perform tail-call optimization, reusing the calling function's stack frame when the last action of a function is to call another, so deep recursion does not exhaust memory. It was also among the first languages to expose first-class continuations, the ability to capture the rest of the program's execution as a manipulable value, letting programmers build non-local control constructs such as coroutines, whose execution can be suspended and resumed, and backtracking search.

## Syntax and homoiconicity

Programs are built from s-expressions, or symbolic expressions: parenthesized lists where a prefix operator is followed by its arguments, as in `(+ 1 2)`. The same list structure is used for code and data, a property called homoiconicity. Scheme inherits the list-processing primitives `cons`, `car`, and `cdr` from earlier Lisps: `cons` constructs a pair, while `car` and `cdr` return its first element and the rest of the list. Procedures are first-class values, assignable to variables and passable as arguments.

## Minimalism and the lambda core

Of the 23 s-expression-based syntactic constructs in the R5RS standard (1998, the most widely implemented), 14 are derived forms, definable as macros on top of nine fundamental forms (`define`, `lambda`, `quote`, `if`, `define-syntax`, `let-syntax`, `letrec-syntax`, `syntax-rules`, `set!`). For example, `let` is a macro that expands to a `lambda` application. The designers later remarked that this minimalism was not planned: "we had accidentally designed something that met all our goals but was much simpler than we had intended."

## Lexical scope and block structure

Earlier Lisps such as Maclisp used dynamic scope, where a free variable, one not bound inside the function itself, resolves to whatever binding is active at call time, producing surprising aliases. Scheme adopted lexical scope, so bindings are determined by program text. Sussman's exposure to ALGOL prompted this choice, and the closure mechanism that makes it work was adapted from Peter J. Landin, via Joel Moses's 1970 description of lexical closures: a function bundled with the environment in which it was defined. Block structure comes from ALGOL too. The binding constructs `let`, `let*`, and `letrec` introduce local bindings; `let*` allows later bindings to refer to earlier ones, while `letrec` enables mutually recursive procedures.

## Proper tail recursion

Scheme requires implementations to optimize tail calls so that an unbounded number of active tail calls runs in constant space, a property called proper tail recursion. Iteration is therefore expressed with tail-recursive procedures, often through the named let, a label bound to a recursive procedure whose arguments are updated on each call, making recursion equivalent in cost to a loop. The built-in `do` loop exists but is less idiomatic.

## First-class continuations

`call-with-current-continuation` (or `call/cc`) captures the current continuation, the remaining computation awaiting a result, as an escape procedure. Invoking it abandons the current path and supplies a value as if the call had returned normally. Continuations enable non-local returns, coroutines, generators, and backtracking.

## Numerical tower

Scheme treats numbers as a tower of types (integer, rational, real, complex), each absorbed into the next. R5RS required only a coherent subset; R6RS (2007) mandated the full tower. Numbers carry an exactness flag: operations on exact numbers yield exact results, and inexactness propagates. `exact?` tests this property.

## Hygienic macros and evaluation

R5RS introduced `syntax-rules`, a hygienic macro system that extends syntax through pattern matching while respecting lexical scope, preventing the variable-capture bugs common in older macro systems. R6RS replaced it with the more expressive `syntax-case`. Scheme does not fix an evaluation order for procedure arguments; the implementation may choose any order, provided the observable effect is sequential. Until R5RS there was no standard `eval`, because lexical scope makes evaluation results depend on the environment. R5RS resolved this with environment-returning procedures and an `eval` that takes an explicit environment.

## Naming, namespaces, and conventions

Unlike Common Lisp, Scheme uses a single namespace for procedures and variables, a "Lisp-1," so the same primitives bind data and functions. In conditionals, only `#f` is false; everything else, including the empty list `'()`, is true. Predicates end in `?`, mutators in `!`, and type converters contain `->`. `eq?` tests pointer identity, `eqv?` adds value-based comparison for numbers and characters, and `equal?` compares structures recursively.

## Standards

Scheme is standardized by the IEEE and through the *Revised n Report on the Algorithmic Language Scheme* (RnRS), a title echoing the ALGOL 60 standard. The widely implemented R5RS appeared in 1998. R6RS (2007) added a module system, Unicode source, libraries, exception handling, and the full numerical tower, but broke with the earlier unanimity tradition and drew criticism for departing from minimalism. In response, R7RS-small (2013) preserves a minimal core while a separate larger language addresses industrial needs.

## Influence

Scheme's ideas shaped Common Lisp, JavaScript, Python, Ruby, Haskell, Clojure, Rust, and Scala. It is used in education through SICP-based courses, including at MIT and Berkeley, and in industry as an embedded scripting language: Guile inside GnuCash and GNU LilyPond, TinyScheme inside GIMP, and Kawa inside Google App Inventor for Android, where it compiles to JVM bytecodes.
