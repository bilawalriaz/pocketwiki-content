# Econometrics

Econometrics is the application of statistical methods to economic data, giving empirical content to economic relationships. A 1954 report for the journal *Econometrica* defined it as "the quantitative analysis of actual economic phenomena based on the concurrent development of theory and observation, related by appropriate methods of inference." The term in its modern sense was coined by Ragnar Frisch; Jan Tinbergen is the other founding figure.

## The core tool: linear regression

The multiple linear regression model is the basic tool, and the most common starting point even though other methods are now used. Estimating a regression on two variables can be visualised as fitting a line through a scatter of paired data points. An early example is Udny Yule's 1889 study of how receiving public assistance affected poverty rates in England, using 1871 and 1881 census data.

A macroeconomic example is Okun's law, which links GDP growth to the change in the unemployment rate:

Δ Unemployment = β₀ + β₁ Growth + ε

The unknown parameters β₀ and β₁ are estimated from data. In the classic estimate, β₀ ≈ 0.83 and β₁ ≈ −1.77, so a 1 percentage point rise in GDP growth predicts a 1.77 point fall in unemployment, other things held constant. The model is then tested for statistical significance: if the estimate of β₁ were not significantly different from zero, the test would fail to confirm a relationship.

## Theory: choosing estimators

An estimator is a rule for computing a parameter's value from data. Econometricians seek estimators with three desirable properties: unbiasedness (expected value equals the true parameter), consistency (the estimate converges to the truth as the sample grows), and efficiency (lower standard error than other unbiased estimators).

Ordinary least squares (OLS) is widely used because, under the Gauss-Markov assumptions, it produces the BLUE, the "best linear unbiased estimator." When those assumptions fail, or when other properties are wanted, methods such as maximum likelihood estimation, generalised method of moments, or generalised least squares take over. Bayesian estimators, which incorporate prior beliefs, are an alternative to classical "frequentist" approaches.

## Applied econometrics and the causal problem

Applied econometrics uses real-world data to assess economic theories, build models, analyse economic history, and forecast. Most economic data are observational rather than from controlled experiments, which makes the field resemble astronomy, epidemiology, or sociology more than laboratory science. Because supply and demand are theorised to interact simultaneously, the field developed methods for identifying and estimating systems of simultaneous equations.

A labour-economics example shows why this matters:

ln(wage) = β₀ + β₁(years of education) + ε

Here β₁ measures how much an extra year of education raises the natural log of wages, while ε captures all other influences. If ε is uncorrelated with education, OLS gives an unbiased estimate. In reality, experiments that randomly assign education cannot be run, so the econometrician observes people who differ along many dimensions. If people born in certain places tend to have both higher wages and more education, the OLS coefficient on education partly reflects birthplace unless birthplace is controlled for. Including additional covariates, or using an instrumental variable (a variable that affects education but not wages except through education), can recover a less biased estimate.

In the absence of true experiments, econometricians seek natural experiments, real situations that mimic random assignment, or apply quasi-experimental methods to draw credible causal inference. The main tools are regression discontinuity design, instrumental variables, and difference-in-differences. These advances, formalised in the 2001 "credibility revolution" in empirical economics, have largely resolved earlier objections to causal inference from observational data.

## Limitations and criticisms

Badly specified models can show spurious relationships, variables that are correlated but causally unrelated. Deirdre McCloskey has argued that economists often over-rely on p-values, neglect type II errors, omit effect sizes, and fail to use economic reasoning in variable selection. Edward Leamer urged that researchers "properly withhold belief until an inference can be shown to be adequately insensitive to the choice of assumptions." P-hacking, the practice of searching specifications until a result appears significant, is a separate, related failure of researcher behaviour; it is rejected by the profession and countered by data-and-code disclosure policies.

Robert Lucas's critique of macroeconometrics argued that large-scale models estimated on historical data break down when policy changes, because economic actors revise their expectations and behaviour. A good macro model should therefore incorporate microfoundations and rational expectations.

The Austrian school rejects much of econometric modelling on the grounds that past correlations cannot establish causation. Econometricians answer with randomised controlled trials, where feasible, and with quasi-experimental methods otherwise, though they concede that without randomisation the size of remaining selection bias is inherently unknown.

Source: adapted from "Econometrics" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Econometrics
