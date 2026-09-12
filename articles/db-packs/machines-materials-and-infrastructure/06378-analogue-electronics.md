# Analogue electronics

Analogue electronics are electronic systems whose signal varies continuously, in contrast to digital electronics, where signals usually take only two discrete levels. The term *analogue* describes a proportional relationship between a signal and the voltage or current representing it, and comes from the Greek *analogos*, meaning "proportional".

## Analogue signals

An analogue signal uses some attribute of a medium to convey information. An aneroid barometer uses the angular position of a needle on a contracting and expanding box to represent atmospheric pressure; the needle's angle is proportional to the pressure.

Electrical signals represent information by varying their voltage, current, frequency, or total charge. A transducer converts energy from another physical form (sound, light, temperature, pressure, position) into an electrical signal; a microphone converts sound into voltage or current. The signal may take any value from a given range, each value representing different information. If one volt represents one degree Celsius, then 10 volts represents 10 °C and 10.1 volts represents 10.1 °C. Any change in the signal is meaningful, because the signal level corresponds directly to the level of the phenomenon it represents.

A signal can also be conveyed by modulation, where a property of a base carrier signal is altered by the source information. Amplitude modulation (AM) alters the amplitude of a sinusoidal carrier; frequency modulation (FM) alters its frequency; phase modulation alters its phase. In an analogue sound recording, varying air pressure striking a microphone creates a corresponding variation in the current through it or the voltage across it, with a louder sound producing a proportionally larger fluctuation while preserving the waveform shape. Mechanical, pneumatic, and hydraulic systems can also carry analogue signals.

## Inherent noise

Analogue systems invariably include noise, the random disturbances caused in part by the thermal vibrations of atomic particles. Because every variation of an analogue signal is significant, any disturbance is equivalent to a change in the original signal and so appears as noise. As the signal is copied, re-copied, or transmitted over long distances, these random variations accumulate, leading to signal degradation. Other sources include crosstalk from neighbouring signals and poorly designed components; shielding and low-noise amplifiers can reduce these effects.

## Analogue versus digital

All operations possible on an analogue signal, including amplification and filtering, can also be performed in the digital domain, and every digital circuit is also an analogue circuit, since the behaviour of any digital circuit can be explained using the rules that govern analogue circuits. Microelectronics has made digital devices cheap and widely available.

The effect of noise on an analogue circuit scales with the noise level: as noise grows, the signal becomes gradually less usable, a behaviour described as "failing gracefully"; intelligible information can still be recovered from a very noisy analogue signal. Digital circuits are unaffected by noise up to a threshold, at which point they fail catastrophically. Digital telecommunications can raise that threshold with error detection and correction coding, but a limit remains. Because digital information is quantised, a signal that stays within a range of values represents the same information, and the signal is regenerated at each logic gate, which lessens or removes noise. Analogue signal loss can be restored with amplifiers, but each amplifier adds its own noise according to its noise figure, and noise accumulates through the system.

## Precision

Signal precision depends chiefly on the noise present in the original signal and the noise added by processing, summarised as the signal-to-noise ratio. Fundamental physical limits, such as shot noise in components, set a floor on the resolution of analogue signals. In digital electronics, additional precision is obtained by using more digits to represent the signal; the practical limit is set by the analogue-to-digital converter (ADC), which takes an analogue signal and produces a series of binary numbers. A digital-to-analogue converter (DAC) performs the reverse, converting binary numbers back into an analogue signal. ADCs appear in thermometers, light meters, digital sound recording, and data acquisition; DACs appear in op-amp gain-control systems that feed digital amplifiers and filters.

## Design and construction

Analogue circuits are typically harder to design than comparable digital systems, because the application is built into the hardware and the circuit is usually designed by hand. Digital hardware shares much commonality across applications, can be mass-produced in standardised form, and consists largely of repeated identical blocks, so its design is highly automated. This is a main reason digital systems have displaced analogue ones in many roles, though any digital device that interacts with the real world still needs an analogue interface. Every digital radio receiver, for example, has an analogue preamplifier as its first stage. Software circuit simulators such as SPICE have eased analogue design by allowing circuits to be defined and tested in code.

Analogue circuits can be entirely passive, made from resistors, capacitors, and inductors, or active, adding transistors. Traditional circuits are built from discrete lumped elements; an alternative is distributed-element circuits built from transmission line.
