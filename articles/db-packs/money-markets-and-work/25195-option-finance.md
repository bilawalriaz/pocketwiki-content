# Option (finance)

An option is a contract giving its holder the right, but not the obligation, to buy or sell a specified quantity of an underlying asset at a fixed *strike price* on or before an expiration date. The seller (writer) takes the opposite obligation. The holder pays a *premium* for this right, which the writer keeps whether or not the option is exercised. If expiration passes without exercise, the holder forfeits the premium.

A *call* gives the right to buy; a *put* gives the right to sell. Calls are exercised only when the strike is below the market price, and puts only when the strike is above it, so the holder's payoff is non-negative. Holding an option does not grant voting rights or dividends from the underlying.

## Trade structure and market venues

A standard US equity option contract represents 100 shares. Four basic positions combine long or short stock with buying or writing calls and puts:

| Position | Expectation | Maximum loss |
|---|---|---|
| Long call | Price rises | Premium paid |
| Long put | Price falls | Premium paid |
| Short call | Price flat or falls | Unlimited (rising price) |
| Short put | Price flat or rises | Strike minus premium |

In a long call with strike 100 and premium 10, the position breaks even at a stock price of 110 and profits above that; below 100 at expiry, only the premium is lost. A long put with the same numbers profits only below 90. The trader need not own the stock to exercise a put, because most stocks can be *shorted* (sold borrowed shares).

Options trade either on regulated exchanges through a clearing house, which guarantees settlement (the Options Clearing Corporation in the United States), or as bilateral over-the-counter (OTC) contracts tailored to a buyer's needs. OTC contracts carry *counterparty risk*, the chance the seller cannot deliver, and the writer is usually a well-capitalized institution to mitigate this. Exchanges list standardized stock, bond, interest rate, index, and futures options; OTC markets dominate interest-rate, currency, swap, and mortgage-backed-securities options.

## History

Option-like contracts date to antiquity. The Greek philosopher Thales of Miletus reportedly reserved olive presses before a predicted bumper harvest, then rented them at a higher rate when the prediction proved correct. Joseph de La Vega's 1688 *Confusion of Confusions* described "opsies" on the Amsterdam exchange. In 1690s London, puts and "refusals" (calls) became common under William and Mary. Nineteenth-century American "privileges" were OTC options with three-month expiries and no secondary market.

The Chicago Board Options Exchange (CBOE), founded in 1973, introduced standardized contracts with clearing-house guarantee. Options are now a major class of *derivatives*, instruments whose value derives from an underlying asset.

## Styles

American options may be exercised on any trading day before expiry; European options only at expiry; Bermudan options only on specified dates. Asian options pay based on the average underlying price over a period; barrier options activate only if the underlying crosses a price level; binary options pay a fixed amount or nothing based on a condition at expiry. American and European together are called *vanilla*.

## Valuation

An option's value splits into *intrinsic value* (market price minus strike when favorable, otherwise zero) and *time value* (the discounted expected payoff at expiry). Pricing models combine a stochastic process for the underlying price with a mathematical solution.

The Black–Scholes model (1973, Fischer Black and Myron Scholes, building on Robert C. Merton and earlier work by Louis Bachelier) gave a closed-form European-option price and earned Scholes and Merton the Nobel Prize in Economics. Its assumptions of continuous trading, constant volatility, and a constant interest rate are unrealistic, so practitioners also use *stochastic volatility* models (Heston is a closed-form prototype) and *local volatility* models, which treat volatility as a deterministic function of price and time. Since the 1987 crash, market data show a *volatility smile*: implied volatility is higher for low-strike options, implying volatility varies with price level.

Standard inputs for any pricing model are the underlying's current price, the strike (in the money or out of the money), the cost of holding the underlying (interest and dividends), time to expiry, and expected future volatility. Interest-rate derivatives use short-rate models (Black-Derman-Toy, Hull–White) or the Heath–Jarrow–Morton framework, which models the entire yield curve rather than a single rate.

For American options or complex payoffs, numerical methods replace closed-form solutions. The *binomial tree* (Cox, Ross, Rubinstein, 1979) builds a discrete tree of possible future prices and handles dividends and early exercise. *Monte Carlo* simulation draws random underlying paths and averages their payoffs. *Finite-difference* methods solve the pricing partial differential equation on a grid. *Trinomial trees* add a "stable" branch.

## Risks and the Greeks

Option payoffs are non-linear in the underlying price, so standard risk models must be extended. By Itô's lemma, the change in option value is

*dC = Δ dS + Γ·dS²/2 + κ dσ + θ dt,*

where Δ (delta), Γ (gamma), κ (vega), and θ (theta) are the "Greeks," hedge parameters measuring sensitivity to underlying price *S*, volatility *σ*, and time *t*. Delta also approximates the option's probability of expiring in the money. A *delta-neutral* portfolio, holding −Δ shares of the underlying against each option, is hedged against small price moves but remains exposed to gamma, vega, and theta.

Worked example. A 99-day call on 100 shares of XYZ, struck at $50 with the stock at $48 and 25% expected volatility, has theoretical value $1.89 and Greeks (Δ, Γ, vega, θ) of (0.439, 0.0631, 9.6, −0.022). If XYZ rises to $48.50 and implied volatility falls to 23.5% the next day, the predicted price change is

*dC = 0.439·0.5 + 0.0631·(0.5²/2) + 9.6·(−0.015) − 0.022·1 = 0.0614,*

so the option rises to $1.9514, a $6.14 profit on the 100-share contract. Under the same move, a delta-neutral portfolio that also shorted 44 shares would lose $15.86, illustrating that delta hedging only neutralizes small, linear price moves.

*Pin risk* arises when the underlying closes very near the strike on the final trading day: the writer cannot tell if the option will be exercised and may carry an unwanted position into the next session. Counterparty risk, the danger that the other side defaults, persists even for OTC options written by strong institutions, since systemic crises can overwhelm any intermediary.

Source: adapted from "Option (finance)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Option_%28finance%29
