# Blocking (statistics)

In the design of experiments, **blocking** is the practice of grouping similar experimental units together so that a known source of unwanted variation is absorbed by the group rather than allowed to contaminate the comparison of treatments. The blocking variable is a *nuisance factor*: it is not the focus of the study, but it can distort the outcome if left uncontrolled. The idea originated with Ronald A. Fisher in the early twentieth century alongside his development of analysis of variance (ANOVA), and it is the basis of the randomized block design.

## Why blocking helps

Suppose an engineer tests a new pesticide on a grass plot with a steep elevation change. Plants at the top of the hill receive different sun, water runoff, and soil than plants at the bottom. If sprayed and unsprayed plots are scattered across the slope by chance, the elevation effect becomes tangled up with the pesticide effect, inflating the experimental error. By placing a sprayed plot and an unsprayed plot inside each elevation zone, the two treatments share the same elevation. Any remaining difference must come from the pesticide rather than the slope.

A variable qualifies as a blocking factor only when every level of the primary factor occurs the same number of times within each level of the nuisance factor. Under that condition, the nuisance effect cancels out of the treatment comparison, and the analysis can focus on the primary factor within each block.

## A canonical example

Consider a double-blind trial of a diet pill. Sex is a nuisance factor because men and women may lose weight at different baseline rates. The investigator divides volunteers into a male block and a female block, then randomly assigns the diet pill or a placebo to equal numbers of men and equal numbers of women. The treatment-to-control ratio is one-to-one inside each block, so sex no longer masquerades as a drug effect, and the pill's effect is estimated more precisely.

A more sensitive variant, the **randomized complete block design**, uses each subject as their own block. In a shoe-sole trial with *n* volunteers, rather than giving half the group new soles and half ordinary soles, the experimenter gives every person one of each, randomly choosing which foot receives the new sole. Each person now acts as their own control, so person-to-person variability in walking style, weight, and gait is removed from the comparison, and the treatment effect emerges from a much smaller residual error.

## The implementation rule

The standard guidance is: *block what you can; randomize what you cannot.* A few of the most important nuisance variables are absorbed through blocking, which yields higher statistical significance than randomization alone. Remaining nuisance variation, the kind that is hard to identify or stratify, is handled by random assignment of treatments within blocks. The number of blocks is a design choice: more blocks mean fewer residual degrees of freedom for estimating the block effect, and different ways of assigning treatments to blocks produce different patterns of confounding, so the assignment scheme is sometimes preferred over purely random assignment. By running a different design for each replicate, with a different effect confounded each time, interaction effects are partially confounded rather than completely sacrificed.

## The model and its estimates

For a randomized block design with one nuisance factor, the observation *Y*_{*i*,*j*} for the *i*-th level of the treatment factor *X*₁ and the *j*-th level of the blocking factor *X*₂ is modelled as

*Y*_{*i*,*j*} = μ + *T*_{*i*} + *B*_{*j*} + random error,

where μ is the overall mean, *T*_{*i*} is the additive effect of treatment *i*, and *B*_{*j*} is the additive effect of block *j*. The three quantities are estimated from the data by simple averages:

- μ̂ = mean of all observations,
- *T̂*_{*i*} = mean of observations with *X*₁ = *i* − grand mean,
- *B̂*_{*j*} = mean of observations with *X*₂ = *j* − grand mean.

A two-factor design with *L*₁ levels of the primary factor and *L*₂ levels of the blocking factor therefore requires *L*₁ × *L*₂ runs. A *k*-factor randomized block design with *L*₁, *L*₂, …, *L*_{*k*} levels per factor needs *L*₁ · *L*₂ · ⋯ · *L*_{*k*} runs, and the trials correspond to the cell indices of a *k*-dimensional matrix.

## Worked example: a semiconductor furnace

An engineer compares four dosage levels of a wafer implant, with three wafers per dosage, but the diffusion furnace varies from run to run, and only four experimental wafers fit in any single run. Running all twelve wafers in one furnace would erase the nuisance factor entirely, but production wafers have priority. The blocked solution is to place one wafer of each of the four dosages into each of three furnace runs, randomizing only which of the three identical-dosage wafers goes to which run. Furnace-to-furnace variability is then absorbed by the block effect, and the dosage comparison is made within each furnace.

## Generalizations

Latin square designs extend blocking to two nuisance factors simultaneously, such as row and column, under the assumption that the two blocking factors do not interact. Graeco-Latin and hyper-Graeco-Latin squares push this further by adding additional orthogonal blocking factors. Generalized randomized block designs relax the no-interaction assumption so that block-by-treatment interactions can be estimated. Across all of these, the principle is identical: group the units so that the comparison of interest is made on a background that is as uniform as possible.
