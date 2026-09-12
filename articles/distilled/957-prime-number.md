# Prime number

## Overview
A prime number is a natural number greater than 1 that cannot be formed by multiplying two smaller natural numbers. Primes are the fundamental building blocks of arithmetic: the fundamental theorem of arithmetic states that every integer greater than 1 is either prime or factors uniquely into a product of primes (up to order). There are infinitely many primes, a fact proven by Euclid c. 300 BC. While no simple formula generates all primes, their statistical distribution is described by the prime number theorem (proven 1896), which states that the density of primes near a large number *n* is approximately 1/log *n*. Major unsolved problems include Goldbach's conjecture (every even integer > 2 is the sum of two primes) and the twin prime conjecture (infinitely many prime pairs differ by 2). Primes underpin modern public-key cryptography (e.g., RSA), which relies on the computational difficulty of factoring large numbers into their prime components.

## Timeline
- **c. 1550 BC** — Rhind Mathematical Papyrus contains Egyptian fraction expansions for prime and composite denominators.
- **c. 300 BC** — Euclid's *Elements* proves infinitude of primes, fundamental theorem of arithmetic, and constructs perfect numbers from Mersenne primes; Sieve of Eratosthenes invented.
- **c. 1000 AD** — Ibn al-Haytham discovers Wilson's theorem; Ibn al-Banna' optimizes sieve to check divisors only up to √*n*.
- **1202** — Fibonacci's *Liber Abaci* introduces trial division (up to √*n*) to Europe.
- **1640** — Fermat states Fermat's little theorem; investigates Fermat numbers (2²ⁿ+1); Mersenne studies Mersenne primes (2ᵖ−1).
- **1742** — Goldbach conjectures every even integer > 2 is the sum of two primes (in letter to Euler).
- **1852** — Chebyshev proves Bertrand's postulate: a prime exists between *n* and 2*n* for *n* > 1.
- **1859** — Riemann publishes paper on zeta function, linking its zeros to prime distribution; Riemann hypothesis posed.
- **1896** — Hadamard and de la Vallée Poussin independently prove the prime number theorem (π(*n*) ~ *n*/log *n*).
- **1970s** — Public-key cryptography (RSA) invented, giving primes major practical application.
- **2004** — Green–Tao theorem proves arbitrarily long arithmetic progressions of primes exist.
- **2013** — Yitang Zhang proves infinitely many prime gaps of bounded size exist.

## Body

### Definition and Elementary Properties
A natural number *n* > 1 is **prime** if its only positive divisors are 1 and *n* itself; otherwise it is **composite**. The number 1 is neither prime nor composite (it is a **unit**). Equivalently, *n* items cannot be arranged into a rectangular grid more than one dot wide and high. The first 25 primes (all < 100) are: 2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89, 97. No even number > 2 is prime; all primes > 5 end in 1, 3, 7, or 9 in decimal notation. The set of all primes is denoted **P** or **ℙ**.

**Unique Factorization:** Writing a number as a product of primes is its **prime factorization** (e.g., 50 = 2 × 5²). The **fundamental theorem of arithmetic** guarantees this factorization exists and is unique up to the order of factors. This makes primes the "basic building blocks" of natural numbers. Uniqueness relies on **Euclid's lemma**: if a prime *p* divides a product *ab*, then *p* divides *a* or *p* divides *b*.

**Infinitude:** Euclid's proof (c. 300 BC) shows any finite list of primes is incomplete. Multiply the listed primes *p₁...pₙ* and add 1 to get *N*. *N* has a prime factor (by fundamental theorem), but leaves remainder 1 when divided by any listed prime, so its factor is new. Thus no finite list contains all primes. The numbers *N* = 1 + ∏*pᵢ* are **Euclid numbers**; the first five are prime, but the sixth (30031 = 59 × 509) is composite.

