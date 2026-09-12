# Statistics

## Overview

Statistics is the discipline concerned with the collection, organization, analysis, interpretation, and presentation of data. It is both the science of uncertainty and the technology of extracting information from data. Statistics is deeply related to mathematics, physics, chemistry, geography, and geopolitics, and is widely employed in government, business, and the natural and social sciences. The discipline provides tools for planning data collection (surveys and experiments), summarizing data, drawing inferences from samples to populations, and making decisions in the face of uncertainty.

## Timeline

- **8th–13th centuries** — Islamic Golden Age mathematicians develop early statistical inference, including frequency analysis (Al-Kindi) and sample size considerations (Ibn Adlan).
- **1589** — Girolamo Ghilini introduces the term "statistic" referring to facts about a state.
- **1663** — John Graunt publishes *Natural and Political Observations upon the Bills of Mortality*, the earliest European statistical writing.
- **1749** — Gottfried Achenwall begins using "statistik" as a collection of quantitative information.
- **Late 17th century** — Probability theory takes shape, notably in Jacob Bernoulli's posthumous *Ars Conjectandi*.
- **1790s** — The term "statistics" gains its modern meaning in John Sinclair's works.
- **1805** — Adrien-Marie Legendre first describes the method of least squares (Gauss presumably used it earlier in 1795).
- **1853** — Adolphe Quetelet organizes the First International Statistical Congress in Brussels.
- **Late 19th–early 20th century** — First wave of modern statistics led by Francis Galton and Karl Pearson; they found *Biometrika* and Pearson founded the world's first university statistics department at University College London.
- **1910s–1920s** — Second wave initiated by William Sealy Gosset, culminating in Ronald Fisher's work: he originated variance, sufficiency, null hypothesis, and rigorous design of experiments.
- **1930s** — Final wave: Egon Pearson and Jerzy Neyman introduce Type II error, power of a test, and confidence intervals; Neyman (1934) shows stratified random sampling is generally better than purposive sampling.

## Body

### Foundations and data collection

Statistics deals with every aspect of data. When census data (comprising every member of the target population) cannot be collected, statisticians collect sample data by developing specific experiment designs and survey samples. Representative sampling ensures that inferences and conclusions can reasonably extend from the sample to the population as a whole. Sampling theory is part of probability theory: probability theory starts with given parameters of a total population to deduce probabilities pertaining to samples, while statistical inference moves in the opposite direction—inductively inferring from samples to the parameters of a larger population.

An experimental study involves taking measurements of the system under study, manipulating the system, and then taking additional measurements to determine if the manipulation modified the values. An observational study does not involve experimental manipulation; instead, data are gathered and correlations between predictors and response are investigated. The famous Hawthorne study examined changes to illumination at the Western Electric Company plant; productivity improved, but the study is criticized for lack of a control group and blindness. The Hawthorne effect refers to outcomes changing due to observation itself.

### Types of data

Stanley Smith Stevens defined four levels of measurement: nominal (no meaningful rank order), ordinal (meaningful order but imprecise differences), interval (meaningful distances, arbitrary zero, as with Celsius), and ratio (meaningful zero and distances). Nominal and ordinal measurements are grouped as categorical variables; ratio and interval measurements are grouped as quantitative variables, which can be discrete or continuous. Other categorizations have been proposed by Mosteller and Tukey (1977) and Nelder (1990).

### Descriptive and inferential statistics

Descriptive statistics summarize data from a sample using indexes such as the mean or standard deviation, characterizing central tendency (the central or typical value) and dispersion (the extent to which members depart from the center). Inferential statistics draw conclusions from data subject to random variation, using probability theory. A statistic is a random variable that is a function of the random sample but not of unknown parameters; an estimator is a statistic used to estimate a function of an unknown parameter. Commonly used estimators include sample mean, unbiased sample variance, and sample covariance. A pivotal quantity (or pivot) is a random variable whose probability distribution does not depend on the unknown parameter; widely used pivots include the z-score, chi-square statistic, and Student's t-value.

