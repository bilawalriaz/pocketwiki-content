# Design by contract

Design by contract (DbC) is a software design approach in which a software component's behaviour is described by formal, precise, verifiable interface specifications called "contracts". These contracts extend ordinary abstract data type definitions with three pieces: preconditions, postconditions, and invariants. The metaphor comes from business contracts, where a client and supplier each have obligations and benefits.

## The central metaphor

In DbC, a method is a supplier and the code that calls it is the client. The supplier:

- Expects a condition to hold on entry: the precondition, an obligation for the client and a benefit for the supplier, because the method does not handle cases outside the precondition.
- Guarantees a property on exit: the postcondition, an obligation for the supplier and the main benefit for the client.
- Maintains a property assumed on entry and preserved on exit: the class invariant.

The three questions every contract answers are: What does it expect? What does it guarantee? What does it maintain? A contract is semantically equivalent to a Hoare triple, the standard {precondition} program {postcondition} notation from formal verification.

## Trust, verification, and "fail hard"

DbC assumes every client will meet the preconditions required for an operation. Where that assumption is too risky, as in multi-channel or distributed systems, the inverse approach is taken: the server tests that preconditions hold before or during processing and replies with an error if they do not.

A supplier that actively checks contract conditions is practising offensive programming, with the general idea that code should "fail hard" so bugs surface where the contract is broken rather than later as invalid results. This differs from defensive programming, where the supplier figures out what to do when a precondition is broken, usually by throwing an exception; in both cases the client must still respond, but DbC makes the supplier's job easier.

DbC also defines a correctness criterion: if the class invariant and precondition are true before the supplier is called, then the invariant and postcondition will be true after the service completes. A module should never violate a supplier's preconditions when making calls.

## Contracts and inheritance

Subclasses in an inheritance hierarchy may weaken preconditions (but not strengthen them) and strengthen postconditions and invariants (but not weaken them). These rules approximate behavioural subtyping, the property that a subtype can be substituted for its supertype without breaking any contract the supertype offered to its clients.

## How contracts are written

Contracts can be written in code comments, enforced by a test suite, or both, even without special language support. A typical method-level contract documents acceptable and unacceptable inputs and their meanings, return values and their meanings, error and exception conditions, side effects, preconditions, postconditions, invariants, and (more rarely) performance guarantees such as time or space bounds.

DbC considers contracts so central to software correctness that they should be part of the design process; in effect, DbC advocates writing the assertions first. A short C++ example, using the contracts proposal that became part of C++26, illustrates the three pieces:

```
int f(const int x)
  pre(x != 1)                 // precondition
  post(r: r == x && r != 2)   // postcondition; r names the result
{
  contract_assert(x != 3);    // assertion statement
  return x;
}
```

## Performance

Contract conditions should never be violated in a bug-free program, so they are typically checked only in debug mode during development and disabled in release builds. In C and C++, `assert` is compiled away in release mode; C# and Java deactivate assertions similarly, and launching the Python interpreter with `-O` (for "optimise") causes the code generator to emit no bytecode for asserts at all, so the run-time cost of the checks is zero in production.

## Relationship to testing

DbC does not replace unit, integration, or system testing; it complements them with internal self-tests that can be activated for isolated tests and during a test phase in production code. Because these self-tests detect errors before they appear as invalid results at the client, they produce earlier and more specific error detection. The assertions themselves act as a test oracle for the design-by-contract implementation.

## Language support

Native DbC support appears in Ada 2012, SPARK, Ciao, Clojure, Cobra, C++ (since C++26), D, Dafny, Eiffel, Fortress, Kotlin, Mercury, Oxygene, Racket, Sather, Scala, Vala, and the Vienna Development Method. In the Common Lisp Object System, the standard method qualifiers `:before`, `:after`, and `:around` allow contracts to be written as auxiliary methods.

## Origins

The term was coined by Bertrand Meyer in connection with his design of the Eiffel programming language, first described in articles starting in 1986 and in the two editions (1988, 1997) of his book *Object-Oriented Software Construction*. DbC draws on formal verification, formal specification, and Hoare logic. Its original contributions include a clear client/supplier metaphor, a formalism for redefinition and dynamic binding in inheritance, application to exception handling, and the connection with automatic software documentation.
