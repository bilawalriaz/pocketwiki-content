# Time value of money

The time value of money is the principle that a sum available today is worth more than the same nominal sum at a future date, because money in hand can be invested to earn a positive return. This is why interest is paid and earned: a lender postpones spending, and interest compensates for that delay and for inflation.

## Core mechanics

In a discrete-time model with periods numbered t = 0, 1, 2, ... and a constant effective rate i applied once per period, an amount PV invested at time 0 grows to

FV = PV × (1 + i)^n

after n periods. The factor (1 + i)^n is the accumulation factor. Discounting reverses this: the present value of a sure sum FV due at time n is

PV = FV × (1 + i)^(−n) = FV / (1 + i)^n,

and (1 + i)^(−n) is the discount factor. For a stream of dated cash flows CF_t (positive for receipts, negative for payments), present value is the discounted sum

PV = Σ (t=0 to n) CF_t / (1 + i)^t.

A higher discount rate always lowers present value, so choosing the correct rate is central to valuation. Nominal cash flows must be discounted at nominal rates, and real cash flows (with inflation removed) at real rates; mixing conventions changes the answer mechanically.

## Standard formulas

All other time-value formulas derive from the two core relations. For a level annuity (payment A each period for n periods):

PV(A) = (A/i) × [1 − 1/(1 + i)^n].

For an annuity due (payments at the start of each period), multiply by (1 + i). For a growing annuity with payment growth rate g and i ≠ g:

PV = [A/(i − g)] × [1 − ((1 + g)/(1 + i))^n].

When n → ∞, the annuity becomes a perpetuity:

PV = A/i,

and a growing perpetuity (with g < i) becomes PV = A/(i − g), the Gordon growth model used for stock valuation. Future-value forms follow the same pattern: FV(A) = A × [(1 + i)^n − 1]/i. Any of these can be solved for any variable by numerical methods; financial calculators and spreadsheets implement them directly. The interest rate i must match the payment frequency: a mortgage with monthly payments uses the annual rate divided by 12.

## Origins

Compound interest and the comparison of payments at different dates long predate the modern terminology. Systematic treatment of life-contingent payments developed alongside probability theory and mortality data, with annuity pricing as a major context. Irving Fisher's *The Theory of Interest* (1930) formalised intertemporal valuation by linking interest to impatience (time preference) and to investment opportunities, shaping later discounting theory.

## Continuous compounding

When interest compounds continuously rather than per period, the discount factor becomes an exponential: PV = FV × e^(−rt), where e is the base of the natural logarithm and r is the continuously compounded rate. With a discount rate that varies over time as r(t), present value generalises to PV = FV × exp(−∫₀ᵀ r(t) dt). Continuous compounding smooths analysis, approximates daily compounding, and is the natural setting for time-varying rates; equivalent formulas for annuities and perpetuities replace (1 + i) with e and sums with integrals.
