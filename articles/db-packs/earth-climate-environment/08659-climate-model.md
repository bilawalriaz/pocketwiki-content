# Climate model

A climate model is a set of mathematical equations, run on a computer, that simulates how the atmosphere, ocean, land surface, and ice exchange energy, mass, and momentum. Models apply the laws of fluid motion, thermodynamics, and radiative transfer, divide the planet into a three‑dimensional grid, and solve the equations forward in time at each cell while exchanging information with neighbours. The output is a synthetic climate of temperature, wind, humidity, currents, and ice, used to project future climate and to study how human activity has altered specific weather events.

## How the equations work

The energy balance of the whole planet is the simplest possible model. Incoming sunlight is short‑wave radiation (visible and near‑infrared); outgoing Earth radiation is long‑wave (far‑infrared). When the two are equal, the climate is in equilibrium. The zero‑dimensional form is

(1 − a) S π r² = 4 π r² ε σ T⁴,

where S is the solar constant (about 1367 W·m⁻²), r is Earth's radius, a is planetary albedo (about 0.3), σ is the Stefan–Boltzmann constant, and ε is the effective emissivity of surface plus atmosphere combined. For Earth's measured surface temperature of roughly 288 K, ε works out to about 0.61. Surface emissivity alone is 0.96–0.99, but clouds (covering about half the planet at roughly 258 K) average around 0.5, pulling the planet‑wide value down. With no geography, the equation still shows that temperature responds to changes in solar input, reflectivity, or atmospheric emissivity.

Adding a single atmospheric layer above the surface gives a one‑layer model that better matches observed surface and tropospheric temperatures and shows how greenhouse gases warm the surface while cooling the upper atmosphere. Svante Arrhenius published a version of this calculation in 1896.

A one‑dimensional radiative‑convective model adds two transport processes: upwelling and downwelling radiation through absorbing and emitting layers, and convective heat transport in the lower troposphere. These models reproduce the observed fall of temperature with altitude and the surface warming that follows a rise in carbon dioxide, and have been used to study feedbacks such as ice–albedo coupling.

Extending the picture horizontally produces zonal‑average energy balance models, exemplified by the Budyko–Sellers model of 1969. These treat the planet as latitude bands and showed that positive feedbacks, such as ice reflecting more sunlight as it grows, are central to climate sensitivity.

The most physically complete tools are general circulation models (GCMs). An atmospheric GCM solves the Navier–Stokes equations on a rotating sphere with thermodynamic terms for radiation and latent heat. Coupled to an ocean GCM, a sea‑ice model, and a land‑surface model, the result is an atmosphere–ocean GCM (AOGCM), the workhorse of modern climate projection. AOGCMs that additionally include the carbon cycle, land‑use change, and atmospheric chemistry are called Earth system models. Finer meshes used for cloud‑resolving runs require exascale machines such as Frontier (about 29 MW), which can simulate one year of climate per day of wall‑clock time.

## Simpler alternatives

Between the single equation and a multi‑million‑line GCM sit several intermediate tools. Box models reduce the climate to a few reservoirs connected by fluxes, governed by conservation of mass and energy; Henry Stommel's 1961 two‑box ocean was the first. Models of intermediate complexity (EMICs) such as Climber‑3 trade spatial resolution for speed, allowing long integrations and many ensemble members. Network models treat climate fields as a graph where grid points are nodes and links encode statistical similarity between time series, a way to find large‑scale patterns that explicit physics may miss. Smaller models can sometimes be solved analytically, isolate a single feedback, or run thousands of times to explore uncertainty, complementing the physically detailed GCM.

## Processes the equations must capture

Radiation, with short‑wave in and long‑wave out, modulated by clouds, aerosols, and greenhouse gases. Fluid motion, with winds and ocean currents driven by pressure gradients, the Coriolis effect, and buoyancy. Heat transfer by radiation, conduction, and convection, including water‑vapour transport, since humidity sets atmospheric emissivity. Surface exchanges of evaporation, precipitation, and runoff, with heat storage in the deep ocean setting the slow timescale of climate variability. External drivers such as changes in the Sun, volcanic aerosols, and human forcing from greenhouse gases and aerosols. Parametrization, where processes smaller than a grid cell (cloud formation, raindrop fall, turbulence) are represented by simplified formulae, is the leading source of spread between models.

## Brief history and confidence

Norman Phillips built the first successful numerical climate model in 1956. The first coupled atmosphere–ocean model was developed at NOAA's Geophysical Fluid Dynamics Laboratory in the late 1960s. By 1975, Syukuro Manabe and Richard Wetherald had a three‑dimensional model in which doubling CO₂ raised global temperature by roughly 2 °C, and several independent groups produced similar results. From the 1980s, models added interactive vegetation and soil, and the Community Atmosphere Model became widely shared. The Coupled Model Intercomparison Project, running since 1995, organises community experiments, and pattern agreement between successive phases and observations has improved steadily. Meta‑analyses find past models have generally been accurate but slightly conservative, under‑predicting observed warming. The 2010 IPCC assessment stated considerable confidence in model‑based quantitative estimates, higher for temperature than for precipitation.

Source: adapted from "Climate model" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Climate_model
