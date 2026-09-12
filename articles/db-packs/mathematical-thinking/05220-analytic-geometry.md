# Analytic geometry

Analytic geometry studies geometric shapes through a coordinate system, assigning each point a tuple of numbers so that algebra can answer geometric questions. It is also called coordinate geometry or Cartesian geometry, named after René Descartes.

## Historical development

Apollonius of Perga used a diameter and a tangent as reference axes in *Conics* and wrote relations between them equivalent to equations of curves, but he never used coordinates to define a curve from an equation, and he did not handle negative magnitudes. Omar Khayyam, in his *Treatise on Demonstrations of Problems of Algebra* (1070), bridged part of the gap between numerical and geometric algebra by solving the general cubic geometrically.

The decisive step came in 17th-century Western Europe, when René Descartes and Pierre de Fermat independently invented analytic geometry. Descartes published his method in *La Géométrie* (1637), an appendix to his *Discourse on the Method*; Fermat circulated *Ad locos planos et solidos isagoge* the same year. Fermat began with an equation and described the curve it defined; Descartes began with a curve and derived its equation, which forced him to develop methods for higher-degree polynomials. Leonhard Euler later applied coordinate methods systematically to space curves and surfaces.

## Coordinate systems

In Cartesian coordinates a planar point is (x, y) and a spatial point is (x, y, z), giving signed distances from two or three perpendicular axes that meet at the origin. In polar coordinates a planar point is (r, θ), where r is the distance from the origin and θ is the angle measured counterclockwise from the positive x-axis; the conversions are x = r cos θ, y = r sin θ, r = √(x² + y²). Cylindrical coordinates (r, θ, z) combine polar form in the xy-plane with height z, while spherical coordinates (ρ, θ, φ) use distance from the origin, an azimuthal angle, and a polar angle from the z-axis; physics texts sometimes swap the names of the two angles.

## Equations as loci

Any equation in the coordinates specifies a subset of the plane or space called its locus: the set of points whose coordinates satisfy the equation. Linear equations give lines or planes, quadratic equations in two variables give conic sections, and a single equation in three variables gives a surface. A curve in three dimensions is the intersection of two surfaces, or is given parametrically.

A non-vertical line in the plane is written y = mx + b, where m is the slope and b is the y-intercept. A plane in three dimensions is described by a point P₀ = (x₀, y₀, z₀) and a normal vector n = (a, b, c) perpendicular to it; the plane consists of all points whose position vector r satisfies n · (r − r₀) = 0, which expands to ax + by + cz + d = 0 with d = −(ax₀ + by₀ + cz₀). A straight line in three dimensions needs parametric form, x = x₀ + at, y = y₀ + bt, z = z₀ + ct, where (a, b, c) is a direction vector.

A quadratic in two variables, Ax² + Bxy + Cy² + Dx + Ey + F = 0 with A, B, C not all zero, gives a conic section. The class is determined by the discriminant B² − 4AC: negative gives an ellipse (a circle when B = 0 and A = C), zero gives a parabola, positive gives a hyperbola (a rectangular hyperbola when A + C = 0). The three-dimensional analogue is the quadric surface, including ellipsoids, paraboloids, hyperboloids, cylinders, cones, and planes.

## Distance and angle

Analytic geometry expresses geometric quantities by formulas consistent with the underlying Euclidean geometry. The distance between (x₁, y₁) and (x₂, y₂) in the plane is d = √((x₂ − x₁)² + (y₂ − y₁)²), an application of the Pythagorean theorem; in three dimensions the formula adds (z₂ − z₁)² under the root. The angle θ between two Euclidean vectors A and B is given by the dot product A · B = ‖A‖ ‖B‖ cos θ, so the dot product is zero exactly when the vectors are perpendicular.

## Transformations

Replacing the variables in a relation R(x, y) moves, stretches, or rotates its graph: x → x − h shifts it right by h, y → y − k shifts it up by k, x → x/b stretches it horizontally by factor b, y → y/a stretches it vertically. The substitutions x → x cos A + y sin A and y → −x sin A + y cos A rotate the graph through angle A. These operations apply to any geometric equation, whether or not it represents a function.

## Intersections and intercepts

The intersection of two objects given by relations P(x, y) and Q(x, y) is the solution set of the simultaneous system. The standard methods are substitution, solving one equation for one variable and inserting it into the other, and elimination, adding or subtracting multiples of the equations to cancel a variable. Two conics can share up to four points. For the line y = mx + b, the y-intercept is b (the point (0, b)) and the x-intercept is found by setting y = 0.

## Tangents and normals

The tangent line to a plane curve y = f(x) at (c, f(c)) is the line through that point with slope f′(c), the derivative of f, and is the best straight-line approximation to the curve at that point because it shares a position and a direction with the curve there. In three dimensions the analogous object is the tangent plane to a surface, with normal vector perpendicular to that plane. The notion of normality, perpendicularity between a line or vector and a given object, generalises to orthogonality in higher-dimensional Euclidean spaces.
