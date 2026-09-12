# Lisp (programming language)

Lisp is a family of programming languages built around one idea: program code and data share the same structure, so a Lisp program can manipulate other Lisp programs as easily as a list of numbers. John McCarthy specified Lisp in 1958 at MIT; Steve Russell implemented it in 1960 on an IBM 704, making it the second-oldest high-level language still in use after Fortran. The name is short for "List Processor," because its primary data structure is the linked list and its syntax is nothing but nested lists.

## Code as data

Every Lisp expression is written as a parenthesized list called an *S-expression*. The first element names what to do (a function, operator, or special form); the remaining elements are its arguments. So `(f arg1 arg2 arg3)` calls function `f` with three arguments, and `(+ 1 2 3 4)` returns 10. There is no separate statement syntax: every form is an expression that yields a value. This uniform prefix notation produces Lisp's dense forest of parentheses, and it gives the language its power, because the same list structure that represents data can represent code.

This property is called *homoiconicity*: a program's text is a human-readable form of the same internal data structure the interpreter or compiler uses. Lisp exploits this with a macro system far more capable than a C-style text preprocessor. Macros are ordinary Lisp functions that return code, so any list-manipulation tool can build new syntax or entire domain-specific languages embedded inside Lisp.

## Lists, conses, car, and cdr

A Lisp list is a singly linked list of *cons cells*. Each cons holds two pointers called *car* (the head) and *cdr* (the tail, pronounced "could-er"). The names are IBM 704 relics: "Contents of the Address part of Register" and "Contents of the Decrement part of Register." A proper list is either the empty list `nil` or a cons whose car is a datum and whose cdr is another proper list; the convenient notation `(a b c)` abbreviates the chain `(a . (b . (c . nil)))`. Because lists are chains of pointers, two lists can share their tail. Structure sharing is cheap, but a destructive update to one list can silently change another.

The original LISP had two data types, atoms and lists. An atom is a number or a *symbol*, a unique named item usable as a variable or as data. Modern Lisps add vectors, hash tables, and structures, but cons-based lists remain the language's core.

## History

McCarthy designed Lisp in 1958 as a mathematical notation for programs, drawing on Alonzo Church's lambda calculus. His original paper described two notations: *S-expressions* for data and code, and a more Algol-like *M-expression* syntax for functions. Programmers immediately preferred S-expressions, and M-expressions were abandoned. Steve Russell read the paper, realized that McCarthy's `eval` function could run as machine code, and built the first Lisp interpreter on the IBM 704, an act McCarthy called "confusing theory with practice." McCarthy published the design in *Communications of the ACM* in 1960. Tim Hart and Mike Levin wrote the first self-hosting Lisp compiler at MIT in 1962, introducing incremental compilation that mixes compiled and interpreted functions. Daniel Edwards developed garbage collection for Lisp before 1962.

Through the 1970s, Lisp was the standard tool of artificial intelligence research, especially on DEC PDP-10 systems. The 1980s and 1990s consolidated diverging dialects (Maclisp, ZetaLisp, NIL, Spice Lisp, with Scheme influences) into Common Lisp, standardized by ANSI in 1994. Scheme, designed by Guy Steele and Gerald Jay Sussman at MIT in 1975, took a minimalist path emphasizing lexical scoping, tail-call optimization, and clear semantics. Clojure, created in the 2000s, targets the Java Virtual Machine, emphasizes immutability, and is not backwards compatible with other Lisps. After a dip during the "AI winter" of the 1990s, Lisp revived in the 2000s and 2010s around Common Lisp, Scheme, Emacs Lisp, Clojure, and Racket.

## Innovations

Lisp was the first language with several now-mainstream features: conditionals in their modern `if-then-else` form (McCarthy's `cond`), first-class and higher-order functions, recursion as the primary control structure, automatic garbage collection, dynamic typing with strong runtime guarantees, a symbol data type distinct from strings, programs composed entirely of expressions with no statement class, code represented directly as a standard data structure (homoiconicity) enabling macros and a self-hosting compiler, and the read-eval-print loop (REPL) as an interactive command line, typically `(loop (print (eval (read))))`.

The Common Lisp Object System (CLOS), part of ANSI Common Lisp since 1994, was the first standardized object-oriented language. It supports multiple inheritance, multimethods with multiple dispatch, and a metaobject protocol that lets programs redefine the object system itself.

## Evaluation and control flow

Lisp evaluates expressions eagerly. Common Lisp evaluates arguments in applicative (leftmost-innermost) order; Scheme leaves order unspecified for compiler optimization. Quoting with `'` (short for the `quote` special operator) returns its argument unevaluated, so `'foo` is the literal symbol. A backquote introduces a quasiquoted template where commas evaluate and interpolate sub-expressions and `,@` splices a list, the standard tool for writing macro expansions.

Scheme requires proper tail-call optimization, so tail-recursive functions run in constant stack space. Common Lisp does not require it and offers imperative-style constructs like `loop`, `do`, and `dolist`. Both dialects expose higher-order functions such as `map` (Scheme) and `mapcar` (Common Lisp). Destructive updates like `set-car!` in Scheme, marked with a "bang," or `rplaca` in Common Lisp mutate cons cells in place, and modifying a quoted literal is undefined behavior in ANSI Common Lisp because the compiler may place such constants in write-protected memory.

A recursive factorial in Common Lisp:

```lisp
(defun factorial (n)
  (if (zerop n) 1 (* n (factorial (1- n)))))
```

## Influence

Lisp influenced an unusually broad set of later languages, including JavaScript, Python, Ruby, Perl, Lua, Haskell, ML, Scala, Julia, Swift, Smalltalk, R, Dylan, Forth, Elixir, and the Wolfram Language. Alan Kay, who led Smalltalk's development, considered Lisp and Smalltalk the only two languages truly conceived around object-oriented principles, because of their late binding and reflective metaclass systems. MIT replaced Scheme with Python in its introductory computer science curriculum and its MITx MOOC.

Source: adapted from "Lisp (programming language)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Lisp_%28programming_language%29
