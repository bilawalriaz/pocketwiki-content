# Eiffel (programming language)

Eiffel is an object-oriented programming language designed by Bertrand Meyer, conceived in 1985 and first released in 1986 to make commercial software more reliable. It is built around a small set of principles that shape both the language and the way programs are written, most importantly *design by contract*, in which every routine states what must be true before it runs and what it guarantees afterwards.

## Design principles

Six principles drive Eiffel. **Design by contract** (DbC) attaches executable preconditions, postconditions, and class invariants to routines, turning assumptions into checkable code. **Command–query separation** says a routine either returns information (a query) or changes state (a command), never both. The **uniform-access principle** lets callers write `a_vehicle.speed` whether `speed` is a stored field or a computed function. The **single-choice principle** discourages repeated `if` branches for the same condition, the **open–closed principle** favors extending classes rather than modifying them, and **option–operand separation** keeps configuration out of argument lists. These rules push Eiffel toward declarative, readable code rather than clever tricks.

## How a program is organised

A program is a collection of classes grouped into clusters (directories). Every class defines *features* (the Eiffel term for methods, attributes, or routines), and standard types like `INTEGER` and `STRING` are themselves classes, so a uniform type system handles values and references alike. Each system has one *root* class whose *root procedure* starts execution. Eiffel has only five executable statement kinds: assignment, object creation, routine call, condition, and iteration. Every block has exactly one entry and one exit, a strict structured-programming rule.

## Scoping, contracts, and void safety

Eiffel forbids direct assignment to another object's attributes. All attributes are private, and changes go through setter procedures, which is how class invariants are preserved. Visibility is controlled statically by `export` clauses, for example `feature {NONE}` for internal use; there are no `public`/`private` keywords. Void safety, an extension of the type system using `attached` and `detachable` declarations, lets the compiler guarantee statically that a reference is non-null at the point of use. Under inheritance, preconditions may only be weakened, postconditions only strengthened, and invariants must still hold.

## Genericity, inheritance, and deferred classes

Classes can be generic: `LIST [G]` is a list of any type `G`, and `HASH_TABLE [G, KEY -> HASHABLE]` constrains the key type to a descendant of `HASHABLE`. Eiffel supports multiple inheritance with explicit `rename` and `redefine` clauses to avoid name clashes, and disallows argument overloading within a class so each name has exactly one meaning. A class declared `deferred class`, or one containing `deferred` features, cannot be instantiated; concrete descendants supply the missing routines. The mechanism serves a role similar to Java interfaces, made workable because Eiffel already has multiple inheritance.

## Agents, once routines, conversions, and exceptions

An *agent* wraps a routine as an object so it can be passed around, for iteration (`my_list.do_all (agent my_action)`) or filtering (`do_if`). Arguments marked `?` are *open* (supplied when the agent is called), while others are *closed*, mirroring bound and free variables in lambda calculus. A routine declared with `once` instead of `do` runs its body only on the first call and returns the cached result thereafter, a decentralised alternative to the singleton pattern; by default it runs once per thread, configurable to once per process or per object. *Conversions* let one type be assigned to another (for example `INTEGER` to `REAL`, or a `DATE` to a `STRING`) without inheritance, on the condition that no type both converts to and conforms to another. Exceptions, handled with `rescue` and `retry`, are reserved for contract violations, not ordinary control flow.

## Syntax, operators, and conventions

Eiffel uses Pascal-style keywords but separator-free syntax: semicolons are optional, comments start with `--`, and the language is case-insensitive, though style conventions prescribe ALL-CAPS class names, lower-case feature names, and underscore-separated identifiers like `average_temperature`. Every operation is conceptually a call on a target, so `a + b` is `a.plus (b)`. Eiffel allows custom infix and prefix *alias* operators, a class-wide `[]` bracket operator, and *assigner commands* that let `phone_book ["JILL SMITH"] := New_person` call a setter without breaking information hiding. A standard "Hello, world!" program is a single class:

```
class HELLO_WORLD
create make
feature
   make
      do print ("Hello, world!%N")
      end
end
```

## Implementations, standards, and influence

EiffelStudio is the main IDE, compiling to C, .NET CIL, or running directly. Other implementations include LibertyEiffel, SmartEiffel, Visual Eiffel, Gobo Eiffel, and "The Eiffel Compiler" tecomp. The language became an ISO standard in 2005 through ECMA-367, with a second edition in 2006, though some implementations, notably SmartEiffel, diverged from the standard. Many ideas first introduced in Eiffel were later adopted by Java, C#, D, Ruby, Scala, and Sather, and Eiffel itself was influenced by Ada, Simula, and Z. SCOOP (Simple Concurrent Object-Oriented Programming) provides a contract-based concurrency model available in EiffelStudio but not yet part of the official standard.
