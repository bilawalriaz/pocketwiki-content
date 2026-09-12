# Astronomical seeing

In astronomy, *seeing* is the blurring, twinkling, and shimmering of celestial objects caused by turbulence in Earth's atmosphere. Without an atmosphere, a large telescope would resolve a point-like star into a sharp *Airy diffraction pattern* (a tiny disk surrounded by faint rings, set by the telescope's aperture). Through the atmosphere, the same star breaks into dancing *speckles* that change faster than the eye can follow; in any long-exposure image those speckles average into a fuzzy disc called the *seeing disc*. Seeing is the main reason ground-based telescopes usually cannot reach the fine resolution their size should allow.

The atmosphere acts as many small, churning pockets of air, each with a slightly different temperature and therefore a different *refractive index* (the degree to which the air slows light). Each pocket bends incoming light by a different amount, distorting the wavefront. Because the pockets move and change, the wavefront arriving at the telescope jitters more than a hundred times per second, scrambling the image on the same timescale.

## Measuring seeing

Astronomers describe seeing with three linked quantities.

The **seeing disc diameter**, measured as the *full width at half maximum* (FWHM) of the star's blurred image, is quoted in arcseconds. A 1.0″ disc is a decent night at a typical site; 0.4″ counts as excellent, and the best mountaintop observatories on isolated peaks such as Mauna Kea or La Palma approach this. Warm, gusty, or cloudy nights are worse, because rising warm air (convection) and shear near the ground add turbulence. Stable air that has travelled over ocean or high above cloud, arriving without touching the ground, is best.

The **Fried parameter *r*₀** is the size of a typical coherent air pocket. It is defined so that a telescope of diameter *r*₀ would give the same resolution as a much larger one limited only by the atmosphere. At good sites, *r*₀ is 10–20 cm at visible wavelengths and 20–40 cm in the near-infrared I-band. If a telescope's aperture is smaller than *r*₀, diffraction dominates and the image sharpens as the mirror grows. Once the aperture exceeds *r*₀, resolution stops improving: the atmosphere has set a ceiling equivalent to a 10–20 cm space telescope. *r*₀ also sets the spacing of actuators needed in an adaptive-optics system.

The **Greenwood time *t*₀** is how long the turbulence pattern stays roughly the same, typically a few tens of milliseconds. Adaptive-optics systems must correct faster than this to keep up with the changing wavefront.

The **Cₙ² profile** records the turbulence strength as a function of altitude. It is used to decide what kind of adaptive optics to build or whether a new site is worth developing, and is measured by instruments such as SCIDAR, SLODAR, MASS, and balloon-borne temperature sensors.

## Why larger telescopes hit a wall

Because *r*₀ is small, a 7–8 m mirror contains many turbulence cells across its pupil. Light passing through different cells interferes, and a short-exposure image fractures into the speckle patterns seen in high-magnification views. Numerical models based on the **Kolmogorov model of turbulence** (developed by Tatarski from Kolmogorov's 1941 work) describe how the phase variance between two points in the wavefront grows with their separation, and predict the speckle statistics that are observed. Real turbulence departs from the simple Gaussian assumption through *intermittency*, which is sporadic bursts of stronger mixing.

## How astronomers fight seeing

Four strategies are in use. **Space telescopes** (Hubble being the best-known example) escape the atmosphere entirely, at the cost of a much smaller mirror and a much higher price. **Speckle imaging** and **lucky imaging** freeze the distortion by taking thousands of very short exposures, then combine the sharpest few; lucky imaging works well on small amateur telescopes but breaks down on the largest mirrors, where too many turbulence cells cover the pupil. **Optical interferometers** combine light from several separate mirrors to mimic a much larger aperture and reach the highest angular resolution, but only on bright sources. **Adaptive optics** is the dominant solution on large telescopes: a deformable mirror, driven hundreds of times per second, reshapes the wavefront to cancel the measured distortion. The best systems, such as SPHERE on ESO's Very Large Telescope and GPI on Gemini, reach a Strehl ratio of 90% at 2.2 µm, meaning 90% of the light lands in the diffraction-limited core of the image. Because adaptive-optics correction is only accurate within a very small region of sky around a bright reference star, astronomers create an artificial one with a powerful laser when no natural guide star is available nearby. Multiconjugate adaptive optics extends the corrected field by using several deformable mirrors conjugated to different atmospheric layers.

Source: adapted from "Astronomical seeing" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Astronomical_seeing
