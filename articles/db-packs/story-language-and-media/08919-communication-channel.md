# Communication channel

A communication channel is a physical or logical pathway that carries an information signal from one or more senders to one or more receivers. The signal may be a digital bit stream or an analog waveform. Every channel has a capacity, expressed as bandwidth in hertz (Hz) or as a data rate in bits per second.

Two broad classes of physical medium exist. Transmission-line media include twisted-pair, coaxial, and fiber-optic cables. Broadcast media include microwave, satellite, radio, and infrared. A logical channel is created on top of a physical one by multiplexing, sharing one medium among many signals through frequency-division or time-division.

In information theory, a channel is any system that maps an input to an output with some probability of error. A storage device such as a disk or tape counts as a channel because it sends a message across time, from writing to reading.

## Real-world examples

- A telephone circuit between two endpoints.
- A single path in a cable, or one slot in a frequency- or time-division multiplexed link.
- A radio frequency, pair, or band named with a letter, number, or codeword. Marine VHF uses about 88 channels in the VHF band; Channel 16 sits at 156.800 MHz.
- A television channel. North American analog Channel 2 was at 55.25 MHz, Channel 13 at 211.25 MHz, each 6 MHz wide, sized for analog signals. Digital television (DTV) uses image compression to fit several virtual channels inside one 6 MHz physical channel.
- A Wi-Fi channel in the ISM bands (original Wi-Fi offered 13 channels from 2412 MHz to 2484 MHz in 5 MHz steps).
- A ham radio repeater, which transmits on one frequency and listens about 600 kHz (0.6 MHz) away.

## Channel models

Real channels distort signals and add noise, so designers use models that map a transmitted input to a received output and predict errors.

Physically, a model can try to calculate what happens to the signal, such as every reflection of a radio wave in a room, and add random noise to mimic interference.

Statistically, a channel is an input alphabet, an output alphabet, and a transition probability *p(i, o)* for each pair: the probability that output *o* is received when input *i* is sent. A common wireless model combines a random attenuation of the signal (called fading) with additive noise; if the attenuation is complex, it also encodes propagation delay. Physical and statistical descriptions are usually combined.

The simplest statistical assumption is a memoryless channel, where each output depends only on the current input. When outputs depend on a sequence of inputs, the channel has memory.

## Digital and analog models

A digital channel model treats the message as bits at a given protocol layer, hiding the layers below, and reports bit rate, bit errors, delay, and delay variation. Common examples:

- Binary symmetric channel (BSC): a memoryless channel that flips each bit with a fixed probability.
- Binary asymmetric channel (BAC): like the BSC, with unequal flip probabilities for 0→1 and 1→0.
- Binary bursty bit error channel: errors arrive in clumps, so the channel has memory.
- Binary erasure channel (BEC): the receiver detects that a bit is missing rather than reading a wrong value.
- Packet erasure channel: whole packets are lost with a given packet loss or packet error rate.
- Arbitrarily varying channel (AVC): the channel's behaviour can change randomly.

An analog channel model treats the message as a continuous waveform and can be linear or non-linear, time-continuous or time-discrete, memoryless or dynamic, time-invariant or time-varying, baseband or passband. Typical impairments include additive white Gaussian noise (AWGN), a baseline linear noise model; phase noise; interference such as crosstalk or intersymbol interference (one symbol smearing into the next); distortion, including non-linear intermodulation; frequency response with attenuation and phase shift; fading (Rayleigh, Ricean, log-normal shadow, frequency-selective); Doppler shift, which makes the system time-variant; and ray tracing or propagation-graph models for specific transmitter–receiver geometries and terrain.

## Types of channel

Channels are classified along independent axes that combine in real systems:

- Digital (discrete) or analog (continuous).
- Transmission medium, such as a fiber-optic cable.
- Multiplexed channel, with several logical channels on one physical medium.
- Simplex, half-duplex, or duplex: one-way only, both ways but not at once, or both ways simultaneously.
- Uplink (upstream) or downlink (downstream), sometimes with a return channel.
- Broadcast, unicast, or multicast: to all users, to one user, or to a subscribing group.

## Performance measures

Capacity and quality use a small set of standard measures:

- Spectral bandwidth in hertz and symbol rate in baud (symbols per second).
- Digital bandwidth in bits per second: gross bit rate (signalling rate), net bit rate (information rate), channel capacity, and maximum throughput.
- Channel utilization and spectral efficiency.
- Signal-to-noise ratio in decibels, including signal-to-interference ratio and E_b/N_0.
- Bit error rate (BER) and packet error rate (PER).
- Latency in seconds: propagation time, transmission time, round-trip delay, end-to-end delay, and packet delay variation.

## Multi-terminal channels

When several endpoints share one medium, the channel is multi-terminal rather than a point-to-point pipe. Any complex multi-terminal network can be decomposed into a combination of these building blocks.

- Point-to-multipoint channel (broadcast medium): one sender reaches several destinations. The downlink of a single cellular cell, ignoring inter-cell interference, is an example. Most wireless media are physically broadcast but may not provide a broadcast service.
- Multiple access channel: many senders share a medium to reach one or a few receivers, requiring a channel access scheme such as a media access control (MAC) protocol combined with multiplexing. The uplink of a cellular network fits this model.
- Relay channel: intermediate nodes (relays, repeaters, or gap fillers) help carry a message to its destination.
- Interference channel: two senders each send to their own receiver, with possible crosstalk or co-channel interference. Inter-cell interference in cellular systems is the canonical case; in 3G spread-spectrum systems, interference can also arise inside a cell when non-orthogonal codes are used.

Source: adapted from "Communication channel" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Communication_channel
