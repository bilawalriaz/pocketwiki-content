# Materials with memory

A steel spring stretched and released obeys Hooke's law and carries no record of what came before. A growing class of real substances does not behave this way: their response at a given instant depends on the entire past history of the deformation, temperature, electric field, or magnetic field they have experienced. In continuum physics these are called **materials with memory**, or materials with hereditary effects.

## What "memory" means

A **constitutive equation** is the rule that links a material's response to the variables acting on it. In an elastic solid the local stress **T** at a point **x** and time *t* is a function only of the local strain **E** at the same point and time. The generalisation for materials with memory is that the local stress (or heat flux, electric current, polarisation, magnetisation, or any other constitutive quantity) at time *t* is a **functional** of the past history of the state variables up to *t*. A functional takes an entire past trajectory as input and returns a single value, rather than evaluating only the present. Past deformation, temperature, electric field, and magnetic field each leave a trace that influences the present response.

This idea originated in the late nineteenth century. Ludwig Boltzmann, writing in 1874 and 1878, and Vito Volterra, writing in 1912 and 1930, sought an extension of the elastic model in which local stress at time *t* depends on the history of local deformation up to *t*.

## The fading memory hypothesis

A naive history-dependent model would give equal weight to a deformation that happened yesterday and one that happened a year ago. Real materials do not work that way. The principle that the remote past matters less than the recent past was formalised in modern continuum mechanics as the **fading memory principle** by Bernard Coleman and Walter Noll in 1961. The closer in time a past event occurred, the stronger its influence on the present response.

The same idea appears in a different guise in Volterra's earlier closed cycle principle. If the deformation history is restricted to cyclic patterns, the closed cycle condition constrains the form of the constitutive relation to a **convolution integral** over past times, which is the mathematical signature of a fading-memory material.

## Linear constitutive relations

When the dependence on past history is taken to be linear, the constitutive equation for stress becomes a **Volterra equation**:

**T**(***x***, *t*) = **G**₀(***x***) **E**(***x***, *t*) + ∫₀^{+∞} **G**′(***x***, *s***) **E**(***x***, *t* − *s***) d*s*

The first term is the instantaneous elastic response, governed by **G**₀(***x***). The integral is the memory term: the strain **E** at every past time *t* − *s* is multiplied by a kernel **G**′(***x***, *s***) and integrated from *s* = 0 (the present) back through all of history. The decay of **G**′ with increasing *s* encodes fading memory. For short *s* the kernel is large, so recent strain dominates the stress; for large *s* the kernel is small, so distant strain contributes little.

The same integral structure describes dielectric relaxation, magnetic hysteresis-like effects, viscoelastic fluids and solids, viscoplastic metals, and biological tissues.

Source: adapted from "Materials with memory" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Materials_with_memory
