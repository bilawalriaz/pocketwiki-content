# Bootstrapping (statistics)

Bootstrapping is a resampling method that estimates the uncertainty of a sample statistic (such as its variance, bias, or confidence interval) by treating the observed sample as if it were the population, then drawing many new samples from it with replacement.

## The central idea

A single sample yields a single estimate of a statistic, but the true variability of that estimate across samples is unknown. The bootstrap resolves this by using the observed data as a stand-in for the population. You draw a new sample of the same size as the original, but with replacement: some observations appear multiple times, others are omitted (roughly 26.4% of points are dropped from a typical resample). You compute the statistic on this resample and repeat, usually 1,000 to 10,000 times. The distribution of those repeated estimates, called the bootstrap distribution, approximates the sampling distribution of the statistic. A histogram of bootstrap means, for example, shows how the sample mean varies from sample to sample.

The logic is a loop: inference about a population from a sample (sample → population) is modeled by inference about a sample from a resampled version of it (resampled → sample). Because the "population" inside the loop (the original sample) is known, the error of the resample-based statistic against it can be measured directly. If the empirical distribution of the observed data approximates the true population distribution, the quality of inference carries over.

## How a resample is constructed

The standard algorithm, called case resampling, has three steps: draw N items with replacement from the original N-item data set, compute the statistic on that resample, and repeat many times. Resampling five times from [1, 2, 3, 4, 5] might give [2, 5, 4, 4, 1]. An "exact" version enumerates every possible distinct resample, but the count grows explosively: for n = 5, 10, 20, 30 the counts are 126, 92 378, 6.89 × 10¹⁰, and 5.91 × 10¹⁶, so Monte Carlo resampling is the practical default.

## Why the bootstrap is useful

The bootstrap replaces difficult or impossible analytic calculations with a uniform computational recipe. It is most valuable when the sampling distribution of the statistic is unknown, when the sample is too small for the central limit theorem to give a good approximation, or when a pilot study needs variance estimates for a power calculation. Beyond standard errors and confidence intervals, the bootstrap can build hypothesis tests and extends to regression, time series, and clustered data. Under broad conditions, it is asymptotically more accurate than normal-based intervals.

## Variants

Different data structures call for different resampling schemes.

- **Parametric bootstrap**: fit a parametric model (usually by maximum likelihood), then draw new samples from that fitted model rather than from the raw data.
- **Smooth bootstrap**: add a small amount of zero-centered random noise (often normal, or Student-t with n−1 degrees of freedom for variance estimation) to each resampled observation, equivalent to sampling from a kernel density estimate of the data.
- **Residual bootstrap (regression)**: fit the model once, then for each replicate keep the fitted values fixed and add a randomly resampled residual to them, so the explanatory variables retain all their original information.
- **Wild bootstrap**: a variant for heteroskedastic regression, where each residual is multiplied by a random variable with mean 0 and variance 1 (such as a Rademacher ±1 variable, a standard normal draw, or Mammen's two-point distribution with values about −0.618 and +1.618).
- **Block bootstrap**: when observations are correlated in time or within clusters, resample whole blocks of consecutive observations (moving block, stationary, or maximum entropy variants) so the dependence structure is preserved.
- **Gaussian process bootstrap**: fit a Gaussian process to temporally correlated data and draw replicates from the posterior predictive distribution.
- **Bayesian bootstrap**: assign random Dirichlet weights to the original observations, producing a posterior-like distribution on parameters.

For computational reasons, several efficient alternatives exist. The Poisson bootstrap draws independent Poisson(1) counts for each observation instead of correlated multinomial counts. The Bag of Little Bootstraps (BLB) pre-aggregates the data into about n^0.7 buckets, making the method scalable to massive data sets. Most bootstrap procedures are embarrassingly parallel, so independent resamples can run on separate cores. On sample size, more than 100 resamples rarely improves standard error estimates noticeably, and Efron himself reports that 50 resamples often give a "fairly good" estimate.

## Limits and warnings

The bootstrap's apparent simplicity hides assumptions. It works only when the empirical distribution is a reasonable stand-in for the true one. If the underlying distribution has infinite variance, as in a power law, the naive bootstrap on the mean fails: Athreya showed the bootstrap distribution does not converge to the right limit, so confidence intervals from a Monte Carlo bootstrap can be misleading. The naive bootstrap should not be trusted for heavy-tailed distributions without further justification.

Even when the bootstrap is asymptotically consistent, it has no general finite-sample guarantee, and its results depend on the representativeness of the original sample. Assumptions such as independence between observations and a sufficiently large sample are easy to overlook. The method can also be time-consuming, and standard statistical packages offer limited automated support.

## Confidence intervals from the bootstrap

Several interval constructions are in use:

- **Percentile method**: take the α/2 and 1−α/2 percentiles of the bootstrap distribution directly. Simple and transformation-invariant, but biased when the bootstrap distribution is asymmetric.
- **Basic (reverse percentile) method**: reflect the bootstrap percentiles around the observed statistic, using the formula (2θ̂ − θ*_(1−α/2), 2θ̂ − θ*_(α/2)). Easy to justify but less accurate in general.
- **Studentized (bootstrap-t) method**: bootstrap a pivotal t-statistic instead of the raw estimator, which often gives second-order accuracy.
- **Bias-corrected and accelerated (BCa)**: Efron's 1987 method, which adjusts both the bias and the skewness of the bootstrap distribution.

For small samples (under about 50), basic and percentile intervals for the variance are too narrow: with n = 20, a nominal 90% interval covers the true variance only about 78% of the time.

## Where the bootstrap sits among resampling methods

The jackknife, the bootstrap's predecessor, estimates variance and bias by leaving out one observation at a time. Cross-validation does the same for prediction error on held-out data. Bagging (bootstrap aggregating) trains many models on bootstrap samples and averages their predictions. U-statistics generalize the idea of averaging a statistic over many small subsamples.

The bootstrap was introduced by Bradley Efron in 1979, inspired by the earlier jackknife. A Bayesian extension followed in 1981, the bias-corrected and accelerated (BCa) interval in 1987, and the approximate bootstrap confidence (ABC) procedure in 1992.

Source: adapted from "Bootstrapping (statistics)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Bootstrapping_%28statistics%29
