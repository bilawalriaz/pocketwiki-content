# B (programming language)

B is a programming language created around 1969 at Bell Labs by Ken Thompson, with Dennis Ritchie joining maintenance soon after. It was built for recursive, non-numeric, machine-independent work such as system and language software, and it is the immediate ancestor of C.

## One type, many meanings

B's central design choice is that it is typeless, with exactly one data type: the machine's natural memory word. Depending on context, the same word is treated as an integer or as a memory address to be dereferenced. On word-oriented machines such as the DEC PDP-7 or the Honeywell GE 645, this was a natural fit. On the byte-addressable PDP-11, which arrived at Bell Labs and exposed ASCII character data packed inside words, the design became a friction point: there was no clean way to express a character as distinct from an integer.

That PDP-11 problem is what drove B out of use. Starting in 1971, Ritchie added data typing for variables while rewriting the compiler to emit machine code. B passed through "New B" (NB) during 1971–1972 and emerged as C. In Thompson's own framing, "B and the old old C were very very similar languages except for all the types."

## Origins and lineage

Thompson began B as a Fortran compiler for the PDP-7, but the first version exceeded available memory. Iterating to shrink the compiler, he extracted a subset of BCPL semantics and gave them a new syntax. The name "B" has been explained as short for BCPL or for Bon, another Thompson language, but Thompson confirmed neither story. He described the result as "BCPL semantics with a lot of SMALGOL syntax." B's ancestors were Fortran, BCPL, PL/I, and TMG; its direct descendant was C.

## Mechanics that survived

Two B features passed into C and beyond.

- **Two-address assignment operators**, written `x =+ y` rather than C's `+=`. The form came from Douglas McIlroy's implementation of TMG, where B's compiler was first written, and traces back to ALGOL 68's `x +:= y`.
- **`++` and `--`** increment and decrement operators, with prefix and postfix forms that determine whether the value is read before or after the operand changes. These were absent from the earliest B. A common myth holds that they exploited PDP-11 auto-increment address modes, but the PDP-11 postdates B's creation, so this is historically impossible.

B also had a generalized `for` loop, later carried into C, that Thompson adapted from earlier work by Stephen Johnson, plus a small library that loosely resembled C's standard I/O.

## Implementations and survival

Early B ran on the PDP-7 and PDP-11 under early Unix, and on Honeywell GE 645 36-bit mainframes running GCOS. The PDP-7 build compiled to threaded code, while Ritchie wrote a TMG-based compiler that produced machine code. When a PDP-11 arrived in 1970, an assembler, `dc`, and B itself were all written in B to bootstrap the machine, and an early `yacc` was produced in this setup.

B is now nearly extinct, displaced by C. It still sees use on GCOS mainframes and on some embedded systems, where limited hardware, existing libraries, tooling, and licensing considerations keep it in service. The multiplayer game AberMUD was originally written in B.

## Reading a B program

A short routine from Thompson's *Users' Reference to B* illustrates the language's character:

```c
printn(n, b) {
    extrn putchar;
    auto a;
    if (a = n / b)
        printn(a, b);
    putchar(n % b + '0');
}
```

`printn` recursively prints a non-negative number `n` in any base `b` from 2 to 10, relying on the fact that ASCII `'0'` through `'9'` have sequential code values. Note `if (a = n / b)`, where a single `=` assigns and yields the value rather than testing equality, the role `==` plays in C.
