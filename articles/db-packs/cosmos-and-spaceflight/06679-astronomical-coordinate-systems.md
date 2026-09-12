# Astronomical coordinate systems

Astronomers locate objects in the sky using spherical coordinates on an imaginary celestial sphere. As on Earth, where latitude and longitude are measured from the equator and a prime meridian, a sky position is given by a latitude-like angle from a chosen fundamental plane and a longitude-like angle from a chosen primary direction (0° longitude). The two angles are enough when distance is unknown or irrelevant; distance adds a third number when needed.

Different problems call for different fundamental planes, so several coordinate systems coexist. Each is named after its fundamental plane, and each also picks a center point (origin of distance) and a primary direction. The poles sit ±90° from the fundamental plane.

| System | Center | Fundamental plane (0° latitude) | Latitude | Longitude (0° from…) |
|---|---|---|---|---|
| Horizontal (alt–az) | Observer | Horizon | Altitude *a* | Azimuth *A* (north or south point) |
| Equatorial | Earth (or Sun) | Celestial equator | Declination δ | Right ascension α (or hour angle *h*) from March equinox |
| Ecliptic | Earth (geocentric) or Sun (heliocentric) | Ecliptic (Earth's orbital plane) | Ecliptic latitude β | Ecliptic longitude λ |
| Galactic | Sun | Galactic plane (Milky Way) | Galactic latitude *b* | Galactic longitude *l* (Galactic Center) |
| Supergalactic | — | Supergalactic plane (rich galaxy region) | SGB | SGL (intersection with galactic plane) |

Horizontal (alt–az) is what a ground observer literally sees: altitude above the horizon and azimuth around it. It is intuitive and good for tracking, but coordinates of a fixed star change constantly because Earth rotates once per sidereal day (23 h 56 min 4.091 s).

Equatorial is the standard system for astronomy. Declination mirrors Earth's latitude projected onto the sky, and right ascension is measured eastward from the March equinox, the point where the Sun crosses the celestial equator. Because the poles and equinox move slightly over decades (precession, nutation), modern catalogs use the J2000 reference, with B1950 as the older standard; "of date" coordinates apply to a specific moment, and "mean" versions average out nutation while "true" versions include it. Star maps, telescope setting circles on equatorial mounts, and most professional catalogs all use equatorial coordinates because they stay fixed as Earth turns.

Ecliptic uses the plane of Earth's orbit as its reference and is the natural system for Solar System bodies. The geocentric version dominated ancient astronomy and underlies the zodiac; the heliocentric version (centered on the Solar System's barycenter, just inside the Sun) describes planetary orbits and orbital elements.

Galactic and supergalactic systems orient the user to the Milky Way and to the local concentration of galaxies, and matter mostly for mapping structure beyond the Solar System.

## Converting between systems

Conversions are rotations of the celestial sphere, carried out with spherical trigonometry or equivalently with rotation matrices. They are governed by three key angles: the obliquity of the ecliptic ε ≈ 23.4° (tilt between the equatorial and ecliptic planes), the local sidereal time θ_L, and the observer's latitude and longitude.

The simplest case relates hour angle *h* and right ascension α: *h* = θ_L − α, since both measure the same east-west angle from different starting points. Equatorial and ecliptic coordinates are linked by ε; the convenient form is

```
tan(λ) = (sin α cos ε + tan δ sin ε) / cos α,
sin β = sin δ cos ε − cos δ sin ε sin α,
```

with ε tilting the planes. Converting to horizontal coordinates additionally requires the observer's latitude φ_o, because the horizon plane tilts with position on Earth.

Because arctan repeats every 180° while cos and sin repeat every 360°, the two-argument function atan2(*y*, *x*) is used for longitudes to pick the correct quadrant. The altitude equations ignore atmospheric refraction and diurnal parallax, the latter significant for the Moon, smaller for planets, and negligible for stars. Azimuth conventions also differ (south-through-west in classical texts versus north-through-east in navigation and most modern software), so the sign must be checked against the source being used.
