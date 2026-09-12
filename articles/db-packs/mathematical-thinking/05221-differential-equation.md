# Differential equation

A differential equation is a mathematical statement that links an unknown function with one or more of its derivatives, the rates at which the function changes. Because a derivative encodes how fast a quantity is changing, the equation expresses a rule tying a quantity's rate of change to its current value or to other quantities.

In practice, differential equations appear wherever a system is described by a rule about change: a planet's velocity changes under gravity, a population grows, heat diffuses through a solid. Solving the equation means finding the specific function of time or space that the rule forces. Most physical laws, from Newton's second law to Fourier's law of heat conduction, take this form.

## How equations are solved

A closed-form solution is an explicit formula for the unknown function. Only the simplest equations admit one. For everything else, two other routes exist. Numerical methods, such as the Euler method, compute approximate values step by step, replacing the continuous equation with a related difference equation in which the variable takes only discrete values. Qualitative theory, drawn from dynamical systems, asks about long-term behaviour: does the solution settle, oscillate, or grow without bound, without ever writing the formula.

A general solution to an ordinary differential equation of order *n* contains *n* arbitrary constants, one for each integration step. Pinning down a particular solution requires *n* extra conditions. When the independent variable is time, these are initial conditions, such as a particle's starting position and velocity, and together with the equation they form an initial value problem. When conditions are given at different positions, for example a string held fixed at both ends, they are boundary conditions and form a boundary value problem.

A first-order equation $\frac{dy}{dx} = g(x,y)$ with $y(a) = b$ has a local solution whenever $g$ is continuous on a rectangle around $(a,b)$, the content of the Peano existence theorem. The same equation need not have a unique solution. Existence and uniqueness are nontrivial in general and remain major topics of study.

## Classification

Equations are sorted by structural features that determine which techniques apply.

- Ordinary versus partial. An ODE involves a function of one variable, such as $y(x)$, and ordinary derivatives. A PDE involves a function of several variables and partial derivatives, with $u(x,y)$ depending on $x$ and $y$ simultaneously. PDEs are the natural language of fields that vary in space, from heat conduction to fluid flow.
- Linear versus nonlinear. A linear equation is linear in the unknown function and its derivatives; the harmonic oscillator $\frac{d^2 u}{dx^2} + \omega^2 u = 0$ is the prototype. Linear equations have a well-developed theory, and many can be solved in terms of integrals. A nonlinear equation, such as the pendulum equation $L\frac{d^2 u}{dx^2} + g\sin u = 0$, is harder: few exact methods exist, solutions can display chaotic behaviour, and even basic existence and uniqueness questions remain open in important cases such as the Navier–Stokes equations. Nonlinear equations are often studied by linearising them around a known solution, an approximation valid only in a restricted regime such as small oscillations.
- Homogeneous versus inhomogeneous. A linear equation is homogeneous if every term contains the unknown function or one of its derivatives. If a term involves only the independent variable, such as $x^2$ in $\frac{du}{dx} = cu + x^2$, the equation is inhomogeneous.
- Order. The order is the highest derivative that appears; most natural phenomena are governed by first- or second-order equations, with rare higher-order cases such as the fourth-order thin-film equation.

A delay differential equation (DDE) makes the derivative depend on the function's value at earlier times. Stochastic differential equations (SDEs) and stochastic partial differential equations (SPDEs) replace ordinary unknowns with random processes, such as Wiener-driven diffusion. An integro-differential equation mixes derivatives with integrals, and a differential-algebraic equation (DAE) pairs differential relations with algebraic constraints. Difference equations, in which the variable takes only discrete values, are the discrete cousins of differential equations and form the basis of most numerical solvers.

## A brief history

The subject began with calculus. In 1671 Newton listed three forms in *Methodus fluxionum et Serierum Infinitarum*, $\frac{dy}{dx} = f(x)$, $\frac{dy}{dx} = f(x,y)$, and a partial-equation form, and solved them with infinite series. In 1695 Jacob Bernoulli proposed the Bernoulli equation $y' + P(x)y = Q(x)y^n$, solved by Leibniz the following year. In 1746 d'Alembert derived the one-dimensional wave equation for a vibrating string; within a decade Euler extended it to three dimensions. The 1750s brought the Euler–Lagrange equation from the tautochrone problem, the curve along which a weighted particle falls to a fixed point in equal time regardless of starting point, which Lagrange solved in 1755 and which became the foundation of Lagrangian mechanics. In 1822 Fourier published *Théorie analytique de la chaleur*, introducing his heat equation based on Newton's law of cooling.

## Why the same equation shows up everywhere

Sound in air, light, and ripples on a pond are all described by the same second-order partial differential equation, the wave equation, which is why they are grouped as wave phenomena. Heat conduction and a wide class of diffusion processes are all governed by Fourier's heat equation. When a single equation captures superficially different systems, its mathematics acts as a shared explanatory backbone, and the methods developed for it transfer from one field to the next.
