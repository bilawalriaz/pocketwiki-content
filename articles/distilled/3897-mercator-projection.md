# Mercator projection

## Overview
The Mercator projection is a conformal cylindrical map projection created by Gerardus Mercator in 1569, designed to aid marine navigation by representing lines of constant compass bearing (rhumb lines) as straight lines. While revolutionary for navigation, its use for general world maps is controversial because it severely distorts the size of landmasses far from the equator, making them appear much larger than they are.

## Timeline
- **13th c.** — Earliest extant portolan charts with windrose networks appear.
- **1511** — Erhard Etzlaub engraves "compass maps" possibly using a similar projection.
- **1537** — Pedro Nunes describes the rhumb line and proposes an equirectangular atlas.
- **1569** — Gerardus Mercator publishes his world map introducing the Mercator projection.
- **1599** — Edward Wright publishes the first accurate tables for constructing the projection.
- **c. 1645** — Henry Bond publicizes the first mathematical formulation.
- **Mid-18th c.** — Invention of the marine chronometer allows the projection to be fully adopted for navigation.
- **19th c.** — The Mercator projection becomes dominant for commercial and educational world maps.
- **1972** — Arno Peters proposes the Gall–Peters projection as an equal-area alternative.
- **2005** — Google Maps begins using the Web Mercator variant for online mapping.
- **2017** — Google Maps drops the Mercator projection for desktop world views.

## Body

### History and Development
The projection's development built on earlier work, including the rhumb line concept described by Pedro Nunes in 1537. Gerardus Mercator introduced it in 1569 with a large world map intended for sailors. However, its mathematical construction was not published until Edward Wright's work in 1599. The projection was ahead of its time; practical navigation required the later invention of the marine chronometer and knowledge of magnetic declination, leading to its full adoption in the mid-18th century. It became the standard for world maps in the 19th century but faced criticism for its size distortions, leading to a decline in the 20th century. Its use resurged in the 21st century with the advent of Web Mercator for online mapping.

### Properties and Distortion
The Mercator projection is conformal, meaning it preserves angles and shapes locally. It is constructed by projecting the globe onto a cylinder tangent at the equator. A key property is that rhumb lines (paths of constant bearing) appear as straight lines, which is ideal for navigation. However, this conformality causes extreme areal distortion at high latitudes. The linear scale increases with latitude, making landmasses like Greenland and Antarctica appear vastly larger than they are relative to equatorial regions like Africa. The poles cannot be shown, as the scale becomes infinite.

### Uses and Criticisms
The projection remains the standard for marine charts due to its navigational utility. It is also widely used for local-area web maps (Web Mercator) where distortion is minimal at high zoom levels. For general world maps, it has been heavily criticized for misrepresenting the relative sizes of continents, which some argue influences perceptions of global importance. Alternatives like the equal-area Gall–Peters projection have been promoted, but a 1989 resolution by North American geographical groups discouraged using any cylindrical projection for general-purpose world maps.

### Mathematical Formulation
For a spherical Earth, the projection's formulas are: x = R(λ − λ₀) and y = R ln[tan(π/4 + φ/2)], where R is the map scale factor, λ is longitude, and φ is latitude. The scale factor k = sec φ, meaning it increases with latitude. For an ellipsoidal Earth model, the formulas are modified to maintain conformality, but the correction is small (less than 1%). The projection must be truncated at high latitudes (e.g., ±85.05113° for Web Mercator) as y approaches infinity at the poles.

## Terms
- **Conformal projection**: A map projection that preserves angles and shapes locally, but not area.
- **Cylindrical projection**: A map projection where the Earth's surface is projected onto a cylinder.
- **Rhumb line (loxodrome)**: A path of constant compass bearing on the Earth's surface.
- **Scale factor (k)**: The ratio of distance on the map to true distance on the Earth; for Mercator, k = sec φ.
- **Web Mercator**: A variant of the Mercator projection used by online mapping services, truncated at high latitudes.
- **Equal-area projection**: A map projection that preserves the relative area of features, unlike the Mercator.
- **Gudermannian function**: A function linking circular and hyperbolic angles, used in Mercator's mathematical formulation.

## Debates and Open Questions
The primary debate concerns the Mercator projection's suitability for general world maps due to its severe areal distortion, which critics argue perpetuates a Eurocentric worldview by inflating the size of northern continents. The 1989 resolution by North American geographical groups formally discouraged its use for this purpose. The projection's resurgence in web mapping has renewed discussions about its visual impact. There is also historical debate about possible precursors, such as whether 13th-century portolan charts or Chinese star charts used similar projections, though evidence for this is lacking.

Source: adapted from "Mercator projection" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Mercator_projection
