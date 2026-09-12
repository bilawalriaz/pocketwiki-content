# Statistics

Statistics is the discipline of collecting, organising, analysing, interpreting, and presenting data. It is often called "the science of uncertainty and the technology of extracting information from data." When a full census is impossible, statisticians use random sampling to extend conclusions from sample to population, a move grounded in probability theory. The field splits into two branches: **descriptive statistics** (summarising observed data) and **inferential statistics** (drawing conclusions under random variation). Probability and statistics are conceptually distinct: probability deduces sample behaviour from a general model, while statistics induces population statements from data.

## The two main branches

**Descriptive statistics** compresses a dataset into a few numbers. A **statistic** is any function of the random sample, such as the sample mean, as opposed to an unknown population parameter. The most useful summaries capture two things: *central tendency* (a typical value, such as the mean) and *dispersion* (spread, such as the standard deviation).

**Inferential statistics** reasons from sample to population. Its tools include estimators (rules that guess a parameter), hypothesis tests, and confidence intervals. Common estimators are compared by efficiency (low mean squared error), unbiasedness, and consistency; standard methods for finding them include maximum likelihood and least squares.

## Hypothesis testing and intervals

A hypothesis test contrasts a **null hypothesis** H₀, usually "no effect" or "no relationship," with an alternative. Like a criminal trial that presumes innocence until evidence proves guilt "beyond a reasonable doubt," failure to reject H₀ does not prove it true. Two errors are possible: a **Type I error** is a false positive (rejecting a true null); a **Type II error** is a false negative (failing to reject a false one). A test's **power** is its probability of correctly rejecting a false null. The **significance level** is the largest p-value at which H₀ is rejected; lower significance lowers the Type I rate.

A **confidence interval** is a range that, under repeated sampling, would contain the true population value in a stated percentage of cases (commonly 95%). Under the frequentist view the true value is fixed, so one cannot say there is a 95% probability it lies in any single computed interval; that probabilistic reading applies to **Bayesian credible intervals** instead.

Criticisms of hypothesis testing are well established: statistical significance can lack practical significance, p-values do not measure effect size, and under heavy-tailed distributions p-values can be seriously miscalculated. The transposed-conditional fallacy also leads people to favour the null simply because H₀ is the hypothesis being tested.

## Bayesian statistics

The Bayesian paradigm updates a **prior probability** with evidence through Bayes' theorem to obtain a **posterior probability**. A standard mammogram example shows the base-rate effect. Suppose 1 in 1000 women have breast cancer and a test catches every cancer but falsely flags 5% of healthy women. The prior odds of cancer are 1:1000, the likelihood ratio from a positive result is 20:1, and the posterior odds become roughly 1:50, about a 2% chance of cancer even after a positive screen. In one study only 18% of doctors answered this correctly, most overestimating because they ignored the base rate. Modern Bayesian models tend to be hierarchical, and computing advances have made them practical through numerical methods such as Markov Chain Monte Carlo.

## Data and measurement

Stevens classified data into four **measurement levels**: **nominal** (unordered categories), **ordinal** (meaningful order but imprecise differences), **interval** (meaningful distances with an arbitrary zero, like Celsius), and **ratio** (meaningful zero and distances). The first two are categorical; the last two are quantitative, either discrete or continuous. Which methods fit which levels is debated, partly because transforming data can change which techniques are appropriate.

## Data collection and causal inference

When a census is infeasible, statisticians rely on **representative sampling**; how representative a sample really is, and how safely results extend to the whole population, is a central practical problem. Two kinds of study produce data. An **experimental study** measures, manipulates, and re-measures a system; an **observational study** gathers data without manipulation and investigates correlations. Smoking and lung cancer, for instance, have been studied with cohort and case-control designs. For non-randomised data, structured methods such as difference-in-differences and instrumental variables aim to recover causal effects. Any statistical method is valid only when the system's assumptions hold, a point underlined by the Hawthorne study at Western Electric, where productivity rose under varied illumination but the original research lacked a control group; the resulting "Hawthorne effect" now names the way observation itself can change outcomes.

## Correlation is not causation

A recurring source of error is reading causation from correlation. Two variables can move together because a **confounding** (lurking) third variable drives both; income, for example, correlates with lifespan largely because higher income buys leisure time for exercise. The slogan "correlation does not imply causation" exists to head off this mistake. Huff's *How to Lie with Statistics* offers related safeguards, and the everyday skill of handling statistical information is called **statistical literacy**.

## Origins and modern shape

The word *statistics* comes from the German *Statistik* ("description of a state") and entered English in the late 18th century, originally meaning a collection of facts about a country. Formal inference has older roots: during the Islamic Golden Age, Al-Khalil used permutations and combinations in cryptography, Al-Kindi described frequency analysis for codebreaking, and Ibn Adlan wrote on sample size. European statistics began with John Graunt's 1663 *Bills of Mortality*, and probability theory took shape in the 17th century through games-of-chance and Jacob Bernoulli's posthumous *Ars Conjectandi*. Adolphe Quetelet organised the first International Statistical Congress in 1853 and popularised the "average man."

The modern field arrived in three waves. Francis Galton and Karl Pearson made statistics rigorous mathematics, introducing standard deviation, correlation, regression, and the Pearson distribution; Pearson also founded *Biometrika* and the first university statistics department at University College London. William Gosset and Ronald Fisher then gave statistics its experimental backbone, with Fisher's *Statistical Methods for Research Workers* (1925), *The Design of Experiments* (1935), sufficiency, Fisher information, and the coining of "null hypothesis" during the Lady tasting tea experiment. In the 1930s Egon Pearson and Jerzy Neyman added Type II error, power, and confidence intervals, and Neyman showed that stratified random sampling generally beats purposive quota sampling.

## Applications and computing

Applied statistics serves scientific, industrial, and social problems, from business and econometrics to biostatistics and statistical process control in manufacturing. Machine learning models are statistical and probabilistic at their core. Computing power since the mid-20th century has made nonlinear models, generalised linear and multilevel models, resampling methods (permutation tests, the bootstrap), and Gibbs sampling practical, along with software such as R, SAS, SPSS, and Mathematica.

Source: adapted from "Statistics" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Statistics
