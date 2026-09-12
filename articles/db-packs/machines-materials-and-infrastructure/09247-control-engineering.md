# Control engineering

Control engineering is the discipline of making dynamic systems behave the way you want. It models a system in terms of inputs, outputs, and components, then designs a controller that drives the actual output toward a desired value (the *setpoint*) while keeping the response fast, accurate, and stable. The systems it targets include mechanical, electrical, fluid, chemical, financial, and biological ones. A washing machine, a car's cruise control, a fighter aircraft, and an industrial chemical reactor are all targets of the same basic theory.

## How a control loop works

In a *closed-loop* or *feedback* system, a sensor measures the *process variable* (PV), such as speed or temperature, and the controller compares it with the setpoint (SP). The difference, called the *error* (SP − PV), drives a corrective action: open a throttle, heat a furnace, push a rudder. Feedback lets the controller correct disturbances in real time.

A *PID controller* is the most common feedback controller. It combines three terms: proportional (respond to current error), integral (eliminate persistent steady-state error), and derivative (anticipate future error from its rate of change). Cruise control uses this idea by continually measuring vehicle speed and adjusting engine torque to hold the set speed. Control theory provides the mathematical tools (Laplace transforms, transfer functions, block diagrams) to predict stability and tune such controllers.

*Open-loop* control skips the feedback step. A washing machine that runs a fixed timed cycle without measuring the water or laundry state is open-loop: it cannot correct for load variations, so its design must be conservative enough to work in the worst case. Open-loop control is simpler but less robust than closed-loop control.

## A short history

Automatic control has existed for over two thousand years. The earliest documented feedback device is Ktesibios's water clock in Alexandria, around the third century BCE, which regulated flow by keeping a water level constant. Later mechanical feedback devices include a furnace temperature regulator attributed to Drebbel around 1620 and James Watt's centrifugal flyball governor of 1788, which held steam engine speed steady by throttling the valve as spinning weights flew outward.

In 1868, James Clerk Maxwell analyzed the flyball governor with differential equations and explained why it sometimes became unstable, demonstrating that mathematical models could predict the behavior of a control system. Routh (1874), Sturm, and Hurwitz (1895) later formalized stability criteria; Minorsky developed PID control theory from 1922 onward. Optimal control emerged in the 1950s and 1960s; stochastic, robust, adaptive, and nonlinear methods followed in the 1970s and 1980s. David Q. Mayne (1930–2024) developed rigorous algorithms for model predictive control, now used in tens of thousands of industrial applications.

## Continuous, discrete, and digital control

Classical control theory works in the continuous (time and frequency) domain and uses the Laplace transform. When computers entered the loop, designs had to handle the *discrete* domain, where a clock governs signals between a digital controller and a physical plant. The Z-transform plays the role of the Laplace transform in discrete-time analysis. Modern industrial systems mix both, with many continuous components (mechanical, fluid, biological, analog electrical) governed by a few digital controllers; engineers typically map the digital parts into the continuous domain to do the design.

Design has evolved from manual calculation to computer-aided design and then to computer-automated design using evolutionary computation, which can synthesize novel controller structures rather than just tune an existing one. *Resilient control systems* extend traditional robustness against planned disturbances to handle unexpected faults, malicious actions, and abnormal failure modes by adapting the controller's behavior on the fly.

## Education and practice

Control engineering is taught mainly within electrical and mechanical engineering, but also appears in mechatronics, aerospace, chemical (where it is called *process control*), and computer science programs. A typical curriculum starts with linear control in the time and frequency domains, then covers digital control and nonlinear control. Dedicated departments exist at institutions such as the University of Sheffield and the United States Naval Academy.

In industry, most control engineering work is embedded in roles like systems design, process engineering, instrumentation, or product development, and applies wherever a system can be modeled dynamically: aerospace, manufacturing, automotive, power, chemical, petroleum, and government.

Source: adapted from "Control engineering" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Control_engineering
