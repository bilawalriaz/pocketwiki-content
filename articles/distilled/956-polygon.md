# Polygon

## Overview
A polygon is a plane figure formed by a closed chain of line segments (edges) meeting at vertices (corners). It is the two-dimensional instance of the general polytope. Polygons are classified by side count, convexity, symmetry, and self-intersection. Simple polygons do not cross themselves and bound a solid region; self-intersecting polygons (like star polygons) cross their own boundaries. Core geometric properties—angle sums, area, and centroid—depend on vertex coordinates and winding order. The concept generalizes to spherical surfaces, skew chains in higher dimensions, infinite apeirogons, and abstract algebraic structures.

## Timeline
- **7th century BC** — Pentagram (regular star polygon) appears on a krater by Aristophanes.
- **14th century** — Thomas Bradwardine conducts the first known systematic study of non-convex polygons.
- **1952** — Geoffrey Colin Shephard generalizes polygons to the complex plane (complex polygons).
- **1963** — Lopshits describes the area formula for simple polygons using side lengths and exterior angles.

## Body

### Definition and basic classification
A polygon consists of edges (sides) and vertices (corners). An *n*-gon has *n* sides. A **simple polygon** has no self-intersections; its boundary encloses a **solid polygon** (body). A **self-intersecting** polygon crosses its own boundary (e.g., star polygons). A **skew polygon** has vertices not lying in a single plane. Polygons are primarily classified by the number of sides.

### Convexity and intersection types
- **Convex**: Any line meets the boundary at most twice; all interior angles < 180°. Equivalently, every segment between boundary points lies entirely inside.
- **Non-convex**: Some line meets the boundary more than twice; some segment between boundary points passes outside.
- **Concave**: Non-convex and simple; at least one interior angle > 180°.
- **Star-shaped**: The whole interior is visible from at least one point without crossing an edge. Must be simple; all convex polygons are star-shaped.
- **Self-intersecting**: Boundary crosses itself. **Star polygon**: Self-intersects in a regular way (cannot be both a star polygon and star-shaped).

### Equality and symmetry
- **Equiangular**: All corner angles equal.
- **Equilateral**: All edges equal length.
- **Regular**: Both equilateral and equiangular.
- **Cyclic**: All vertices lie on a single circle (circumcircle).
- **Tangential**: All sides tangent to an inscribed circle.
- **Isogonal (vertex-transitive)**: Vertices lie in one symmetry orbit; implies cyclic and equiangular.
- **Isotoxal (edge-transitive)**: Edges lie in one symmetry orbit; implies equilateral and tangential.
- A polygon is regular iff it is both isogonal and isotoxal, or both cyclic and equilateral. A non-convex regular polygon is a **regular star polygon**.
- **Rectilinear**: Sides meet at right angles (interior angles 90° or 270°).
- **Monotone** (w.r.t. line *L*): Every line orthogonal to *L* intersects the polygon ≤ twice.

### Angles
A polygon has as many corners as sides. For a simple *n*-gon, the sum of interior angles is (*n* − 2) × 180° (derived by partitioning into *n* − 2 triangles). Each interior angle of a convex regular *n*-gon is (1 − 2/*n*)π radians = 180 − 360/*n* degrees. For a regular star polygon {*p*/*q*} (*p*-gon with central density *q*), each interior angle is π(*p* − 2*q*)/*p* radians = 180(*p* − 2*q*)/*p* degrees (first studied by Poinsot). The **exterior angle** is the supplement of the interior angle. Tracing a convex *n*-gon, the sum of exterior angles (turning angles) is 360°. For general *n*-gons, the sum is an integer multiple *d* × 360°, where *d* is the density (turning number); e.g., 720° for a pentagram, 0° for a figure-eight.

### Area
**Simple polygons** (vertices (*x*₀,*y*₀)…(*x*ₙ₋₁,*y*ₙ₋₁) in order, with (*x*ₙ,*y*ₙ)=(*x*₀,*y*₀)):
- **Shoelace (surveyor’s) formula**: *A* = ½ ∑(*xᵢ yᵢ₊₁* − *xᵢ₊₁ yᵢ*). Signed area is positive for counterclockwise vertex order.
- **Side-length/exterior-angle formula** (Lopshits, 1963): *A* = ½ ∑ₖ *aₖ* [sum of products of subsequent sides with sines of cumulative exterior angles].
- **Pick’s theorem**: If vertices are grid points, *A* = *I* + *B*/2 − 1 (*I* = interior grid points, *B* = boundary grid points).
- **Isoperimetric inequality**: *p*² > 4π*A* for perimeter *p* and area *A*.
- **Bolyai–Gerwien theorem**: Any two simple polygons of equal area are equidecomposable (one can be cut and reassembled into the other).
- Side lengths alone do not determine area, but for simple cyclic polygons they do. Among *n*-gons with given side lengths, the cyclic one has maximum area; with given perimeter, the regular *n*-gon has maximum area.

