# Models of DNA evolution

Substitution models describe how one DNA base (A, G, C, T) replaces another over evolutionary time. They are phenomenological: they do not model the mechanism of mutation or natural selection, only the relative rates at which different substitutions occur. Those rates are typically higher for transitions (purine↔purine, A↔G; or pyrimidine↔pyrimidine, C↔T) than for transversions (purine↔pyrimidine), because mutational bias and purifying selection both favour chemically conservative changes. Phylogenetics uses these models to compute the likelihood of a tree and to estimate evolutionary distances between sequences from observed differences.

## The rate-matrix formulation

Each model is a 4×4 rate matrix Q whose off-diagonal entry μₓᵧ is the instantaneous rate of changing from base x to y, and whose diagonal entry −μₓ makes every row sum to zero. Given a starting state and a branch length ν (the expected number of substitutions per site), the probability of each descendant state is given by the matrix exponential

P(ν) = exp(νQ).

Models differ only in which off-diagonal rates they allow to differ. The matrix is rescaled by a factor β so that ν = 1 means one expected substitution per site; β is computed from Q and the equilibrium base frequencies πᵢ, not fitted separately. Most common models also assume time reversibility, meaning πₓμₓᵧ = πᵧμᵧₓ, which lets one parameterise the matrix by symmetric exchangeabilities sₓᵧ = μₓᵧ/πᵧ. With four bases, the 12 off-diagonal entries of Q are then determined by 6 exchangeabilities plus 3 independent frequencies (since the four πᵢ sum to 1), giving 8 identifiable degrees of freedom after the overall rate scaling. A single-site, time-homogeneous, irreducible chain is ergodic and has a unique stationary distribution π, the equilibrium base composition at which frequencies no longer change.

## Assumptions used in practice

Single-site models are applied to whole loci by assuming sites evolve independently and identically distributed. The identical-distribution assumption holds under neutrality; when selection constrains some sites more than others, a separate among-site rate-variation layer is added on top of a single relative-rate Q.

## The standard models

| Model | Parameters beyond JC69 |
|---|---|
| JC69 | Baseline: equal base frequencies (πᵢ = 0.25), equal rates between every pair of bases. |
| K80 (K2P) | Transition/transversion rate ratio κ; equal frequencies. |
| K81 (K3ST) | Three substitution-type rates α (transition), β (amino/keto transversion), γ (weak/strong transversion); equal frequencies. Rarely best-fitting but tractable via the Hadamard transform. |
| F81 | Unequal base frequencies πᵢ, otherwise as JC69. |
| HKY85 | Combines K80's κ with F81's unequal frequencies. |
| T92 | Like K80 with G+C content θ as a parameter (πG = πC, πA = πT), useful for genomes such as *Drosophila* mitochondrial DNA with strong GC bias. |
| TN93 | Two transition rates κ₁ (A↔G) and κ₂ (C↔T), one transversion rate, unequal frequencies. |
| GTR | Most general time-reversible 4-state model: six independent exchangeabilities α, β, γ, δ, ε, η plus free frequencies. |

GTR has 8 free parameters for DNA; for an alphabet of size n the count generalises to n²/2 + n/2 − 2. Twenty amino acids would require 208 parameters, and the 64 codons even more, so codon models replace a generic GTR framework with empirically or mechanistically structured rates.

## Distances from observed differences

Raw differences underestimate true divergence because of multiple hits at the same site. Each model's P(ν) inverts this: one plugs in the observed proportions of differences (and, for K80 and above, the transition and transversion proportions) and solves for ν. JC69 yields d̂ = −(3/4) ln(1 − 4p/3), where p is the p-distance; K80 separates transitions and transversions; T92 also incorporates G+C content.

## Variants beyond four bases

Nucleotides can be recoded as purines versus pyrimidines (RY-coding), weak-strong, or amino-keto, giving a two-state Markov chain. The symmetric version is the Cavender-Farris-Neyman model, equivalent to JC69 on two states; unequal equilibrium frequencies give CFu or GTR2. Lie Markov models form a family closed under matrix multiplication that admits taxa to be added or removed without disturbing site-pattern structure over the remaining taxa; JC and F81 are Lie models, whereas GTR is not. A branch length expressed as expected substitutions per site equals the product of elapsed time and mean substitution rate, but sequence data cannot separate the two factors, so a phylogenetic tree supplies only relative rates of evolution.

Source: adapted from "Models of DNA evolution" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Models_of_DNA_evolution
