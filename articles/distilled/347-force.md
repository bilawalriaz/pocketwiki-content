# Force

## Overview
In physics, **force** is a vector quantity (magnitude and direction) that causes an object to change its velocity (accelerate), deform, or resist other forces. The SI unit is the **newton (N)**. Force is central to classical mechanics, codified by Newton's three laws of motion (1687), which describe inertia, the quantitative link between net force and momentum change ($F=dp/dt$), and action-reaction pairs. In modern physics, forces are understood as manifestations of four **fundamental interactions**—strong, electromagnetic, weak, and gravitational—mediated by gauge bosons. General relativity reinterprets gravity not as a force but as spacetime curvature, while quantum field theory treats forces as momentum exchange via virtual particles.

## Timeline
- **Antiquity** — Aristotle and Archimedes study force in simple machines and cosmology; Aristotle erroneously claims a force is required to sustain motion.
- **17th Century** — Galileo Galilei disproves Aristotelian motion; shows objects retain velocity unless acted upon (e.g., by friction), establishing inertia.
- **1687** — Isaac Newton publishes *Philosophiæ Naturalis Principia Mathematica*, defining three laws of motion and universal gravitation.
- **1784** — Charles-Augustin de Coulomb describes the electrostatic force (inverse-square law).
- **1864** — James Clerk Maxwell unifies electricity and magnetism; predicts electromagnetic waves at light speed.
- **1905** — Einstein's special relativity revises momentum ($p = \gamma m_0 v$), showing force requirements diverge at near-light speeds.
- **1915** — Einstein's general relativity redefines gravity as spacetime curvature, not a force.
- **1970s–1980s** — High-energy experiments confirm electroweak unification (weak and electromagnetic forces as aspects of one interaction).
- **Modern** — Standard Model describes three forces (strong, electromagnetic, weak) via gauge boson exchange; gravity remains described by general relativity.

## Body

### Pre-Newtonian Concepts
Ancient philosophers recognized force in simple machines (mechanical advantage: less force over greater distance). **Aristotle** distinguished "natural motion" (elements seeking natural place, e.g., heavy bodies falling) from "violent motion" (requiring continuous force). He struggled to explain projectiles, proposing displaced air pushes them forward. **Archimedes** formulated buoyant forces and lever principles. These views persisted until **Galileo** (17th century), influenced by the medieval *impetus* concept, rolled balls down inclines to show acceleration due to gravity is mass-independent and that a force is needed to *change* motion, not sustain it—a direct refutation of Aristotle.

