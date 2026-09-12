# Latitude

## Overview
Latitude is a geographic coordinate specifying the north-south position of a point on Earth or another celestial body, measured as an angle from −90° at the South Pole to 90° at the North Pole, with 0° at the Equator. It is fundamental to the geographic coordinate system, used with longitude to specify locations, and its precise definition depends on the mathematical model (sphere or ellipsoid) used to represent the Earth's shape.

## Timeline
- **1687** — Isaac Newton proves a rotating fluid body forms an oblate ellipsoid.
- **18th century** — Geodetic measurements confirm Newton's ellipsoidal model.
- **20th century** — Adoption of geocentric ellipsoids (e.g., WGS84) for GPS.

## Body

### Definition and Background
Latitude is defined on a reference surface that models the Earth. First, the physical surface is approximated by the geoid (mean sea level extended under land). The geoid is then approximated by a simpler mathematical surface: a sphere or, more accurately, an ellipsoid of revolution. Latitude is the angle between the equatorial plane and the normal (perpendicular) to this reference surface at a point. The standard, unqualified term "latitude" refers to geodetic latitude on the ellipsoid. Latitude and longitude, with a height specification, form a geographic coordinate system.

### Latitude on the Sphere
On a spherical Earth model, the graticule (grid) is formed by parallels (lines of constant latitude) and meridians (lines of constant longitude). The Equator is 0°, the North Pole is 90° N, and the South Pole is 90° S. The latitude of a point is the angle between the equatorial plane and the radial line from the Earth's center to that point. This is called spherical latitude. Significant parallels include the Tropics (latitude equal to the Earth's axial tilt, *i*) and the polar circles (latitude 90° - *i*).

### Latitude on the Ellipsoid
The Earth is more accurately modeled as an oblate ellipsoid of revolution, defined by its equatorial radius (*a*), polar radius (*b*), flattening (*f*), or eccentricity (*e*). On an ellipsoid, the normal at a point does not generally pass through the center. Geodetic latitude (ϕ) is the angle between this normal and the equatorial plane. Geocentric latitude (θ) is the angle between the radius vector and the equatorial plane; the two differ by up to about 11.5 minutes of arc at 45° latitude. The precise latitude of a point depends on the chosen reference ellipsoid (e.g., WGS84 for GPS).

### Meridian Distance
The length of a degree of latitude varies with the Earth model. On a sphere with mean radius 6,371 km, one degree of latitude is approximately 111.2 km. On the WGS84 ellipsoid, the distance varies slightly with latitude, given by a specific formula. The quarter meridian distance from equator to pole is 10,001.965729 km.

### Auxiliary Latitudes
Six auxiliary latitudes are defined on the ellipsoid for specialized applications in geodesy and map projections. They are mathematical transformations of geodetic latitude. Key examples include:
*   **Geocentric latitude (θ):** Angle from the center.
*   **Parametric latitude (β):** Used in geodesic calculations.
*   **Conformal latitude (χ):** Preserves angles for conformal map projections.
*   **Authalic latitude (ξ):** Preserves area for equal-area projections.
*   **Rectifying latitude (μ):** Preserves meridian scale.
*   **Isometric latitude (ψ):** Used in Mercator projections; tends to infinity at the poles.

### Coordinate Systems and Astronomical Latitude
Geodetic latitude is used in geodetic coordinates (ϕ, λ, h). Geocentric latitude is used in spherical polar coordinates. Parametric latitude is used in ellipsoidal-harmonic coordinates. Astronomical latitude (Φ) is the angle between the equatorial plane and the true vertical (direction of a plumb line), which is influenced by local gravity and differs slightly from geodetic latitude.

## Terms
*   **Geoid:** The surface that approximates mean sea level and its continuation under land.
*   **Ellipsoid of revolution (oblate ellipsoid):** A reference surface formed by rotating an ellipse about its shorter axis; a common model for the Earth's shape.
*   **Geodetic latitude (ϕ):** The standard latitude, defined as the angle between the normal to the reference ellipsoid and the equatorial plane.
*   **Geocentric latitude (θ):** The angle between the radius vector from the Earth's center and the equatorial plane.
*   **Graticule:** The network of lines of constant latitude and longitude on a reference surface.
*   **Flattening (f):** A measure of an ellipsoid's compression, defined as (a - b)/a.
*   **Eccentricity (e):** A parameter describing the deviation of an ellipse from circularity.
*   **Auxiliary latitude:** Any of six mathematical latitudes (e.g., conformal, authalic) defined on the ellipsoid for use in map projections and geodesy.

## Debates and Open Questions
The article notes that without specifying the full coordinate reference system (including the reference ellipsoid), latitude and longitude coordinates are "ambiguous at best and meaningless at worst." This is a critical issue in precise applications like GPS, where different ellipsoids yield different latitude values for the same physical point. The choice of ellipsoid and the transformation between different datums is a fundamental, ongoing consideration in geodesy and mapping.