# Geoid

## Overview
The geoid is the shape the ocean surface would take under Earth's gravity and rotation alone, extended through the continents. It represents an equipotential surface where gravity acts perpendicular everywhere, making it fundamental for defining vertical heights in geodesy and satellite positioning systems like GPS.

## Timeline
- **1828** — Carl Friedrich Gauss first describes the geoid as the "mathematical figure of the Earth."
- **1849** — George Gabriel Stokes publishes his integral formula for determining geoid undulation from gravity anomalies.
- **Mid-20th century** — Satellite geodesy enables precise definition of the geoid.
- **1996** — The EGM96 geoid model is released, a common reference for undulation.
- **March 2009** — ESA launches the GOCE satellite to map Earth's gravity with high accuracy.
- **June 2010** — First geoid products from GOCE data become available online.
- **31 March 2011** — A new geoid model is unveiled at the Fourth International GOCE User Workshop.
- **2020** — The EGM2020 model is developed as an international collaborative project.

## Body

### Description and Properties
The geoid is an irregular but smooth surface, considerably smoother than Earth's physical topography. Its deviation from a reference ellipsoid (a slightly flattened sphere) ranges from +85 m over Iceland to -106 m in the southern Indian Ocean. All points on the geoid share the same geopotential (the sum of gravitational and centrifugal potential energy). Consequently, a plumb line is perpendicular to it, and a bubble level is parallel to it. The geoid corresponds to the hypothetical free surface of water at rest if only gravity and rotation were acting.

### Formulation and Practical Use
The geoid undulation, *N*, is the height of the geoid above a reference ellipsoid, calculated as *N = h - H*, where *h* is the ellipsoidal height from GPS and *H* is the orthometric height (height above mean sea level). GPS receivers measure *h* relative to a geocentric ellipsoid. To obtain the familiar *H*, they must correct for *N* using a pre-computed geoid model like EGM96. Discrepancies on a ship's GPS are due to tides, atmospheric pressure, and other factors, not geoid undulation.

### Determination and Mathematical Models
Geoid undulation is determined using gravity anomaly data (Δg) and formulas like Stokes' integral. However, requiring global gravity data is impractical. Modern solutions combine satellite data (from missions like GRACE and GOCE) for low-resolution global coverage with terrestrial gravimetry for high-resolution details. Spherical harmonics are used to approximate the geoid's shape. The EGM96 model uses coefficients up to degree and order 360, describing features down to ~55 km. Higher-resolution models like EGM2008 extend to degree 2160.

### Relationship to Mass and Temporal Change
Geoid height variations reflect anomalous mass distributions within Earth. A mass excess (positive gravity anomaly) creates a geoid high, while a deficit creates a low. The largest low is the Indian Ocean Geoid Low (-106 m). Satellite missions now study time-variable geoid signals, revealing changes in hydrologic cycles, ice sheet mass, and postglacial rebound, which helps deduce mantle viscosity.

## Terms
- **Geoid**: The equipotential surface of Earth's gravity field that would coincide with mean sea level if the oceans were at rest and extended through the continents.
- **Reference Ellipsoid**: A mathematically defined, slightly flattened sphere used as a smooth approximation of Earth's shape for calculations.
- **Geoid Undulation (N)**: The height of the geoid above the reference ellipsoid at a given point.
- **Orthometric Height (H)**: The height of a point above the geoid (approximately mean sea level).
- **Ellipsoidal Height (h)**: The height of a point above the reference ellipsoid, as measured by GPS.
- **Geopotential**: The sum of gravitational potential energy and centrifugal potential energy at a point.
- **Gravity Anomaly (Δg)**: The difference between the observed gravity and the theoretical gravity from a reference model.
- **Spherical Harmonics**: Mathematical functions used to model the global shape of the geoid and Earth's gravitational potential.

## Debates and Open Questions
- The precise definition and computation of the geoid remain mathematically challenging, with ongoing improvements in accuracy (e.g., Vaníček's solution achieving millimeter-to-centimeter precision).
- The exact causes of major geoid features, like the North Atlantic Geoid High, are still studied, involving factors like ice-age loading and mantle convection.
- The unreleased status (as of 2025) of the planned EGM2020 model indicates continued international effort to refine geoid representation with better data.