# Parton (particle physics)

In particle physics, a **parton** is one of the point-like constituents that make up a hadron, a composite particle such as a proton or neutron bound by the strong force. The parton model treats a high-energy hadron as a loose cloud of these constituents, letting physicists predict violent collisions by assuming each constituent scatters independently.

## Origins

Richard Feynman proposed the parton model in 1969 to interpret the cascades of debris produced in high-energy hadron collisions. James Bjorken and Emmanuel Paschos soon applied it to electron–proton deep inelastic scattering, where an electron strikes a proton hard enough to shatter it. Later, when Bjorken scaling was observed, the quark model was validated, and asymptotic freedom in quantum chromodynamics (QCD) was confirmed, partons were identified with quarks and gluons. The model remains a justifiable approximation at high energies. Murray Gell-Mann, who named quarks, preferred the term "put-ons". Leonard Susskind used partons in 1994 to model holography.

## What partons are

At low resolution, a baryon contains three valence partons (quarks) and a meson contains two (a quark and an antiquark). At higher resolution, additional sea partons appear: transient quark–antiquark pairs and extra gluons that emerge from the vacuum when the hadron is probed finely. Just as accelerated electric charges radiate photons, accelerated coloured partons radiate gluons. Because gluons themselves carry colour charge, each emitted gluon can radiate further gluons, producing a self-multiplying parton shower.

The hadron is described in a reference frame where it carries almost infinite momentum, valid at high energies. Time dilation slows the internal motion, and Lorentz contraction flattens the hadron's charge distribution, so an incoming probe sees the partons as frozen and scatters off each one independently and instantly.

## Scale dependence and parton distribution functions

Partons are defined relative to a length scale set by the probe: shorter wavelengths (higher momentum transfer Q) resolve finer detail. At one scale a parton may appear as a single quark; at a smaller scale that same quark resolves into a quark plus gluons and sea quarks. The number of effective partons inside a hadron therefore grows with momentum transfer.

A parton distribution function (PDF) gives the probability density for finding a parton carrying a fraction x of the parent hadron's longitudinal momentum at resolution scale Q². Because partons cannot be isolated as free particles, their distribution is non-perturbative and must be fitted to experimental data. Major fitted sets include ABM, CTEQ, GRV/GJR, HERA, MSHT, and NNPDF, all delivered through the LHAPDF Fortran/C++ library. The variation of PDFs with Q² is predictable by QCD, and the predictions match experiment well, a key confirmation of the theory. A 2013 result by Xiangdong Ji showed PDFs can also be calculated directly using lattice QCD with the large-momentum effective field theory approach.

Generalized parton distributions (GPDs) extend PDFs by adding transverse momentum and spin as variables. In the forward limit, where the extra variables vanish, GPDs reduce to ordinary PDFs, but they also encode form factors and the Ji sum rule, which relates their integrals to the total angular momentum carried by quarks and gluons inside the proton. Early names were "non-forward", "non-diagonal", or "skewed" parton distributions. They are accessed through exclusive processes such as deeply virtual Compton scattering, where every final-state particle is detected.

## Simulation

Parton showers are central to computational particle physics, especially at the Large Hadron Collider. Monte Carlo event generators such as PYTHIA and HERWIG evolve a hard scattering into a parton shower down to a fixed scale, at which point hadronization, the recombination of partons into observable hadrons, takes over. These simulations calibrate detectors and interpret collision data.

Source: adapted from "Parton (particle physics)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Parton_%28particle_physics%29
