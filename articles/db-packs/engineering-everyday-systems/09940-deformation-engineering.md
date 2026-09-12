# Deformation (engineering)

In engineering, **deformation** is any change in the size or shape of an object caused by an applied force. An object that barely changes is **rigid**; one that changes easily is **flexible** or **pliable**. The intrinsic resistance to deformation is its **stiffness** (or **rigidity**).

A deformation is **elastic** if the object returns to its original shape once the force is removed, and **plastic** if some permanent change remains. Whether a material behaves elastically or plastically depends on the magnitude of the stress relative to its **yield point**, the stress beyond which permanent distortion begins.

## Displacement, deformation, and strain

Three related ideas describe how an object responds to load. **Displacement** is the movement of any point on the object, including rigid translations and rotations. **Deformation** is the change in the *relative* positions of internal points, excluding rigid-body motion. **Strain** is the dimensionless, relative deformation of an infinitesimal material element.

**Stress** is the internal force per unit area that resists an applied load. For most engineering materials, the relationship between stress and strain is linear and reversible up to the yield point.

## Linear elastic deformation

In the elastic range, stress and strain are linked by **Hooke's law**:

$$\sigma = E\,\varepsilon$$

where σ is the applied stress, ε is the resulting strain, and **E** is **Young's modulus** (also called the elastic modulus), a material constant. The slope of the linear portion of a stress–strain curve equals E, and engineers extract it from tensile tests. The area under this region is the material's **resilience**, the elastic energy it absorbs per unit volume.

Not all elastic materials are linear. Concrete, gray cast iron, and many polymers respond nonlinearly, so Hooke's law does not apply. Elastomers, shape-memory alloys such as Nitinol, and rubber exhibit large but nonlinear elastic ranges; ordinary metals, ceramics, and most crystals show linear elasticity with smaller elastic limits.

For small strains (below about 1%), the **engineering strain** ε = ΔL / L₀ is adequate. Beyond that, the simple definition breaks down and measures such as **stretch**, **logarithmic strain**, **Green strain**, or **Almansi strain** are used instead.

## Plastic deformation

Above the yield point, plastic deformation takes over. In a ductile metal under tension, this region shows three stages. **Strain hardening** occurs first: atomic dislocations multiply and tangle, strengthening the material as it deforms. Once the **ultimate tensile strength** is reached, the cross-section begins to **neck** (localise) because work hardening can no longer compensate for the shrinking area. Necking proceeds rapidly until **fracture** ends the test.

Ductility varies sharply. Soft thermoplastics, copper, silver, gold, and steel have large plastic ranges; cast iron, hard thermosetting plastics, rubber, crystals, and ceramics have minimal plastic deformation before fracture. Wet chewing gum stretches to dozens of times its original length.

## Compressive failure and buckling

Under compression, bars and columns shorten, and sides may bulge outward as internal lateral forces resist the load. Compressive failure occurs by **yielding** in ductile materials (most metals, some soils and plastics) or by **rupture** in brittle ones (cast iron, glass, geomaterials).

Long, slender members fail differently. A column or truss bar may suddenly bend sideways through **buckling** at a stress well below the material's compressive strength, a failure driven by geometry rather than material strength.

## Engineering versus true stress and strain

The stress–strain curve plotted using the original cross-section A₀ and gauge length L₀ is the **engineering stress–strain curve**:

$$\sigma = \frac{F}{A_0}, \qquad \varepsilon = \frac{L - L_0}{L_0}$$

Stress has units of pascals (1 Pa = 1 N/m²); strain is dimensionless.

Because the cross-section actually shrinks and elongation compounds as the sample deforms, the **true stress and true strain** use the instantaneous area A and length L:

$$\sigma_t = \frac{F}{A}, \qquad \varepsilon_t = \ln\!\left(\frac{L}{L_0}\right) = \ln(1 + \varepsilon)$$

Assuming constant volume (A₀L₀ = AL), the two are related by σ_t = σ(1 + ε). In a tensile test the true stress is always larger than the engineering stress, and the true strain is always smaller; the difference grows with plastic deformation and is negligible in the elastic region. The **ultimate tensile strength** is the maximum on the engineering curve but, on the true curve, marks the balance between work hardening and area shrinkage that initiates necking.

A common empirical description of the true curve is the power law σ_t = K(ε_t)ⁿ, where **K** is the strength coefficient and **n** is the strain-hardening exponent, typically 0.02 to 0.5 for metals at room temperature; higher n means greater resistance to necking. A graphical method called the **Considère construction** uses a secant line on the true stress–λ diagram (with λ = L/L₀) to distinguish necking from uniform drawing.

## A common misconception

A material that bends is not necessarily weak. Steel deforms substantially yet absorbs stresses that would shatter glass; its large elastic and plastic ranges are what allow it to do so.
