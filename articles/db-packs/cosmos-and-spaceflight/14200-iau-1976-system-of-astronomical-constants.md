# IAU (1976) System of Astronomical Constants

The IAU (1976) System of Astronomical Constants is a self-consistent set of numerical values adopted by the International Astronomical Union at its 16th General Assembly in Grenoble. It was prepared by Commission 4 (Ephemerides), led by P. Kenneth Seidelmann, to standardise the reduction of astronomical observations and the computation of ephemerides (predicted positions of solar-system bodies). It replaced the IAU (1964) system, took effect in the *Astronomical Almanac* in 1984, and remained standard until the IAU (2009) System. In 1994 the IAU recognised that several parameters had become outdated, but kept the 1976 values for continuity and began publishing a parallel set of "current best estimates", including new constants for relativistic time scales.

The system was part of a broader modernisation of astronomical reference data: a new standard epoch (J2000.0) was adopted at the same time, followed by a new reference frame with the FK5 fundamental catalogue, updated expressions for precession of the equinoxes, a 1979 relation between Universal Time and sidereal time, and 1979–1980 nutation theory. Because reliable planetary rotation elements were scarce, a Joint Working Group on Cartographic Coordinates and Rotational Elements was set up to compile recommended values.

## The astronomical system of units

The constants are anchored to a small system of units built on three astronomical quantities plus the Gaussian gravitational constant *k*.

- **Time:** the day (D) = 86,400 SI seconds, close to the mean solar day of civil time.
- **Mass:** the mass of the Sun (S).
- **Length:** the astronomical unit (A or au), defined indirectly by fixing *k*. In these units *k* has dimensions A^(3/2) S^(−1/2) D^(−1), and its value is set exactly to **0.017 202 098 95**. This *k* is the angular velocity in radians per day of an infinitesimally small mass in a circular orbit of radius 1 AU around the Sun. The astronomical unit then emerges as roughly the mean Earth–Sun distance, without being tied to a physical measurement of it.
- **Constant of gravitation G:** in SI units, ≈6.672 × 10⁻¹¹ m³ kg⁻¹ s⁻², with relative uncertainty about 6 × 10⁻⁴, by far the weakest link in the system.

## Defining, primary, and derived constants

The published set divides into three tiers. *Defining constants* are fixed by convention; *primary constants* are measured with stated uncertainty; *derived constants* follow from those above them. The constants that anchor the rest of the table are listed below with their values, units, and relative uncertainties.

| # | Quantity | Symbol | Value | Unit | Rel. uncert. |
|---|---|---|---|---|---|
| 1 | Gaussian gravitational constant | *k* | 0.017 202 098 95 | A^(3/2) S^(−1/2) D^(−1) | defined |
| 2 | Speed of light | *c* | 299 792 458 | m s⁻¹ | 4 × 10⁻⁹ |
| 3 | Light-time for unit distance | *τ_A* | 499.004 782 | s | 4 × 10⁻⁹ |
| 6 | Geocentric gravitational constant | *GE* | (3 986 005 ±3) × 10⁸ | m³ s⁻² | 8 × 10⁻⁷ |
| 7 | Constant of gravitation | *G* | (6.672 ±4.1) × 10⁻¹¹ | m³ kg⁻¹ s⁻² | 6.1 × 10⁻⁴ |
| 12 | Unit distance | *A* = *cτ_A* | (149 597 870 ±2) × 10³ | m | 1 × 10⁻⁸ |
| 16 | Heliocentric gravitational constant | *GS* = *A*³*k*²/*D*² | (132 712 438 ±5) × 10¹² | m³ s⁻² | 4 × 10⁻⁸ |
| 19 | Mass of the Sun | *S* = *GS/G* | (19 891 ±12) × 10²⁶ | kg | 6 × 10⁻⁴ |

Two chains illustrate how the table hangs together. Multiplying the speed of light *c* by *τ_A* gives *A*, the astronomical unit in metres. *A*³*k*²/*D*² gives *GS*, the heliocentric gravitational constant in SI units; dividing *GS* by *GE* yields the Sun/Earth mass ratio (332 946.0 ±0.3), while dividing *GS* by *G* yields the Sun's mass in kilograms. Because *G* is known only to about 0.06 %, any derived mass in kilograms inherits that uncertainty, while angular quantities and mass ratios remain sharp.

## Supporting data for ephemerides

The system also tabulated masses of the largest minor planets (Ceres 5.9, Pallas 1.1, Vesta 1.2, all ×10⁻¹⁰ solar masses), the satellite/planet mass ratios needed for the major moons (Io 4.70, Europa 2.56, Ganymede 7.84, Callisto 5.6, all ×10⁻⁵; Titan 2.41 × 10⁻⁴; Triton 2 × 10⁻³), equatorial radii in km (Mercury 2 439, Venus 6 052, Earth 6 378.140, Mars 3 397.2, Jupiter 71 398, Saturn 60 000, Uranus 25 400, Neptune 24 300, Pluto 2 500, Moon 1 738, Sun 696 000), and gravity-field coefficients *J₂, J₃, J₄, C₂₂, S₂₂, S₃₁* for Earth, Mars, Jupiter, Saturn, Uranus, and Neptune, plus a Moon gravity-field block built from the inclination *I* = 5 552.7″, the moment *C/MR²* = 0.392, and Stokes-like coefficients for lunar librations.