**Regular polygons**:
- *A* = ½ *p* *r*, where *p* is perimeter and *r* (apothem) is inscribed circle radius.
- *A* = *R*² · *n*/2 · sin(2π/*n*) = *R*² · *n* · sin(π/*n*) cos(π/*n*), where *R* is circumradius.

**Self-intersecting polygons**: Two area definitions yield different results:
1. **Density-weighted**: Regions have multiplicities (e.g., central pentagon of a pentagram has density 2); signed densities can sum to zero (cross-quadrilateral).
2. **Point-set area**: Area of the covered plane region (e.g., cross-quadrilateral treated as two simple triangles).

### Centroid
For a solid simple polygon (signed area *A*):
- *Cₓ* = (1/6*A*) ∑(*xᵢ* + *xᵢ₊₁*)(*xᵢ yᵢ₊₁* − *xᵢ₊₁ yᵢ*)
- *Cᵧ* = (1/6*A*) ∑(*yᵢ* + *yᵢ₊₁*)(*xᵢ yᵢ₊₁* − *xᵢ₊₁ yᵢ*)
The vertex-set centroid (average of vertices) coincides with the solid centroid only for triangles (*n* = 3).

### Generalizations
- **Spherical polygon**: Arcs of great circles on a sphere; permits a **digon** (2 sides), impossible in the plane. Used in cartography and Wythoff’s construction of uniform polyhedra.
- **Skew polygon**: Vertices not coplanar; zigzags in ≥3 dimensions. **Petrie polygons** of regular polytopes are examples.
- **Apeirogon**: Infinite sequence of sides/angles, not closed but extending indefinitely in both directions.
- **Skew apeirogon**: Non-planar infinite polygon.
- **Polygon with holes**: Multiply-connected planar region with one outer boundary and ≥1 inner boundaries.
- **Complex polygon**: Exists in the complex plane (two real + two imaginary dimensions).
- **Abstract polygon**: Algebraic partially ordered set representing elements and connectivity; geometric polygons are realizations.
- **Polyhedron**: 3D solid bounded by polygonal faces. Higher-dimensional analogues are **polytopes** (or polyhedra in some conventions, with polytopes necessarily bounded).

### Naming
Names combine Greek numerical prefixes with “-gon” (e.g., pentagon, dodecagon). Exceptions: triangle, quadrilateral, nonagon. Beyond 12 sides, numerical notation is standard (17-gon, 257-gon). For 20–99 sides, prefixes are concatenated (optionally with “kai” for 13+). Special names exist for some regular star polygons (e.g., pentagram).

### History
Regular polygons known to ancient Greeks; pentagram appears 7th century BC. First systematic study of non-convex polygons by Thomas Bradwardine (14th century). Shephard generalized to complex polygons (1952).

### In nature
Crystals exhibit flat polygonal facets (angles depend on mineral). Basalt columns form regular hexagons (Giant’s Causeway, Devil’s Postpile). Honeycombs are arrays of hexagons.

### Computer graphics
Polygons are primitives for modelling/rendering. Stored as vertex arrays (coordinates, color, texture), connectivity, and materials. Surfaces are **polygon meshes** (tessellations). A square mesh with *n*+1 points per side has *n*² squares or 2*n*² triangles. Rendering pipeline: database → active memory → display system, with perspective correction. **Point-in-polygon test** determines if a point lies inside a simple polygon.

## Terms
- **Simple polygon** — A polygon whose boundary does not cross itself; the only intersections are shared endpoints of consecutive edges.
- **Solid polygon** — The planar region bounded by a simple polygon (its interior/body).
- **Convex polygon** — A polygon where any line meets the boundary at most twice; all interior angles < 180°; all segments between boundary points lie inside.
- **Star-shaped polygon** — A simple polygon whose entire interior is visible from at least one point without crossing an edge.
- **Star polygon** — A self-intersecting polygon that crosses itself in a regular way (e.g., {*p*/*q*}). Cannot be star-shaped.
- **Regular polygon** — Both equilateral (equal sides) and equiangular (equal angles); equivalently, cyclic and equilateral, or isogonal and isotoxal.
- **Cyclic polygon** — All vertices lie on a single circle (circumcircle).
- **Apothem** — The radius *r* of the inscribed circle of a regular polygon; used in area formula *A* = ½ *p* *r*.
- **Shoelace formula** — *A* = ½ ∑(*xᵢ yᵢ₊₁* − *xᵢ₊₁ yᵢ*) for simple polygon area from vertex coordinates.
- **Density (turning number)** — Integer *d* such that the sum of exterior angles of an *n*-gon is *d* × 360°; also the multiplicity factor for regions in self-intersecting polygons.

## Debates and open questions
- **Terminology for self-intersecting polygons**: The term “complex polygon” is sometimes used for self-intersecting polygons, but this conflicts with the standard meaning of a polygon in the complex Hilbert plane (two complex dimensions).
- **Naming conventions**: Use of “kai” in concatenated prefixes (e.g., icosikaihenagon vs. icosihenagon for 21-gon) is not universal; Conway advocated it for clarity in polyhedron naming, but many sources omit it.
- **Dimensional terminology**: Whether “polyhedron” and “polytope” are dimension-specific (polyhedron = 3D, polytope = *n*D) or used interchangeably with “polytope” implying boundedness varies by convention.