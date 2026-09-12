# Binomial theorem

The binomial theorem gives the expansion of a two-term expression $(x+y)$ raised to a positive whole number $n$:

$$(x+y)^n = \binom{n}{0}x^n + \binom{n}{1}x^{n-1}y + \binom{n}{2}x^{n-2}y^2 + \cdots + \binom{n}{n}y^n$$

Each term has powers of $x$ and $y$ summing to $n$. The coefficient $\binom{n}{k}$, read "$n$ choose $k$", counts how many ways to pick $k$ items from a set of $n$.

## The coefficients

$$\binom{n}{k} = \frac{n!}{k!\,(n-k)!} = \frac{n(n-1)\cdots(n-k+1)}{k!}$$

The result is always a whole number. Across $k = 0, 1, \ldots, n$ for fixed $n$ these form the $n$th row of *Pascal's triangle*. Pascal's rule says each interior entry equals the sum of the two above it:

$$\binom{n}{k} = \binom{n-1}{k-1} + \binom{n-1}{k}$$

Each row is symmetric: $\binom{n}{k} = \binom{n}{n-k}$.

## A concrete example

For $n = 4$:

$$(x+y)^4 = x^4 + 4x^3y + 6x^2y^2 + 4xy^3 + y^4$$

Expanding $(x+y)^n$ gives $2^n$ raw products before collecting like terms, then $n+1$ terms whose coefficients sum to $2^n$. For $(x+y)^3$ the eight raw products include $xyx$, $yxy$, $yyx$ that all collapse to $xy^2$, and $1+3+3+1 = 8 = 2^3$.

Substituting $y = 2$:

$$(x+2)^3 = x^3 + 3x^2(2) + 3x(2)^2 + 2^3 = x^3 + 6x^2 + 12x + 8$$

With a negative second term, signs alternate: $(x-2)^3 = x^3 - 6x^2 + 12x - 8$. Setting $y=1$ gives the single-variable form $(x+1)^n = \sum_{k=0}^{n}\binom{n}{k}x^k$.

## Why the formula works

Write $(x+y)^n$ as $n$ copies of $(x+y)$ multiplied. Expanding with the distributive law, each choice of $x$ or $y$ from each copy yields a product $x^{n-k}y^k$. The number of choices producing $x^{n-k}y^k$ equals the number of ways to select which $k$ of the $n$ factors contribute a $y$, which is $\binom{n}{k}$. This is why $\binom{n}{k}$ controls both the algebra and the count of $k$-element subsets of an $n$-element set.

## A geometric view

For $n=2$, a square of side $a+b$ splits into a square of side $a$, a square of side $b$, and two $a \times b$ rectangles. For $n=3$, a cube of side $a+b$ splits into two cubes plus three $a \times a \times b$ and three $a \times b \times b$ boxes. The same picture in $n$ dimensions gives a geometric reason that the derivative $(x^n)' = nx^{n-1}$: increasing one side by $\Delta x$ adds volume equal to the combined $(n-1)$-dimensional area of $n$ faces.

## Beyond nonnegative integer exponents

Newton's generalisation extends the theorem to any real or complex exponent $r$ as an infinite series, convergent when $|y/x| < 1$:

$$(x+y)^r = x^r + rx^{r-1}y + \frac{r(r-1)}{2!}x^{r-2}y^2 + \frac{r(r-1)(r-2)}{3!}x^{r-3}y^3 + \cdots$$

Here $\binom{r}{k} = \frac{r(r-1)\cdots(r-k+1)}{k!}$. For non-integer $r$ the series never terminates. Two important cases:

$$\sqrt{1+x} = 1 + \tfrac{1}{2}x - \tfrac{1}{8}x^2 + \tfrac{1}{16}x^3 - \tfrac{5}{128}x^4 + \cdots \quad (|x|<1)$$

$$\frac{1}{1+x} = 1 - x + x^2 - x^3 + \cdots \quad (|x|<1)$$

The second recovers the geometric series. For sums of more than two terms, the *multinomial theorem* states $(x_1+\cdots+x_m)^n$ is a sum over exponent tuples $(k_1,\ldots,k_m)$ with sum $n$, with coefficient $\frac{n!}{k_1!\,k_2!\cdots k_m!}$, which counts ways to partition an $n$-set into subsets of those sizes. The general Leibniz rule gives the same form for the $n$th derivative of a product: $(fg)^{(n)}(x) = \sum_{k=0}^{n}\binom{n}{k}f^{(n-k)}(x)g^{(k)}(x)$.
