# Geographic coordinate system

## Overview
A geographic coordinate system (GCS) is a spherical coordinate system used to specify positions on Earth as latitude and longitude. It is the oldest and most widely used spatial reference system, forming the basis for most others. Unlike a Cartesian system, it uses angular measurements on a curved surface, not a flat plane.

## Timeline
- **3rd century BC** — Eratosthenes of Cyrene is credited with inventing the geographic coordinate system.
- **2nd century BC** — Hipparchus of Nicaea improved the system using stellar measurements and lunar eclipses.
- **1st/2nd century AD** — Marinus of Tyre created a world map using coordinates from a prime meridian at the Fortunate Isles.
- **2nd century AD** — Ptolemy's *Geography* used the same prime meridian but measured latitude from the Equator.
- **9th century** — Al-Khwārizmī's work corrected errors in Ptolemy's geography, shifting the prime meridian for Arabic cartography.
- **c. 1300** — Maximus Planudes recovered Ptolemy's text, reviving mathematical cartography in Europe.
- **c. 1407** — Jacopo d'Angelo translated Ptolemy's text into Latin.
- **1884** — The International Meridian Conference adopted the Greenwich meridian as the global prime meridian.
- **1911** — France adopted Greenwich Mean Time, replacing local Paris Observatory time.

## Body

### Latitude and Longitude
Latitude (φ) is the north-south angle from the Equator. Its definition varies by system: astronomical (using a plumb line), geodetic (using a normal to an ellipsoid), or geocentric (using Earth's center). Lines of equal latitude are called parallels. Longitude (λ) is the east-west angle from a reference meridian. The international prime meridian is defined by the Royal Observatory in Greenwich. The combination of latitude and longitude specifies any surface location, forming a grid called a graticule. The system's origin (0°, 0°) is in the Gulf of Guinea.

### Geodetic Datum
A geodetic datum binds a mathematical model of Earth's shape (an ellipsoid) to the physical planet, allowing precise coordinate measurement. A horizontal datum is for latitude/longitude; a vertical datum is for elevation. Different datums yield different coordinates for the same point, sometimes by hundreds of meters. Global datums like WGS 84 (used for GPS) and ITRF represent the whole Earth. Regional datums, like OSGB36 for Britain, fit the ellipsoid to a specific area. Earth's surface moves due to tectonics and other forces, which is significant for global datums but less so for regional ones.

### Length of a Degree
The physical distance covered by one degree of latitude or longitude varies. On the WGS 84 spheroid at the Equator, one degree of latitude is about 110.6 km, and one degree of longitude is about 111.3 km. The length of a degree of longitude decreases toward the poles, while the length of a degree of latitude changes only slightly. Formulas exist to calculate these distances precisely based on latitude.

### Alternative Encodings
To simplify communication, latitude-longitude pairs can be encoded into alphanumeric strings or words. Examples include the Maidenhead Locator System (for radio), Open Location Code ("Plus Codes"), Geohash, and What3words. These are alternative representations, not distinct coordinate systems.

## Terms
- **Geographic Coordinate System (GCS):** A spherical system using latitude and longitude to define positions on Earth.
- **Geodetic Datum:** A reference system that ties a mathematical model of Earth's shape to the physical planet for precise measurement.
- **Ellipsoid:** A mathematical model approximating Earth's shape as a slightly flattened sphere.
- **Prime Meridian:** The reference meridian (0° longitude) from which east-west angles are measured; internationally set at Greenwich.
- **Graticule:** The network of latitude and longitude lines on a map.
- **Parallels:** Lines of constant latitude, which are circles parallel to the Equator.
- **Meridians:** Lines of constant longitude, which are halves of great circles converging at the poles.
- **WGS 84:** The World Geodetic System 1984, a global datum and ellipsoid used for GPS.
- **Helmert Transformation:** A mathematical method used to convert coordinates between different datums.

## Debates and Open Questions
The source notes that while the Greenwich meridian is the international standard, some organizations, like France's Institut national de l'information géographique et forestière, continue to use other meridians for internal purposes. The choice of datum remains critical, as using a global datum makes small, continuous movements of the Earth's surface (like continental drift) statistically significant.

Source: adapted from "Geographic coordinate system" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Geographic_coordinate_system
