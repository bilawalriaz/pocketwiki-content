# Electricity market

An electricity market is a system for trading electrical energy through the grid. Generation, transmission, distribution, and retailing are often run by separate firms, even when the wires themselves are natural monopolies. One physical fact shapes everything else: electricity must be produced and consumed at the same instant, so supply and demand are balanced continuously while the grid's frequency (either 50 or 60 hertz) stays inside a narrow band. A sustained mismatch causes equipment to disconnect and can trigger a blackout.

## Why markets exist

Before restructuring, most countries had vertically integrated utilities that owned generation, wires, and retail together, with regulated prices and no supplier choice. From the early 1980s, Chile, then the UK and the US, began separating these activities and introducing competition in generation, wholesale trading, and retail supply, while keeping transmission and distribution as regulated monopolies. Later reforms focused on integrating variable renewable energy, improving flexibility, and cutting greenhouse gas emissions.

## Market structure

Most electricity markets have two layers. A wholesale market matches generators with retailers (and, in some regions, large end-users) through auctions for time slices of five, fifteen, or sixty minutes. A retail market lets end customers choose among competing suppliers, though many consumers still pay fixed or averaged prices rather than real-time ones.

An energy-only market leaves generators no income for reserves that are almost never called upon, so modern designs add capacity mechanisms (payments for keeping spare plant available), ancillary services markets (frequency control, voltage support, operating reserves), and, where local market power is a concern, cost-based dispatch that replaces bids with audited costs. Carbon pricing is sometimes layered on top to reflect emissions. Hedging instruments, including forwards, futures, contracts for differences, and financial transmission rights, let participants manage the extreme price volatility that arises when peak prices run roughly 100 times off-peak levels.

## Auctions and pricing

Two auction designs dominate. In a double auction (used by Nord Pool), buyers and sellers submit bids and the operator clears where the curves cross. In a single reverse auction, the operator ranks supply offers alone and dispatches the cheapest stack. To settle, pay-as-bid (PAB) pays each winner its own bid, while uniform or marginal pricing (MPS, also called pay-as-clear) pays every winner the highest accepted bid. PAB invites strategic overbidding; MPS pays generators above their marginal cost by design, so some markets combine MPS day-ahead with PAB intra-day.

An efficient wholesale market runs "bid-based, security-constrained, economic dispatch with nodal prices," meaning every node on the transmission network gets its own locational marginal price (LMP) that reflects the cost of delivering one more megawatt-hour there, subject to the constraint that the grid must keep working even if one line or generator fails. Where prices diverge across a congested link, congestion rents accrue to whoever owns those wires. Some systems use zonal or regional prices instead, averaging nodes within an area.

## Centralized versus decentralized design

In a centralized market the transmission system operator (TSO) takes unit-based bids covering start-up, no-load, and marginal production costs, then solves commitment and dispatch itself, day-ahead and in real time, using nodal prices. This integrated approach handles non-convexities and long ramp-up times well, but is computationally heavy. A TSO that also owns the wires could profit from congestion, so in the US the TSO is separated as an Independent System Operator (ISO).

In a decentralized market generators commit to price and quantity but choose how to deliver, including by buying from other producers, while the TSO intervenes mainly in real time. This is lighter and allows intra-day trading, and is the model most European countries use. In the early 2020s North American markets moved toward more centralization while European ones moved the opposite way.

| Market | Type | Day-ahead | Pricing |
|---|---|---|---|
| PJM (US) | Centralized | Yes | Nodal |
| ERCOT (Texas) | Centralized since 2010 | Yes | Nodal (GNP) |
| MISO (US Midwest) | Centralized | Yes | Nodal |
| CAISO (US) | Centralized | Yes | Nodal |
| ISO New England | Centralized | Yes | Nodal (GNP) |
| Nord Pool | Decentralized | No | Zonal |
| Great Britain | Decentralized since 2001 | No | — |
| Germany | Decentralized | No | Zonal |
| Ireland | Decentralized since 2018 | No | Zonal |
| NEM, Australia | Decentralized | No | Regional |
| New Zealand | Decentralized | Yes | Nodal |
| Chile | Cost-based | Yes | — |

## Capacity and the missing money problem

A persistent issue is resource adequacy. Energy-only markets cap offer prices below the value of lost load, so generators cannot recover the cost of building plants that sit idle most of the time. This "missing money problem" leads to underinvestment and threatens reliability. To fix it, regulators require retailers to procure firm capacity equal to 110–120% of annual peak, either through bilateral contracts or centralized capacity markets such as ISO New England's Forward Capacity Auction and the UK's T-1 and T-4 auctions. As of 2026 PJM's Reliability Pricing Model is the last remaining three-year-ahead design.

## Outcomes of deregulation

The record is mixed. Schmalensee finds plausible evidence that restructuring lowered wholesale prices in the US and UK, while MacKay and Mercadal, analyzing 1994–2016, find that deregulated utilities charged higher prices because vertically separated firms extracted profit margins twice. Major failures including the 2001 California electricity crisis and the Enron collapse slowed reforms in some regions, and the 2022 European gas crisis renewed debate over decoupling power prices from natural gas.
