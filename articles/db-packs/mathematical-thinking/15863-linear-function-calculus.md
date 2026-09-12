# Linear function (calculus)

A linear function is a real-valued function whose graph in the Cartesian plane is a non-vertical straight line. Its defining property is proportionality: a change in the input produces a change in the output proportional to that of the input. In symbols,

$$f(x) = ax + b,$$

where $a$ and $b$ are constants and $x$ ranges over the real numbers $\mathbb{R}$.

## Form, slope, and intercept

The expression $ax + b$ is a polynomial in $x$ of degree at most one, a *linear polynomial*. The coefficient $a$ is called the *slope*; $b$ is the *y-intercept*, the value $f(0) = b$ at which the line crosses the y-axis. The y-intercept is also called the initial value of $f$.

When $a \neq 0$ the line also crosses the x-axis at the *x-intercept* $(-b/a, 0)$. That x-value, the solution of $f(x) = 0$, is the *root* or *zero* of $f$.

When $a = 0$, $f(x) = b$ is a *constant function* whose graph is a horizontal line. Some authors exclude constants from the class of linear functions; this article includes them. When $b = 0$, $f(x) = ax$ is *homogeneous* and its line passes through the origin. In advanced texts, "linear function" often means specifically the homogeneous case, with *affine function* reserved for the general form $ax + b$.

## Slope as a rate of change

The slope $a$ measures the line's steepness. Geometrically it is the rise-over-run ratio $\Delta y / \Delta x$ between any two points on the line. Algebraically it expresses a constant rate of change: increasing the input by one unit always changes the output by $a$ units,

$$f(x + 1) = f(x) + a,$$

and more generally $f(x + \Delta x) = f(x) + a\,\Delta x$ for any increment $\Delta x$. When $a > 0$ the function is increasing; when $a < 0$ it is decreasing.

Because the rate of change is the same at every point, the derivative of a linear function is the constant $f'(x) = a$. Linear functions are the only real functions with a constant derivative: if $f'(x) = a$ everywhere, then $f(x) = ax + b$ with $b = f(0)$.

## Linear approximation and tangent lines

Smooth curves are locally straight. Near any point $x = c$ where a function $f$ is differentiable, the curve $y = f(x)$ is approximated by the *tangent line*

$$f(x) \approx f'(c)(x - c) + f(c),$$

a linear function with slope $f'(c)$ passing through $(c, f(c))$. For most functions this approximating slope changes from point to point; for a linear function it does not, because $f'(x) = a$ everywhere.

## Three equivalent forms

The same line can be written three ways:

| Form | Equation | Highlights |
|---|---|---|
| Slope-intercept | $f(x) = ax + b$ | slope $a$ and y-intercept $b = f(0)$ |
| Point-slope | $f(x) = a(x - x_0) + y_0$ | slope $a$ and one known point $(x_0, y_0)$ |
| Two-point | $f(x) = \dfrac{y_1 - y_0}{x_1 - x_0}(x - x_0) + y_0$ | slope computed from two known points |

The two-point form comes from the identity

$$\frac{y - y_0}{x - x_0} = \frac{y_1 - y_0}{x_1 - x_0},$$

which says the rise-over-run between any point $(x, y)$ on the line and the reference point $(x_0, y_0)$ equals the constant slope set by the two known points.

## Relationship with linear equations

A linear equation $Ax + By = C$ describes a line in the xy-plane. If $B \neq 0$, solving for $y$ gives $y = -\tfrac{A}{B}x + \tfrac{C}{B} = ax + b$, a linear function. If $B = 0$, the result is the vertical line $x = C/A$, which cannot be written as $y = f(x)$ and so is not a function in this sense.

## Worked example: a budget problem

Suppose salami costs €6/kg, sausage costs €3/kg, and the budget is €12. If $x$ kg of salami and $y$ kg of sausage are bought, then $6x + 3y = 12$. Solving for $y$ gives $y = f(x) = -2x + 4$. The slope $-2$ means each extra kilogram of salami costs two kilograms of sausage. The y-intercept $(0, 4)$ is buying only sausage, four kilograms; the x-intercept $(2, 0)$ is buying only salami, two kilograms. Negative amounts are not meaningful, so the relevant domain is $0 \leq x \leq 2$. Choosing $y$ as the independent variable instead gives the inverse $x = g(y) = -\tfrac{1}{2}y + 2$, valid on $0 \leq y \leq 4$.

## Linear versus exponential and power laws

A straight line on standard Cartesian axes always represents a linear function, but on transformed axes it may represent something else. If $\log y = ax + b$ then $y = r^b \cdot (r^a)^x$, an exponential function of $x$: a linear function adds a fixed amount $a$ per unit increase in $x$, while an exponential multiplies by a fixed base. If $\log_r y = a \log_r x + b$ then $y = r^b \cdot x^a$, a power law, which appears as a straight line only when both axes use a logarithmic scale.

## Linear in polar coordinates

In polar coordinates $(r, \theta)$, the equation $r = a\theta + b$ has the algebraic shape of a linear function but its graph is not a straight line. When $a \neq 0$ it traces an Archimedean spiral, winding outward at a constant rate; when $a = 0$ it is $r = b$, a circle of radius $b$ centred at the origin.

Source: adapted from "Linear function (calculus)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Linear_function_%28calculus%29
