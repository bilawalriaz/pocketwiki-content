# Circuit (computer science)

In theoretical computer science, a circuit is a model of computation in which values flow through a sequence of gates, each of which applies a function to its inputs. Circuits generalise Boolean circuits (the wiring diagrams behind real digital logic) and serve as a mathematical model for digital logic circuits.

## Core definition

A circuit is a triplet `(M, L, G)`:

- **M** is the set of values that can appear at a gate. In a Boolean circuit M = {0, 1}; in an integer circuit M is the family of finite subsets of integers.
- **L** is a set of gate labels. Each label is a function `M^i → M` for some non-negative integer *i*, where *i* is the number of inputs that gate accepts. A gate of in-degree *i* may be labelled by an element of L only if that label is defined on `M^i`.
- **G** is a labelled directed acyclic graph whose vertices are the gates. Because the graph is acyclic, values only flow forward and the computation always terminates.

In a Boolean circuit the gate set is conjunction (AND), disjunction (OR), and negation (NOT). In an integer circuit the gate set includes set union, set intersection, set complement, integer addition, and integer multiplication, all operating on sets of integers.

## Terminology and layout

Gates with in-degree 0 are **inputs** or **leaves**; gates with out-degree 0 are **outputs**. When an edge runs from gate *g* to gate *h*, *h* is a **child** of *g*. Ordering the vertices lets one refer to the *k*th child of a gate.

Standard measurements:

- **Size** of a circuit is its total number of gates.
- **Depth of a gate *g*** is the length of the longest path in *G* that starts at *g* and ends at an output; outputs are the only gates of depth 1.
- **Depth of a circuit** is the maximum depth of any gate, equal to the longest chain of dependent computations.
- **Width** of a levelled circuit is the maximum number of gates at any single level.
- A **levelled circuit** restricts edges so that each gate at depth *i* receives wires only from depth *i*+1 or from the inputs; edges exist only between adjacent levels.

## Evaluating a circuit

The exact value *V(g)* of a gate *g* with in-degree *i* and label *l* is defined recursively:

```
V(g) = l                          if g is an input
        l(V(g_1), ..., V(g_i))      otherwise
```

where each *g_j* is a parent of *g*. The circuit's overall output is the value produced at each output gate.

## Circuits as functions

Treating leaf labels as variables drawn from M turns a circuit with *n* leaves into a function `M^n → M`. It is then natural to consider a **family of circuits** `(C_n)_{n ∈ N}`, an infinite list indexed by input size where *C_n* has *n* variables. Such a family realises a function `M* → M`, mapping every finite string over M to an element of M. Size, depth, and width extend to families by becoming functions of *n*, so that `size(n)` is the gate count of the *n*th circuit in the sequence.

## Computational consequences

Two algorithmic facts anchor the theory:

- Computing the output of a given Boolean circuit on a fixed input is **P-complete**: solvable in polynomial time, and the hardest problem that still stays in polynomial time.
- For an integer circuit, it is **unknown** whether the corresponding evaluation problem is even decidable, that is, whether an algorithm exists that always halts with the correct answer.

**Circuit complexity** classifies Boolean functions by the size or depth of the smallest circuit that computes them. Two extensions beyond Boolean circuits are widely studied: **arithmetic circuit complexity**, which focuses on addition and multiplication over a field, and **quantum circuits**, which use quantum gates and underpin the complexity class BQP (the class of problems efficiently solvable on a quantum computer).
