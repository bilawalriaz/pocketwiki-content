# Prime number theorem

The prime number theorem describes how primes thin out among the integers. Letting π(x) denote the number of primes less than or equal to x, the theorem states

$$\lim_{x\to\infty}\frac{\pi(x)}{x/\log x}=1,$$

or equivalently π(x) ∼ x / log x, where log means the natural logarithm. A random integer up to x is prime with probability about 1 / log x, the average gap between consecutive primes below x is roughly log x, and doubling the number of digits halves the chance of primality (so among positive integers of at most 1000 digits, about one in 2300 is prime, versus one in 4600 among those of at most 2000 digits).

## Equivalent statements

The theorem has several equivalent forms. The nth prime p_n satisfies p_n ∼ n log n. Replacing log x with log π(x) leaves the limit equal to 1, as does using the Chebyshev function ψ(x) = Σ_{n≤x} Λ(n), where Λ is the von Mangoldt function, or the Mertens function M(x) = Σ_{n≤x} μ(n), which must satisfy M(x)/x → 0.

A more accurate approximation replaces x / log x with the logarithmic integral Li(x) = ∫₂ˣ dt / log t. Asymptotically π(x) ∼ Li(x). The difference π(x) − x / log x grows without bound even as the ratio tends to 1; Li(x) − π(x) changes sign infinitely often.

## History of the proof

Legendre conjectured in 1797–1798 that π(x) ≈ x / (A log x + B) with specific constants, and Gauss considered the same question around 1792–1793. In 1838 Dirichlet proposed the approximation li(x). Pafnuty Chebyshev attempted a proof in 1848 and 1850, establishing that if the limit of π(x) / (x / log x) exists at all, it must equal 1, and bounding the ratio between 0.92129 and 1.10555 for large x; this sufficed to prove Bertrand's postulate that there is always a prime between n and 2n for n ≥ 2.

Riemann's 1859 memoir introduced the analytic extension of the zeta function and showed that the distribution of primes is governed by its complex zeros. Building on these ideas, Jacques Hadamard and Charles Jean de la Vallée Poussin independently proved the theorem in 1896, each showing that ζ(s) has no zeros on the line Re(s) = 1.

In 1949 Atle Selberg and Paul Erdős separately produced "elementary" proofs, though the term means free of complex analysis; both proofs are technically intricate and were followed by a priority dispute. D. J. Newman gave a notably short proof in 1980 using only Cauchy's integral theorem.

## Sketch of the proof

The standard route replaces π(x) with the smoother Chebyshev function ψ(x). The PNT is equivalent to ψ(x)/x → 1, which follows from estimates linking ψ(x) to π(x) log x.

The next step uses the identity −ζ′(s)/ζ(s) = Σ Λ(n) n^{-s}. Applying Perron's formula to this Dirichlet series yields the explicit formula

$$\psi(x) = x - \log(2\pi) - \sum_{\zeta(\rho)=0}\frac{x^{\rho}}{\rho},$$

where the sum runs over all nontrivial zeros ρ of ζ(s). The term x on the right-hand side is the desired leading order; the remaining terms depend on the location of the zeros. The trivial zeros at −2, −4, −6, … contribute a vanishing amount.

The crucial remaining task is to show that no nontrivial zero has real part equal to 1. Writing s = x + iy and using the Euler product ζ(s) = ∏_p (1 − p^{-s})^{-1}, one obtains the bound |ζ(x)^3 ζ(x+iy)^4 ζ(x+2iy)| ≥ 1 for x > 1, which forces ζ(1 + iy) ≠ 0 for y ≠ 0. The limit lim ψ(x)/x = 1 then follows, with Tauberian arguments needed to justify swapping a limit and an infinite sum.

## Refinements and consequences

De la Vallée Poussin (1899) showed π(x) = Li(x) + O(x e^{-a√(log x)}); sharper bounds now give |π(x) − li(x)| ≤ 0.2795 x / (log x)^{3/4} · exp(−√(log x / 6.455)) for x ≥ 229. Under the Riemann hypothesis, Helge von Koch proved in 1901 that π(x) = Li(x) + O(√x · log x), with an explicit constant worked out by Lowell Schoenfeld in 1976. J. E. Littlewood proved in 1914 that π(x) − li(x) changes sign infinitely often; the first sign reversal is expected near 10^{316} (Skewes' number).

For arithmetic progressions, de la Vallée Poussin proved that primes are asymptotically equidistributed among the residue classes coprime to d: π_{d,a}(x) ∼ Li(x) / φ(d). Explicit versions with effective constants are given by the Siegel–Walfisz theorem and refined estimates of Bennett, Martin, O'Bryant, and Rechnitzer.

Among primes themselves, persistent biases appear: primes congruent to 3 mod 4 outnumber those congruent to 1 mod 4 for all x below 26861, and the lead in this "prime number race" switches back and forth infinitely often (Chebyshev's bias). Similar biases affect the last digit of primes: those ending in 3 or 7 tend to slightly outnumber those ending in 1 or 9, because 1 and 9 are quadratic residues mod 10 while 3 and 7 are not.

## Non-asymptotic bounds

The asymptotic statement itself yields only an "ineffective" bound, with no explicit threshold. Effective explicit inequalities include Dusart's: π(x) > x / log x · (1 + 1 / log x) for x ≥ 599, π(x) < x / log x · (1 + 1 / log x + 2.51 / (log x)^2) for x ≥ 355991, and the simpler π(x) < x / (log x − 1.1) for x ≥ 60184. Rosser proved p_n > n log n for all n ≥ 2.

## An analogue over finite fields

Over a finite field F with q elements, the monic irreducible polynomials of degree n play the role of primes. The Möbius-inversion formula N_n = (1/n) Σ_{d|n} μ(n/d) q^d, classical and known to Gauss, gives the exact count and yields the analogue N_n ∼ q^n / n. A cleaner version states N_n = q^n / n + O(q^{n/2} / n), which is the finite-field Riemann hypothesis and whose proof is short and combinatorial.

Source: adapted from "Prime number theorem" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Prime_number_theorem
