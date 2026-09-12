# Mathematical statistics

Mathematical statistics applies probability theory and other mathematical tools to statistics, focusing on analysing data rather than collecting it. The core techniques drawn on are mathematical analysis, linear algebra, stochastic analysis, differential equations, and measure theory.

## Descriptive and inferential statistics

Statistics splits into two halves. *Descriptive statistics* summarises a dataset and its typical properties. *Inferential statistics* goes further: it picks a probability model for the data, checks whether the data satisfy the model's conditions, and quantifies uncertainty, often with confidence intervals.

Data collection is the upstream concern: designing randomised experiments and planning surveys with random sampling. Once data exist, analysing them, including secondary analyses that follow up on initial findings or propose new studies, is mathematical statistics. These tools work best on randomised data, where the design fixes the data-generating model, and they are also applied to natural experiments and observational studies, where the model must be chosen by the statistician and inference is more subjective.

## Probability distributions

A probability distribution assigns a probability to each measurable subset of outcomes from a random experiment, survey, or inference procedure. It is *univariate* for one random variable and *multivariate* (a joint distribution) for a random vector of two or more. Discrete variables use a probability mass function; continuous variables use a probability density function; stochastic processes in continuous time may need general probability measures.

Common univariate distributions include the binomial, hypergeometric, and normal. The multivariate normal is the standard multivariate case. Other distributions carry specific roles: Bernoulli for a single trial outcome; Poisson for event counts in a fixed interval; exponential and gamma for waiting times between Poisson events; chi-squared for sums of squared standard normals, used in inference about sample variance; Student's *t* for inference about a mean with unknown variance; beta for a probability on [0,1].

## Statistical inference

Statistical inference draws conclusions from data subject to random variation such as sampling error. It proceeds from a statistical model of the data-generating process plus a realised dataset. Procedures should give reasonable answers in well-defined settings and remain general across situations. The output can be a parameter estimate, a hypothesis test, or a decision about further experiments, surveys, or policy.

## Regression analysis

Regression analysis estimates how the typical value of a dependent variable changes as independent variables vary, with other independents held fixed. The standard target is the conditional expectation of the dependent variable, though quantiles or other location parameters are sometimes used; this conditional quantity is the regression function, and a probability distribution describes variation around it. Familiar methods such as linear regression are parametric: the regression function is determined by a finite number of unknown parameters estimated from the data, typically by ordinary least squares. Nonparametric regression lets the regression function lie in a specified set of functions, possibly infinite-dimensional.

## Nonparametric statistics

Nonparametric statistics are computed from data without assuming the data come from a parameterised family of distributions. They cover both descriptive and inferential procedures. Because they assume less, they apply more widely and are more robust, especially for ranked data with no clear numerical interpretation such as movie ratings, where they yield ordinal-level results. The cost is lower statistical power: with small samples, a nonparametric test is more likely to miss a real effect than its parametric counterpart. The Neyman–Pearson lemma and the likelihood-ratio test show many parametric methods are the most powerful available. Nonparametric methods also win on simplicity and reduced risk of misuse.

## The mathematical core of statistics

Mathematical statistics is the mathematical core of the wider discipline of statistics. Gauss, Laplace, and C. S. Peirce applied decision theory, using probability distributions together with loss or utility functions to guide choices. Abraham Wald revived this approach, and his successors extended it with scientific computing, analysis, and optimisation. For designing experiments, statisticians draw on algebra and combinatorics. Probability and decision theory underlie much of statistical practice, yet applying them remains contested, particularly when the model chosen for non-randomised data injects the statistician's judgement into every subsequent inference.
