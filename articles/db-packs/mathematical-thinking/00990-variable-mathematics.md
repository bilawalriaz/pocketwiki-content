# Variable (mathematics)

A variable in mathematics is a symbol, usually a letter, that stands for an unspecified mathematical object: a number, function, set, vector, matrix, or space. Variables let one write a general relationship, an unknown to be solved, or a parameter that changes between problems, all in a single expression. In mathematical logic, a variable is a symbol that either represents an unspecified constant of the theory or is being quantified over. The same symbol can serve as both a variable and a constant: π, e, and 1 look variable in form but are fixed in value.

## A short history of the idea

Algebra began without symbols. The Moscow Mathematical Papyrus (c. 1500 BC) posed "Aha problems" asking for an unknown from relations between it and its parts, but the unknown was described in words. Old Babylonian mathematics (c. 2000–1500 BC) solved quadratic and cubic equations the same rhetorical way. Euclid's *Elements* (c. 300 BC) treated algebraic identities, including the distributive property, as geometric facts about rectangles and line segments. Diophantus of Alexandria (c. 200 AD) introduced syncopated algebra in his *Arithmetica*, mixing symbols for unknowns and powers with words, though he still lacked modern signs for equality and exponents. In seventh-century India, Brahmagupta distinguished unknowns from one another using different colours of ink.

The decisive change came in the late 16th century, when François Viète began using letters for both known and unknown numbers, with consonants for knowns and vowels for unknowns. In 1637 René Descartes fixed the convention still in use: x, y, z for unknowns and a, b, c for knowns. The development of calculus by Newton and Leibniz in the 1660s required variables representing quantities changing over time and their rates of change. By the late 19th century, Karl Weierstrass replaced the image of a "varying" quantity with a static, quantifier-based definition of a limit, so a variable became a symbol denoting a mathematical object rather than a thing that moves.

## Notation and conventions

Variables are usually single letters from the Latin or Greek alphabets, often with subscripts for indexing (x₁, x₂, x₃). Letters early in the alphabet (a, b, c) typically denote parameters or coefficients, while letters near the end (x, y, z) denote unknowns or function arguments. In print, variables and constants are italicised to set them apart from surrounding text. Different fields layer further conventions on this base: physics chooses names tied to the physical quantity being modelled, while probability and statistics use capitals (X, Y, Z) for random variables and lower-case (x, y, z) for the values they take in a specific outcome.

## Kinds of variables

The same letter can play several different roles, and the role, not the letter, is what gives a symbol its meaning.

| Role | What it does | Example |
|------|--------------|---------|
| Unknown | A value to be solved for from an equation | x in x + 3 = 7 |
| Parameter | Fixed during one problem, can change between problems | a, b, c in ax² + bx + c |
| Indeterminate | A formal symbol in a polynomial or power series, constant in the polynomial ring but used as a variable | x in the polynomial ring ℝ[x] |
| Dependent variable | A value determined by one or more other variables | y in y = f(x) |
| Independent variable | A variable free to take values, with others depending on it | x in y = f(x) |
| Free variable | A variable not bound by a quantifier or index | x in x + 1 |
| Bound variable | A variable introduced by a quantifier or index | i in Σᵢ₌₁ⁿ i |
| Random variable | A mapping from outcomes of a random process to numbers | X, the result of a die roll |

An indeterminate causes a common confusion: in a polynomial ring such as ℝ[x], the symbol x is technically a constant of that ring, yet it is used as a variable whenever the ring is interpreted as functions, so the same object wears both hats.

## Dependent and independent variables

In calculus and the applied sciences, variables are often linked by a function. If y = f(x), then x is the independent variable and y is the dependent one. In a physical system, pressure, volume, and temperature are all functions of time, so each is a dependent variable with respect to t.

The label "dependent" or "independent" is contextual, not a fixed property of the symbol. In f(x, y, z), all three arguments can be treated as independent, or y and z can depend on x. The ideal gas law, PV = NkBT, makes this concrete: solving for V puts V in the dependent role, while solving for T puts T there instead.

## Moduli spaces

When a family of objects is described by parameters, those parameters can themselves be treated as variables, and the set of all possible parameter values becomes a space. The quadratic y = ax² + bx + c is the family of all parabolas, each picked out by a triple (a, b, c). Letting a, b, and c vary turns the set of parabolas into a three-dimensional moduli space in which each point is one parabola. Letting the constants of one problem become the variables of a larger one is one of the main ways modern mathematics links algebra to geometry and produces new objects from old ones.