**Formulas for Primes:** No non-constant polynomial takes only prime values. No efficient formula generates the *n*-th prime. Formulas exist (e.g., based on Wilson's theorem, Mills' theorem, Wright's theorem) but require knowing primes to compute constants, making them impractical for generation.

### History of Prime Number Theory
Early Greeks studied primes (*prōtos arithmòs*). Euclid established core theorems. Islamic mathematicians (c. 1000 AD) advanced the field: Ibn al-Haytham found Wilson's theorem (*n* divides (*n*−1)! + 1 iff *n* is prime); Ibn al-Banna' limited trial division to √*n*. Fibonacci transmitted these methods to Europe (1202).

17th–18th centuries: Fermat stated his little theorem (*aᵖ⁻¹* ≡ 1 mod *p*) and studied Fermat numbers; Mersenne studied Mersenne primes (2ᵖ−1). Goldbach conjectured every even number is a sum of two primes (1742). Euler proved the Euclid–Euler theorem (even perfect numbers ↔ Mersenne primes), introduced analysis (proving infinitude via divergence of Σ 1/*p*), and proved the divergence of the sum of reciprocals of primes.

19th century: Legendre and Gauss conjectured π(*x*) ~ *x*/log *x* (prime number theorem). Chebyshev proved Bertrand's postulate (1852). Riemann's 1859 zeta-function paper outlined a proof; Hadamard and de la Vallée Poussin completed it (1896). Dirichlet proved arithmetic progressions *a* + *bn* (with coprime *a*, *b*) contain infinitely many primes. Specialized primality tests emerged: Pépin's test for Fermat numbers (1877), Proth's theorem (c. 1878), Lucas–Lehmer test for Mersenne numbers (originated 1856).

20th–21st centuries: Since 1951, largest known primes found via computer tests (GIMPS project). Cryptography (1970s) revolutionized practical importance. Green–Tao theorem (2004): arbitrarily long arithmetic progressions of primes. Zhang (2013): infinitely many bounded prime gaps.

**Primality of One:** Historically debated. Greeks often excluded 1 from "number" concept. Some medieval/Renaissance mathematicians listed 1 as prime (Lehmer, 1914; lists until 1956). By early 20th century, consensus settled on excluding 1 to preserve unique factorization (otherwise *n* = *n* × 1 × 1...) and sieve functionality.

### Analytic Properties
**Analytic number theory** uses continuous functions to study integers. Euler solved the Basel problem (Σ 1/*n²* = π²/6 = ζ(2)). The **Riemann zeta function** ζ(*s*) = Σ 1/*nˢ* = ∏ (1 − *p*⁻ˢ)⁻¹ (Euler product) connects primes to complex analysis. The reciprocal 6/π² is the probability two random integers are coprime.

**Analytical Proof of Infinitude:** Euler showed Σ 1/*p* diverges (grows past any bound *x*), proving infinite primes. Mertens' second theorem describes its growth rate. By contrast, Σ 1/*n²* converges. **Brun's theorem**: Σ (1/*p* + 1/(*p*+2)) over twin primes converges, so Euler's method cannot resolve the twin prime conjecture.

**Prime Counting Function:** π(*n*) = number of primes ≤ *n*. **Prime number theorem**: π(*n*) ~ *n*/log *n* (ratio → 1). Implies *n*-th prime ~ *n* log *n* and average prime gap ~ log *n*. A sharper estimate is the **offset logarithmic integral** Li(*n*) = ∫₂ⁿ dt/log *t*.

**Arithmetic Progressions:** An infinite progression *a*, *a*+*q*, *a*+2*q*... contains >1 prime iff *a* and *q* are coprime. **Dirichlet's theorem**: if coprime, it contains infinitely many primes. **Green–Tao theorem** (2004): arbitrarily long finite progressions of only primes exist.

**Quadratic Polynomials:** Euler's *n²* − *n* + 41 yields primes for 1 ≤ *n* ≤ 40. No quadratic polynomial is proven to yield infinitely many primes. **Ulam spiral** visually suggests clustering on diagonals. **Bunyakovsky conjecture** (1857): irreducible polynomials with positive leading coefficient and no fixed divisor produce infinitely many primes. Generalized by Schinzel's Hypothesis H, Dickson's conjecture, Bateman–Horn conjecture.

**Zeta Function and Riemann Hypothesis:** ζ(*s*) = Σ *n*⁻ˢ = ∏ (1 − *p*⁻ˢ)⁻¹ for Re(*s*) > 1. **Riemann hypothesis** (1859, Millennium Prize Problem): all non-trivial zeros have real part 1/2. Original prime number theorem proof used a weak form (no zeros with Re(*s*)=1). Riemann's explicit formula expresses π(*x*) as a sum over zeta zeros; the main term is Li(*x*), fluctuations come from zeros. If hypothesis true, prime distribution is regular on short intervals (~√*x*).

### Abstract Algebra
**Modular Arithmetic & Finite Fields:** Arithmetic modulo *n* uses remainders {0, 1, ..., *n*−1}. Division by all non-zero elements is possible **iff** *n* is prime. Thus, modulo a prime forms a **finite field** (a ring where division works); composite moduli yield only a **ring**. **Fermat's little theorem**: *aᵖ⁻¹* ≡ 1 (mod *p*) for *a* ≢ 0. **Wilson's theorem**: *p* > 1 is prime iff (*p*−1)! ≡ −1 (mod *p*). **Giuga's conjecture**: the converse of the sum-of-powers condition is also sufficient for primality.

**p-adic Numbers:** The **p-adic order** νₚ(*n*) counts factors of *p* in *n*. The **p-adic absolute value** |*q*|ₚ = *p*⁻ᵛᵖ⁽ᑫ⁾ makes numbers close if their difference is divisible by a high power of *p*. Completing ℚ under this metric yields the **p-adic numbers** ℚₚ. **Ostrowski's theorem**: the only valuations on ℚ are the real absolute value and the p-adic ones. The **local–global principle** solves problems over ℚ by combining solutions from all completions (ℝ and ℚₚ).

**Prime Elements in Rings:** In a commutative ring *R*, a non-zero non-unit *p* is **prime** if *p* | *xy* ⇒ *p* | *x* or *p* | *y*. It is **irreducible** if not a product of two non-units. In ℤ, prime = irreducible = {±2, ±3, ±5...}. In general, prime ⇒ irreducible; converse holds in **unique factorization domains (UFDs)**. Example UFD: **Gaussian integers** ℤ[*i*] = {*a*+*bi*}. Rational primes ≡ 3 (mod 4) remain prime (Gaussian primes); primes ≡ 1 (mod 4) factor (e.g., 2 = (1+*i*)(1−*i*)) by Fermat's theorem on sums of two squares.

**Prime Ideals:** Not all rings are UFDs (e.g., ℤ[√−5] where 21 = 3·7 = (1+2√−5)(1−2√−5)). **Ideals** (subsets closed under addition and multiplication by ring elements) restore unique factorization. **Prime ideals** generalize prime elements (principal ideal of a prime element is prime). The **Lasker–Noether theorem** generalizes fundamental theorem: every ideal in a Noetherian ring is an intersection of primary ideals (generalizations of prime powers). The **spectrum** of a ring (its prime ideals as points) bridges algebra and geometry. Applications: quadratic reciprocity via prime ideals in quadratic fields; Kummer's **regular primes** (related to unique factorization failure in cyclotomic integers) for Fermat's Last Theorem; **Chebotarev's density theorem** on splitting of primes in extensions (generalizes Dirichlet's theorem).

**Group Theory:** **Sylow theorems**: if *pⁿ* divides group order, a subgroup of order *pⁿ* exists. **Lagrange's theorem**: groups of prime order are cyclic. **Burnside's theorem**: groups whose order has only two prime divisors are solvable.

### Computational Methods
**Trial Division:** Test divisibility by integers 2 to √*n* (or just primes in that range). Simple but exponential in digit length; impractical for large *n*. Used as a fast filter for small factors.

**Sieves:** **Sieve of Eratosthenes** (ancient) generates primes up to a limit by iteratively marking multiples. **Sieve of Atkin** is asymptotically faster. **Sieve theory** applies similar methods to other problems.

**Primality Testing vs. Proving:**
*   **Probabilistic (Monte Carlo):** Fast, tiny error chance. **Miller–Rabin** / **Solovay–Strassen**: repeat *k* times to reduce error to 2⁻ᵏ. A composite passing is a **pseudoprime**.
*   **Deterministic / Las Vegas (Guaranteed Correct):** **AKS primality test** (2002): polynomial time (proven), but slow in practice. **Elliptic curve primality proving (ECPP)**: fastest in practice, provides a quickly verifiable **primality certificate**, but runtime only heuristically proven.
*   **Strategy:** Use fast probabilistic test to filter candidates, then guaranteed-correct test to verify.

**Special-Purpose Algorithms:** Numbers of special forms allow faster tests. **Lucas–Lehmer test** determines primality of **Mersenne numbers** (2ᵖ−1) deterministically in time comparable to one Miller–Rabin iteration. Consequently, since 1992 the largest known prime has always been a Mersenne prime (GIMPS project). Prizes exist for 10M, 100M, 1B digit primes.

**Integer Factorization:** Harder than primality testing. **Trial division** / **Pollard's rho** find small factors. **Elliptic curve factorization** finds moderate factors. **Quadratic sieve** / **General number field sieve (GNFS)** handle arbitrary large numbers (GNFS is fastest for large *n*). **Special number field sieve** for special forms. Largest factored by general algorithm: RSA-240 (240 digits, 795 bits, Dec 2019). **Shor's algorithm** factors in polynomial time on a quantum computer; largest factored so far: 21 (2012).

**Other Applications:**
*   **Cryptography:** **RSA** relies on difficulty of factoring *xy* given product. **Diffie–Hellman** relies on easy modular exponentiation vs. hard discrete logarithm. 2048-bit primes standard.
*   **Hashing:** Universal hashing (Carter–Wegman) uses random linear functions modulo large primes; *k*-independent hashing uses higher-degree polynomials. Prime table sizes in quadratic probing ensure full coverage.
*   **Checksums:** ISBN uses modulo 11 (detects single-digit errors and transpositions). Adler-32 uses modulo 65521 (largest prime < 2¹⁶).
*   **Pseudorandom Generators:** Linear congruential generators, Mersenne Twister.

### Other Applications
**Constructible Polygons:** **Fermat primes** *Fₖ* = 2²ᵏ + 1. First five (3, 5, 17, 257, 65537) are prime; *F₅* and higher verified are composite. A regular *n*-gon is constructible with straightedge/compass **iff** odd prime factors of *n* are distinct Fermat primes. With angle trisector: prime factors can be 2, 3, and distinct **Pierpont primes** (2ᵃ3ᵇ + 1). Convex polygon partition into *n* equal-area/perimeter pieces possible **iff** *n* is a prime power.

**Quantum Mechanics:** Since 1970s (Montgomery, Dyson), speculation links Riemann zeta zeros to energy levels of quantum chaotic systems. Primes appear in quantum information (mutually unbiased bases, SIC-POVMs).

**Biology:** Cicadas (*Magicicada*) have life cycles of 7, 13, or 17 years (primes). Hypothesis: prime cycles prevent predator synchronization. Bamboo flowering intervals are hypothesized to be **smooth numbers** (only small prime factors).

**Arts & Literature:** Olivier Messiaen used prime-length motifs (e.g., 41, 43, 47, 53) for ametrical rhythms. Carl Sagan (*Contact*) proposed prime factorization for alien communication. Mark Haddon (*Curious Incident*) uses prime chapter numbers. Paolo Giordano (*Solitude of Prime Numbers*) uses primes as metaphor for isolation. Movie *Sneakers* (1992) features fictional fast factoring breaking encryption.

## Terms
- ****Prime number**** — Natural number > 1 with exactly two positive divisors: 1 and itself.
- ****Composite number**** — Natural number > 1 that is not prime (has divisors other than 1 and itself).
- ****Fundamental theorem of arithmetic**** — Every integer > 1 is either prime or factors uniquely into a product of primes (up to order).
- ****Prime factorization**** — Expression of a number as a product of prime numbers (e.g., 50 = 2 × 5²).
- ****Euclid's lemma**** — If prime *p* divides product *ab*, then *p* divides *a* or *p* divides *b*.
- ****Prime-counting function π(*n*)**** — Number of primes ≤ *n*.
- ****Prime number theorem**** — π(*n*) ~ *n*/log *n*; density of primes near *n* is ~1/log *n*.
- ****Riemann zeta function ζ(*s*)**** — Σ *n*⁻ˢ = ∏ (1 − *p*⁻ˢ)⁻¹ (Re(*s*) > 1); connects primes to complex analysis.
- ****Riemann hypothesis**** — Conjecture: all non-trivial zeros of ζ(*s*) have real part 1/2.
- ****Mersenne prime**** — Prime of form 2ᵖ − 1 where *p* is prime; largest known primes are of this type.
- ****Finite field**** — Modular arithmetic modulo a prime *p*; division by all non-zero elements is possible.
- ****p-adic numbers**** — Completion of rational numbers under metric where distance is *p*⁻ᵛᵖ⁽ˣ⁻ʸ⁾ (high powers of *p* = close).
- ****Prime ideal**** — Ideal *P* in a ring such that if *xy* ∈ *P*, then *x* ∈ *P* or *y* ∈ *P*; generalizes prime elements.
- ****Unique factorization domain (UFD)**** — Ring where every non-zero non-unit factors uniquely into irreducibles (e.g., ℤ, ℤ[*i*]).
- ****Probabilistic primality test**** — Fast algorithm (e.g., Miller–Rabin) with small, controllable error probability.
- ****AKS primality test**** — Deterministic polynomial-time primality test (theoretically important, slow in practice).
- ****Integer factorization**** — Decomposing a composite number into its prime factors; computationally harder than primality testing.
- ****RSA cryptosystem**** — Public-key encryption relying on the difficulty of factoring the product of two large primes.

## Debates and open questions