# Magnetic resonance (quantum mechanics)

Magnetic resonance is the resonant flipping of a quantum magnetic dipole between its spin energy levels when an oscillating magnetic field drives it at the matching frequency. A steady field $\mathbf{B_0}$ sets the level spacing; a weaker oscillating field $\mathbf{B_1}$ tips the dipole. The flip probability peaks when the driving frequency equals the natural one, the same way a swing responds only to pushes at its own rhythm.

## Energy levels of a spin in a steady field

A spin-½ particle with magnetic moment $\mathbf{m} = \tfrac{\hbar}{2}\gamma\boldsymbol{\sigma}$ in $\mathbf{B_0} = B_0\hat{z}$ has Hamiltonian $\hat{H} = -\mathbf{m}\cdot\mathbf{B_0} = -\tfrac{\hbar}{2}\omega_0\sigma_z$, where $\omega_0 := \gamma B_0$ is the Larmor precession frequency and $\gamma$ the gyromagnetic ratio. The two eigenstates sit at energies $\pm\tfrac{\hbar}{2}\omega_0$, a gap of $\hbar\omega_0$. These stationary states are stable only for an isolated system; a perturbation can drive transitions between them.

## What resonance does

Add a weak field $\mathbf{B_1}$ rotating in the x–y plane at angular frequency $\omega$. In the frame rotating with $\mathbf{B_1}$ the Hamiltonian becomes time-independent:
$$\hat{H'} = \tfrac{\hbar}{2}\begin{pmatrix}\Delta\omega & -\omega_1\\ -\omega_1 & -\Delta\omega\end{pmatrix},$$
with detuning $\Delta\omega = \omega - \omega_0$ and drive strength $\omega_1 = \gamma B_1$. A dipole starting in spin-up has probability
$$P_{12}(t) = \frac{\omega_1^2}{\Delta\omega^2 + \omega_1^2}\,\sin^2\!\left[\tfrac{1}{2}\sqrt{\omega_1^2 + \Delta\omega^2}\,t\right]$$
of being found in spin-down. At exact resonance ($\omega = \omega_0$) the prefactor becomes 1 and the probability oscillates between 0 and 1: at $t = (2n+1)\pi/\omega_1$ the dipole is in spin-down with certainty. This back-and-forth is the Rabi cycle, with rate $\Omega = \sqrt{\omega_1^2 + \Delta\omega^2}$, which is not the same as the driving frequency $\omega$. Off resonance the prefactor shrinks and the dipole barely transitions.

## Reading the resonance curve

Real states have finite lifetime $\tau$. Accounting for decay gives a steady-state transition rate proportional to
$$\frac{n}{2}\,\frac{\omega_1^2}{(\delta\omega)^2 + \omega_1^2 + 1/\tau^2},$$
a Lorentzian in the detuning. Three measurements follow from it. Sweeping the static field $B_0$ shifts $\omega_0$, and the peak's abscissa gives $\gamma$ via $\omega = \gamma(B_0)_\text{max}$. With $\gamma$ known, sweeping the driving frequency $\omega$ yields the local field $B_0$, even at a lattice site inside a crystal, precise enough for sensitive magnetometers. Sweeping the drive amplitude $B_1$ changes the half-width $d = \sqrt{\omega_1^2 + 1/\tau^2}$; extrapolating $d$ versus $\omega_1$ to zero gives $\tau$, the state lifetime. For nuclei, where electronic spins balance out, $\gamma$ yields the nuclear magnetic moment, which constrains models of the nuclear force.

## Rabi's molecular-beam experiment

Stern and Gerlach had shown that atoms carry spin by splitting a beam in an inhomogeneous field, but the small deflection angle left the measured moment uncertain. Rabi's improvement strung three magnets in a row. The outer two were inhomogeneous and oriented to push the two spin states in opposite directions; the middle produced only a uniform field and applied no force. An oscillating horizontal field in the middle region drives spin flips when its frequency equals the Larmor frequency $\omega_p = geB/2\hbar$. Flipped atoms then take the wrong path through the third magnet and miss the detector, so the detector current dips. Sweeping the driving frequency and locating the dip locates $\omega_p$, from which the Landé g-factor and the magnetic moment $\mu = gq\hbar/4m$ follow. The result is far more accurate than Stern–Gerlach.

## Classical correspondence

Classically, a magnetic moment in a field obeys $d\mathbf{m}/dt = \gamma\,\mathbf{m}\times\mathbf{B}$. In the rotating frame the effective field becomes $\mathbf{B}_\text{eff} = (\Delta\omega\,\hat{z} - \omega_1\hat{X})/\gamma$. At exact resonance the moment precesses around this field with large amplitude, giving the same complete flip. The expectation value obeys
$$\frac{d}{dt}\langle\mathbf{m}(t)\rangle = \gamma\,\langle\mathbf{m}(t)\rangle \times \langle\mathbf{B}(t)\rangle,$$
the same equation again, an instance of Bohr's correspondence principle. The coherent precession is therefore classical in character. What has no classical origin is the existence of discrete spin states, definite energy eigenstates, and a fixed magnetic moment for an elementary particle, the genuinely quantum fact that resonance exploits.

## Applications

Because many nuclei behave as magnetic dipoles, resonance with nuclear spin underlies nuclear magnetic resonance (NMR), NMR spectroscopy, and magnetic resonance imaging (MRI). In MRI, protons in body water split into two spin levels $\pm\gamma\hbar B/2$ in a strong field, with a small excess in the lower level by the Boltzmann distribution $N_0 e^{-E/kT}$. A resonant rotating field flips the excess, absorbing radio-wave energy; once the field is removed the protons re-equilibrate and re-emit at the resonance frequency. Electron paramagnetic resonance (EPR) uses unpaired electron spins instead, to detect free radicals.
