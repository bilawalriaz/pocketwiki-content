# Calculus

Calculus is the mathematics of continuous change. It splits into two interlocking halves. Differential calculus measures how fast something is changing at a single instant, encoding the slope of a curve at a point. Integral calculus accumulates continuous quantities, recovering the total area under a curve, the total distance from a velocity, or any quantity built by summing infinitely many small pieces. The two halves are connected by the fundamental theorem of calculus, which says that differentiation and integration are inverse operations: undoing one gives the other. This single relationship is why calculus works. Everything from physics to economics uses calculus because real systems change continuously, and continuous change is what calculus was built to describe.

## The Two Branches

A derivative is a precise version of slope. For a function f at a point a, the derivative is the limit of the difference quotient:

$$f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}.$$

Geometrically, it gives the slope of the tangent line at that point. When the input represents time, the derivative is the instantaneous rate of change. Position's derivative is velocity; velocity's derivative is acceleration. Two notations coexist: Lagrange's f′ and Leibniz's dy/dx.

An integral comes in two forms. An indefinite integral, or antiderivative, is a function whose derivative equals a given function, written ∫f(x)dx = F(x) + C. The constant C appears because any two functions differing by a constant share the same derivative. A definite integral, written ∫ₐᵇ f(x)dx, computes the signed area between a curve and the x-axis from a to b. It is defined as the limit of Riemann sums, which approximate the area by summing thin rectangles of width h and height f(xᵢ). The elongated S in the integral symbol suggests summation, and dx names the variable of integration.

## The Fundamental Theorem

The fundamental theorem states that if f is continuous on [a, b] and F is any antiderivative of f, then

$$\int_a^b f(x)\,dx = F(b) - F(a).$$

The derivative of an integral recovers the original function: d/dx ∫ₐˣ f(t)dt = f(x). Together these let you compute areas by finding antiderivatives instead of evaluating limits of sums, turning integration into a routine algebraic task rather than a hard geometric estimate. The theorem also serves as a prototype for solving differential equations, since it shows that dy/dx = f(x) reduces to finding an antiderivative.

## Foundations: Limits and Infinitesimals

Newton and Leibniz originally formulated calculus using infinitesimals, quantities treated as real numbers but infinitely small, greater than zero yet smaller than any positive real. This made the subject powerful but imprecise, drawing criticism such as Berkeley's 1734 mockery of "ghosts of departed quantities." In the 19th century, Cauchy and Weierstrass replaced infinitesimals with the epsilon-delta definition of limits, which describes a function's behavior at an input through its values at nearby inputs using only the structure of the real numbers. Limits became the standard rigorous foundation. In the 1960s, Abraham Robinson revived infinitesimals rigorously through non-standard analysis, working with hyperreal numbers that contain infinitely small and infinitely large elements; smooth infinitesimal analysis offers another alternative based on category theory. All three frameworks produce the same theorems, differing only in language.

## Brief History

Calculus grew from older methods for measuring curved areas and volumes. Eudoxus in 4th-century BC Greece developed the method of exhaustion, a rigorous way to compute areas by bounding them between inscribed and circumscribed polygons, and Archimedes used indivisibles and exhaustion in the 3rd century BC to solve problems later treated as integral calculus. Liu Hui independently discovered exhaustion in 3rd-century China, and Kepler's 1615 *Stereometria Doliorum* formed a basis for integral calculus. Modern calculus emerged in 1665–1666 when Newton developed his method of fluxions, and independently in 1684 when Leibniz published "Nova Methodus pro Maximis et Minimis." A priority dispute over who first invented calculus divided English and continental European mathematicians for years; how much Leibniz drew from Isaac Barrow, Newton's teacher, remains hard to determine.

## Extensions

Multivariable and vector calculus extend these ideas to functions of several variables and to vector fields in three-dimensional space, underpinning differential geometry and partial differential equations. Differential equations relate unknown functions to their derivatives, modeling everything from planetary orbits to electrical circuits. Real analysis provides the rigorous foundations on which calculus rests, while complex analysis studies functions of complex variables, where differentiability is a much stronger condition but produces holomorphic functions that are automatically infinitely differentiable. The calculus of variations handles optimization over whole functions, using the Euler–Lagrange equation to find the function that minimizes a given quantity, the same machinery that underlies Lagrangian mechanics.

Source: adapted from "Calculus" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Calculus
