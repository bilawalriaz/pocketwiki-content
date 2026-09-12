# Probability density function

A probability density function (PDF) describes an absolutely continuous random variable: a real-valued quantity whose outcomes are not single points but whole intervals. "Absolutely continuous" here means the distribution can be written entirely as an integral over its density, with no point masses. For such a variable, the probability of landing on any single value is exactly zero, because there are infinitely many possible values packed into any interval. The PDF answers the useful question instead: how probable is the variable to fall inside some range?

## Density, not probability

A PDF's value at a point, written f(x), is not a probability. It is a probability *per unit* of x, so its units are the inverse of x's units (for a time variable, f has units of "per hour"). The actual probability of landing in an interval [a, b] is the area under the curve over that interval:

Pr[a ≤ X ≤ b] = ∫ from a to b of f(x) dx.

Two consequences follow. First, f(x) must be nonnegative everywhere. Second, the total area under the curve over the entire real line must equal one, because the variable must land somewhere. Because density can exceed one, a high PDF value does not mean a high probability at that point; it means the probability is concentrated near that point per unit of x.

A concrete example makes this clear. Suppose a bacterium's lifespan is a continuous random variable, and the probability it dies within any tiny window around 5 hours is proportional to the window's length, with constant2 per hour. Then f(5 hours) = 2 hour⁻¹, and the probability of dying between 5 and 5.01 hours is 2 hour⁻¹ × 0.01 hour = 0.02. Shrinking the window by a factor of ten shrinks the probability by the same factor, leaving the density unchanged.

## The integral and the derivative

A continuous random variable X with PDF f has cumulative distribution function (CDF)

F(x) = Pr[X ≤ x] = ∫ from −∞ to x of f(u) du.

Where F is differentiable, the PDF is its derivative:

f(x) = dF(x)/dx.

So f(x) dx is the probability of X falling in the infinitesimal interval [x, x+dx].

## Which distributions have a PDF

A distribution has a PDF exactly when its CDF is absolutely continuous. Discrete random variables, which assign positive probability to individual points, do not. The Cantor distribution is a subtler counterexample: it is continuous (no single point gets positive mass) yet still has no PDF.

## Common examples

The continuous uniform distribution on [0, 1/2] has f(x) = 2 for x in [0, 1/2] and zero elsewhere, illustrating that density can exceed one. The standard normal distribution has

f(x) = (1/√(2π)) e^(−x²/2),

which peaks at about 0.4 but never reaches one.

## Expected value

If X has PDF f and the expectation exists, then

E[X] = ∫ from −∞ to ∞ of x f(x) dx.

The expectation of any function g(X) can also be computed without first finding the PDF of g(X), using the law of the unconscious statistician:

E[g(X)] = ∫ from −∞ to ∞ of g(x) f(x) dx.

## Joint, marginal, and independent densities

Several continuous variables X₁, …, Xₙ can share a joint PDF f(x₁, …, xₙ), with

Pr[(X₁, …, Xₙ) ∈ D] = ∫ over D of f(x₁, …, xₙ) dx₁ … dxₙ,

and the joint PDF is the n-th mixed partial derivative of the joint CDF: f = ∂ⁿF / ∂x₁ … ∂xₙ. The marginal density of Xᵢ is obtained by integrating the joint density over all other variables. The variables are independent precisely when the joint density factors as a product of the marginals: f(x₁, …, xₙ) = f₁(x₁) ··· fₙ(xₙ).

## Change of variables

If Y = g(X) for a monotonic g with inverse g⁻¹, the PDF of Y is

f_Y(y) = f_X(g⁻¹(y)) · |d/dy g⁻¹(y)|,

because |f_Y(y) dy| = |f_X(x) dx| must hold under any change of variables. For non-monotonic g the formula sums over all preimages. For a bijective multivariate transform, the scalar derivative is replaced by the absolute value of the Jacobian determinant of the inverse transform.

## Sums, products, and quotients

The PDF of the sum of two independent variables U and V is the convolution of their densities: f_{U+V} = f_U ∗ f_V. Products and quotients are handled by introducing an auxiliary variable and applying the change-of-variables formula. The quotient of two independent standard normals, for instance, has density

p(y) = 1 / (π (y² + 1)),

which is the standard Cauchy distribution: heavy-tailed enough that its mean does not exist.

This is shorter than the original, preserves all the working ideas, fixes the missing gloss on "absolutely continuous," and ends naturally on a fact.

Source: adapted from "Probability density function" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Probability_density_function
