# Function (mathematics)

A function is a rule that assigns to each input from a set called the *domain* exactly one output from a set called the *codomain*. Written \(f: X \to Y\), it sends every element \(x \in X\) to a unique element \(y = f(x) \in Y\); the uniqueness means the answer to "what is \(f(3)\)?" is always a single value, never several. The collection of all input–output pairs \(\{(x, f(x)) \mid x \in X\}\) is the *graph* of the function. The codomain is the set of allowed outputs; the actual outputs that appear, called the *image* or *range*, may be a proper subset of the codomain.

This single rule captures dependency: the position of a planet as a function of time, the cost of an item as a function of quantity purchased, the result of an algorithm as a function of its input.

## Set-theoretic definition

The rigorous modern definition, codified in the late 19th century, treats a function as a special kind of binary relation. A relation \(R \subseteq X \times Y\) is a function when, for every \(x \in X\), there exists exactly one \(y \in Y\) with \((x, y) \in R\). This freed functions from the earlier assumption that they had to be given by smooth formulas, allowing arbitrary, possibly pathological mappings that do not arise from any classical expression.

## Variations

A **partial function** relaxes the requirement that every input be assigned a value: each \(x \in X\) maps to at most one \(y \in Y\), and the subset where values are defined is the *domain of definition*. In computability theory, general recursive functions are partial functions from the integers to themselves whose defined values are exactly those an algorithm halts on.

A **multivariate function** takes several arguments, with domain a Cartesian product \(X_1 \times \cdots \times X_n\) such as \(\mathbb{R} \times \mathbb{R}\). It is written \(f(x_1, \ldots, x_n)\).

## Notation

Common notations include \(f(x)\) (functional notation, introduced by Euler in 1734), \(x \mapsto f(x)\) (arrow notation, which defines a function inline without naming it), and \(f_x\) (index notation, used for sequences, which are functions on the natural numbers).

Functions are specified by listing values on finite domains, by formulas (polynomials, rational functions, exponentials), by recurrences such as \(n! = n \cdot (n-1)!\), by differential equations such as the exponential being its own derivative, or by power series such as \(e^x = \sum_{n=0}^{\infty} x^n / n!\). When a formula involves division or roots, the domain excludes points where the formula breaks down, such as the zeros of a denominator.

## Key properties

**Composition.** Given \(f: X \to Y\) and \(g: Y \to Z\), the composition \(g \circ f: X \to Z\) is defined by \((g \circ f)(x) = g(f(x))\). Composition is associative, so the order of grouping does not matter, but not commutative, since \(g(f(x))\) and \(f(g(x))\) are generally different or undefined.

**Image and preimage.** For a subset \(A \subseteq X\), the image \(f(A) = \{f(x) \mid x \in A\}\). For \(B \subseteq Y\), the preimage \(f^{-1}(B) = \{x \in X \mid f(x) \in B\}\).

**Injective, surjective, bijective.** A function is *injective* (one-to-one) if distinct inputs produce distinct outputs, so \(f(x_1) = f(x_2)\) forces \(x_1 = x_2\). It is *surjective* (onto) if every element of the codomain is hit, meaning the image equals the codomain. It is *bijective* if both, and only bijective functions have inverses.

**Restriction and extension.** Restricting a function to a suitable subset of its domain can make it injective, which is how standard inverse functions are built: arccosine is cosine restricted to \([0, \pi]\). Extension goes the other way, enlarging the domain, as in analytic continuation.

## Multi-valued functions

The square root of a positive real and the complex logarithm seem to have several outputs. The complex logarithm exhibits monodromy: its value shifts when one loops continuously around a singularity. Such cases are handled by choosing a principal value, enforced with a branch cut that rules out one route, or by treating the object as a genuinely multi-valued function.

A *function space* in analysis is a set of functions sharing a property such as continuity or smoothness; equipped with a topology, it becomes the natural setting for studying differential equations and distributions.

## Foundations

In ordinary set theory the domain and codomain of a function must be sets, but a few natural constructions, such as the map \(x \mapsto \{x\}\) that sends every set to the singleton containing it, require the larger collection called a class, as in von Neumann–Bernays–Gödel set theory. In type theory and in lambda calculus, functions are taken as primitive rather than built from relations, which is also the basis of functional programming in computer science. Computability theory studies several models, including general recursive functions, lambda calculus, and Turing machines, all of which define the same class of computable functions; this equivalence is the content of the Church–Turing thesis, a non-provable but central claim that these models capture exactly what can be computed effectively, with open questions about whether quantum computation extends the class. The equivalence of surjectivity with the existence of a right inverse itself depends on the axiom of choice.

Source: adapted from "Function (mathematics)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Function_%28mathematics%29
