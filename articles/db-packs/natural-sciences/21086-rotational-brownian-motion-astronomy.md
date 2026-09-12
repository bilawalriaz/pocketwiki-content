# Rotational Brownian motion (astronomy)

In astronomy, rotational Brownian motion is the random walk in the orientation of a binary star's orbital plane, driven by gravitational tugs from passing field stars. A binary consists of two massive bodies of masses M₁ and M₂, with total mass M₁₂ = M₁ + M₂, orbiting their common centre of mass inside a stellar system full of other stars. Each distant encounter is tiny, but the accumulated effect slowly randomises the direction the orbit points.

**How a flyby tugs the orbit.** A field star of mass m approaching with impact parameter p and velocity V passes a distance r_p from the binary, where gravitational focusing (the bending of the star's path by the binary's gravity) makes

p² ≈ 2 G M₁₂ r_p / V²

when focusing dominates. Only stars that come within the semi-major axis a deliver a strong kick. The rate of such encounters is

n π p² σ ≈ 2π G M₁₂ n a / σ,

where n is the number density and σ the velocity dispersion of field stars. As the field star passes, it picks up a velocity change of order

ΔV ≈ V_bin = √(G M₁₂ / a),

comparable to the relative orbital speed of the two binary components. Its specific angular momentum l about the binary therefore changes by Δl ≈ a V_bin. Conservation of angular momentum forces the binary's own specific angular momentum l_bin to recoil by

Δl_bin ≈ −(m / μ₁₂) Δl,

where μ₁₂ = M₁ M₂ / M₁₂ is the binary's reduced mass. A change in the magnitude of l_bin alters the binary's orbital eccentricity through e = 1 − l_bin² / (G M₁₂ μ₁₂ a), while a change in its direction tilts the orbital plane. The tilt accumulates as a random walk.

**The diffusion coefficient.** The mean-square change of the tilt angle per unit time is

⟨Δξ²⟩ ≈ (m / M₁₂) · (G ρ a / σ),

with ρ = m n the mass density of field stars. Dense, slow-moving stellar neighbourhoods rotate the binary's plane faster.

**Orientation as a random walk.** Let F(θ, t) be the probability that the rotation axis points at angle θ at time t. The evolution equation is

∂F/∂t = (1/sinθ) ∂/∂θ [ sinθ · ⟨Δξ²⟩/4 · ∂F/∂θ ].

If ⟨Δξ²⟩, a, ρ, and σ are constant, this reduces to the Legendre diffusion equation in μ = cosθ,

∂F/∂τ = ½ ∂/∂μ [ (1 − μ²) ∂F/∂μ ],

with dimensionless time τ = t / t_rel, where the relaxation time is

t_rel ≈ (M₁₂ / m) · (σ / G ρ a).

The mean alignment, μ̄, then decays exponentially,

μ̄ = μ̄₀ e^(−τ),

so t_rel is the e-folding time for the binary's orientation to be randomised by stellar torques.

**Why it matters: supermassive black hole spins.** Rotational Brownian motion was first studied for binary supermassive black holes at galactic centres. In N-body simulations of such galaxies, the massive binary sinks toward the core by dynamical friction, where it scatters passing stars. The same gravitational slingshot that shrinks the binary by stealing energy from interlopers also torques its plane. The root-mean-square tilt accumulated from binary formation until coalescence is roughly

δθ ≈ √(20 m / M₁₂).

The two holes finally merge by emitting gravitational waves, and the spin axis of the resulting black hole aligns with the orbital angular momentum of the pre-merger binary. A process that randomises orbital orientations therefore also randomises final spin directions, helping to explain why observed spins of supermassive black holes appear randomly aligned with respect to their host galaxies.
