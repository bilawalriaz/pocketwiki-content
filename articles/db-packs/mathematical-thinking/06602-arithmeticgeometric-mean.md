# Arithmetic–geometric mean

The arithmetic–geometric mean (AGM) of two positive numbers x and y is the common limit of two interdependent sequences built from successive arithmetic and geometric means. It is used in fast algorithms for π, elliptic integrals, and elementary transcendental functions.

## The iteration

Starting from a₀ = x and g₀ = y (with x ≥ y > 0), define

- aₙ₊₁ = ½(aₙ + gₙ), the arithmetic mean of the previous pair,
- gₙ₊₁ = √(aₙ gₙ), the geometric mean of the previous pair.

Because the geometric mean of two positive numbers never exceeds their arithmetic mean, the pair is always ordered gₙ ≤ aₙ. The g-sequence is nondecreasing, the a-sequence is nonincreasing, and both are trapped between y and x; the inequalities are strict when x ≠ y. A monotone convergence argument then shows both sequences share a single limit M(x, y), which lies between the geometric and arithmetic means of x and y. The notation M(x, y), agm(x, y), and AGM(x, y) are interchangeable.

The number of correct digits roughly doubles at each step.

## Worked example

For a₀ = 24, g₀ = 6:

| n | aₙ | gₙ |
|---|---|---|
| 0 | 24 | 6 |
| 1 | 15 | 12 |
| 2 | 13.5 | 13.416 407… |
| 3 | 13.458 203 9… | 13.458 139 0… |
| 4 | 13.458 171 481 7… | 13.458 171 481 7… |

After four iterations the two columns agree to about 9 digits, giving M(24, 6) ≈ 13.458 171 481 725 615 420 766 8.

## Key properties

M(x, y) is homogeneous: M(rx, ry) = r·M(x, y) for any r ≥ 0.

Gauss gave the integral representation

M(x, y) = (π/2) · [ ∫₀^{π/2} dθ / √(x²cos²θ + y²sin²θ) ]⁻¹,

equivalently M(x, y) = (π/4) · (x + y) / K((x − y)/(x + y)), where K(k) = ∫₀^{π/2} dθ / √(1 − k²sin²θ) is the complete elliptic integral of the first kind. The identity follows from a change of variables that maps the integrand for (x, y) to the same integrand evaluated at (a₁, g₁); iterating gives I(x, y) = I(M, M) = π/(2M).

## Gauss's constant

The reciprocal 1/M(1, √2) is Gauss's constant G = 0.834 626 8…, and Gauss showed in 1799 that M(1, √2) = π/ϖ, where ϖ is the lemniscate constant. Schneider proved M(1, √2) is transcendental in 1941. The pair {π, M(1, 1/√2)} is algebraically independent over ℚ, but adding the derivative M′(1, 1/√2) breaks independence, since π = 2√2 · M(1, 1/√2)³ / M′(1, 1/√2).

A geometric–harmonic mean follows the same template: GH(x, y) = 1/M(1/x, 1/y) = xy/M(x, y).

## Applications

π. The Gauss–Legendre algorithm starts with a₀ = 1, g₀ = 1/√2, and cⱼ = ½(aⱼ₋₁ − gⱼ₋₁), using cⱼ = cⱼ₋₁² / (4aⱼ) to avoid cancellation, and produces

π = 4·M(1, 1/√2)² / (1 − Σⱼ 2^{j+1} cⱼ²).

Elliptic integrals. With a₀ = 1 and g₀ = cos α, the iteration gives M(1, cos α) = π / (2K(sin α)), so K(k) = π / (2·M(1, √(1−k²))). This is the standard method for the quarter period of elliptic functions, and it underlies elliptic filter design.

Elementary functions. Brent introduced the first AGM algorithms for fast evaluation of eˣ, sin x, and cos x by combining the iteration with Landen's ascending transformations.

Source: adapted from "Arithmetic–geometric mean" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Arithmetic%E2%80%93geometric_mean
