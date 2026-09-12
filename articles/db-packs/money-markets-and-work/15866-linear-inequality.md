# Linear inequality

A linear inequality is an inequality that involves a linear function. It looks exactly like a linear equation except the equals sign is replaced by an inequality symbol: `<` (less than), `>` (greater than), `≤` (less than or equal to), `≥` (greater than or equal to), or `≠` (not equal to). Any `>` or `≥` relation can be rewritten as a `<` or `≤` relation by flipping the sides.

## Real variables in two dimensions

A two-dimensional linear inequality has the form `ax + by < c` or `ax + by ≥ c`. Its solution set is a half-plane: every point on one side of the line `ax + by = c`.

The boundary line is excluded when the inequality is strict and included when it is not. To decide which side is the solution set, substitute a convenient point not on the line into `ax + by`. If the inequality holds there, that side is the solution.

For `x + 3y < 9`, draw `x + 3y = 9` as a dotted line because the strict sign excludes it. Test `(0,0)`: `0 + 3(0) = 0 < 9`, so `(0,0)` satisfies the inequality. The half-plane containing `(0,0)` is the solution set.

## Arbitrary dimension

In ℝⁿ, a linear inequality has the form `a₁x₁ + a₂x₂ + ⋯ + aₙxₙ < b` (or `≤ b`), where the `xᵢ` are the unknowns, the `aᵢ` are the coefficients, and `b` is a real constant. Equivalently, it is `f(x̄) < b` with `f` a linear form (a linear functional), or `g(x) < 0` with `g` an affine function, i.e. `a₀ + a₁x₁ + ⋯ + aₙxₙ < 0`; the affine form just moves `b` to the left side.

## Systems

A system of linear inequalities is a collection of linear inequalities in the same unknowns. With `m` inequalities and `n` unknowns it can be written as the matrix inequality `Ax ≤ b`, where `A` is an `m × n` coefficient matrix, `x` an `n × 1` column vector of unknowns, and `b` an `m × 1` column vector of constants; the relation `≤` is read row by row. Strict and non-strict signs may be mixed, and some systems have no solution. Fourier–Motzkin elimination removes variables from such systems.

## Solution geometry

The solution set of one real linear inequality in ℝⁿ is a half-space, one of the two pieces cut out by the corresponding hyperplane. The solution set of a system is the intersection of the half-spaces from each inequality. Each half-space is convex, so the intersection is convex. In non-degenerate cases this convex set is a convex polyhedron, possibly unbounded (a half-space, a slab between parallel half-spaces, or a polyhedral cone); it can also be empty or confined to a lower-dimensional affine subspace of ℝⁿ.

## Linear programming

A linear programming problem asks for the maximum or minimum of an objective function subject to a list of linear inequality constraints. The constraints themselves form a system of linear inequalities, so the feasible region is the convex polyhedron (or empty set) defined by that system, and the optimum is sought there.

Source: adapted from "Linear inequality" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Linear_inequality
