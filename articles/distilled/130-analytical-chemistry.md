# Analytical chemistry

## Overview

Analytical chemistry is the branch of chemistry concerned with developing and applying methods to identify the chemical composition of materials and quantify the amounts of components in mixtures. It encompasses both classical techniques (e.g., titration, gravimetric analysis) and modern instrumental approaches (e.g., spectroscopy, chromatography, mass spectrometry, electrochemical methods). The field underpins applications across biochemistry, medicinal chemistry, forensic science, archaeology, environmental monitoring, materials science, and the pharmaceutical industry, and has become central to interpreting complex results from high-throughput techniques in the age of "big data."

## Timeline

- **Pre-1900** — Systematic elemental analysis developed by Justus von Liebig; systematized organic analysis based on functional group reactions
- **1860** — Robert Bunsen and Gustav Kirchhoff develop flame emissive spectrometry; discover rubidium (Rb) and caesium (Cs)
- **Early 20th century** — Many basic spectroscopic and spectrometric techniques discovered
- **Late 20th century** — Spectroscopic and spectrometric techniques refined; separation sciences transformed into high-performance instruments
- **1970s** — Techniques begin to be combined as hybrid methods for complete sample characterization
- **1970s onward** — Analytical chemistry becomes progressively more inclusive of biological questions (bioanalytical chemistry)
- **Late 20th century** — Expansion into forensic, environmental, industrial, and medical applications (e.g., histology)
- **21st century** — Digitalization: handling large datasets ("big data") from instruments like Orbitrap mass spectrometers; machine learning becomes essential
- **21st century** — Green Analytical Chemistry emerges as a subfield focused on minimizing environmental impact

## Body

### History

Analytical chemistry has been important since the early days of chemistry, providing methods for determining which elements and chemicals are present in a given object. The first instrumental analysis was flame emissive spectrometry, developed by Robert Bunsen and Gustav Kirchhoff, who discovered rubidium (Rb) and caesium (Cs) in 1860. Most major developments occurred after 1900, when instrumental analysis became progressively dominant. In the 1970s, techniques began to be used together as hybrid techniques for complete sample characterization, and the field became increasingly inclusive of biological questions. The late 20th century saw expansion from academic chemical questions to forensic, environmental, industrial, and medical applications. Modern analytical chemistry is dominated by instrumental analysis; many methods are kept purposely static so data can be compared over long periods, particularly in industrial quality assurance (QA), forensic, and environmental applications. The 21st century has been defined by digitalization, with advanced data analysis including machine learning becoming essential, alongside a focus on sustainability through Green Analytical Chemistry.

### Classical Methods

Although modern analytical chemistry is dominated by sophisticated instrumentation, traditional techniques still form the backbone of most undergraduate educational labs. Qualitative analysis includes chemical tests (e.g., the acid test for gold, the Kastle-Meyer test for blood) and the flame test, which uses a systematic scheme of reactions to confirm the presence of aqueous ions or elements. These tests are rarely used with modern instrumentation but remain useful for education and fieldwork. Quantitative analysis measures the quantities of chemical constituents by mass (gravimetric analysis) or volume (volumetric analysis). Gravimetric analysis determines amount by weighing the sample before and/or after a transformation—for example, heating a hydrate to remove water and measuring the weight difference. Volumetric analysis includes titration, which involves the gradual addition of a measurable reactant to an exact volume of solution until an equivalence point is reached; the amount of moles used determines concentration or composition. Common types include acid-base titration with a color-changing pH indicator (e.g., phenolphthalein), potentiometric titrations, and precipitation titrations.

### Instrumental Methods

Spectroscopy measures the interaction of molecules with electromagnetic radiation and includes techniques such as atomic absorption spectroscopy, ultraviolet-visible spectroscopy, infrared spectroscopy, Raman spectroscopy, nuclear magnetic resonance spectroscopy, and fluorescence spectroscopy. Mass spectrometry measures the mass-to-charge ratio of molecules using electric and magnetic fields; a small sample is ionized and converted to gaseous ions, then separated and analyzed. Ionization methods include electron ionization, chemical ionization, electrospray ionization, fast atom bombardment, and matrix-assisted laser desorption/ionization; mass analyzers include magnetic-sector, quadrupole, quadrupole ion trap, time-of-flight, and Fourier transform ion cyclotron resonance. Electrochemical analysis measures potential (volts) and/or current (amps) in an electrochemical cell containing the analyte, with four main categories: potentiometry (electrode potential difference measured), coulometry (transferred charge measured over time), amperometry (current measured over time), and voltammetry (current measured while actively altering potential). Calorimetry and thermogravimetric analysis measure the interaction of a material with heat. Separation processes—chromatography, electrophoresis, and field flow fractionation—decrease the complexity of material mixtures. In chromatography, different components move at different speeds due to differing tendencies to adsorb onto the stationary phase or dissolve in the mobile phase; components are identified by their Rƒ values (ratio between migration distance of the substance and the solvent front). Types include thin-layer chromatography, gas chromatography, and high-performance liquid chromatography. Hybrid or hyphenated techniques combine two or more methods, such as gas chromatography-mass spectrometry, liquid chromatography-mass spectrometry, and capillary electrophoresis-mass spectrometry. Microscopy—optical, electron, and scanning probe—enables visualization of single molecules, cells, and nanomaterials. Lab-on-a-chip devices integrate multiple laboratory functions on a single chip of millimeters to a few square centimeters, handling fluid volumes down to less than picoliters.

