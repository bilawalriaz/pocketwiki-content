# Atomic battery

An atomic battery is a device that generates electricity from the decay of a radioactive isotope. Like a nuclear reactor it draws on nuclear energy, but unlike a reactor it uses no chain reaction. Despite the name, it is not electrochemical and cannot be recharged. Atomic batteries are expensive, but they are long-lived and energy-dense, so they power equipment that must run unattended for years: spacecraft, pacemakers, underwater sensors, and remote scientific stations.

The physics is simple: every decaying nucleus emits charged particles, photons, or heat, and a converter turns some of that emission into electrical current. Most designs reach 0.1–5% efficiency; the best betavoltaic cells reach 6–8%.

## Thermal and non-thermal converters

Engineers divide atomic batteries by how they harvest decay energy.

**Thermal converters** let the radioisotope heat a structure, then use that temperature difference to drive electricity. The dominant type is the radioisotope thermoelectric generator (RTG), which uses the Seebeck effect in thermocouples (a junction of two different metals produces a voltage when one end is hotter than the other), typically made from bismuth telluride or silicon–germanium. RTGs are reliable, silent, and maintenance-free, but their efficiency is low, so they are reserved for spacecraft and defence work. NASA first flew an RTG in 1961, fuelled by plutonium-238. Other thermal approaches include thermionic converters (electrons boil off a hot electrode), thermophotovoltaic cells (infrared glow from a hot surface drives a photocell), and Stirling radioisotope generators, which use a Stirling engine across the same temperature gap. Most remain experimental because of efficiency, cost, or material limits; NASA's advanced Stirling radioisotope generator was cancelled in 2013 after cost overruns.

**Non-thermal converters** capture the radiation before it degrades into heat, so they need no thermal gradient and are easier to miniaturise. They fall into four families:

- *Electrostatic* designs, dating to Henry Moseley's 1913 demonstration, let emitted charged particles accumulate on a conductor until the built-up voltage can be drawn off. Moseley's prototype used a radium source inside a silvered glass globe and produced 150 kV at 0.01 nA.
- *Electromechanical* designs flex a plate under the electrostatic force, then drive a piezoelectric material or a linear generator, producing milliwatt-scale pulses.
- *Radiovoltaic* cells use a semiconductor junction, like a solar cell, but driven by alpha, beta, or gamma particles. Betavoltaic devices, which harvest low-energy beta electrons from tritium or nickel-63, attract the most interest because they cause little radiation damage and need no heavy shielding. In January 2024 the Chinese firm Betavolt announced a coin-sized pilot that uses nickel-63 between two diamond semiconductor layers, producing 100 µW at 3 V with a claimed 50-year life.
- *Radiophotovoltaic* devices first convert particles into light with a scintillator or phosphor, then harvest that light with a normal photovoltaic cell. The radiovoltaic and radiophotovoltaic effects can be stacked to lift efficiency.

## Choosing the isotope

The ideal source emits low-energy beta particles, which minimise the production of penetrating bremsstrahlung X-rays (secondary radiation produced when charged particles are suddenly decelerated) and therefore the shielding weight. Tritium, nickel-63, promethium-147, and technetium-99 are common beta sources; plutonium-238, curium-242, curium-244, and strontium-90 are also used. Plutonium-238 is made by neutron irradiation of neptunium-237 and locked into a stable plutonium-oxide ceramic. Strontium-90 is a cheap fission product but must be immobilised as strontium titanate, which halves its power density. Caesium-137 is rarely used because it is hard to lock into a chemically inert form and is contaminated with other caesium isotopes.

## Applications

The longest-running medical use was the plutonium-238 pacemaker developed by Medtronic and Alcatel. The Numec NU-5 used a 2.5 Ci slug of plutonium-238 (a curie is 37 billion decays per second), and 139 units implanted in the 1970s were expected to outlast the 88-year half-life of their fuel. Production stopped in 1988 when lithium batteries reached a 10-year life without the regulatory burden. Betavoltaic cells are now being revisited for lead-free pacemakers that can be implanted without surgical battery replacement.

Researchers at the University of Wisconsin–Madison have built micro-batteries from polonium or curium that drive oscillating MEMS cantilevers and let the devices communicate by radio. Modern wide-bandgap semiconductor designs (materials such as diamond or gallium nitride that tolerate high-energy particles without degrading) extend the same logic to nano-scale sensors for use inside the body, in space, and in remote locations where no one will ever service a battery.

Source: adapted from "Atomic battery" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Atomic_battery
