# Antibiotic sensitivity testing

Antibiotic sensitivity testing (also called antibiotic susceptibility testing) measures how well a bacterial isolate is inhibited by specific antibiotics. The result tells a clinician whether a given drug is likely to cure the infection, allowing a switch from empiric therapy (an educated guess based on symptoms and likely causative bacteria) to directed therapy tailored to the organism's actual sensitivities. Bacteria may be resistant because of an intrinsic trait, prior antibiotic exposure, or genes acquired from other bacteria via plasmids.

## How results are reported

The central quantitative measure is the minimum inhibitory concentration (MIC): the lowest antibiotic concentration that stops visible bacterial growth. The MIC is compared to breakpoints, standardised thresholds set by bodies such as the Clinical and Laboratory Standards Institute (CLSI) and the European Committee on Antimicrobial Susceptibility Testing (EUCAST). Breakpoints depend on both the organism–drug pair and the site of infection. For example, CLSI classifies *Streptococcus pneumoniae* as sensitive to intravenous penicillin when MIC ≤ 0.06 μg/mL, intermediate from 0.12 to 1 μg/mL, and resistant at ≥ 2 μg/mL, but the breakpoints for meningitis are considerably lower. The result is reported as sensitive, intermediate, or resistant, and certain phenotypes such as extended-spectrum beta-lactamase (ESBL) production or multidrug resistance may be noted explicitly.

## Phenotypic methods

Phenotypic tests expose live bacteria to antibiotics and observe the effect on growth. To make results comparable, the bacterial suspension is first standardised against McFarland turbidity standards, most commonly the 0.5 McFarland standard, using either visual inspection or a photometer.

The cheapest and most widely used approach is the disc diffusion (Kirby–Bauer) test. Antibiotic-impregnated paper discs are placed on an agar plate, usually Mueller–Hinton agar, that has been evenly inoculated with the test organism. After incubation, antibiotics that work produce a clear zone of inhibition around the disc. The zone diameter is compared to CLSI/EUCAST thresholds that correlate with MICs. Some slow-growing or fastidious bacteria (for example, *Streptococcus* species and *Haemophilus influenzae*) need specialised media and conditions. The WHO confirmed Kirby–Bauer as the standard method in 1966.

Gradient strips such as the Etest, available since the 1980s, place a plastic strip carrying a continuous antibiotic concentration gradient on agar; the MIC is read where the teardrop-shaped zone edge intersects the strip's scale. In agar and broth dilution methods, bacteria are grown in a series of tubes or wells at known antibiotic concentrations. The lowest concentration with no visible growth is the MIC, and broth microdilution is considered the gold standard for phenotypic testing.

Automated systems (VITEK 2, BD Phoenix, Microscan) use pre-formulated antibiotic panels and detect growth by turbidimetry, spectrophotometry, or fluorescence, with expert software linking the MIC to a susceptibility category. They are less labour-intensive and more standardised than manual methods, but can be less accurate for certain organism–drug combinations, so disc diffusion remains a useful backup.

## Genetic methods

Genetic tests detect resistance genes directly, using polymerase chain reaction (PCR), DNA microarrays, or loop-mediated isothermal amplification. In PCR, a bacterium's DNA is denatured, primers specific to the target gene (for example *mecA* in methicillin-resistant *Staphylococcus aureus*, or *vanA*/*vanB* in vancomycin-resistant enterococci) bind, and a DNA polymerase doubles the target sequence each cycle; the product is revealed by electrophoresis, southern blotting, or sequencing. Microarrays assess many genes simultaneously. These tests are fast and sensitive, but a detected gene does not always translate into the resistance phenotype that culture would show, and the equipment and trained staff are expensive.

## MALDI-TOF

Matrix-assisted laser desorption ionisation time-of-flight mass spectrometry (MALDI-TOF MS) ionises bacterial molecules and produces a spectral profile that can distinguish strains such as beta-lactamase-producing *E. coli*. It is rapid and automated, but results may not match phenotypic tests and the instruments are costly to buy and maintain.

## Population and clinical context

Aggregated susceptibility data for a hospital or region can be compiled into an antibiogram, which guides empiric therapy before individual results are available. Some countries also run population-level screening (for example for MRSA) to inform public-health policy, and the open-source R package AMR is used to standardise such analyses against international breakpoints.

Specimens are ideally collected before antibiotics are started, from the suspected infection site (blood culture for bacteraemia, sputum for pneumonia, urine for urinary tract infection). Multiple samples may be needed when the source is unclear. Although testing is performed *in vitro*, the results usually reflect *in vivo* activity, but effectiveness also depends on whether the antibiotic reaches the infected tissue, as with abscesses, and on whether the cultured organism is the true pathogen rather than a commensal such as *Staphylococcus epidermidis*.

## History and current direction

Alexander Fleming developed the first susceptibility method, a "gutter" diffusion assay, in the 1920s, and dilution-based testing in 1929. Paper-disc diffusion followed in the 1940s, the WHO standardised the Kirby–Bauer method in 1966, the Etest appeared in 1980, MALDI-TOF in the 2000s, and PCR for resistance genes was first published in 2001.

Traditional culture-based tests take 12 to 48 hours, sometimes up to five days, while rapid molecular diagnostics are defined as feasible within an 8-hour shift. Active research aims to shorten this further using microfluidics, biosensors, single-cell imaging, and whole-genome sequencing. The 2014 Longitude Prize (£8 million) for a fast, affordable, easy point-of-care bacterial infection test was awarded in 2024 to Sysmex Astrego AB for a 45-minute point-of-care antibiotic susceptibility test for urinary tract infections based on single-cell imaging. As of 2017, point-of-care molecular tests were already available for MRSA, rifampin-resistant *Mycobacterium tuberculosis*, and vancomycin-resistant enterococci via the Cepheid GeneXpert system.

Source: adapted from "Antibiotic sensitivity testing" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Antibiotic_sensitivity_testing
