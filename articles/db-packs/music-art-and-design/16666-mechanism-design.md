# Mechanism design

Mechanism design is the branch of economics and game theory that works backwards from a desired outcome to construct the rules of a game that produces it. Standard game theory starts with a game and predicts how rational players will behave; mechanism design starts with a goal, then designs the institution whose equilibrium delivers that goal. Leonid Hurwicz, a founder of the field, called this "reverse game theory."

## The basic game

Following Harsanyi's (1967) "Bayesian" formulation, nature privately draws each player's *type* θ from a known distribution, encoding preferences, valuation, or other hidden information. Each player observes their own type and sends a *reported type* θ̂ to the mechanism, which can be a strategic lie. The principal commits in advance to an outcome function y(θ̂), split into an allocation of goods x(θ̂) and a monetary transfer t(θ̂). The timing is fixed: commit, receive reports, execute.

The benchmark is a *social choice function* f(θ) mapping the true type profile directly to the desired outcome. A mechanism *implements* f when the equilibrium outcome matches f.

## The revelation principle

Searching over every possible game and reasoning about every possible lie would be intractable. The *revelation principle* removes this burden: for every Bayesian-Nash equilibrium of any mechanism, there exists an equivalent *direct* mechanism in which players truthfully report their types and obtain the same outcome. The designer therefore only needs to design mechanisms where truth-telling is a Bayesian-Nash equilibrium and check that the outcome is desirable.

A mechanism is *truthfully implementable*, equivalently *incentive compatible* (IC), when reporting θ maximizes each player's expected utility:
> u(x(θ), t(θ), θ) ≥ u(x(θ̂), t(θ̂), θ) for every type θ and every lie θ̂.

When players can opt out, a participation or *individual rationality* (IR) constraint is added: each type must prefer playing to its outside option.

## When is an allocation implementable?

An allocation x(θ) is implementable only when some transfer t(θ) satisfies the IC constraint. The necessary condition is roughly:
> ∂/∂θ (MRS between goods and money) · ∂x/∂θ ≥ 0.

The first piece says the agent's marginal rate of substitution (MRS) between goods and money must rise with type: higher types intrinsically value the good more, otherwise a high type would mimic a low type and gain. The second piece says allocations must be *monotonic* in type: higher types receive weakly more of the good.

Designers typically impose the *Spence–Mirrlees condition*, also called the single-crossing or sorting condition, that MRS increases monotonically in type. Under it, any monotonic x(θ) is implementable by some t(θ), and in single-good settings monotonicity is both necessary and sufficient. If the solution to a design problem produces a non-monotonic schedule, it must be "ironed" by flattening the offending region, bunching distinct types onto the same contract.

## Three foundational results

*Revenue equivalence (Vickrey, 1961).* Under independent private values, a continuous distribution, monotone hazard rate, and allocation to the highest valuation, every such auction yields the same expected revenue. To earn more, the seller must accept the risk of sometimes not selling.

*Vickrey–Clarke–Groves (VCG) mechanisms.* Clarke (1971) and Groves extended Vickrey's second-price auction to public-good settings where agents share a project's cost. VCG picks the allocation that maximizes the sum of reported valuations, then charges each agent the harm his report imposes on others. The penalty makes lying unprofitable and can solve the "tragedy of the commons" under quasilinear utility, without requiring budget balance.

*Gibbard–Satterthwaite impossibility (1973, 1975).* When outcomes have at least three alternatives and preferences are unrestricted, the only social choice functions implementable truthfully are *dictatorial*: one agent's most-preferred outcome always wins. This is the analogue, for general decision rules, of Arrow's impossibility theorem, and motivates the field's "escape routes" such as restricted preferences, side payments, or randomization.

A related negative result, *Myerson–Satterthwaite (1983)*, shows two parties with secret, randomly varying valuations cannot trade efficiently without sometimes forcing one to trade at a loss, a striking exception to the first welfare theorem.

## Worked example: nonlinear pricing

The textbook application is a monopolist selling to customers of unknown type θ, à la Mirrlees (1971) and the optimal-income-tax literature. Customers have quasilinear utility u(x, t, θ) = V(x, θ) − t, the firm has a prior P(θ) and convex cost c(x), and maximizes E_θ[t(θ) − c(x(θ))] subject to IC and IR.

A trick from Mirrlees uses the envelope theorem: along the truth-telling path, dU/dθ = ∂V/∂θ, which lets the firm eliminate the unknown transfer and rewrite the objective in terms of the allocation alone. The IC constraint drops out, the optimum satisfies a pointwise first-order condition featuring the hazard rate (1−P(θ))/p(θ), and the optimal transfer is recovered by integration. When the resulting allocation is non-monotonic (the hazard rate itself not monotone), the firm applies *Myerson ironing*, bunching contiguous types onto a single price-quantity bundle and flattening the schedule.

This framework underlies airline fare discrimination among business, leisure, and student travelers, and generalizes to auctions, market design, inter-domain routing on the internet, and the advertisement auctions run by Google and Facebook. The 1996 Nobel Memorial Prize honoured William Vickrey for the auction foundations; the 2007 prize went to Hurwicz, Eric Maskin, and Roger Myerson "for having laid the foundations of mechanism design theory."
