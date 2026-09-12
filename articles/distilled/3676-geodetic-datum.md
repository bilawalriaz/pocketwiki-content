# Geodetic datum

## Overview
A geodetic datum is a reference system that provides a consistent framework for determining precise locations on Earth. It is essential for all spatial technologies, including GPS, navigation, surveying, and mapping. Datums define a mathematical model of Earth's shape (like an ellipsoid) and tie it to the physical world through a network of control points, allowing coordinates to be assigned unambiguously.

## Timeline
- **Ancient times** — Greeks develop concepts of latitude/longitude and astronomical measurement methods.
- **1735-1739** — French geodesic missions to Lapland and Peru confirm Earth is oblate (wider at the equator).
- **1816-1855** — Struve Geodetic Arc across Eastern Europe improves estimation of Earth's shape.
- **1802-1871** — Great Trigonometrical Survey of India conducted.
- **1927** — North American Datum (NAD 27) established as the first standard horizontal datum for public use.
- **1929** — Vertical Datum of 1929 (NAVD29) established.
- **1983** — North American Datum of 1983 (NAD 83) released, based on a geocentric origin.
- **1984** — World Geodetic System 1984 (WGS 84) defined for global use, later adopted by GPS.
- **1987** — WGS 84 becomes the reference frame for broadcast GPS orbits.
- **1994** — WGS 84 upgraded in accuracy (WGS 84 (G730)) using GPS measurements.
- **1996** — WGS 84 redefined to align more closely with the ITRF 94 frame (WGS 84 (G873)).

## Body

### What is a Geodetic Datum?
A geodetic datum is a global reference frame for representing positions on Earth. It consists of a model for Earth's shape (a reference ellipsoid or geoid), an origin point where this model is tied to a known location, and a network of precisely measured control points. There are three main types: a **horizontal datum** measures position across the surface (latitude/longitude); a **vertical datum** measures elevation or depth (often relative to mean sea level); and a **three-dimensional datum** combines both. Before GPS, local datums were tied to convenient reference points like the Greenwich Observatory or the nearest coast, leading to significant differences between systems.

### History and Development
The understanding of Earth's spherical shape dates to the ancient Greeks. The Age of Enlightenment brought a demand for greater precision, leading to debates about Earth's exact shape (oblate vs. prolate) and technological innovations like the marine chronometer. Large-scale trigonometric surveys in the 18th and 19th centuries, such as the Great Trigonometrical Survey of India, created regional control networks and improved estimates of Earth's ellipsoid. The first national datums, like NAD 27, emerged in the early 20th century. The advent of satellite geodesy in the later 20th century enabled the creation of more accurate, global datums like WGS 84 and the International Terrestrial Reference Frame (ITRF).

### Horizontal and Vertical Datums
A horizontal datum binds a mathematical reference ellipsoid to the physical Earth, enabling precise latitude and longitude measurements. Regional datums like NAD 27 and NAD 83 use monumented control points, while global datums like WGS 84 are typically geocentric (centered on Earth's mass). A vertical datum provides a reference surface for elevation, such as mean sea level. More accurate models like the Earth Gravitational Model 2008 (EGM2008) are used for precise vertical measurements. Different datums can yield coordinates that differ by hundreds of meters for the same point.

### Datum Shift and Transformation
Because datums use different ellipsoids, origins, and orientations, the same point can have different coordinates in different systems. This difference is called a **datum shift** or **datum transformation**. For example, in Sydney, coordinates can differ by 200 meters between the local AGD and the global WGS 84. Converting coordinates between datums is complex and often requires specialized methods like NADCON for North America, as simple mathematical functions are insufficient due to irregularities in historical survey networks.

### Modern Global Systems: WGS 84 and Plate Tectonics
The World Geodetic System 1984 (WGS 84) is the global datum used by GPS. It has been updated several times (e.g., G730, G873) to improve accuracy and align with the International Terrestrial Reference Frame (ITRF). While WGS 84 is nearly identical to regional datums like NAD 83 and ETRS89, it is a global system. However, because tectonic plates move (50-100 mm per year), coordinates in a global frame change over time. To minimize this for regional mapping, plate-fixed reference frames like NAD 83 (for North America) and ETRS89 (for Europe) are used.

## Terms
- **Geodetic Datum:** A reference system for unambiguously representing positions on Earth.
- **Reference Ellipsoid:** A mathematical model of Earth's shape, defined by a semi-major axis and flattening.
- **Geoid:** The equipotential surface of Earth's gravity field that best fits mean sea level globally.
- **Horizontal Datum:** A datum used to measure positions across Earth's surface (latitude/longitude).
- **Vertical Datum:** A reference surface for measuring elevation or depth.
- **Control Point:** A physically monumented location with precisely known coordinates, used as a reference in a datum.
- **Datum Shift:** The difference in coordinates for the same point when measured in two different datums.
- **WGS 84:** The World Geodetic System 1984, the global datum used by the GPS.
- **ITRF:** The International Terrestrial Reference Frame, a highly accurate global reference frame.
- **Geocentric Datum:** A datum whose origin is at Earth's center of mass.

## Debates and Open Questions
- **Local vs. Global Accuracy:** Local datums can provide a more accurate fit for a specific region than a global datum like WGS 84, but the benefits of a global system often outweigh this local precision.
- **Datum Conversion Complexity:** Converting coordinates between datums is not a simple mathematical process due to the irregular nature of historical survey networks and uneven error distribution.
- **Impact of Plate Tectonics:** Using a global datum means coordinates for a location change over time due to tectonic plate movement, necessitating the use of plate-fixed frames for stable regional mapping.

Source: adapted from "Geodetic datum" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Geodetic_datum