### Data Analysis and Chemometrics

The vast amount of data produced by modern instruments has made computational data analysis integral to the field. Chemometrics uses statistical and mathematical methods to design optimal experimental procedures and extract meaningful information from chemical data. Key areas include multivariate calibration (developing models correlating instrument responses to analyte concentrations), pattern recognition (classifying samples based on analytical profiles, with applications in food authenticity and medical diagnostics), and machine learning and artificial intelligence (used for predictive modeling, optimizing methods, and automating data interpretation).

### Errors

Error is the numerical difference between observed value and true value. Systematic error results from a flaw in equipment or experimental design, while random error results from uncontrolled or uncontrollable variables. Absolute error is εₐ = |x − x̄|, where x is the true value and x̄ is the observed value. Relative error is εᵣ = εₐ/|x|, and percent error is εᵣ × 100%. For a function f with N variables, the propagation of uncertainty is calculated as εₐ(f) ≈ Σ|∂f/∂xᵢ|εₐ(xᵢ).

### Standards

A calibration curve allows determination of the amount of a chemical by comparing unknown samples to a series of known standards. If concentration exceeds the detection range, the sample can be diluted in pure solvent; if below the range, the method of addition can be used, where a known quantity is added and the difference between added and observed concentration gives the amount in the sample. An internal standard is sometimes added at known concentration to aid quantitation; an ideal internal standard is an isotopically enriched analyte, giving rise to isotope dilution. The method of standard addition compares an unknown sample to samples of known concentration and is used instead of a calibration curve to solve the matrix effect problem.

### Signals and Noise

Maximizing the desired signal while minimizing noise is a key component of analytical chemistry; the analytical figure of merit is the signal-to-noise ratio (S/N or SNR). Thermal noise results from thermal motion of charge carriers in an electrical circuit and is white noise (constant power spectral density throughout the frequency spectrum); its root mean square value is v_RMS = √(4k_BTRΔf), where k_B is the Boltzmann constant, T is temperature, R is resistance, and Δf is bandwidth. Shot noise occurs when the finite number of particles (electrons or photons) gives rise to statistical fluctuations; it follows a Poisson process, with root mean square current fluctuation i_RMS = √(2eIΔf), where e is elementary charge and I is average current. Flicker noise has a 1/ƒ frequency spectrum and arises from sources such as impurities in a conductive channel; it can be avoided by signal modulation at higher frequency (e.g., using a lock-in amplifier). Environmental noise arises from surroundings—power lines, radio and television stations, wireless devices, compact fluorescent lamps, and electric motors—and many sources are narrow bandwidth and can be avoided. Noise reduction can be accomplished in hardware (shielded cable, analog filtering, signal modulation) or software (digital filtering, ensemble average, boxcar average, correlation methods).

### Applications

Analytical chemistry has applications across forensic science (DNA fingerprinting, toxicology), bioanalysis (measuring drug concentrations in pharmacokinetic studies), clinical analysis (blood glucose monitoring, COVID-19 PCR testing), environmental monitoring (testing pollutants in water and air), and materials science (quality control of semiconductors and nanomaterials). Great effort is being put into shrinking analysis techniques to chip size through micro total analysis systems (μTAS) or lab-on-a-chip; microscale chemistry reduces the amount of chemicals used. Rapidly expanding biological fields include genomics, proteomics (protein concentrations and modifications), metabolomics (metabolites), transcriptomics (mRNA), lipidomics (lipids), peptidomics (peptides), and metallomics (metal concentrations and binding to proteins). Automated DNA sequencing machines were the basis for completing human genome projects, leading to the birth of genomics; protein identification by mass spectrometry opened the field of proteomics. Analytical chemistry has also been indispensable in nanotechnology development, with surface characterization instruments, electron microscopes, and scanning probe microscopes enabling visualization of atomic structures with chemical characterizations.

## Terms

- **Chemometrics**: Statistical and mathematical methods used to design experiments and extract information from chemical data.
- **Titration**: Gradual addition of a measurable reactant to a solution until an equivalence point is reached, used to determine concentration.
- **Gravimetric analysis**: Determining amount of material by weighing the sample before and/or after a transformation.
- **Spectroscopy**: Measurement of the interaction of molecules with electromagnetic radiation.
- **Mass spectrometry**: Measurement of mass-to-charge ratio of molecules using electric and magnetic fields.
- **Chromatography**: Separation technique where components move at different speeds due to differing adsorption or dissolution tendencies.
- **Rƒ value**: Ratio between the migration distance of a substance and the migration distance of the solvent front during chromatography.
- **Signal-to-noise ratio (S/N or SNR)**: The analytical figure of merit measuring desired signal relative to associated noise.
- **Systematic error**: Error resulting from a flaw in equipment or experimental design.
- **Random error**: Error resulting from uncontrolled or uncontrollable variables in an experiment.
- **Lab-on-a-chip**: Device integrating multiple laboratory functions on a single chip capable of handling extremely small fluid volumes.
- **Green Analytical Chemistry**: Subfield aiming to minimize the environmental impact of chemical analyses.

## Debates and open questions

The source notes that although some lab-on-a-chip systems exist, few compete with traditional analysis techniques, though potential advantages include size/portability, speed, and cost. The source also indicates that many methods, once developed, are kept purposely static so data can be compared over long periods, particularly in industrial QA, forensic, and environmental applications—implying a tension between methodological innovation and the need for consistent, comparable data.

Source: adapted from "Analytical chemistry" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Analytical_chemistry
