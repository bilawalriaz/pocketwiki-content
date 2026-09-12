# Encapsulation (computer programming)

In software systems, **encapsulation** is the bundling of data with the mechanisms or methods that operate on that data, combined with the limiting of direct access to some of that data, such as an object's components. External code is shielded from the internal workings of an object, and the developer presents a consistent interface that is independent of how the object is implemented internally.

## Two meanings

Programmers use "encapsulation" for two related ideas, sometimes separately and sometimes together:

1. **A language mechanism for restricting direct access** to some of an object's components.
2. **A language construct that bundles data with the methods** (or other functions) that operate on those data.

Some researchers treat the first meaning alone, or combined with the second, as a distinguishing feature of object-oriented programming. Others, working with languages that provide lexical closures (functions that carry their surrounding variables with them), treat encapsulation as orthogonal to object orientation. Under the second meaning, hiding is not automatic and can be overridden, so **information hiding** is treated as a separate notion.

Both features are typically supported using classes in object-oriented languages, though other mechanisms exist. Encapsulation can also describe packaging any repetitive or complex process into a single callable unit, applicable to both object-oriented and procedural programming.

## Why bundle and restrict access

Hiding an object's internals protects its integrity by preventing users from setting internal data into an invalid or inconsistent state. A bounded interface lets the developer limit interdependencies between software components, reducing system complexity and increasing robustness.

Encapsulation also encourages putting all code concerned with a given set of data in the same class, which organises it for easy comprehension by other programmers and promotes **decoupling**, meaning components depend on each other through narrow interfaces rather than internal details.

All object-oriented programming systems support encapsulation, but it is not unique to OOP. Abstract data types, modules, and libraries offer the same property, a similarity that programming language theorists have explained in terms of **existential types** (type-system features that hide an internal type behind an interface).

## Encapsulation and inheritance

The authors of *Design Patterns* discuss a tension between inheritance and encapsulation and argue that designers overuse inheritance. Inheritance exposes a subclass to the details of its parent's implementation, breaking encapsulation. The "yo-yo problem" describes how overusing inheritance produces code that becomes too tangled to debug.

## How languages implement access control

Smalltalk and Ruby allow access only through object methods. Most other languages, including C++, C#, Delphi, and Java, give the programmer explicit control over what is hidden using keywords like `public` and `private`. The ISO C++ standard calls these "access specifiers" and states that they do not "hide any information"; in C++, information hiding is achieved by distributing a compiled version of the code that is interfaced through a **header file**.

Almost every language provides a way to override the protection, usually via a reflection API (a runtime mechanism for inspecting and manipulating objects, available in Ruby, Java, and C#), through name mangling (compiler renaming of symbols so that internal names cannot be called directly, used in Python), or through special keywords such as `friend` in C++. Systems that enforce object-capability security (where every reference is itself a narrowly scoped permission, the object-capability model) are an exception and guarantee strong encapsulation.

## Examples

**Restricting data fields.** In C#, a field can be marked `private` so that outside code cannot reach it directly:

```csharp
public class Account {
    private decimal _accountBalance = 500.00m;
    public decimal CheckBalance() { return _accountBalance; }
}
```

Clients call the public `CheckBalance` method but cannot assign to `_accountBalance`. Java follows the same pattern with `private` fields and public getter methods.

**Encapsulation without OOP.** In C, a structure can be declared opaquely in the header file: clients see only a forward declaration such as `typedef struct Entity Entity;` and call functions like `openEntity`, `processEntity`, and `closeEntity`. The structure's members are defined in the implementation file and remain inaccessible to clients, who interact with values of the opaque data type only through the API.

**Convention over enforcement.** Python does not enforce variable access restrictions, but the convention is that any name prefixed with an underscore is treated as private. Nothing in the language stops an outside caller from writing `redcar._maxspeed = 10`; the convention relies on programmer discipline.

Source: adapted from "Encapsulation (computer programming)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Encapsulation_%28computer_programming%29
