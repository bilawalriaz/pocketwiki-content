# Rounding

Rounding replaces a number with a simpler approximate value—$23.4476 becomes $23.45, 312/937 becomes 1/3, √2 becomes 1.414. It makes values easier to communicate and prevents misleading precision when a measurement or computation is accurate only to a certain scale. However, rounding exact numbers introduces round-off error. In long calculation chains these errors accumulate, and in ill-conditioned problems they can render results meaningless. Rounding is unavoidable in division, transcendental functions (square roots, logarithms, sines), and any fixed-precision representation such as floating-point arithmetic.

A rounding method should be a deterministic function: same input always yields same output. Results should stay close to exact calculations and to the original input. The range is a discrete subset of the domain (classically the integers). The method should preserve existing symmetries—avoiding systematic bias toward positive, negative, zero, or infinity—and be fast enough for practical use. No single method satisfies all ideals, so many exist. Rounding is idempotent: rounding a rounded value again at the same precision changes nothing. Rounding functions are monotonic: ordering of inputs is preserved (though distinct inputs may map to the same output). With a discrete range they are piecewise constant.

## Rounding to an integer

The simplest case replaces an arbitrary real number with an integer.

### Directed rounding

Displacements all point toward or away from a single limit (0, +∞, −∞). Used in interval arithmetic and financial calculations.
- **Round down (floor)**: largest integer ≤ x.
- **Round up (ceiling)**: smallest integer ≥ x.
- **Round toward zero (truncate)**: integer part, discarding fraction.
- **Round away from zero**: moves away from zero.

For positive x, round-down = toward-zero and round-up = away-from-zero. For negative x, the pairings reverse.

### Rounding to nearest (tie-breaking at 0.5)

When the fractional part is exactly 0.5, a tie-breaking rule decides direction. Without 0.5 cases, errors would be symmetric.
- **Half up (toward +∞)**: 23.5 → 24; −23.5 → −23.
- **Half down (toward −∞)**: 23.5 → 23; −23.5 → −24.
- **Half toward zero**: 23.5 → 23; −23.5 → −23. Symmetric for sign, but biases toward zero.
- **Half away from zero (commercial rounding)**: 23.5 → 24; −23.5 → −24. Symmetric for sign, biases away from zero. Common in currency.
- **Half to even (bankers' rounding)**: 23.5 → 24; 24.5 → 24; −23.5 → −24. No sign bias, no zero/infinity bias. Minimizes expected error when summing rounded figures. Default in IEEE 754 binary floating-point. Distorts distribution by favoring even results.
- **Half to odd**: 23.5 → 23; 22.5 → 23. Also unbiased, favors odd results. Avoids overflow in even-radix floating-point.

### Randomized rounding

- **Alternating tie-break**: alternate up/down on successive 0.5 cases. Effectively bias-free if 0.5 occurrences are frequent.
- **Random tie-break**: choose up or down with equal probability at each 0.5. Unbiased and fair between even/odd outcomes.
- **Stochastic rounding**: round to ⌊x⌋ with probability 1−(x−⌊x⌋), to ⌊x⌋+1 with probability x−⌊x⌋. Unbiased on average. Adding 0.3 one hundred times with stochastic rounding yields expected sum 30 (correct); deterministic rounding yields 0. Used in machine learning with low-precision arithmetic and for 1D dithering.

## Rounding to other values

**Specified multiple**: Round x to a multiple of m: `round(x/m) × m`. For significant digits, m depends on the number's magnitude (power of 10 for decimal, power of 2 for binary).

**Specified power (logarithmic rounding)**: Round x to a power of b: `b^round(log_b x)`. Common in computing (powers of 2). On a logarithmic scale, whether x rounds to a or b depends on whether x² > ab. Resistor values (E12 series) use this.

**Floating-point rounding**: Convert x to a value y with a fixed number of significant digits in base 2 or 10. y is a multiple of m = base^(exponent−precision). All integer rounding variants apply. IEEE 754 guarantees correctly rounded results for +, −, ×, ÷, fused multiply-add, square root, and remainder. For transcendental functions, correct rounding is the **table-maker's dilemma**: no general way to predict how many extra digits are needed to decide the rounding direction. Libraries typically achieve within 1 ulp; correct rounding requires much higher intermediate precision and is implemented only in specialized libraries. Some computable numbers can never be correctly rounded—this follows from the undecidability of the halting problem.

**Simple fractions and available values**: Round to a "neat" fraction m/n with bounded numerator/denominator (related to Farey sequences, continued fractions). Round to standard sizes (lumber, resistors) by choosing the nearest preferred value; if preferred values are logarithmically spaced, this is scaled rounding.

## Critical phenomena

**Error accumulation**: The 1982 Vancouver Stock Exchange index started at 1000.000. After 22 months it read ~520 despite a rising market. The index was recalculated thousands of times daily and truncated (rounded down) to three decimals each time. Errors accumulated downward. Recalculating with round-to-nearest gave 1098.892 instead of 524.811.

**Double rounding**: Rounding twice to successively coarser precisions can differ from rounding once to the final precision. Example: 9.46 → nearest tenth = 9.5 → nearest integer (half to even) = 10. Direct rounding to integer (half to even) gives 9. IEEE 754-2008 and modern languages forbid double rounding in straightforward calculations.

**Rounding to prepare for shorter precision (RPSP)**: Avoids double-rounding errors by making all intermediate roundings "safe" for a final rounding. In decimal: avoid final digits 0 and 5 when input is inexact. In binary, RPSP = "round to odd": set least significant bit to 1 if result is inexact. Each step must remove at least two binary digits.

**Dithering and error diffusion**: For continuous signals (audio, images), overall effect matters more than per-sample accuracy. Error diffusion accumulates rounding error and adds it to the next sample before rounding. Floyd–Steinberg dithering does this in 2D for images. Delta-sigma modulation controls quantization noise spectrum.

**Exact computation with rounded arithmetic**: If an integer n is known to be a perfect square, compute √n in floating-point and round to nearest integer. If n is small enough, round-off error < 0.5, so the rounded result is exact.

## Standards

Before the 1980s, floating-point rounding was hardware-dependent and inconsistent. IEEE 754 standardized multiple rounding modes with precise definitions, enabling predictable, machine-independent numerics. US weather observations use round-half-up. Floating-point representations distinguish +0 and −0; rounding a negative value to zero may yield −0.

Source: adapted from "Rounding" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Rounding
