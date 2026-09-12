# Dirichlet's theorem on arithmetic progressions

If two positive integers $a$ and $d$ share no common factor other than 1 (they are **coprime**), then the arithmetic progression $a, a+d, a+2d, a+3d, \dots$ contains infinitely many prime numbers. Peter Gustav Lejeune Dirichlet proved this in 1837 using Dirichlet $L$-series, generalisations of the Riemann zeta function $\zeta(s)$ that track how residue classes sit among the integers. The result extends Euclid's theorem that there are infinitely many primes of the form $1+2n$, since $1$ and $2$ are coprime.

The coprimality condition is necessary: if $a$ and $d$ share a prime factor $p$, then every term of the progression is divisible by $p$, so at most one term can be prime. A progression such as $4n+2$ contains only the even number $2$ beyond finitely many composites.

## Stronger forms

Dirichlet's theorem guarantees infinitely many primes in each valid progression but says nothing about density. A stronger refinement states that primes are **asymptotically equally distributed** among the residue classes modulo $d$ that are coprime to $d$, where the number of such classes is $\varphi(d)$, Euler's totient function. Each such class receives a proportion $1/\varphi(d)$ of all primes. For $d=4$, $\varphi(4)=2$, so primes split evenly between the classes $4n+1$ and $4n+3$. For prime modulus $q$, the $q-1$ valid classes each receive proportion $1/(q-1)$. A still stronger form states that the sum of the reciprocals of the primes in any valid progression diverges, as does the sum of reciprocals of all primes.

A subtler phenomenon remains: progressions whose remainder is a quadratic nonresidue tend to contain slightly more primes than those with a quadratic residue remainder, a pattern known as **Chebyshev's bias**.

## A worked example: primes of the form $4n+3$

Euclid's proof of infinitely many primes adapts to specific progressions. For $4n+3$:

1. Suppose only finitely many such primes exist: $3, p_1, p_2, \dots, p_m$.
2. Form $N = 4p_1p_2\cdots p_m + 3$. Then $N \equiv 3 \pmod{4}$, and none of $3, p_1, \dots, p_m$ divides $N$.
3. Factor $N$. Since $N$ is odd, every prime factor is odd, hence $\equiv 1$ or $\equiv 3 \pmod{4}$. A product of primes all $\equiv 1 \pmod 4$ is itself $\equiv 1 \pmod 4$, contradicting $N \equiv 3 \pmod 4$. So $N$ has at least one prime factor $a' \equiv 3 \pmod{4}$.
4. That $a'$ is a prime of the form $4n+3$ not on the original list, contradicting the assumption.

This argument uses no calculus, only the structure of residues mod 4. The general proof, by contrast, shows that the value of the Dirichlet $L$-function at $1$ is nonzero, a step that requires analytic number theory.

## Distribution of primes in progressions

The table lists the first ten primes in several progressions, each of which contains infinitely many by Dirichlet's theorem.

| Progression | First ten primes | OEIS |
|---|---|---|
| $2n+1$ | 3, 5, 7, 11, 13, 17, 19, 23, 29, 31 | A065091 |
| $4n+1$ | 5, 13, 17, 29, 37, 41, 53, 61, 73, 89 | A002144 |
| $4n+3$ | 3, 7, 11, 19, 23, 31, 43, 47, 59, 67 | A002145 |
| $6n+1$ | 7, 13, 19, 31, 37, 43, 61, 67, 73, 79 | A002476 |
| $6n+5$ | 5, 11, 17, 23, 29, 41, 47, 53, 59, 71 | A007528 |
| $8n+1$ | 17, 41, 73, 89, 97, 113, 137, 193, 233, 241 | A007519 |
| $8n+3$ | 3, 11, 19, 43, 59, 67, 83, 107, 131, 139 | A007520 |
| $8n+5$ | 5, 13, 29, 37, 53, 61, 101, 109, 149, 157 | A007521 |
| $8n+7$ | 7, 23, 31, 47, 71, 79, 103, 127, 151, 167 | A007522 |

Progressions with odd $d$ and even remainder are often excluded from tables because half their terms are even, and the remaining half coincides with a progression of smaller modulus. For instance, $6n+1$ yields the same primes as $3n+1$ (from $n=1$), and $6n+5$ yields the same primes as $3n+2$ except for the prime $2$.

## History

Euler laid the groundwork in 1737 by showing $\zeta(1)$ diverges, equivalent to the divergence of the sum of reciprocal primes. In 1775 he proved the special case $a=1$ using cyclotomic polynomials. Legendre conjectured the general theorem in 1785 while attempting to prove quadratic reciprocity, but his proposed proof was later shown to be flawed. Dirichlet succeeded in 1837 with his $L$-series method, founding rigorous analytic number theory. Atle Selberg gave an elementary proof in 1949.

## Generalisations and refinements

The **Bunyakovsky conjecture** extends Dirichlet's theorem to irreducible polynomials of higher degree, asking whether $n^2+1$ takes infinitely many prime values (Landau's fourth problem), an open question. **Dickson's conjecture** and **Schinzel's hypothesis H** generalise further to several polynomials simultaneously. In algebraic number theory, **Chebotarev's density theorem** extends Dirichlet's result to Galois extensions of number fields.

**Linnik's theorem** (1944) bounds how large the smallest prime in a valid progression $a+nd$ must be: it is at most $cd^L$ for absolute constants $c$ and $L$, with $L$ later reduced to 5. Shiu (2000) showed that any valid progression contains arbitrarily long runs of consecutive primes. Sunada and Katsuda (1990) established a dynamical analogue.