### Newtonian Mechanics
**Newton's First Law (Inertia):** An object at rest stays at rest; an object in uniform straight-line motion continues unless acted upon by a net force. This defines **inertial frames** (observers not accelerating).
**Newton's Second Law:** Net force equals the rate of change of momentum: $\mathbf{F} = d\mathbf{p}/dt$. For constant mass $m$, this simplifies to $\mathbf{F} = m\mathbf{a}$. Force and acceleration are vectors; equilibrium implies zero net force.
**Newton's Third Law (Action-Reaction):** If body 1 exerts $\mathbf{F}_{1,2}$ on body 2, body 2 exerts $\mathbf{F}_{2,1} = -\mathbf{F}_{1,2}$ on body 1. Forces are interactions between distinct bodies; internal forces in a closed system sum to zero, conserving total linear momentum.
**Defining Force:** Textbooks sometimes use $F=ma$ as a definition, but this requires an inertial frame and constitutive force laws (e.g., Hooke's law) for predictive power. Ernst Mach and Walter Noll sought explicit operational definitions.

### Combining Forces
Forces are **vectors**; they add via the parallelogram rule. The **resultant (net force)** is the vector sum. **Free-body diagrams** track forces graphically. Forces resolve into **orthogonal components** (independent axes), simplifying calculation.
**Equilibrium:** Resultant force is zero.
*   **Static:** Object at rest (e.g., gravity balanced by normal force). Historically measured via scales/balances; yielded Hooke's law, Boyle's law, Archimedes' principle.
*   **Dynamic:** Object moves at constant velocity (zero net force, e.g., applied force balances kinetic friction). Galileo realized constant velocity is equivalent to rest (no absolute rest frame), contradicting Aristotle.

### Examples of Forces in Classical Mechanics
*   **Gravity:** Newton unified terrestrial fall ($F=mg$, $g \approx 9.81\,\text{m/s}^2$) with celestial motion. Universal law: $\mathbf{F} = -G m_1 m_2 / r^2 \, \hat{\mathbf{r}}$. $G$ measured by Cavendish (1798). Predicted Neptune via perturbation analysis.
*   **Electromagnetic:** Coulomb's law (1784) for static charges. **Electric field** $\mathbf{E} = \mathbf{F}/q$; **magnetic field** $\mathbf{B}$. **Lorentz force**: $\mathbf{F} = q(\mathbf{E} + \mathbf{v} \times \mathbf{B})$. Maxwell's equations (1864) unified fields, predicted light as EM wave.
*   **Normal Force:** Contact force perpendicular to interface; enforces solidity (Newton's 3rd law).
*   **Friction:** Opposes relative motion. **Static friction** $F_{sf} \le \mu_{sf} F_N$ (matches applied force up to limit). **Kinetic friction** $F_{kf} = \mu_{kf} F_N$ (constant, $\mu_{kf} < \mu_{sf}$).
*   **Tension:** Transmitted via ideal strings (massless, inextensible); multiplied by pulleys (mechanical advantage).
*   **Spring (Hooke's Law, 1676):** $F = -k \Delta x$ (restoring force proportional to displacement).
*   **Centripetal:** Net force for uniform circular motion: $F = -mv^2/r \, \hat{\mathbf{r}}$ (directed inward, changes direction only).
*   **Continuum Mechanics:** For extended bodies. Pressure gradient: $\mathbf{F}/V = -\nabla P$. **Viscous drag (Stokes')**: $\mathbf{F}_d = -b\mathbf{v}$. **Stress tensor** $\sigma = F/A$ describes normal (pressure) and shear forces.
*   **Fictitious Forces:** Appear in non-inertial (accelerating) frames (centrifugal, Coriolis). In general relativity, gravity becomes a fictitious force due to curved spacetime.

### Concepts Derived from Force
*   **Torque ($\boldsymbol{\tau}$):** Rotational analog of force. $\boldsymbol{\tau} = \mathbf{r} \times \mathbf{F}$. Newton's laws yield $\boldsymbol{\tau} = I\boldsymbol{\alpha}$ (moment of inertia $I$, angular acceleration $\boldsymbol{\alpha}$) and $d\mathbf{L}/dt = \boldsymbol{\tau}$ (angular momentum $\mathbf{L}$). Conservation of angular momentum follows from 3rd law.
*   **Yank:** Rate of change of force, $\mathbf{Y} = d\mathbf{F}/dt$ (used in biomechanics/robotics).
*   **Kinematic Integrals:**
    *   **Impulse** $\mathbf{J} = \int \mathbf{F}\,dt = \Delta \mathbf{p}$ (Impulse-Momentum Theorem).
    *   **Work** $W = \int \mathbf{F} \cdot d\mathbf{x} = \Delta K$ (Work-Energy Theorem).
    *   **Power** $P = dW/dt = \mathbf{F} \cdot \mathbf{v}$.
*   **Potential Energy:** For **conservative forces**, $\mathbf{F} = -\nabla U$. Energy converts between kinetic and potential; total mechanical energy conserved. Examples: gravity, electromagnetic, spring force.
*   **Nonconservative Forces:** Friction, drag, tension, compression. Macroscopically dissipative (increase entropy/heat); microscopically result from conservative forces (statistical mechanics).

### Units
*   **SI:** **newton (N)** = $1\,\text{kg}\cdot\text{m}\cdot\text{s}^{-2}$.
*   **CGS:** **dyne** = $1\,\text{g}\cdot\text{cm}\cdot\text{s}^{-2}$ ($1\,\text{N} = 10^5\,\text{dyn}$).
*   **English (fps):** **pound-force (lbf)** = force on 1 lb mass at $g=9.80665\,\text{m/s}^2$. **slug** = mass accelerated $1\,\text{ft/s}^2$ by 1 lbf. **poundal** = force to accelerate 1 lb mass at $1\,\text{ft/s}^2$.
*   **Metric (deprecated):** **kilogram-force (kgf)** = force on 1 kg at standard $g$.

### Revisions of the Force Concept
**Special Relativity:** $F = dp/dt$ holds, but momentum redefined: $\mathbf{p} = \gamma m_0 \mathbf{v}$, $\gamma = 1/\sqrt{1-v^2/c^2}$. Force required for same acceleration increases as $v \to c$ ($F_x = \gamma^3 m a_x$, $F_{y,z} = \gamma m a_{y,z}$). Four-vector form $F^\mu = m A^\mu$ restores $F=ma$ structure.
**Quantum Mechanics:** Interactions described via energy, not force. **Ehrenfest theorem** links quantum expectation values to classical $F = -\nabla U$, but resemblance breaks down with strong quantum effects. **Uncertainty principle** and **Pauli exclusion** create degeneracy pressure, balancing electromagnetic attraction for atomic stability.
**Quantum Field Theory (QFT):** Forces are redundant; **fundamental interactions** arise from momentum conservation (symmetry of space). **Gauge bosons** (virtual particles) mediate interactions. **Feynman diagrams** depict matter lines (fermions) interacting at vertices via wavy boson lines.

### Fundamental Interactions
Four known interactions (decreasing strength):
1.  **Strong Nuclear:** Mediated by **gluons** between quarks (QCD). Residual **nuclear force** binds nucleons via meson exchange. **Color confinement** prevents free quarks.
2.  **Electromagnetic:** Mediated by **photons** (QED). Acts between charges. Unifies electricity, magnetism, light.
3.  **Weak Nuclear:** Mediated by massive **$W^\pm, Z^0$ bosons**. No bound states. Causes **beta decay** (charged current) and neutral current interactions. Unified with EM as **electroweak** above $\sim 10^{15}\,\text{K}$ (early Big Bang).
4.  **Gravitational:** Newton: instantaneous action-at-a-distance. **General Relativity (GR):** Not a force. Free objects follow inertial paths (geodesics) in curved spacetime. Curvature sourced by mass/energy. "Force" inferred from curved trajectory in space. Best current theory of gravity.

All macroscopic forces (friction, spring, tension, normal) derive from these four, primarily electromagnetic, operating under quantum constraints (Schrödinger equation, Pauli principle).

## Terms
- ****Force**** — Vector quantity causing acceleration, deformation, or pressure change; SI unit: newton (N).
- ****Inertial Frame**** — Reference frame where Newton's first law holds (non-accelerating observer).
- ****Momentum ($\mathbf{p}$)**** — Product of mass and velocity ($\mathbf{p}=m\mathbf{v}$); relativistic form $\mathbf{p}=\gamma m_0\mathbf{v}$.
- ****Net Force (Resultant)**** — Vector sum of all forces acting on a body; determines acceleration via $\mathbf{F}_{net}=d\mathbf{p}/dt$.
- ****Equilibrium**** — State of zero net force (and zero net torque for extended bodies); static (at rest) or dynamic (constant velocity).
- ****Conservative Force**** — Force expressible as gradient of a potential energy field ($\mathbf{F}=-\nabla U$); conserves mechanical energy (e.g., gravity, spring).
- ****Gauge Boson**** — Force-mediating particle in QFT (photon, gluon, $W/Z$ bosons); exchanged between fermions.
- ****Geodesic**** — Straightest possible path in curved spacetime; trajectory of free-falling objects in GR.
- ****Stress Tensor**** — Mathematical object ($\sigma = F/A$) describing internal force distribution (pressure, shear) in continuum mechanics.
- ****Degeneracy Pressure**** — Quantum mechanical pressure from Pauli exclusion principle; stabilizes matter against gravitational/electromagnetic collapse.

## Debates and open questions
*   **Definition of Force:** Whether Newton's second law ($F=ma$ or $F=dp/dt$) is a definition of force or a physical law with empirical content (Mach, Noll); practice unaffected.
*   **Quantum Gravity:** General relativity (gravity as geometry) and Standard Model (forces as gauge interactions) are mathematically incompatible at Planck scale; no accepted quantum theory of gravity.
*   **Unification:** Electroweak unification confirmed; **Grand Unified Theories (GUTs)** predict strong-electroweak merger at higher energies, untested. **Theory of Everything** including gravity remains speculative.
*   **Dark Matter/Energy:** Observed gravitational effects unexplained by known matter/forces; may indicate new fundamental interactions or modifications to GR.
*   **Measurement Problem (QM):** Ehrenfest theorem provides only an inexact link between quantum expectation values and classical force; the nature of "force" during measurement is interpretation-dependent.