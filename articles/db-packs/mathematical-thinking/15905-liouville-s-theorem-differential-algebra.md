# Liouville's theorem (differential algebra)

Liouville's theorem, formulated by Joseph Liouville between 1833 and 1841, restricts which elementary functions have antiderivatives that are themselves elementary. Some elementary functions, such as $e^{-x^2}$, $\frac{\sin x}{x}$, and $x^x$, possess no elementary antiderivative; their integrals define new nonelementary functions like the error function. The theorem explains why.

## What the theorem says

If $f$ has an elementary antiderivative, that antiderivative must be built from elements already present in $f$, together with a finite number of logarithms. For instance, the antiderivative of $\sec x$ is $\log|\sec x + \tan x|$, a logarithm of trigonometric functions already appearing in $\sec x$. Formally: if $G$ is an elementary differential extension of $F$ with the same constants, and $g \in G$ satisfies $Dg = f \in F$, then there exist constants $c_1, \ldots, c_n$ and elements $f_1, \ldots, f_n, s \in F$ such that

$$f = c_1 \frac{Df_1}{f_1} + \cdots + c_n \frac{Df_n}{f_n} + Ds.$$

The antiderivative is therefore a finite linear combination of logarithmic derivatives of elements of $F$, plus the derivative of an element of $F$.

## Key definitions

A **differential field** $F$ is a field equipped with a derivation $D$ obeying the Leibniz rule $D(ab) = (Da)b + a(Db)$. Its **constants** are the subfield $\operatorname{Con}(F) = \{f \in F : Df = 0\}$.

A **logarithmic extension** of $F$ is a simple transcendental extension $G = F(t)$ where $Dt = Ds/s$ for some $s \in F$; $t$ behaves as a logarithm of $s$, even though $F$ need not contain any actual logarithm function. An **exponential extension** satisfies $Dt/t = Ds$ for some $s \in F$, so $t$ behaves as an exponential of $s$. An **elementary differential extension** is built by a finite chain of algebraic, logarithmic, and exponential extensions from $F$.

## Why it matters

The theorem provides a precise test for the existence of elementary antiderivatives. Take $F = \mathbb{C}(x)$, the rational functions in one variable, with ordinary differentiation. Its constants are $\mathbb{C}$. The function $1/x$ has no antiderivative in $\mathbb{C}(x)$, but $\ln x + C$ lives in the logarithmic extension $\mathbb{C}(x, \ln x)$.

The function $1/(x^2+1)$ appears to break the pattern: its antiderivative $\tan^{-1}x$ does not look like a logarithm of a rational function. Euler's formula resolves this. Writing

$$e^{2i\theta} = \frac{1 + i\tan\theta}{1 - i\tan\theta},$$

one obtains $\theta = \frac{1}{2i}\ln\!\left(\frac{1+i\tan\theta}{1-i\tan\theta}\right)$, and hence

$$\tan^{-1}x = \frac{1}{2i}\ln\!\left(\frac{1+ix}{1-ix}\right).$$

The arctangent is therefore a logarithm of a rational function, as the theorem requires.

## Connection to the Risch algorithm and Galois theory

Liouville's theorem is the theoretical core of the Risch algorithm, which decides, for a given elementary function, whether an elementary antiderivative exists and constructs it when possible.

Although sometimes cast as a result in differential Galois theory, the theorem needs no Galois theory for its proof. The differential Galois group of a simple antiderivative is either trivial or the additive group of constants, encoding only the constant of integration, so it carries no information about whether an elementary antiderivative exists.

Source: adapted from "Liouville's theorem (differential algebra)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Liouville%27s_theorem_%28differential_algebra%29
