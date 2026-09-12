# Projected coordinate system

A projected coordinate system (also called a planar coordinate system or grid reference system) represents Earth locations using Cartesian coordinates (x, y) on a flat surface created by a map projection. Each system is defined by four components: a map projection with specific parameters, a geodetic datum (which includes a reference ellipsoid) that binds coordinates to real Earth locations, an origin point, and a unit of measure (usually the meter or US foot). Hundreds of such systems exist for different regions and purposes.

## History and purpose

The first standardized systems appeared in the 20th century. The US State Plane Coordinate System (1930s) and the British National Grid (1938) were created because distance and area calculations are far simpler in Cartesian coordinates than in the spherical trigonometry of latitude and longitude. World War II accelerated adoption: soldiers needed to report positions quickly, leading to printed grid maps. Theater-specific projections caused confusion, motivating the Universal Transverse Mercator (UTM) system—possibly adapted from a German Wehrmacht design—and the Military Grid Reference System (MGRS) as an alphanumeric encoding for UTM coordinates. After the war, UTM spread in scientific work. Because UTM zones ignore political boundaries, many countries developed national grids. These proliferated in the 1980s with the rise of geographic information systems (GIS), which compute efficiently in Cartesian geometry. Today, global GIS datasets and satellite navigation have increased use of geographic coordinates, but projected systems remain standard in the spatial data infrastructures of cities, counties, states, and small countries.

## System specification

The EPSG Geodetic Parameter Dataset publishes coordinate system definitions in machine-readable form and underpins most GIS software. A projected spatial reference system has three parts:

1. **Cartesian framework**: a planar surface with an origin, orthogonal axes, and a unit of measure. Locations are measured as an easting (x) and northing (y).
2. **Map projection**: converts latitude and longitude into (x, y) coordinates. Conformal projections (preserving local angles) are preferred. Common types include transverse Mercator (UTM, British National Grid, some State Plane zones), Lambert conformal conic (other State Plane zones), and Mercator (Swiss coordinate system). Each projection requires parameters such as the natural origin, false easting/northing, scale factor, and standard parallels.
3. **Geodetic datum**: controls the underlying latitude/longitude framework. The same projection formulas produce different coordinates for different datums—for example, "UTM NAD83 Zone 14N" versus "UTM NAD27 Zone 14N"—because the datum shifts the latitude and longitude values.

## Easting, northing, and false origin

Every projection has a natural origin where the ellipsoid and map surface coincide, yielding (0, 0). To avoid negative coordinates, a false origin is defined by false easting and false northing offsets. In UTM, each northern zone’s origin is placed 500 km west of the central meridian, so all points in the zone have positive easting and northing values.

## Grid north

Grid north is the direction along a projection’s grid lines, distinct from true north (toward the North Pole) and magnetic north (compass direction). On Ordnance Survey maps, grid north matches true north on the central meridian (2°W) and diverges slightly toward the edges—a difference small enough to ignore for most navigation. At the South Pole, grid north conventionally follows the Prime Meridian. Grid north solves a practical problem: meridians converge at the poles, making true east/west directions change rapidly (analogous to gimbal lock).

## Grid reference encodings

Locations are reported as easting-first, northing-second pairs. The peak of Mount Assiniboine (UTM Zone 11) is (0594934mE, 5636174mN). Such precise numbers are easy for computers but hard for humans, so shortening schemes exist:

- **Truncated references** drop leading or trailing digits when context supplies them.
- **Alphanumeric encodings** partition the world into lettered grid squares. MGRS encodes the Mount Assiniboine coordinate as 11U NS 949 361 (longer variants add precision). The Ordnance Survey National Grid divides Great Britain into 100 km squares with two-letter codes, then uses numerical references within each square.

Precision scales with digit count. A six-figure UK grid reference identifies a 100 m square; eight figures give 10 m; ten figures give 1 m. Each additional pair of digits improves precision by a factor of ten. GPS receivers commonly output ten-digit references; converting to a standard six-figure reference requires omitting specific digits, not simply truncating.

## Major examples

- **Universal Transverse Mercator (UTM)**: 60 zones, each 6° of longitude wide, each with its own transverse Mercator projection.
- **Universal Polar Stereographic (UPS)**: Two systems covering the Arctic and Antarctica using a stereographic projection.
- **Ordnance Survey National Grid (OSNG)**: Transverse Mercator centered on 2°W, covering Great Britain with a two-letter 100 km square encoding.
- **State Plane Coordinate System (SPCS)**: Over 120 zones covering US states or portions thereof, using transverse Mercator or Lambert conformal conic.
- **Swiss coordinate system (LV95)**: Covers Switzerland with a Mercator projection.
- **Irish Transverse Mercator (ITM)**: Covers the island of Ireland, jointly defined by Ireland and the UK.