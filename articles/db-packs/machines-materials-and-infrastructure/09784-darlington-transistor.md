# Darlington transistor

A Darlington configuration, or Darlington pair, is a circuit of two bipolar transistors in which the emitter of the first feeds the base of the second, and both collectors are tied together. The current amplified by the first transistor is then amplified again by the second, so the pair behaves and is often packaged as a single transistor with one base, one collector, and one emitter. It was invented in 1953 by Sidney Darlington.

A bipolar transistor is a three-terminal device whose collector current is set by a much smaller base current; the ratio is the current gain β. In normal operation the base–emitter junction is forward-biased (about 0.65 V in silicon) and the base–collector junction is reverse-biased. "Saturation" is the state in which both junctions are forward-biased and the external circuit, not β, sets the collector current.

## Gain

The defining property of the pair is its very high current gain. If the two stages have gains β₁ and β₂, the pair's gain is

β_Darlington = β₁·β₂ + β₁ + β₂.

When both βs are in the hundreds, the sum terms are negligible, and β_Darlington ≈ β₁·β₂. A typical Darlington transistor therefore has a current gain of 1000 or more, so a tiny base current can switch much larger collector currents.

## Penalties

Stacking two transistors between base and emitter produces four practical penalties.

Base–emitter voltage is doubled. Two base–emitter junctions sit in series, so the pair needs about 1.3 V to turn on in silicon, not the 0.65 V of a single transistor. Circuits that expect a 0.7 V threshold can read a Darlington as still off.

Saturation voltage is about one V_BE higher than a single transistor's. Once the first transistor saturates, it applies 100% negative feedback between its collector and the second transistor's base, which prevents the second transistor from saturating. The output collector therefore sits at least one diode drop above the second base, so a silicon Darlington saturates near 0.75–0.85 V instead of the 0.1–0.2 V of a single silicon transistor. The extra drop at the same collector current dissipates more power as heat, and the higher output low level can upset TTL logic inputs.

Switch-off is slower. The first transistor cannot actively pull charge out of the second transistor's base, so stored charge lingers. Designers usually add a resistor of a few hundred ohms between the base and emitter of the second transistor; it provides a discharge path and speeds turn-off at the cost of a small standing current.

High-frequency stability is poorer. Two stages of delay add more phase shift than one, so a Darlington in a negative-feedback loop is more prone to oscillation than a single transistor.

## Construction and variants

Darlington pairs ship as integrated packages or as two discrete transistors wired together. The first stage (Q1) can be a small-signal transistor; the second stage (Q2) must carry the full load current, and the maximum collector current of the pair equals I_C(max) of Q2. Integrated versions save space by sharing a single collector diffusion region. A representative integrated power Darlington, the 2N6282, includes the turn-off resistor and reaches a current gain of about 2400 at I_C = 10 A.

A Darlington triplet adds a third transistor whose base is driven by the second transistor's emitter, with all three collectors tied together. Gain is then roughly β₁·β₂·β₃, but the extra V_BE drop, the worse saturation, and the slower switching rarely justify the gain, so triplets are uncommon.

## Applications

The very high current gain suits any place where a small control signal drives a large load.

Audio power amplifiers use Darlington pairs in the push–pull output stage that drives the loudspeaker. A fully symmetrical circuit uses an NPN Darlington on the positive supply to source current for the positive half of the waveform, and a PNP Darlington on the negative supply to source current for the negative half, both wired as emitter followers. Before high-quality PNP power transistors existed, designers used a quasi-symmetrical version in which only the positive-side pair was a true Darlington; the negative-side pair was a Sziklai pair, a complementary NPN-and-PNP arrangement that mimics a PNP Darlington using more available NPN parts.

A Darlington is sensitive enough that the tiny current passed through skin contact, even at safe extra-low voltages, can trigger it, so it works as the input stage of a touch-sensitive switch. Voltage regulators such as the LM1084 use an internal Darlington to deliver high load currents from a small driver signal, and the same pattern appears wherever a computer or logic output must control a motor or relay coil.

Source: adapted from "Darlington transistor" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Darlington_transistor
