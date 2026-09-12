# Mathematical finance

Mathematical finance is applied mathematics used to model and price financial instruments and to manage the risk of investment portfolios. The field is also called quantitative finance or financial mathematics. It overlaps with computational finance, which focuses on building the numerical tools, and with financial engineering, which focuses on the modeling itself, often using stochastic asset models (models where asset values evolve according to random processes defined over time). Quantitative investing is a closely related activity that replaces traditional fundamental analysis with statistical, numerical, and machine-learning models when managing portfolios.

The field has two main branches. The first is derivatives pricing: what is a fair price today for a complex security, given the prices of more liquid securities? The second is risk and portfolio management: how should a portfolio be allocated given the statistical distribution of future market prices? These two branches use different probability measures, and the distinction between them is the central idea in the subject.

## Two probability worlds: Q and P

In derivatives pricing, the relevant probability is the **risk-neutral probability**, written Q. Under Q, the properly normalized price of a security has constant expected value; a process with this property is called a martingale. The fundamental theorem of arbitrage-free pricing (Harrison and Pliska, 1981) says that a fair price P₀ exists if and only if there is a martingale measure Q such that P₀ equals the expected future price under Q:

P₀ = E^Q(P_t)

Because this must hold at every time t, derivatives pricing is naturally set in continuous time. The main tools are Itô's stochastic calculus (a branch of mathematics that extends ordinary calculus to random processes), simulation, and partial differential equations. Each contract is analyzed individually, so Q-world problems are low-dimensional; the central practical challenge is calibration, meaning fitting the model parameters to prices already observed in the market.

In risk and portfolio management, the relevant probability is the **real-world probability**, written P. The goal is to estimate the actual future distribution of market prices and to choose a portfolio that improves the prospective profit-and-loss profile. These problems are high-dimensional and usually handled with discrete-time multivariate statistics. The central practical challenge is estimation, since the data may not support precise parameter estimates.

| | Q world (derivatives pricing) | P world (risk and portfolio) |
|---|---|---|
| Goal | extrapolate the present price | model the future distribution |
| Probability | risk-neutral Q | real-world P |
| Time | continuous | discrete |
| Tools | stochastic calculus, PDEs, simulation | multivariate statistics |
| Dimension | low | high |
| Challenge | calibration | estimation |
| Side of market | sell-side | buy-side |

## Brief history

Quantitative derivatives pricing began with Louis Bachelier's 1900 doctoral thesis, *The Theory of Speculation*, which modeled stock prices as a random walk driven by Brownian motion. The theory was dormant until Fischer Black and Myron Scholes, with Robert Merton, applied geometric Brownian motion to option pricing; Scholes and Merton received the 1997 Nobel Memorial Prize in Economic Sciences for this work (Black had died in 1995 and was ineligible).

On the portfolio side, Harry Markowitz and William Sharpe introduced mathematics to investment management; together with Merton Miller they shared the 1990 Nobel Prize. Edward Thorp applied statistical methods originally developed for card counting in blackjack to systematic investing. Modern portfolio theory has moved from one-period mean-variance models to continuous-time models with general utility functions, and more recently to concerns about estimation risk.

The Black–Scholes equation and its pricing formula are the most widely used results, and many universities now offer dedicated degrees in mathematical finance.

## Criticism and limits

The credibility of mathematical finance models was damaged by the 2008 financial crisis. Nassim Taleb, in *The Black Swan*, argues that asset prices cannot be captured by simple models and that current practice can be dangerously misleading. Paul Wilmott and Emanuel Derman addressed similar concerns in the 2009 Financial Modelers' Manifesto. Benoît Mandelbrot showed in the 1960s that price changes follow heavy-tailed Lévy alpha-stable distributions rather than Gaussian ones: large moves are more common than a Gaussian model predicts, and volatility scales with the time interval raised to a power slightly above 1/2. Heavy tails make parameter estimation and risk control harder, not easier.

A deeper critique comes from the Lucas critique (rational expectations): observed empirical relationships may not be structural, so models fitted to historical data can fail when policies or conditions change. Mathematical finance models also tend to omit behavioral elements such as the self-fulfilling panics that drive bank runs. Bodies such as the Institute for New Economic Thinking now work on alternative theories.

Source: adapted from "Mathematical finance" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Mathematical_finance
