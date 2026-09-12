# Velocity

## Overview
Velocity is a vector quantity in kinematics describing the rate of change of an object's position with respect to time, requiring both magnitude (speed) and direction for its definition. It is the derivative of position and the integral of acceleration, making it central to equations of motion. Unlike speed (a scalar), constant velocity requires motion in a straight line at constant speed; any change in direction constitutes acceleration. Velocity underpins derived quantities like momentum and kinetic energy and behaves differently under Galilean (Newtonian) versus Lorentz (relativistic) transformations.

## Timeline
- **17th Century** — Development of calculus by Newton and Leibniz enables formal definition of instantaneous velocity as derivative of position.
- **1687** — Newton's *Principia* establishes laws of motion linking velocity to momentum ($p=mv$) and force.
- **18th–19th Century** — Formulation of *suvat* equations for constant acceleration; development of kinetic energy ($E_k = \frac{1}{2}mv^2$) and fluid drag concepts.
- **1905** — Einstein's special relativity introduces the Lorentz factor ($\gamma$), making velocity relative to the observer's frame and imposing speed of light ($c$) as universal limit.

## Body

### Definition and Core Distinctions
Velocity is the rate of change of position ($\mathbf{v} = d\mathbf{s}/dt$). **Average velocity** is total displacement ($\Delta \mathbf{s}$) divided by time interval ($\Delta t$); **instantaneous velocity** is the limit of this ratio as $\Delta t \to 0$, geometrically the slope of the tangent on a displacement-time graph. The integral of velocity over time yields displacement. **Speed** is the scalar magnitude of velocity ($|\mathbf{v}|$). A critical distinction: an object in uniform circular motion has constant speed but *changing velocity* (due to direction change), thus undergoing centripetal acceleration.

### Equations of Motion
For **constant acceleration** ($\mathbf{a}$), the *suvat* equations apply:
*   $\mathbf{v} = \mathbf{u} + \mathbf{a}t$ (final velocity from initial $\mathbf{u}$)
*   $\mathbf{x} = \frac{(\mathbf{u}+\mathbf{v})}{2}t = \bar{\mathbf{v}}t$ (displacement from average velocity)
*   $v^2 = u^2 + 2(\mathbf{a}\cdot\mathbf{x})$ (Torricelli equation, time-independent)

**Average velocity** for variable motion is $\bar{\mathbf{v}} = \frac{\int \mathbf{v}(t)dt}{\Delta t}$. Special cases for average *speed* (scalar) include the arithmetic mean (equal time intervals) and harmonic mean (equal distance intervals). Average velocity magnitude is always $\le$ average speed because displacement $\le$ distance.

**Acceleration** is the derivative of velocity ($\mathbf{a} = d\mathbf{v}/dt$); conversely, velocity is the integral of acceleration ($\mathbf{v} = \int \mathbf{a}\,dt$). In Newtonian mechanics, acceleration is invariant across inertial frames; in special relativity, it is not.

### Quantities Dependent on Velocity
*   **Momentum** ($\mathbf{p} = m\mathbf{v}$): Vector quantity conserved in closed systems (Newton's 2nd Law).
*   **Kinetic Energy** ($E_k = \frac{1}{2}mv^2$): Scalar; depends on $v^2$.
*   **Drag Force** ($F_D = \frac{1}{2}\rho v^2 C_D A$): Opposes motion through a fluid; depends on density ($\rho$), cross-section ($A$), drag coefficient ($C_D$), and $v^2$.
*   **Escape Velocity** ($v_e = \sqrt{2GM/r} = \sqrt{2gr}$): Minimum *speed* to escape a gravitational body (Earth: ~11,200 m/s). Direction-independent; technically "escape speed."
*   **Lorentz Factor** ($\gamma = 1/\sqrt{1-v^2/c^2}$): Governs time dilation, length contraction, and relativistic momentum/energy in special relativity. Diverges as $v \to c$.

### Relative Velocity
Velocity of object A relative to B: $\mathbf{v}_{A/B} = \mathbf{v}_A - \mathbf{v}_B$ (vector difference in a shared inertial frame). In 1D: $v_{rel} = v - (\pm w)$ depending on direction. In Newtonian mechanics, relative velocity is frame-invariant; in special relativity, velocities add via the Einstein velocity addition formula (not simple vector subtraction), making them frame-dependent.

### Coordinate Systems
*   **Cartesian**: Velocity components are time derivatives of coordinates ($v_x = dx/dt$, etc.). Vector $\mathbf{v} = \langle v_x, v_y, v_z \rangle$; speed $|\mathbf{v}| = \sqrt{v_x^2+v_y^2+v_z^2}$.
*   **Polar (2D)**: Velocity decomposes into **radial velocity** ($v_R = \mathbf{v}\cdot\hat{\mathbf{r}}$, toward/away from origin) and **transverse velocity** ($v_T = \omega r$, perpendicular to radial, $\omega$ = angular speed). Angular momentum $L = m r v_T = m r^2 \omega$. For inverse-square central forces (gravity), $L$ is constant $\implies$ Kepler's laws: $v_T \propto 1/r$, $\omega \propto 1/r^2$, constant areal velocity.

## Terms
- ****Velocity**** — Vector rate of change of position: $\mathbf{v} = d\mathbf{s}/dt$; SI unit m/s.
- ****Speed**** — Scalar magnitude of velocity: $|\mathbf{v}|$.
- ****Instantaneous Velocity**** — Velocity at a specific instant; derivative of position; tangent slope on $s$-$t$ graph.
- ****Average Velocity**** — Total displacement / total time: $\Delta \mathbf{s}/\Delta t$; secant slope on $s$-$t$ graph.
- ****Acceleration**** — Rate of change of velocity: $\mathbf{a} = d\mathbf{v}/dt$; vector.
- ****Momentum**** — $\mathbf{p} = m\mathbf{v}$; conserved vector quantity in classical mechanics.
- ****Kinetic Energy**** — $E_k = \frac{1}{2}mv^2$; scalar energy of motion.
- ****Lorentz Factor ($\gamma$)**** — $\gamma = 1/\sqrt{1-v^2/c^2}$; relativistic correction factor diverging at $v=c$.
- ****Radial Velocity**** — Component of velocity along the position vector (toward/away from origin).
- ****Transverse Velocity**** — Component of velocity perpendicular to position vector; $v_T = \omega r$.
- ****Escape Velocity**** — Minimum speed to escape a gravitational field: $\sqrt{2GM/r}$.

## Debates and open questions
*   **Newtonian vs. Relativistic Velocity Addition**: The source highlights a fundamental divergence: Newtonian mechanics assumes absolute time and Galilean velocity addition (frame-invariant acceleration), while special relativity requires Lorentz transformations (frame-dependent velocities, invariant $c$). The transition between these frameworks at high velocities remains a conceptual boundary.
*   **Terminology: "Escape Velocity"**: The source notes this is a misnomer; the quantity is a scalar speed, independent of direction. The correct term is "escape speed."
*   **Instantaneous Velocity Intuition**: The source acknowledges the concept is "counter-intuitive" (defining motion at a frozen instant via limits/calculus), resolved by interpreting it as the velocity the object would maintain if acceleration ceased at that instant.

Source: adapted from "Velocity" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Velocity
