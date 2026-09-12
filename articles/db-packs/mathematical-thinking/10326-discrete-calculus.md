# Discrete calculus

Discrete calculus studies change one step at a time, the way geometry studies shape and algebra studies arithmetic. Where ordinary calculus examines smooth, continuous change, discrete calculus examines incremental change across a fixed step Δx = h > 0, measured between neighbouring points a, a+h, a+2h, ... on the real line. Letting h shrink to zero recovers infinitesimal calculus.

Like its continuous cousin, discrete calculus splits into two parts that turn out to be inverses of each other.

## The difference quotient

Discrete differential calculus studies the difference quotient, the discrete analogue of the derivative. Given f defined on points spaced by h, the difference quotient lives on the midpoints of the intervals and encodes how f changes from one point to the next:

Δf/Δx (x + h/2) = (f(x+h) − f(x)) / h.

It is a linear operator: input a function, output a new function whose values are those slopes. Applied to the squaring function f(x) = x², expanding (x+h)² − x² and dividing by h gives Δf/Δx = 2x + h, close to the doubling function 2x; the extra h is the discrete correction that disappears in the limit. The second difference quotient is the difference quotient applied again, the discrete analogue of the second derivative.

## The Riemann sum

Discrete integral calculus studies Riemann sums, the discrete analogue of the integral. Divide [a, b] into n equal segments of width h, evaluate f at each midpoint, and add the rectangles:

∑ᵢ₌₀ⁿ⁻¹ f(a + ih + h/2) · Δx.

Geometrically, this is the area under a piece-wise constant curve. If f is speed measured at successive instants and Δx is the time step, each term is distance covered in that step, and the total is the distance travelled. The sum is again a linear operator.

## The fundamental theorem

The fundamental theorem of discrete calculus states that for a partition of [a, b] with b = a + nh,

∑ᵢ₌₀ⁿ⁻¹ f(a + ih + h/2) · Δx = F(b) − F(a),

provided ΔF/Δx = f. Summing the difference quotients of F across the partition gives the net change of F from one end to the other, the discrete analogue of "the integral of the derivative is the original function." This identity is also a prototype solution of a difference equation, the discrete counterpart of a differential equation.

## From intervals to graphs and manifolds

The same two operations extend beyond a line. On a graph, f lives on nodes and its exterior derivative df lives on edges, with df([a, b]) = f(b) − f(a); the integral of a 1-cochain g over a path σ is the sum of g's values on the edges of σ. Integrating df along any path from a₀ to aₙ gives f(aₙ) − f(a₀), the fundamental theorem on graphs.

For more complex shapes, the natural setting is a simplicial complex (triangles and higher-dimensional analogues) or a cubical complex (squares, cubes, ...). Oriented k-simplices form a vector space Cₖ, and a boundary operator ∂ₖ : Cₖ → Cₖ₋₁ satisfies ∂² = 0: the boundary of a boundary is empty. Taking dual vector spaces reverses the arrows, giving a cochain complex with coboundary d : Cᵏ → Cᵏ⁺¹, also satisfying d² = 0; its elements are discrete differential forms. Cycles (ker d) contain boundaries (im d). Stokes' theorem ∫_Ω dω = ∫_{∂Ω} ω is the unifying statement: the sum of dω over a region equals the sum of ω over its boundary, with interior contributions cancelling in pairs. A Laplace operator Δ = δd + dδ is built from d and its adjoint δ, and is the discrete analogue of the continuous Laplacian used to model diffusion and flux.

## Applications

Discrete calculus underpins difference equations, which model population growth, radioactive decay, reaction rates, heat transfer, wave propagation, and spacecraft trajectories. Kirchhoff's voltage law (1847) was an early application, expressible as a one-dimensional discrete exterior derivative. Maxwell's electromagnetism and Einstein's general relativity have both been rewritten in discrete language, and the planimeter, a device for measuring area on a drawing, implements the discrete analogue of Green's theorem. In machine learning and signal processing, discrete calculus supplies the operators (convolutions, level-set tools) used to analyse data on graphs and meshes.

Source: adapted from "Discrete calculus" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Discrete_calculus
