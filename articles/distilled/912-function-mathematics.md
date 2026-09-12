# Function (mathematics)

## Overview

A function is a mathematical rule that assigns to each element of a set (the domain) exactly one element of another set (the codomain). Functions model dependency relations—such as how a planet's position depends on time—and are central to virtually all areas of mathematics, science, and engineering. The concept evolved from informal use in ancient and early modern mathematics to a rigorous set-theoretic definition in the late 19th century, enabling precise treatment of arbitrary domains and codomains.

## Timeline

- **Ancient–17th century** — Informal use of functional dependence in mathematics and astronomy
- **Late 17th century** — Functions elaborated with the invention of infinitesimal calculus (Leibniz, Newton, Euler)
- **1734** — Euler introduces functional notation \( f(x) \)
- **Until 19th century** — Only differentiable functions considered; high regularity assumed
- **Late 19th century** — Formal set-theoretic definition of a function as a functional relation
- **Early 20th century** — Bourbaki group coins terms "injective," "surjective," "bijective"

## Body

### Definition and Formalization

A function \( f: X \to Y \) assigns to each element \( x \in X \) (the domain) exactly one element \( y \in Y \) (the codomain), written \( y = f(x) \). The set of all such pairs \( (x, f(x)) \) is the graph of the function. Before the 19th century, functions were understood informally, often as differentiable expressions. The formal definition emerged in set theory: a function is a binary relation \( R \subseteq X \times Y \) such that for every \( x \in X \), there exists a unique \( y \in Y \) with \( (x, y) \in R \). This formalization allowed functions with arbitrary domains and codomains, greatly expanding their applicability.

### Partial Functions

A partial function from \( X \) to \( Y \) relaxes the requirement that every element of \( X \) must be assigned a value; it only requires that each \( x \in X \) maps to at most one \( y \in Y \). The domain of definition is the subset of \( X \) where the function is actually defined. In calculus and complex analysis, "function" often refers to partial functions, especially when determining the domain is difficult. For example, the multiplicative inverse \( x \mapsto 1/f(x) \) requires knowing the zeros of \( f \). In computability theory, general recursive functions are partial functions from integers to integers whose values are computable by an algorithm; their domain of definition is the set of inputs for which the algorithm halts.

### Multivariate Functions

A multivariate function (or function of several variables) depends on multiple arguments and has a domain that is a set of \( n \)-tuples, often a Cartesian product \( X_1 \times \cdots \times X_n \). For instance, multiplication of integers is a bivariate function with domain \( \mathbb{Z} \times \mathbb{Z} \). When all input sets are \( \mathbb{R} \) or \( \mathbb{C} \), one speaks of functions of several real or complex variables. These are commonly written as \( f(x_1, \ldots, x_n) \), omitting parentheses around the tuple.

### Notation

Functions are denoted in several standard ways. Functional notation \( f(x) \), introduced by Euler in 1734, names the function and its argument. Arrow notation \( x \mapsto f(x) \) defines a function inline without naming it, useful for specifying rules or partially applied functions. Index notation \( f_x \) is used for sequences (functions on natural numbers) or to distinguish parameters from variables. Placeholder notation, such as \( a(\cdot)^2 \), represents a function without naming the variable. Specialized notations exist in linear algebra (dual pairs), logic (lambda calculus), and category theory (commutative diagrams).

### Specifying Functions

Functions can be specified by listing values (on finite domains), by formulas (e.g., polynomial, rational, algebraic, or elementary functions), by recurrence (e.g., the factorial \( n! = n(n-1)! \)), by differential equations (e.g., the exponential function as its own derivative), or by power series (e.g., \( e^x = \sum_{n=0}^\infty x^n/n! \)). The domain of a function defined by a formula may require excluding values where operations like division by zero or square roots of negative numbers occur.

### Representing Functions

Functions are commonly represented by graphs—the set \( \{(x, f(x)) \mid x \in X\} \)—which, when \( X \) and \( Y \) are subsets of \( \mathbb{R} \), correspond to points in the Cartesian plane. Tables of values are used for discrete or sampled data, and bar charts represent functions on finite or countable domains.

### General Properties

Key properties include:

- **Composition**: Given \( f: X \to Y \) and \( g: Y \to Z \), the composition \( g \circ f: X \to Z \) is defined by \( (g \circ f)(x) = g(f(x)) \). Composition is associative but not commutative.
- **Image and preimage**: The image \( f(A) \) of a subset \( A \subseteq X \) is \( \{f(x) \mid x \in A\} \). The preimage \( f^{-1}(B) \) of \( B \subseteq Y \) is \( \{x \in X \mid f(x) \in B\} \).
- **Injective, surjective, bijective**: A function is injective (one-to-one) if distinct inputs yield distinct outputs; surjective (onto) if every element of the codomain is mapped to by some element of the domain; bijective if both. Bijective functions have inverse functions.
- **Restriction and extension**: Restricting a function to a subset of its domain can yield an injective function, enabling the definition of inverse functions (e.g., arccosine via restricting cosine to \([0, \pi]\)). Extensions enlarge the domain, as in analytic continuation.

### Function Spaces and Multi-valued Functions

In analysis, a function space is a set of functions sharing a property (e.g., continuous, smooth, compactly supported) that forms a topological vector space. These are essential for studying differential equations and distributions. Multi-valued functions arise when extending functions by continuity or analytic continuation, particularly in complex analysis. For example, the square root has two values for positive reals, and complex functions like the logarithm exhibit monodromy—values "jump" when looping around singularities. These are resolved by branch cuts (principal values) or by treating them as multi-valued functions.

### Foundations and Computer Science

In set theory, functions require domains and codomains to be sets; however, some constructions (e.g., the singleton map \( x \mapsto \{x\} \)) require classes, as in von Neumann–Bernays–Gödel set theory. In type theory, functions are primitive, constructed via lambda calculus. In computer science, functions are subroutines implementing mathematical functions; functional programming uses pure functions with no side effects. Computability theory studies models like general recursive functions, lambda calculus, and Turing machines, all defining the same class of computable functions, as asserted by the Church–Turing thesis.

## Terms

- **Domain**: The set of inputs to which a function assigns values.
- **Codomain**: The set containing all possible outputs of a function.
- **Image (range)**: The set of all outputs actually produced by a function.
- **Graph of a function**: The set of all ordered pairs \( (x, f(x)) \).
- **Injective (one-to-one)**: A function where distinct inputs produce distinct outputs.
- **Surjective (onto)**: A function whose image equals its codomain.
- **Bijective**: A function that is both injective and surjective; has an inverse.
- **Partial function**: A function that may not be defined on all elements of its domain.
- **Composition**: Applying one function to the results of another: \( (g \circ f)(x) = g(f(x)) \).
- **Monodromy**: The phenomenon where a multi-valued function's value changes after looping around a singularity.

## Debates and Open Questions

- **Axiom of choice**: The equivalence between surjectivity and the existence of a right inverse depends on the axiom of choice, a foundational assumption debated in set theory.
- **Church–Turing thesis**: While not formally provable, it remains a central philosophical claim about the nature of computability, with ongoing debate about whether alternative models (e.g., quantum computing) might extend the notion of effective computability.
- **Foundational frameworks**: Whether functions should be defined within set theory, type theory, or category theory reflects deeper philosophical disagreements about the foundations of mathematics.

Source: adapted from "Function (mathematics)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Function_%28mathematics%29
