# Prime number

A prime number is a natural number greater than 1 whose only positive divisors are 1 and itself. Every integer greater than 1 is either prime or composite, meaning it can be written as a product of two smaller natural numbers greater than 1. The number 1 is neither prime nor composite; by the early 20th century mathematicians excluded it because including it would break the uniqueness of prime factorisations and the workings of the sieve of Eratosthenes.

Primes are the building blocks of the positive integers. The fundamental theorem of arithmetic states that every integer greater than 1 can be written as a product of primes, and that this product is unique apart from the order of the factors. For example, 50 = 2 × 5², and no other combination of primes multiplies to 50. Proofs usually rely on Euclid's lemma: if a prime p divides the product a·b, then p divides a or p divides b.

## How many primes are there

There are infinitely many primes. Euclid's proof assumes a finite list exists, multiplies the primes together, and adds 1 to form N. The result N leaves remainder 1 when divided by every listed prime, so its prime factors lie outside the list, contradicting completeness. The numbers constructed this way, called Euclid numbers, are not always prime; 30031 = 59 × 509 is a counterexample. Euler later gave a second proof: the sum of the reciprocals of the primes diverges.

As numbers grow, primes become rarer but never disappear. The prime-counting function π(n) counts the primes up to n, and the prime number theorem, proved by Hadamard and de la Vallée Poussin in 1896, shows that π(n) is asymptotic to n/log n, meaning the ratio approaches 1 as n grows. The logarithmic integral Li(n) gives a closer approximation. The average gap between consecutive primes near n is about log n, so gaps grow slowly but without bound.

## Structure and arithmetic of primes

A small observation simplifies the search for primes: any even number greater than 2 equals 2 times another integer, so it is composite. Apart from 2, every prime is odd, and apart from 5 every prime ends in 1, 3, 7, or 9 in decimal. Modular arithmetic modulo a prime p forms a finite field, meaning every nonzero residue has a multiplicative inverse, whereas arithmetic modulo a composite number forms only a ring. Wilson's theorem captures this precisely: p is prime if and only if (p−1)! ≡ −1 mod p.

Primes appear in structured families. Dirichlet's theorem states that any arithmetic progression a + bn with a and b sharing no common factor contains infinitely many primes, so 5, 17, 29, 41, … and 7, 19, 31, 43, … are both infinite. The Green–Tao theorem, proved in 2004, goes further: the primes contain arithmetic progressions of any desired length, such as 5, 11, 17, 23, 29, where every term is prime. Twin primes are pairs such as (3, 5) or (11, 13) that differ by 2; whether there are infinitely many such pairs is unknown.

## Special forms and open questions

A Mersenne prime has the form 2^p − 1 with p prime. The largest known primes are almost always Mersenne primes because the Lucas–Lehmer test checks them far more efficiently than general numbers. A Fermat number has the form 2^(2^n) + 1; the first five Fermat numbers are prime, but no others have been found and most are known to be composite. Euclid showed that if 2^p − 1 is prime, then 2^(p−1) · (2^p − 1) is a perfect number, linking primes to another area of number theory.

Several central questions remain open. Goldbach's conjecture asserts that every even integer greater than 2 is a sum of two primes; it has been verified up to 4·10¹⁸ but never proved. The twin prime conjecture asks whether infinitely many pairs of primes differ by 2, and Polignac's conjecture generalises this to gaps of any even size. The Riemann hypothesis, proposed in 1859, holds that every nontrivial zero of the Riemann zeta function has real part 1/2; a proof would give sharp control over prime distribution even between consecutive integers, and it remains one of the seven Millennium Prize Problems.

## Generalisations and computation

In ring theory, a prime element p in an integral domain has the property that if p divides a product, it divides one of the factors, mirroring Euclid's lemma. In unique factorisation domains such as the Gaussian integers a + bi, factorisation remains unique, though ordinary primes may split: 2 = (1+i)(1−i) in the Gaussian integers, while 3 and 7 remain prime there. Rings where factorisation fails, such as ℤ[√−5] where 21 = 3·7 = (1+2√−5)(1−2√−5), motivated the definition of prime ideals, a central object in algebraic number theory.

Testing whether a number is prime can be done by trial division up to √n, but the work grows exponentially with the number of digits. Probabilistic tests such as Miller–Rabin run quickly but can very rarely be fooled by composite numbers called pseudoprimes. AKS and elliptic curve primality proving give guaranteed answers in polynomial time and dominate in practice. Factoring a large integer is believed to be much harder than testing it for primality, and this asymmetry underlies RSA, the public-key cryptosystem invented in the 1970s. Shor's algorithm could factor large numbers efficiently on a quantum computer, and the largest integer factored this way so far is 21.
