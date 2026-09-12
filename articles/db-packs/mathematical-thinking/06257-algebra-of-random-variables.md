# Algebra of random variables

In statistics, a **random variable** assigns a number to each outcome of a random process, and its **probability distribution** describes how likely each value is. The algebra of random variables collects symbolic rules for manipulating these variables and for computing the **expected value** (mean), **variance** (spread), and **covariance** (co-movement) of the result, without appealing to the full distribution each time. Two random variables are **independent** when knowing the value of one gives no information about the other.

## Elementary symbolic algebra

The symbolic rules mirror ordinary algebra. For two random variables $X$ and $Y$, addition $X+Y$, subtraction $X-Y$, multiplication $XY$, division $X/Y$ (when $Y\neq 0$), and exponentiation $X^Y = e^{Y\ln X}$ all produce another random variable $Z$. The commutative and associative properties of ordinary algebra carry over, and replacing any variable with a constant $k$ (a random variable with $\Pr(X=k)=1$) preserves the rules.

## Expectation algebra

Expectation $E[Z]$ is **linear**: $E[X+Y]=E[X]+E[Y]$ and $E[X-Y]=E[X]-E[Y]$. For products, $E[XY]=E[YX]$ always holds, but $E[XY]=E[X]\cdot E[Y]$ holds only when $X$ and $Y$ are independent. The same independence condition gives $E[X/Y]=E[X]\cdot E[1/Y]$.

For any non-linear function $f$,

$$E[f(X)] \neq f(E[X]).$$

So $E[X^2]\neq E[X]^2$, $E[1/X]\neq 1/E[X]$, $E[e^X]\neq e^{E[X]}$, and $E[\ln X]\neq \ln(E[X])$. The exact value depends on the full distribution of $X$.

## Variance algebra

Writing $V$ for $\operatorname{Var}$ and $C$ for $\operatorname{Cov}$:

- $V[X+Y]=V[X]+2C[X,Y]+V[Y]$
- $V[X-Y]=V[X]-2C[X,Y]+V[Y]$

When $X$ and $Y$ are independent, $C[X,Y]=0$ and additions and subtractions give the same variance:

$$V[X+Y]=V[X-Y]=V[-X-Y]=V[X]+V[Y].$$

For products of independent variables,

$$V[XY]=V[X]\,V[Y]+V[X]\,(E[Y])^2+V[Y]\,(E[X])^2,$$

and an analogous formula holds for $V[X/Y]$, with $1/Y$ in place of $Y$. Shifting by a constant leaves variance unchanged, $V[k+Y]=V[Y]$, while scaling gives $V[kY]=k^2 V[Y]$. Variance does not pass through non-linear functions either: $V[f(X)]\neq f(V[X])$.

Two identities connect the operators:

$$V[X]=C[X,X]=E[X^2]-E[X]^2,\qquad C[X,Y]=E[XY]-E[X]E[Y].$$

## Covariance algebra

For $Z=X+Y$ and a third variable $X$, $C[X+Y,X]=V[X]+C[X,Y]$, which collapses to $V[X]$ under independence. Subtraction works the same way with a minus sign. For products of independent variables $C[XY,X]=V[X]\cdot E[Y]$, and for division $C[X/Y,X]=V[X]\cdot E[1/Y]$. Replacing any variable with a constant $k$ forces $C[X,k]=0$.

## Taylor-series approximation for non-linear functions

When $E[f(X)]$ or $V[f(X)]$ has no closed form, expand $f$ around the mean $\mu=E[X]$ as a Taylor series in $(X-\mu)^n$. The coefficients involve **central moments** $\mu_n(X)=E[(X-\mu)^n]$, with $\mu_0=1$ and $\mu_1=0$. Truncating after $n_{\max}$ terms gives an approximation; accuracy improves as more moments are included.

For a normal variable $X\sim N(\mu,\sigma^2)$, the standard normal $Z\sim N(0,1)$ has moments $\mu_n(Z)=0$ for odd $n$, and for even $n$ equal to $\prod_{i=1}^{n/2}(2i-1)$ (so $1, 3, 15, 105,\dots$). These closed-form moments turn the Taylor sums for $E[f(X)]$ and $V[f(X)]$ into finite expressions in the derivatives of $f$ at $\mu$ and powers of $\sigma$.

## Complex random variables and the algebraic view

In an algebraic axiomatization of probability, the primitive object is the random variable rather than the event. Probabilities are recovered by assigning an expectation to each variable, subject to four axioms: $E[k]=k$ for constants, $E[X^*X]\ge 0$, linearity $E[X+Y]=E[X]+E[Y]$, and homogeneity $E[kX]=kE[X]$. Random variables with commutativity and a conjugation operation $X\mapsto X^*$ (satisfying $(XY)^*=Y^*X^*$ and $X^{**}=X$) form a complex commutative $*$-algebra; a variable with $X=X^*$ is called "real." Relaxing commutativity leads to noncommutative probability, which underpins quantum probability, random matrix theory, and free probability.

Source: adapted from "Algebra of random variables" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Algebra_of_random_variables
