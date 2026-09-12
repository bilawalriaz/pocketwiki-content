# Thermodynamic free energy

Free energy is the portion of a system's internal energy that remains available to do useful work once the unavoidable losses dictated by the second law have been subtracted. Those losses grow with temperature and entropy, so free energy is defined as internal energy minus the temperature–entropy product. Because free energy contains an arbitrary zero of potential energy, only its changes are physically meaningful.

## The two main potentials

The Helmholtz free energy $A = U - TS$ describes systems held at constant temperature and volume. Its decrease equals the maximum reversible work obtainable under those conditions, which is why $A$ is called the work content. In statistical mechanics, $A = -kT \ln Z$, where $Z$ is the canonical partition function, making $A$ the natural potential for gas-phase work.

The Gibbs free energy $G = H - TS = U + pV - TS$ includes the $pV$ term so that expansion or compression against constant pressure is already accounted for. The change in $G$ therefore measures work other than $pV$ work, such as electrical work in a battery or mechanical work in a contracting muscle. This makes $G$ the standard potential for chemists and biochemists working at atmospheric pressure.

In physics, "free energy" usually means $A$; in chemistry it usually means $G$. The two values are often close, so the intended meaning is sometimes left implicit.

## Free energy and spontaneity

The second law, in the Clausius form $\Delta S > q/T_\text{surr}$, implies that any spontaneous process at constant $T$ and $p$ must have $\Delta G < 0$, and at constant $T$ and $V$ must have $\Delta A < 0$. At equilibrium under those conditions, $dG = 0$ and $G$ sits at a minimum. A negative change is a necessary condition for spontaneity, not a measure of reaction rate.

## Work and the cycle

For a reversible isothermal process, $\Delta A = \Delta U - T\Delta S = \Delta U - q_\text{rev} = w_\text{rev}$, so the decrease of $A$ equals the maximum extractable work. For a cyclic device such as a Carnot heat engine, $\Delta_\text{cyc} A = 0$ even though the engine delivers nonzero work each cycle. Free energy therefore does not characterise engines well; internal energy and enthalpy do.

## The family of potentials

Free energy functions are Legendre transforms of the internal energy $U$, obtained by swapping one natural variable for its conjugate. The full family includes $U(S,V,\{N_i\})$, $H = U + pV$, $A = U - TS$, $G = U + pV - TS$, and the Landau (grand) potential $\Omega = U - TS - \sum_i \mu_i N_i$. Each is most simply expressed in its own natural variables:

| Potential | Formula | Natural variables |
|---|---|---|
| $U$ | internal energy | $S, V, \{N_i\}$ |
| $H$ | $U + pV$ | $S, p, \{N_i\}$ |
| $A$ | $U - TS$ | $T, V, \{N_i\}$ |
| $G$ | $U + pV - TS$ | $T, p, \{N_i\}$ |
| $\Omega$ | $U - TS - \sum \mu_i N_i$ | $T, V, \{\mu_i\}$ |

The differentials

$$dA = -p\,dV - S\,dT + \sum_i \mu_i\,dN_i$$

$$dG = V\,dp - S\,dT + \sum_i \mu_i\,dN_i$$

show that changes in $G$ at fixed $T$ and $p$ come entirely from compositional changes through the chemical potentials $\mu_i$. Work forms beyond $pV$, including electrical, magnetic, elastic, and polarisation work, can be added through extra conjugate pairs. Surface free energy, the cost per unit area of creating new interface, is a direct geometric application of the same framework. The numerical values of $A$ and $G$ for a given state differ by $pV$, so the choice between them is set by which variables a process holds constant.

Source: adapted from "Thermodynamic free energy" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Thermodynamic_free_energy