A standard procedure involves proposing a hypothesis for the statistical relationship between two data sets, as an alternative to a null hypothesis of no relationship. Working from a null hypothesis, two forms of error are recognized: Type I errors (null hypothesis falsely rejected, a "false positive") and Type II errors (null hypothesis fails to be rejected when false, a "false negative"). Statistical significance refers to the probability of a value accurately rejecting the null hypothesis (the p-value). The statistical power of a test is the probability that it correctly rejects the null hypothesis when it is false. Confidence intervals express how closely a sample estimate matches the true population value; a 95% confidence interval would include the true value in 95% of all possible repeated samples, though this does not imply a 95% probability that the true value lies in a given interval.

### Bayesian statistics

An alternative to the frequentist paradigm uses Bayes' theorem to update the prior probability of hypotheses based on the likelihood of evidence, obtaining a posterior probability. In one example, 1 in 1000 women have breast cancer; the test detects all cancers but has a 5% false positive rate. A woman with a positive mammogram has roughly a 2% chance of actually having cancer (posterior odds 20:1000 = 1:50). In one study, only 18% of doctors got the correct answer. Bayesian models tend to be hierarchical, and Bayesian methods have been aided by increased computing power using numerical approximation techniques like Markov Chain Monte Carlo.

### History and applications

The word "statistics" ultimately comes from the Latin *Status*, meaning "situation" or "condition" in society. Early applications revolved around states needing demographic and economic data for policy. The mathematical foundations developed from discussions on games of chance among Cardano, Pascal, Fermat, and Huygens. The modern field emerged in three waves: Galton and Pearson's transformation into a rigorous mathematical discipline; Fisher's textbooks and concepts (variance, null hypothesis, experimental design); and the Neyman-Pearson refinement of testing and confidence intervals.

Today, statistics is applied in all fields involving decision-making. Machine learning models are statistical and probabilistic models that capture patterns through computational algorithms. Increased computing power has led to interest in nonlinear models, generalized linear models, multilevel models, and computationally intensive methods like permutation tests and the bootstrap. Statistical software includes Mathematica, SAS, SPSS, and R. Business statistics is applied in financial management, marketing, production, and auditing; econometrics applies statistical methods to economic data.

### Misuse

Misuse of statistics can produce subtle but serious errors in description and interpretation. The statistical significance of a trend may not agree with an intuitive sense of its significance. Misuse can occur when conclusions are overgeneralized, often by overlooking sampling bias. Correlation does not imply causation: two correlated variables may be connected through a third, previously unconsidered factor called a lurking or confounding variable. For example, higher incomes may allow more leisure time for exercise, which could cause longer lifespans—raising income alone does not cause longer life.

## Terms

- **Null hypothesis**: The hypothesis that no relationship exists among variables or no change occurred over time; it is assumed true and tested against an alternative.
- **Type I error**: Rejecting the null hypothesis when it is in fact true (a "false positive").
- **Type II error**: Failing to reject the null hypothesis when it is in fact false (a "false negative").
- **p-value**: The probability, assuming the null hypothesis is true, of observing a result at least as extreme as the test statistic.
- **Confidence interval**: A range where, if sampling and analysis were repeated, the interval would include the true population value in a given percentage (often 95%) of all possible cases.
- **Estimator**: A statistic used to estimate a function of an unknown parameter; desirable properties include unbiasedness, efficiency (lower mean squared error), and consistency.
- **Pivotal quantity**: A random variable that is a function of the random sample and unknown parameter, but whose probability distribution does not depend on the unknown parameter.
- **Hawthorne effect**: The finding that an outcome changed due to observation itself, rather than the experimental manipulation.
- **Confounding variable**: A third, previously unconsidered factor that may produce an observed correlation between two variables.
- **Statistical power**: The probability that a test correctly rejects the null hypothesis when the null hypothesis is false.

## Debates and open questions

Several problems are associated with the hypothesis-testing framework: a difference that is highly statistically significant can still be of no practical significance; the p-value does not indicate the size or importance of the observed effect and can exaggerate minor differences in large studies. The "prosecutor's fallacy" (fallacy of the transposed conditional) arises because hypothesis testing evaluates the probability of the observed result given the null hypothesis, not the probability of the null hypothesis given the observed result—Bayesian inference offers an alternative but requires establishing a prior probability. Rejecting the null hypothesis does not automatically prove the alternative hypothesis. Under fat tails, p-values may be seriously mis-computed. There is also a general perception that statistical knowledge is frequently intentionally misused by interpreting only favorable data, and statistical literacy—the basic skills and skepticism needed to deal with information—remains an ongoing concern.

Source: adapted from "Statistics" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Statistics
