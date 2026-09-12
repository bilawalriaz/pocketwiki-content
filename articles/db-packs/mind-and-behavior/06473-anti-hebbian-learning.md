# Anti-Hebbian learning

Anti-Hebbian learning is a class of learning rule in which the strength of the synapse between two neurons is *reduced* when one neuron helps drive the other to fire. It is the deliberate inverse of Hebb's postulate, often paraphrased as "neurons that fire together wire together." Where Hebbian rules strengthen correlated firing, anti-Hebbian rules weaken it, giving a circuit a way to suppress predictable, self-generated, or redundant signals.

## Evidence from the mormyrid electric fish

The clearest evidence comes from mormyrid electric fish, which probe their surroundings with a self-generated electric organ discharge (EOD). The electrosensory lateral-line lobe (ELL) receives input from knollenorgan electroreceptors that sense the local electric field. In parallel, the EOD command nucleus sends a copy of every motor command to fire the electric organ, an *efference copy* (an internal neural duplicate of a motor command), to the ELL.

The copy travels by two routes that converge on Purkinje-like Medium Ganglion cells, which also receive electrosensory input. These cells fire a *broad spike* (an action potential that propagates through the apical dendrites) when their combined inputs push them past threshold.

The plastic synapse sits between parallel fibers carrying the EOD command and the apical dendrites of the Medium Ganglion cells. The rule is time-locked: if parallel-fiber activation arrives just before a broad spike, that connection is *weakened*; in every other case, including arrival well before or at any point after the spike, the synapse is *strengthened*.

## Why the system needs it

Because the ELL receives both the efference copy of the motor output and the afferent input caused by that output, the fish can predict what its receptors will sense. A Hebbian rule would lock in those predictable signals. The anti-Hebbian rule instead cancels the expected reafference while preserving, and even strengthening, anything that does not match the predicted pattern. The result is a neural filter that highlights novel disturbances in the electric field, the signature of an object nearby.

The circuit also adapts: synaptic growth stops when excitation alone is enough to push the cell near threshold, so the neuron sits poised and small deviations from the now-familiar input again drive a broad spike. Slow drifts in the expected input come from growth, changes in water salinity, low water levels, and injury.

## Predicted location and application

Anti-Hebbian plasticity is thought to operate in the cerebellum, where similar circuitry could explain how the brain cancels predictable sensory consequences of movement. Understanding it may inform treatment of cerebellar disorders and the design of machine-learning systems that adjust to redundant inputs while flagging genuine changes.

## A worked algorithm: Földiák (1990)

Péter Földiák proposed a small network that puts the idea into equations. Input neurons $(x_1, \dots, x_n)$ connect to output neurons $(y_1, \dots, y_m)$ through weights $Q_{ij}$, and the outputs connect to each other through a symmetric weight matrix $W$ (so $W_{ij} = W_{ji}$). Each output unit's activity is a fixed point of

$$y_j = f\!\left(\sum_i x_i Q_{ij} + \sum_i y_i W_{ij} - t_j\right),$$

where $f(t) = 1/(1+e^{-\lambda t})$ is the logistic activation function and $t_j$ is the threshold. In matrix form, $y = f(xQ + yW - t)$, solved by integrating $\dot y = y - f(xQ + yW - t)$.

For each input vector, the network performs three updates. The anti-Hebbian step decorrelates the outputs:

$$\Delta W_{ij} = -\alpha\,(y_i y_j - p^2),$$

with $W_{ij}$ clamped to zero when $i = j$ or $W_{ij} > 0$. A Hebbian step feeds input through to active outputs:

$$\Delta Q_{ij} = \beta\, y_i (x_j - q_{ij}),$$

and a threshold step

$$\Delta t_i = \gamma\,(y_i - p)$$

keeps each output firing at a target rate $p$. Common inputs are pushed toward sparse, efficient codes that resemble a Huffman code emerging from the statistics of the data.

Source: adapted from "Anti-Hebbian learning" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Anti-Hebbian_learning
