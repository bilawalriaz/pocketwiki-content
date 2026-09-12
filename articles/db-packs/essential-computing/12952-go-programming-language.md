# Go! (programming language)

Go! is an agent-based programming language in the Prolog tradition of logic-based programming. Francis McCabe and Keith Clark introduced it in a 2003 paper, and the last public preview was released on 30 September 2007. It runs on Unix-like systems, is distributed under the GPLv2 licence, and is influenced by Prolog. It must be distinguished from Google's unrelated "Go" language, released in November 2009.

## What kind of language it is

The designers describe Go! as multi-paradigm and aimed at "secure, production quality and agent-based applications." It combines concurrent, logic, functional, imperative, and object-based styles. It is strongly typed, so every value has a fixed type checked by the compiler, and higher-order in the functional sense, so functions can be passed to and returned from other functions.

An agent is an autonomous process that runs its own threads. Threads execute action procedures, calling functions and querying relations as needed. Threads in different agents communicate by sending asynchronous messages, where the sender does not wait for a reply. Threads within the same agent share Linda-style tuple stores, which are shared memory spaces that hold tuples addressed by content rather than by location.

The authors also argue Go! is well suited to representing ontologies. An ontology is a formal specification of the entities in a domain and the relations between them. By integrating logic, functional, and imperative styles, Go! lets an ontology be expressed directly as code.

## The declaration style

Go! uses a short syntax for declaring data and interfaces. A type declared with `::=` is an algebraic data type, whose only members are built from a fixed set of constructors. For example:

```
Sex ::= male | female.
```

declares that a `Sex` is either `male` or `female` and nothing else.

An interface declared with `<~` lists the properties an object must expose. A `person` interface, for instance, specifies that `dayOfBirth` is a function returning a `day`, `age` is a function returning an integer, `sex` returns a `Sex`, `name` returns a string, `home` returns a string, and `lives` is a relation over strings, so it can hold several string values rather than just one.

A `$=` declaration gives a theory label, with the functor `person`, that defines how to construct a concrete person from four parameters: a name of type `string`, a birthday of type `day`, a sex of type `Sex`, and a home of type `string`. The `newPerson` action procedure packages those four values into a new person. This split between interface, theory, and constructor is what the authors call "ontology-oriented" programming.

## Conflict with Google

In November 2009, Google released its own language called Go. McCabe objected that Google was "steam-rolling over us" and asked them to rename it. Technology news sites picked up the dispute, and several called Go! "obscure." A Google developer closed the public thread on 12 October 2010 with the custom status "Unfortunate," commenting that in the eleven months since Google's release there had been minimal confusion between the two languages.

Source: adapted from "Go! (programming language)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Go%21_%28programming_language%29
