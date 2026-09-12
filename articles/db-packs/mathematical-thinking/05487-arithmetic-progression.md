# Arithmetic progression

An arithmetic progression is a list of numbers where each term is obtained by adding a fixed amount, called the common difference, to the previous term. The sequence 5, 7, 9, 11, 13, 15, ... is arithmetic with common difference 2. If the first term is $a_1$ and the common difference is $d$, the $n$-th term is

$$a_n = a_1 + (n-1)d.$$

A negative $d$ produces a decreasing sequence, and $d=0$ gives a constant one. A finite arithmetic progression is a bounded initial segment of such a sequence, and the sum of its terms is an arithmetic series.

## Sum of a finite progression

Writing the series forwards and backwards, then adding, pairs each term with one that sums to $a_1 + a_n$. With $n$ such pairs and the doubled total divided by 2:

$$S_n = \frac{n}{2}\bigl(a_1 + a_n\bigr) = \frac{n}{2}\bigl(2a_1 + (n-1)d\bigr).$$

For $2+5+8+11+14$, $n=5$ and the sum is $5(2+14)/2 = 40$. The formula also handles negative and fractional terms: $(-3/2)+(-1/2)+1/2 = 3(-3/2+1/2)/2 = -3/2$.

The arithmetic mean of the terms is $S_n/n = (a_1+a_n)/2$, the same expression as the mean of a discrete uniform distribution, because an arithmetic progression is a uniformly spaced sample.

## Product of a finite progression

The product of the $n$ terms factors as a rising factorial (a product of consecutive terms starting at some value):

$$a_1 a_2 \cdots a_n = \prod_{k=0}^{n-1}(a_1+kd) = d^n\left(\frac{a_1}{d}\right)^{\overline{n}}.$$

The rising factorial equals a ratio of Gamma functions, where the Gamma function extends the factorial to non-integer arguments via $\Gamma(z+1)=z\,\Gamma(z)$:

$$a_1 a_2 \cdots a_n = d^n\,\frac{\Gamma(a_1/d + n)}{\Gamma(a_1/d)}.$$

For $1\times 2\times\cdots\times n$ with $a_1=1$, $d=1$, the result is $n!$. For $m(m+1)\cdots n$ with positive integers $m\le n$, it is $n!/(m-1)!$. The first ten odd numbers, $1\cdot 3\cdot 5\cdots 19$, equal $2^{10}\,\Gamma(10.5)/\Gamma(0.5) = 654{,}729{,}075$. The formula requires $a_1/d>0$.

## Standard deviation

Because the terms are evenly spaced, the standard deviation of the $n$ terms is

$$\sigma = |d|\sqrt{\frac{(n-1)(n+1)}{12}},$$

matching the standard deviation of a discrete uniform distribution over those $n$ equally likely points, with $|d|$ as the step size.

## Intersections and subsets

The intersection of two arithmetic progressions extending infinitely in both directions is either empty or another arithmetic progression, found using the Chinese remainder theorem (a method for solving simultaneous congruences). If every pair in a family of such progressions overlaps, they all share a common number, so infinite arithmetic progressions form a Helly family, a family where pairwise overlap implies a common element. Intersecting infinitely many infinite progressions can collapse to a single number rather than a full progression.

Within $\{1,2,\ldots,n\}$, the number of arithmetic subsets of length $k$ is

$$a(n,k) = \frac{1}{2(k-1)}\Bigl((n-1)\bigl(n-(k-2)\bigr) + \phi(n+1,\,k-1)\Bigr),$$

where $\phi(\eta,\kappa)=0$ if $\kappa$ divides $\eta$, and otherwise $\phi(\eta,\kappa)=\bigl([\eta \bmod \kappa]-2\bigr)\bigl(\kappa-[\eta \bmod \kappa]\bigr)$. For $n=7$, $k=3$, this gives $a(7,3)=9$, matching the nine triples: $\{1,2,3\},\{2,3,4\},\{3,4,5\},\{4,5,6\},\{5,6,7\},\{1,3,5\},\{3,5,7\},\{2,4,6\},\{1,4,7\}$.

## Historical note

The pairwise-summation trick behind the series formula is older than the often-repeated primary-school anecdote about Gauss. Similar rules appear in the work of Archimedes, Hypsicles, and Diophantus, with Zhang Qiujian in China, Aryabhata, Brahmagupta, and Bhaskara II in India, Alcuin, Dicuil, Fibonacci, and Sacrobosco in medieval Europe, and in Tosafist commentary on the Talmud, with the Pythagoreans of the 5th century BC as a likely earlier source.
