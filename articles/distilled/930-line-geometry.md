# Line (geometry)

## Overview
A line is a fundamental geometric object: an infinitely long, one-dimensional figure with no width, depth, or curvature. It is the idealization of physical straightedges, taut strings, or light rays, and serves as a building block for both classical and modern geometry. While Euclid defined it as a "breadthless length" lying evenly with its points, modern treatments define it either as a primitive notion governed by axioms or as the set of points satisfying a linear equation.

## Timeline
- **c. 300 BC** — Euclid's *Elements* defines the straight line and introduces foundational postulates
- **Late 19th century** — Non-Euclidean, projective, and affine geometries generalize the concept of a line
- **Early 20th century** — Hilbert's axiomatic system formalizes Euclidean geometry with rigorous line properties

## Body

### Axiomatic Foundations
In Euclid's *Elements*, a general line (now called a curve) is a "breadthless length," and a straight line lies evenly with respect to its points. These definitions rely on physical intuition rather than formal logic and are not used in subsequent proofs. Modern axiomatic systems, such as Hilbert's, treat the line as a primitive notion whose properties are given by axioms. Key properties include: any two distinct points determine a unique line; two distinct lines intersect at most once; and in two dimensions, non-intersecting lines are parallel, while in higher dimensions, non-intersecting lines are either parallel (coplanar) or skew (non-coplanar).

### Analytic Representations
In Cartesian coordinates, every line is the set of points $(x, y)$ satisfying a linear equation $ax + by = c$, where $a$ and $b$ are not both zero. Vertical lines correspond to $b = 0$. The slope-intercept form $y = mx + b$ expresses a line in terms of its slope $m$ and y-intercept $b$. For a line through two points $P_0(x_0, y_0)$ and $P_1(x_1, y_1)$, the equation can be written as $(y - y_0)(x_1 - x_0) = (y_1 - y_0)(x - x_0)$. In three dimensions, a line is the intersection of two non-parallel planes, described by two simultaneous linear equations.

### Parametric and Vector Forms
Parametric equations express coordinates as functions of a parameter $t$: $x = x_0 + at$, $y = y_0 + bt$, $z = z_0 + ct$, where $(x_0, y_0, z_0)$ is a point on the line and $(a, b, c)$ is a direction vector. The vector form $\mathbf{r} = \mathbf{a} + \lambda(\mathbf{b} - \mathbf{a})$ describes the line through points with position vectors $\mathbf{a}$ and $\mathbf{b}$. Limiting $\lambda \geq 0$ or $\lambda \leq 0$ yields rays starting at $\mathbf{a}$.

### Special Forms and Coordinate Systems
The Hesse normal form $x \cos \varphi + y \sin \varphi - p = 0$ uses the angle $\varphi$ of the normal segment from the origin and its length $p$. In polar coordinates, a line not passing through the origin is $r = \frac{p}{\cos(\theta - \varphi)}$, where $p$ is the perpendicular distance from the origin and $\varphi$ is the angle of the normal. A line through the origin making angle $\alpha$ with the x-axis satisfies $\theta = \alpha$ or $\theta = \alpha + \pi$.

### Collinearity
Three or more points are collinear if they lie on the same line. In affine coordinates, points $X$, $Y$, $Z$ are collinear if the matrix $\begin{bmatrix}1&x_1&x_2&\cdots&x_n\\1&y_1&y_2&\cdots&y_n\\1&z_1&z_2&\cdots&z_n\end{bmatrix}$ has rank less than 3. For three planar points, collinearity holds if and only if the determinant of this matrix is zero, or equivalently, if the slopes between all pairs of points are equal.

### Relationships with Other Figures
All Euclidean lines are congruent, but they take special roles relative to other objects. With conics, lines can be tangent (touching at one point), secant (intersecting at two points), exterior (not meeting the conic), or directrix (used in conic definition). For algebraic curves, lines may be i-secants (meeting the curve in $i$ points) or asymptotes (approached but not touched). Special lines associated with triangles include the Euler line, Simson lines, and central lines. The Newton line connects midpoints of a quadrilateral's diagonals, while the Pascal and Pappus lines arise from hexagons inscribed in conics.

### Generalizations
In modern mathematics, the concept of a line varies with the geometry. In differential geometry, a line may be a geodesic—the shortest path between points. In projective geometry, a line can be a 2-dimensional vector space. In elliptic geometry, lines are represented by great circles on a sphere with opposite points identified, or by planes through the origin. These representations preserve the property that two points determine a unique line, even though they differ visually from Euclidean lines.

## Terms
- **Primitive notion**: A concept left undefined in an axiomatic system, with properties specified by axioms.
- **Collinear**: Points that lie on the same straight line.
- **Skew lines**: Non-intersecting lines in three or more dimensions that are not coplanar.
- **Tangent line**: A line touching a curve at exactly one point.
- **Secant line**: A line intersecting a curve at two or more points.
- **Asymptote**: A line that a curve approaches arbitrarily closely without intersecting.
- **Geodesic**: The shortest path between two points on a surface or in a metric space.
- **Hesse normal form**: A line equation using the perpendicular distance from the origin and the angle of the normal.
- **Ray (half-line)**: A part of a line starting at a point and extending infinitely in one direction.
- **Line segment**: A part of a line bounded by two distinct endpoints.

## Debates and open questions
The definition of a line remains debated across geometries. Euclid's intuitive definition is not used in formal proofs, leading to reliance on axiomatic or analytic approaches. Whether a line should be treated as a primitive notion or defined via coordinates depends on the mathematical framework. In non-Euclidean and projective geometries, the visual representation of lines diverges significantly from the Euclidean ideal, raising questions about the universality of geometric intuition. The applicability of rays and betweenness concepts is limited to ordered geometries, excluding projective and complex geometries.

Source: adapted from "Line (geometry)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Line_%28geometry%29
