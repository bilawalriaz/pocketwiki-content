# Engineering disasters

Most engineering disasters share a small set of root causes: miscalculated loads, ignored material limits, shortcuts driven by cost or schedule, and miscommunication between teams. Because engineered systems are designed near the edge of what their materials can tolerate, any error in assumption, fabrication, or coordination tends to show up as sudden failure.

A structure fails when the load on it exceeds what it was designed to carry. **Static overload** occurs when a single applied force exceeds the material's strength. Engineers characterise a material by pulling a sample in a tensile test, recording load and elongation, and plotting a stress–strain curve where stress σ = force per area and strain ϵ = elongation per original length. In the linear elastic region, σ = Eϵ, where E is Young's modulus. The **yield strength** is the stress beyond which deformation becomes permanent; the **ultimate tensile strength** is the stress at which the specimen breaks. Static load tests (tensile, bending, torsion) establish how much load a design can carry without permanent damage.

**Fatigue failure** is different: it occurs under repeated sub-yield loading. Each cycle grows tiny micro-cracks, which propagate until a final cycle triggers sudden fracture. Fatigue proceeds in three stages: crack initiation under repeated stress, crack propagation under tensile stress, and sudden fracture once the crack becomes unstable. A related time-dependent effect is **creep**, permanent deformation produced by sustained load combined with high temperature; both stress and temperature accelerate it. Safety-critical design requires that expected operating stresses stay far below the threshold at which creep, fatigue, or yielding can accumulate damage over the system's lifetime.

Three practices prevent failure. **Tensile testing** and other material tests produce the data behind stress–strain curves. **Finite element analysis (FEA)** simulates how stresses distribute across a complex geometry. **Failure theories** combine these inputs to predict the maximum load a part can safely carry. Skipping or truncating any step, often to save money or time, is a common thread in disasters.

Communication failures cause disasters even when individual calculations are correct. When teams use different unit systems, transmit flawed specifications, or revise a design without recalculating it, the structure that gets built is not the structure that was analysed. The Mars Climate Orbiter was lost because Lockheed Martin ground software delivered results in U.S. customary units while NASA's navigation system expected SI units, a mismatch neither side caught.

Engineering disasters in practice:

| Date | Event | Cause |
|------|-------|-------|
| 1876 | Ashtabula River bridge | Angle-block lug failure under thrust and cold |
| 1879 | Tay Bridge | Wind loading not accounted for |
| 1889 | Johnstown Flood | Dam modifications reduced storm capacity |
| 1907/1916 | Quebec Bridge | Chord members improperly designed |
| 1928 | St. Francis Dam | Defective foundation and design flaws |
| 1940 | Tacoma Narrows Bridge | Wind-induced aeroelastic flutter |
| 1981 | Hyatt Regency walkway | Revised design not recalculated |
| 1986 | Challenger | O-ring seal failure at launch |
| 2003 | Columbia | Foam impact damaged thermal tiles |
| 2005 | New Orleans levees | Inadequate design and construction |
| 2018 | Ponte Morandi | Section collapse during rainstorm |
| 2021 | Champlain Towers South | Partial collapse, investigation ongoing |
| 2023 | Titan submersible | Carbon-fibre hull design flaws; warnings ignored |

Software has caused disasters of its own: the Therac-25 radiation therapy machine delivered six overdoses; a clock-drift bug in Patriot Missile software at Dharan caused a failure to intercept; the Boeing 737 MAX MCAS contributed to Lion Air Flight 610 and Ethiopian Airlines Flight 302. In each case, a unit mismatch, an unverified control law, or an ignored warning combined with the absence of an independent test that would have caught it.
