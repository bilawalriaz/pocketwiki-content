# Logarithm

## Overview

A logarithm answers the question: to what exponent must a fixed base be raised to produce a given number? Formally, if \( x = b^y \), then \( y = \log_b x \). Introduced by John Napier in 1614, logarithms revolutionized computation by converting multiplication into addition via the identity \( \log_b(xy) = \log_b x + \log_b y \). They remain central to mathematics, science, engineering, and computer science, appearing in fields ranging from signal processing (decibels) to number theory (prime counting) and algorithm analysis.

## Timeline

- **c. 1600** — Jost Bürgi develops early logarithmic techniques
- **1614** — John Napier publishes *Mirifici Logarithmorum Canonis Descriptio*
- **1617** — Henry Briggs compiles first base-10 logarithm table
- **1647** — Grégoire de Saint-Vincent publishes hyperbolic quadrature results
- **1675** — Leibniz adopts notation Log y and connects it to \( \int dy/y \)
- **1714** — Roger Cotes shows \( \log(\cos\theta + i\sin\theta) = i\theta \)
- **18th century** — Euler formalizes connection between logarithms and exponential functions

## Body

### Definition and Basic Properties

Given a positive real base \( b \neq 1 \), the logarithm \( \log_b x \) is the unique real number \( y \) such that \( b^y = x \). This makes \( \log_b \) the inverse function of \( x \mapsto b^x \). Key identities include:

- **Product rule**: \( \log_b(xy) = \log_b x + \log_b y \)
- **Quotient rule**: \( \log_b(x/y) = \log_b x - \log_b y \)
- **Power rule**: \( \log_b(x^p) = p \log_b x \)
- **Change of base**: \( \log_b x = \frac{\log_k x}{\log_k b} \)

These identities allow logarithms to reduce complex arithmetic operations to simpler ones—multiplication becomes addition, division becomes subtraction, and exponentiation becomes multiplication.

### Particular Bases

Three bases dominate applications:

- **Base 10 (common logarithm)**: Used in science and engineering; relates directly to decimal digit counts.
- **Base e ≈ 2.71828 (natural logarithm)**: Ubiquitous in mathematics and physics due to its simple derivative \( d/dx[\ln x] = 1/x \).
- **Base 2 (binary logarithm)**: Essential in computer science, information theory, and music theory.

When the base is clear from context, it is often omitted: \( \log x \) typically means \( \ln x \) in pure mathematics and \( \log_{10} x \) in applied sciences.

### Historical Development

Napier coined "logarithm" from Greek *logos* (ratio) + *arithmos* (number), meaning "ratio-number." His goal was computational efficiency: replacing tedious multiplications with table lookups and additions. Briggs refined this into base-10 logarithms, creating extensive tables accurate to 14 digits. The slide rule, based on logarithmic scales, became an indispensable tool for engineers and scientists until the 1970s.

The natural logarithm emerged from attempts to quadrature the hyperbola. Saint-Vincent's work led A. A. de Sarasa to connect it with existing logarithmic traditions, calling it the "hyperbolic logarithm." Euler later unified logarithms with exponential functions and introduced \( e \) as the natural base.

### Analytic Properties

The logarithm function \( \log_b x \) is the inverse of the strictly monotonic exponential function \( b^x \), ensuring its existence and uniqueness for positive reals. Its derivative is \( \frac{d}{dx}\log_b x = \frac{1}{x \ln b} \), making \( \ln x \) unique among antiderivatives of \( 1/x \).

The natural logarithm can be defined analytically as:
$$ \ln t = \int_1^t \frac{1}{x} dx $$

This integral definition derives all logarithmic identities without reference to exponentials. The harmonic series \( \sum_{k=1}^n \frac{1}{k} \) relates closely to \( \ln n \), converging to the Euler–Mascheroni constant \( \gamma \approx 0.5772 \).

### Computation Methods

Before electronic calculators, logarithms were computed using:

