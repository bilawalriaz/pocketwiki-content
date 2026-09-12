# Pythagorean theorem

The Pythagorean theorem relates the three sides of a right triangle, a triangle with one 90° angle. If the two shorter sides, called the legs, have lengths $a$ and $b$, and the side opposite the right angle, called the hypotenuse, has length $c$, then

$$a^2 + b^2 = c^2.$$

Geometrically, the square built on the hypotenuse has the same area as the two squares built on the legs combined. The theorem holds only in flat, or Euclidean, geometry and only for right triangles.

## Proofs

The rearrangement proof works with two copies of a square of side $a+b$. In the first, four copies of the right triangle fill the corners and leave a tilted square of side $c$ in the middle, giving area $4 \cdot \tfrac{1}{2}ab + c^2 = 2ab + c^2$. In the second, the same four triangles are rearranged to leave two upright squares of sides $a$ and $b$, giving area $2ab + a^2 + b^2$. Equating the two expressions for $(a+b)^2$ and cancelling $2ab$ yields $a^2 + b^2 = c^2$.

Euclid gave the oldest surviving axiomatic proof (Elements, Book I, Proposition 47). It compares areas inside a large square built on the hypotenuse with the two smaller squares on the legs, using side-angle-side congruence to show each smaller square has the same area as one of two rectangles that together fill the large square. A different proof drops an altitude from the right angle onto the hypotenuse, splitting the original triangle into two smaller triangles that are each *similar* to it, meaning they have the same shape and their corresponding sides are proportional. The proportionality then gives $a^2 = c \cdot d$ and $b^2 = c \cdot e$ where $d$ and $e$ are the two pieces of the hypotenuse, and adding these recovers $a^2 + b^2 = c^2$.

## Converse and triangle classification

The converse is also true: if a triangle has sides $a$, $b$, $c$ with $a^2 + b^2 = c^2$, then the angle between $a$ and $b$ is a right angle, the statement of Euclid's Proposition 48. The same comparison classifies every triangle when $c$ is the longest side: $a^2 + b^2 = c^2$ means right, $a^2 + b^2 > c^2$ means acute, and $a^2 + b^2 < c^2$ means obtuse.

## Pythagorean triples

A Pythagorean triple is a set of three positive integers satisfying $a^2 + b^2 = c^2$, the side lengths of a right triangle with whole-number edges. The smallest is $(3, 4, 5)$; others include $(5, 12, 13)$ and $(8, 15, 17)$. A triple is *primitive* if the three numbers share no common factor. Euclid's formula generates every primitive triple: for any positive integers $m > n$,

$$a = m^2 - n^2, \quad b = 2mn, \quad c = m^2 + n^2.$$

## Uses and consequences

The theorem gives the distance formula in the Cartesian plane, the standard $x$-$y$ grid used to plot points. The distance between $(x_1, y_1)$ and $(x_2, y_2)$ is $\sqrt{(x_1 - x_2)^2 + (y_1 - y_2)^2}$, because the segment between the points is the hypotenuse of a right triangle with those coordinate differences as legs. The same pattern extends to any number of dimensions, giving the Euclidean length of a vector as the square root of the sum of squared components. In three dimensions, applying the theorem twice to a cuboid gives the body diagonal $d^2 = a^2 + b^2 + c^2$. For a complex number $z = x + iy$, where $i$ is the imaginary unit with $i^2 = -1$, the modulus $|z| = \sqrt{x^2 + y^2}$ is the distance from $z$ to the origin in the complex plane. In a right triangle with hypotenuse $c = 1$, the legs equal $\sin\theta$ and $\cos\theta$ for the angle $\theta$ between a leg and the hypotenuse, so the identity $\sin^2\theta + \cos^2\theta = 1$ falls out directly.

The theorem also revealed a problem. In a right isosceles triangle with legs of length 1, the hypotenuse has length $\sqrt{2}$, which cannot be written as a ratio of whole numbers. This discovery of incommensurable lengths is credited by ancient sources to Hippasus of Metapontum, and according to legend he was drowned for revealing it, since it contradicted the Pythagorean school's belief that all lengths were rational multiples of a common unit. The relation generalises: similar figures erected on the three sides of a right triangle have areas that satisfy the same rule, because area scales with the square of any linear dimension. The theorem is also a special case of the law of cosines, $a^2 + b^2 - 2ab\cos\theta = c^2$, which reduces to Pythagoras when $\theta = 90°$ and $\cos\theta = 0$.

Source: adapted from "Pythagorean theorem" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Pythagorean_theorem
