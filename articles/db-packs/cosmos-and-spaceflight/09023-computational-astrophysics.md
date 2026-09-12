# Computational astrophysics

Computational astrophysics is the branch of research that uses numerical methods and high‑performance computing to model objects and processes in space. It is both a sub‑field of theoretical astrophysics and an interdisciplinary activity that borrows from computer science, applied mathematics, and physics. Most practitioners enter through an applied‑mathematics or astrophysics PhD programme.

## Why computation is essential

Many astrophysical problems cannot be solved analytically. Equations governing magnetised gases, radiation, self‑gravity, and curved spacetime usually have no closed‑form answer, and the regimes involved (supernovae, galaxy mergers, neutron‑star interiors) cannot be reproduced in a laboratory. Simulations are frequently the sole means of studying stellar collisions, galaxy mergers, and black‑hole interactions.

## Core methods

The methods used fall into a small number of families:

- **N‑body methods** for tracking the gravitational evolution of many particles, from star clusters to galaxies.
- **Grid‑based fluid solvers**, including adaptive mesh refinement codes, for gases in situations like stellar structure or accretion disks.
- **Grid‑free or particle methods** for fluids, of which smoothed particle hydrodynamics (SPH) is the leading example.
- **Particle‑in‑cell (PIC) and particle‑mesh (PM)** techniques for plasmas with electric and magnetic fields.
- **Monte Carlo methods** for problems driven by random processes such as radiation transport.
- **Numerical analysis techniques** for the ordinary and partial differential equations that describe the underlying physics.

These solvers are rarely used in isolation. A simulation of a supernova, for example, typically couples a fluid code to radiative transfer, Newtonian or relativistic gravity, and nuclear reaction networks.

## Application areas

Computational methods underpin several well‑established areas of astrophysics: magnetohydrodynamics, astrophysical radiative transfer, stellar and galactic dynamics, and astrophysical fluid dynamics. Numerical relativity is a newer sub‑field that simulates strong‑field gravity, including binary black‑hole mergers. Fluid simulations are particularly important because gases are involved in most phenomena of astronomical interest; the same coupled models that describe a supernova explosion are adapted to relativistic jets, active galactic nuclei, gamma‑ray bursts, planetary formation, and the structure and evolution of stars and galaxies.

## Hardware and software infrastructure

The required computing power is large enough that a desktop machine is rarely sufficient. Supercomputers and dedicated clusters are standard, and graphics processing units (GPUs) are increasingly used; as of 2010 the DEGIMA N‑body code reached roughly 190 teraflops on a cluster of GPUs. A historically notable special‑purpose architecture is the Japanese GRAPE (Gravity Pipe) hardware, built specifically to accelerate gravitational N‑body calculations.

Software tends to be community‑maintained. Most codes are either N‑body packages or fluid solvers. Representative examples include the N‑body packages ChaNGa, MODEST, nbodylab, and Starlab, and the fluid/gravity codes GADGET, SWIFT, RAMSES, ENZO, FLASH, and ART. The AMUSE framework takes a different approach: it acts as an interface, sometimes called Noah's Ark, that lets a user mix specialist modules for stellar dynamics, stellar evolution, hydrodynamics, and radiative transport within a single simulation.

## Community and recognition

Computational work is now organised at the international level. Important initiatives include the US Department of Energy SciDAC collaboration for astrophysics, the now defunct European AstroSim network, and the Virgo Consortium, which focuses on large cosmological simulations. In August 2015 the International Astronomical Union inaugurated Commission C.B1 on Computational Astrophysics, formally recognising computing as a driver of astronomical discovery. Large flagship runs such as the Millennium, Eris, and Bolshoi cosmological simulations serve as standard reference points in cosmology, and the defining limit of the field is set not by the equations but by the available compute: more demanding physics, finer resolution, and bigger dynamic ranges all translate directly into the need for faster machines and more efficient algorithms.

Source: adapted from "Computational astrophysics" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Computational_astrophysics