1. **Tables**: Pre-calculated values with interpolation for precision
2. **Slide rules**: Mechanical devices using logarithmic scales
3. **Series expansions**: Taylor series \( \ln(1+z) = z - z^2/2 + z^3/3 - \cdots \) for \( |z| < 1 \)
4. **Arithmetic-geometric mean**: High-precision method by Gauss
5. **Feynman's algorithm**: Bit-processing technique for binary computers

Modern computers use optimized versions of these methods, including CORDIC algorithms and look-up tables.

### Applications

**Logarithmic scales** compress wide-ranging data:
- **Decibels**: \( 10 \log_{10}(\text{power ratio}) \) for sound and signals
- **pH**: \( -\log_{10}[\text{H}^+] \) for acidity
- **Richter scale**: \( \log_{10}(\text{earthquake energy}) \)
- **Stellar magnitude**: Logarithmic brightness measure

**Algorithm analysis** uses logarithms to describe divide-and-conquer complexity:
- Binary search: \( O(\log_2 N) \) comparisons
- Merge sort: \( O(N \log N) \) time

**Information theory** quantifies information as \( \log_2 N \) bits for \( N \) equally likely outcomes.

**Number theory** connects logarithms to prime distribution:
- Prime Number Theorem: \( \pi(x) \sim \frac{x}{\ln x} \)
- Stirling's approximation: \( \ln(n!) \approx n \ln n - n \)

**Music theory** measures intervals logarithmically:
- Octave: frequency ratio 2:1
- Semitone: \( \log_{2^{1/12}}(\text{ratio}) \)
- Cent: 1200 × base-2 logarithm of frequency ratio

### Generalizations

**Complex logarithm**: Multi-valued inverse of complex exponential. For \( z = re^{i\phi} \), all solutions to \( e^a = z \) are \( a_k = \ln r + i(\phi + 2k\pi) \). Selecting a principal branch requires restricting \( \phi \) to an interval like \( (-\pi, \pi] \), introducing branch cuts.

**Discrete logarithm**: In finite groups, solves \( b^n = x \) for integer \( n \). Computationally hard in some groups, forming the basis of cryptographic protocols like Diffie-Hellman key exchange.

**Other inverses**: Matrix logarithm (inverse of matrix exponential), p-adic logarithm, and logarithmic maps in differential geometry extend the concept across mathematical structures.

## Terms

- **Base**: The fixed value \( b \) raised to a power in exponentiation; determines the logarithm's scaling
- **Characteristic**: Integer part of a common logarithm; equals digit count minus one
- **Mantissa**: Fractional part of a common logarithm; found in log tables
- **Antilogarithm**: Inverse function of logarithm; equivalently the exponential function \( b^x \)
- **Natural logarithm**: Logarithm with base \( e \approx 2.71828 \); denoted \( \ln x \)
- **Common logarithm**: Base-10 logarithm; denoted \( \log_{10} x \) or simply \( \log x \) in applied contexts
- **Binary logarithm**: Base-2 logarithm; denoted \( \log_2 x \); fundamental in computer science
- **Branch cut**: Curve in the complex plane where a multi-valued function is made discontinuous to define a single-valued branch
- **Logarithmic derivative**: \( f'(x)/f(x) \); derivative of \( \ln(f(x)) \)
- **Logarithmic scale**: Scale where equal distances represent equal ratios rather than equal differences

## Debates and Open Questions

- **Riemann Hypothesis**: Concerns the distribution of zeros of the Riemann zeta function, equivalent to precise bounds on \( \pi(x) - \text{Li}(x) \)
- **Complexity of discrete logarithm**: Whether quantum algorithms (Shor's algorithm) render current cryptographic systems insecure remains an active area of research
- **Benford's law compliance**: While widely observed, the extent to which real-world datasets follow Benford's distribution and its forensic applications continue to be debated
- **Convergence of logarithm series**: Optimal methods for high-precision computation balance speed, numerical stability, and implementation complexity

Source: adapted from "Logarithm" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Logarithm
