# Difference engine

A difference engine is an automatic mechanical calculator, conceived by Charles Babbage in the 1820s, that tabulates polynomial functions using only addition. The name comes from the method of finite differences, a way to evaluate many nearby values of a polynomial without ever multiplying.

## Why polynomials matter

Most tables in 19th-century science, engineering, and navigation depended on logarithms and trigonometric functions. Both can be approximated to arbitrary precision by polynomials, and any polynomial can be tabulated by repeated addition of constant differences. A machine that handles polynomials therefore handles almost everything navigators and astronomers needed.

## The method of finite differences

For a polynomial of degree *n*, build a table where each column is the difference of the column to its left. For the quadratic p(x) = 2x² − 3x + 2:

| x | p(x) | diff1 | diff2 |
|---|------|-------|-------|
| 0 | 2    | −1    | 4     |
| 1 | 1    | 3     | 4     |
| 2 | 4    | 7     | 4     |
| 3 | 11   | 11    | 4     |
| 4 | 22   |       |       |

The second-difference column is constant. For any polynomial of degree *n*, the (*n*+1)th-difference column is always constant. Once the table is initialised, every new value is produced by walking diagonally down and right, adding only. No multiplication appears.

To compute p(5): add the constant 4 to the last diff1 entry (11) to get 15, then add 15 to the last p(x) entry (22) to get 37. Each iteration is one or two additions. A degree-*n* polynomial needs storage for *n* numbers.

## How the engine stores and adds

The machine has columns numbered 1 to *N*. Column 1 holds the running polynomial value, column *N* holds a constant. Each iteration, every even column is added to its odd neighbour on the left, then the reverse on the next half-cycle. Four crank turns complete one full cycle. A 4:1 reduction gear was added because the force at 1:1 was too much for a hand crank.

Carries propagate leftward digit by digit, as in any decimal adding machine. Negative numbers use ten's complement (each digit subtracted from 9, plus 1), so subtraction becomes addition of a negative. Modern binary computers use the analogous two's complement.

## Initialising the machine

For a polynomial a₀ + a₁x + a₂x² + …, the starting values for each column can be written down directly from the coefficients, without evaluating the polynomial:

- Column 1 = a₀
- Column 2 = a₁ + a₂ + a₃ + a₄ + …
- Column 3 = 2a₂ + 6a₃ + 14a₄ + 30a₅ + …

Non-polynomial functions such as sines and logarithms can be expressed as power series, for example a Taylor series. The same column-initials apply, with each aₙ replaced by the *n*th derivative at the start, divided by *n*!. Because these series are infinite, the engine gives exact results for the first *N* steps and approximations afterwards, and errors grow as the series diverges. Curve fitting offers a remedy: calculate a few true values across the range, fit a polynomial through them, and tabulate that polynomial instead, which keeps the error bounded.

## Babbage's machines

Babbage completed a small prototype, Difference Engine No. 0, by 1822 and announced it to the Royal Astronomical Society the same year. The British government funded a full-scale No. 1 in 1823 with £1,700, expecting cheaper, faster tables. The 1830 design called for about 25,000 parts, weighed 4 tons, and would have worked on 20-digit numbers to sixth-order differences. Metalworking of the time could not economically hit the required tolerances, and the project consumed over £17,000 before the government abandoned it in 1842. A small working model at one-seventh scale, 6 digits, second-order, was demonstrated in 1832.

While No. 1 stalled, Babbage moved on to the more general analytical engine, which made the difference engine concept obsolete in the government's view. He later drafted an improved Difference Engine No. 2 in 1846 to 1849, with 31-digit numbers, seventh-order differences, fewer parts, and faster operation. It was not built in his lifetime.

A working No. 2 was finally constructed at the London Science Museum from 1985 to 1991, led by Doron Swade, using only 19th-century manufacturing tolerances. It contains about 8,000 parts, weighs 5 tons, and holds 8 numbers of 31 decimal digits, enough to tabulate seventh-degree polynomials at full precision. Its printer produces stereotype plates by pressing type into soft plaster, which removes the human typesetting step that had introduced many errors in earlier tables. A second complete No. 2, funded by Nathan Myhrvold, was displayed at the Computer History Museum in Mountain View from 2008 to 2016 and is now at Intellectual Ventures in Seattle.

## Other engines

J. H. Müller described the basic principles in 1786 but never obtained funding. Per Georg Scheutz and his son Edvard built the first working printing calculator, sold to the Dudley Observatory in Albany, New York in 1857, with a second British-government machine following in 1859. Later implementations include Martin Wiberg (c. 1859), Alfred Deacon (c. 1862), George B. Grant (1876), Christel Hamann (1909), a 1912 Burroughs machine for the Nautical Almanac Office (replaced in 1929 by a Burroughs Class 11), and Alexander John Thompson's 1927 machine, made of four modified Triumphator calculators, which produced his 20-decimal *Logarithmetica Britannica*. Leslie Comrie showed in 1928 and 1931 that ordinary commercial calculators could be repurposed as difference engines.
