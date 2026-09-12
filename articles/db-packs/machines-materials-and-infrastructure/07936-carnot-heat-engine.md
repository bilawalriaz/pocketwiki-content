# Carnot heat engine

A Carnot heat engine is a theoretical device that converts heat into work by moving a working fluid through a cycle between a hot reservoir at absolute temperature $T_H$ and a cold reservoir at $T_C$. Absolute temperature is measured in kelvins starting from absolute zero, the coldest possible temperature. The Carnot engine is the most efficient heat engine physically possible, and its efficiency depends only on the two reservoir temperatures. No real engine can match it, but it sets the upper limit against which every real engine is compared.

A heat engine transfers energy from a warm region to a cool one and converts part of that energy into mechanical work. Running the cycle in reverse makes the device move heat from cold to hot, acting as a refrigerator or heat pump.

## Origins

In 1824 the French military engineer Nicolas Léonard Sadi Carnot published *Reflections on the Motive Power of Fire*, a short book aimed at practical engineers. His motivation was economic: in France, as in Cornwall, imported coal was costly, so improving the efficiency of steam engines mattered. Carnot's diagram used two bodies, a hot furnace A and a cold refrigerator B, treated as unlimited reservoirs of "caloric" (heat). A working substance inside a cylinder absorbs heat from A, does work by pushing a piston, and dumps the remaining heat into B.

Benoît Paul Émile Clapeyron restated the ideas graphically in 1834, and Rudolf Clausius developed them mathematically in 1857, work that led directly to the concept of entropy, a measure of how spread out energy is at a given temperature.

## The cycle

A working body (any fluid capable of expansion) draws heat $Q_H$ from the hot reservoir, delivers work $W$ to the surroundings, and rejects waste heat $Q_C$ to the cold reservoir. Energy conservation gives $W = Q_H + Q_C$, with $Q_C$ negative because heat leaves the system.

The idealised cycle has four reversible steps. A reversible process is one that can be run backward without leaving any net change in the system or surroundings.

| Step | Process | What happens |
|------|---------|--------------|
| A→B | Isothermal expansion at $T_H$ | Gas expands at constant temperature, absorbing $Q_H$ from the hot reservoir |
| B→C | Isentropic (reversible adiabatic) expansion | Insulated gas continues to expand, cooling to $T_C$ |
| C→D | Isothermal compression at $T_C$ | Surroundings compress the gas, expelling $Q_C$ to the cold reservoir |
| D→A | Isentropic compression | Insulated gas is compressed, heating back to $T_H$ |

The two isothermal steps transfer entropy between reservoirs, while the two adiabatic steps (no heat enters or leaves) change the gas's temperature without changing its entropy. Because the working fluid returns to its original state, its entropy change over a full cycle is zero.

## Efficiency

Efficiency is the fraction of input heat converted to work:

$$\eta = \frac{W}{Q_H} = 1 + \frac{Q_C}{Q_H}$$

For a reversible cycle the entropy absorbed from the hot reservoir equals the entropy dumped to the cold reservoir: $Q_H/T_H = -Q_C/T_C$. Substituting gives the Carnot efficiency:

$$\eta_I = 1 - \frac{T_C}{T_H}$$

The temperatures must be absolute. On the Celsius or Fahrenheit scale, ratios of temperatures do not give correct efficiencies because those scales have a different zero point than thermodynamics requires.

## Carnot's theorem

Carnot's theorem states that no engine operating between two given reservoirs can be more efficient than a Carnot engine operating between the same reservoirs. A corollary says that all reversible engines sharing the same reservoir temperatures are equally efficient.

Real engines fall short because they are irreversible. Friction, finite temperature differences during heat transfer, and uncontrolled expansion all increase the total entropy of reservoirs and working fluid together. The same inequality that bounds efficiency, $Q_H/T_H \leq -Q_C/T_C$, is a statement of the second law of thermodynamics, and it forces $\eta \leq \eta_I$ for every real engine.

## Why it cannot be built

To stay reversible, every step must be performed infinitely slowly. The hot reservoir must be only infinitesimally hotter than the gas during heat absorption, and the external force on the piston must be reduced by infinitesimal amounts so the gas stays in thermal equilibrium (uniform temperature throughout). These requirements make one cycle take infinite time, so a true Carnot engine produces zero power. It is a theoretical ceiling, not a working machine.

## Diesel and the reach for the ideal

Rudolf Diesel patented an internal combustion engine in 1892 meant to approximate the Carnot cycle. He planned to compress air to 250 atmospheres at 800 °C, then add fuel so slowly that combustion heat was offset by expansion cooling, producing isothermal expansion and an efficiency near 73%. The technology of the day could not supply the huge air mass required, and Diesel settled for a high-compression cycle in which fuel is injected near the end of the compression stroke and ignited by the heat of compression. Practical Diesel engines reached about 40% efficiency by 1969, still well below the Carnot ceiling but far above the 7% achieved by the best steam engines of Diesel's lifetime.

The Carnot cycle also shows that the efficiency of any reversible engine is independent of the working substance. Water vapour, alcohol vapour, mercury vapour, air, or any other fluid gives the same ideal efficiency for given reservoir temperatures, because only the temperatures appear in the formula.
