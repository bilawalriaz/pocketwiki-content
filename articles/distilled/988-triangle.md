# Triangle

## Overview

A triangle is a polygon with three sides and three vertices, forming the simplest closed shape in Euclidean geometry. It is foundational to trigonometry, structural engineering, and computational geometry due to its inherent rigidity and the rich relationships between its angles and sides.

## Timeline

- **c. 300 BC** — Euclid's *Elements* defines triangle terminology and classification
- **c. 100 AD** — Heron of Alexandria gives formula for triangle area from side lengths
- **1600s** — Trigonometric functions formalized for right and general triangles
- **1800s** — Non-Euclidean triangles (spherical, hyperbolic) studied
- **1900s** — Barycentric and trilinear coordinate systems developed

## Body

### Definition, Terminology, and Types

A triangle consists of three line segments whose endpoints are connected, forming three sides and three vertices (corners). The angles at the vertices sum to 180° in Euclidean space. Classification by side length: **equilateral** (all sides equal), **isosceles** (two sides equal), **scalene** (all sides unequal). Classification by angle: **right** (one 90° angle), **acute** (all angles < 90°), **obtuse** (one angle > 90°).

### Properties

**Special points**: The circumcenter (intersection of perpendicular bisectors) is the center of the circumcircle passing through all vertices. The orthocenter (intersection of altitudes) lies inside only for acute triangles. The incenter (intersection of angle bisectors) is the center of the incircle, the largest circle fitting inside the triangle. The centroid (intersection of medians) is the center of mass. The orthocenter (blue point), the center of the nine-point circle (red), the centroid (orange), and the circumcenter (green) all lie on a single line, known as Euler's line (red line). The center of the nine-point circle lies at the midpoint between the orthocenter and the circumcenter, and the distance between the centroid and the circumcenter is half that between the centroid and the orthocenter. Generally, the incircle's center is not located on Euler's line. The nine-point circle passes through midpoints of sides, feet of altitudes, and midpoints between vertices and orthocenter.

**Angle relations**: The exterior angle theorem states an exterior angle equals the sum of the two non-adjacent interior angles. The sum of all three exterior angles is 360°.

**Area**: Given by $T = \frac{1}{2}bh$ (base × height), $T = \frac{1}{2}ab\sin\gamma$ (two sides and included angle), or Heron's formula $T = \sqrt{s(s-a)(s-b)(s-c)}$ where $s$ is the semiperimeter.

**Triangle inequality**: The sum of the lengths of any two sides of a triangle must be greater than or equal to the length of the third side.

**Rigidity**: Unlike rectangles, triangles cannot change shape without altering side lengths, making them structurally stable.

### Similarity and Congruence

Two triangles are **similar** if corresponding angles are equal and sides are proportional. Congruence criteria include SAS (side-angle-side), ASA (angle-side-angle), SSS (side-side-side), and AAS (angle-angle-side).

### Triangulation and Coordinate Systems

**Triangulation** partitions polygons into triangles; a simple polygon with $n$ sides decomposes into $n-2$ triangles via $n-3$ diagonals. The two ears theorem states every simple polygon has at least two ears (vertices whose adjacent diagonal lies entirely within the polygon).

**Trilinear coordinates** specify a point's relative distances from the three sides. **Barycentric coordinates** specify weights at vertices needed to balance the triangle at a point.

### Related Figures

**Inscribed figures**: Every triangle has a unique incircle and Steiner inellipse (tangent at side midpoints, with the greatest area of any ellipse tangent to all three sides of the triangle). The pedal triangle of an interior point connects the nearest points on the sides. Inscribed squares exist in all triangles (three in acute, two in right, one in obtuse).

**Circumscribed figures**: The circumcircle passes through all vertices. Every triangle has a unique Steiner circumellipse, which passes through the triangle's vertices and has its center at the triangle's centroid. Of all ellipses going through the triangle's vertices, it has the smallest area. The tangential triangle is formed by tangent lines to the circumcircle at the vertices.

### Non-Euclidean and Special Triangles

**Spherical triangles** have angle sums exceeding 180°; by Girard's theorem, the sum equals $180° \times (1 + 4f)$ where $f$ is the fraction of the sphere's area enclosed. **Hyperbolic triangles** have angle sums less than 180°. **Circular triangles** have curved sides; a **Reuleaux triangle** is formed by intersecting three equal circles. **Pseudotriangles** are bounded by three smooth curves connecting tangent convex regions.

## Terms

- **Vertex/Vertices**: Zero-dimensional corner points of a triangle
- **Edge/Side**: One-dimensional line segment connecting two vertices
- **Altitude**: Line from a vertex perpendicular to the opposite side
- **Median**: Line from a vertex to the midpoint of the opposite side
- **Centroid**: Intersection point of the three medians; center of mass
- **Orthocenter**: Intersection point of the three altitudes
- **Circumcenter**: Intersection of perpendicular bisectors; center of circumcircle
- **Incenter**: Intersection of angle bisectors; center of incircle
- **Barycentric coordinates**: Point location specified by vertex weights
- **Triangulation**: Partitioning a polygon into triangles

## Debates and Open Questions

- Whether degenerate triangles (collinear vertices) count as triangles is a matter of convention.
- The inscribed square problem asks for a square whose vertices lie on a simple closed curve; the problem discusses inscribed squares in triangles but does not state it is solved for triangles.
- The exact number of triangle centers (over 5200 catalogued) continues to grow as new special points are discovered.