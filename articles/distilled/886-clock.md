# Clock

## Overview
A clock is a device that measures and displays time intervals shorter than natural units like the day or year. It is one of humanity's oldest inventions, evolving from continuous-flow devices (sundials, water clocks) to periodic oscillators (pendulums, quartz crystals, atomic vibrations) that enable far greater accuracy. The critical breakthrough was the **verge escapement** (c. 1300), which regulated the release of stored energy, creating the first true mechanical clocks. Subsequent innovations—spring drives (15th century), the pendulum (1656), the balance spring (1675), and the marine chronometer (mid-18th century)—progressively improved precision, enabling scientific astronomy and global navigation. Modern clocks count oscillations of a **harmonic oscillator** (a resonator vibrating at a precise natural frequency) via a controller, counter chain, and indicator. Atomic clocks, measuring electron transitions in atoms (e.g., caesium-133), now define the second and achieve stability within two parts in 10^18.

## Timeline
- **c. 16th century BC** — Bowl-shaped outflow water clocks exist in Babylon and Egypt.
- **3rd century BC** — Archimedes invents the first known geared clock (astronomical/cuckoo).
- **723–725 AD** — Yi Xing and Liang Lingzan build the first clockwork escapement for a water-powered armillary sphere (Tang China).
- **1088** — Su Song completes the Kaifeng astronomical clock tower, uniting clepsydra and mechanical clock concepts (Song China).
- **c. 1300** — Verge escapement invented in Europe, enabling first weight-driven mechanical clocks.
- **1386** — Salisbury Cathedral clock built; oldest surviving mechanical striking clock.
- **c. 1430** — Earliest existing spring-driven clock (chamber clock of Phillip the Good).
- **1584** — Jost Bürgi invents cross-beat escapement and remontoire; accuracy reaches ~1 minute/day.
- **1656–1657** — Christiaan Huygens invents and builds first pendulum clock (Hague).
- **1670–1671** — William Clement creates anchor escapement and longcase (grandfather) clock (England).
- **1675** — Huygens and Robert Hooke invent the spiral balance spring (hairspring), enabling accurate pocket watches.
- **1714** — British Longitude Act offers £20,000 for accurate longitude determination at sea.
- **1761** — John Harrison’s H4 marine chronometer tested; error < 5 seconds over 10 weeks.
- **1840** — Alexander Bain patents the electric clock.
- **1927** — Warren Marrison and J.W. Horton build first quartz clock (Bell Labs, Canada).
- **1955** — Louis Essen builds first accurate caesium atomic clock (UK National Physical Laboratory).
- **1969** — Seiko releases Astron, the first quartz wristwatch.
- **2013** — Ytterbium atomic clocks achieve stability < 2×10⁻¹⁸.

## Body

### Pre-Mechanical Timekeeping
Before mechanical clocks, societies relied on continuous processes. **Sundials** tracked the sun’s shadow on a marked surface, measuring local solar time within minutes given known latitude; they remained reference standards for calibrating other clocks until the telegraph standardized time zones in the 1830s. **Duration timers** (candle clocks, incense clocks, hourglasses) measured elapsed intervals without reference to time of day. **Water clocks (clepsydrae)**, possibly the oldest instruments after tally sticks, used regulated water outflow (Babylon/Egypt, c. 16th century BC) or inflow. Greek and Roman engineers improved their accuracy; Islamic civilization advanced them further (e.g., the 797/801 gift to Charlemagne). Chinese engineers independently developed sophisticated hydraulic clocks, culminating in Su Song’s 1088 Kaifeng tower—a 10-meter hydromechanical device using a waterwheel escapement, armillary sphere, and liquid mercury for winter operation. These clocks served primarily astronomical and astrological needs, not the rigid scheduling of industrial societies.

### The Mechanical Revolution (c. 1300–1656)
The **verge escapement** (c. 1300) marked the birth of the true mechanical clock. It replaced fluid power with falling weights regulated by an oscillating **foliot** (a crude balance bar), allowing discrete "beats." Early turret clocks (e.g., Dunstable Priory 1283, Norwich 1322) struck bells for canonical hours and modeled the cosmos (astronomical clocks like those of Richard of Wallingford, 1336, and Giovanni de Dondi, 1348–1364). **Spring-driven clocks** appeared by 1430 (Phillip the Good’s chamber clock), solving portability but introducing the problem of diminishing torque as the spring unwound. Solutions included the **stackfreed**, **fusee** (15th century), and eventually the **going barrel** (1760). Jost Bürgi’s **cross-beat escapement** and **remontoire** (1584) isolated the oscillator from drive-force variations, achieving ~1 minute/day accuracy, aiding Tycho Brahe’s astronomy.

### Precision Oscillators: Pendulum to Atomic
**Pendulum clocks** (Huygens, 1656–57) exploited the isochronism of a swinging bob (length ~99.4 cm for a 1-second beat), improving daily error from minutes to seconds. William Clement’s **anchor escapement** (1670) and **longcase** form (1670–71) made them practical. The **spiral balance spring (hairspring)** (Huygens/Hooke, 1675) applied harmonic oscillation to the balance wheel, enabling accurate pocket watches (Thomas Tompion). George Graham’s **deadbeat escapement** (1720) reduced recoil error.

The **marine chronometer** solved the longitude problem: a clock losing <10 seconds/day at sea (no pendulum on a rocking ship). John Harrison’s H4 (tested 1761) used jeweled bearings, a bimetallic compensation balance, and a remontoire, achieving <5 seconds error in 10 weeks, claiming the Longitude Act prizes.

**Electric clocks** (Bain patent, 1840) used electricity to rewind springs or drive pendulums (electromechanical), or counted AC line cycles (synchronous motors, 50/60 Hz). **Quartz clocks** (Marrison/Horton, 1927) used the piezoelectric vibration of a quartz crystal (~32 kHz+), offering high Q (quality factor) and lab-grade precision; they became the US time standard (1929–1960s) and, via integrated circuits, ubiquitous in wristwatches (Seiko Astron, 1969).

**Atomic clocks** (theorized Kelvin 1879; first accurate caesium standard, Essen 1955) lock a microwave oscillator to the hyperfine transition frequency of caesium-133 atoms (9,192,631,770 Hz), defining the SI second. They achieve stability <2×10⁻¹⁸ (ytterbium, 2013), serving as primary standards for UTC, GPS, and scientific calibration.

### Operational Architecture
All modern clocks share four functional blocks:
1.  **Power source**: Weights, springs, batteries, or AC mains.
2.  **Oscillator (resonator)**: The harmonic oscillator (pendulum, balance wheel, tuning fork, quartz crystal, atomic vibration) providing a precise, repetitive "beat." High Q (resonant frequency / energy loss) correlates with precision.
3.  **Controller**: Sustains oscillation and converts beats to pulses. Mechanical: **escapement** (pushes pendulum, releases gear tooth). Electronic: oscillator circuit (drives crystal, outputs clock signal). Atomic: microwave cavity + phase-locked loop (locks to atomic absorption).
4.  **Counter chain**: Accumulates pulses into seconds/minutes/hours. Mechanical: **gear train (wheel train)** with cannon pinion for setting. Digital: binary counters/dividers.
5.  **Indicator**: Displays time. Analog (hands on dial), digital (LCD/LED/VFD), auditory (speaking), tactile (Braille), or projection.

**Synchronized (slave) clocks** lack a high-precision local oscillator; they follow a master (wired pulses, AC line cycles, radio time signals, NTP/Internet, or satellite navigation).

### Display and Classification
Clocks are classified by display: **Analog** (rotating hands on 12/24-hour dial; includes sundials), **Digital** (numeric 12/24-hour), **Hybrid**, **Auditory**, **Word** (sentences), **Projection**, **Tactile** (touch-readable hands or Braille), and **Multi-display** (multiple zones or formats). **Flip clocks** are mechanical digital displays (turning pages) driven by synchronous motors.

### Purposes and Culture
Beyond time display, clocks serve as **alarm clocks**, **timers** (controlling devices: heating, bombs, telescopes), and **clock signals** (synchronizing digital computer CPUs). **Time standards** labs use atomic clocks for calibration. **Navigation** historically required marine chronometers for longitude; GPS now embeds atomic clocks on satellites. **Sports** use stopwatches, chess clocks, and game/shot clocks. Cultural folklore includes UK death superstitions (clocks stopping at a monarch’s death) and Chinese taboo against gifting clocks (*sòng zhōng* homophones "attending a funeral").

## Terms
- ****Escapement**** — The controller in a mechanical clock that gives precise pushes to the oscillator (pendulum/balance wheel) and releases the gear train one tooth per swing, regulating energy release.
- ****Harmonic oscillator**** — A physical resonator (pendulum, balance wheel, quartz crystal, atom) that vibrates at a precise natural resonant frequency determined by its physical properties; the timekeeping element in all modern clocks.
- ****Verge escapement**** — The first mechanical escapement (c. 1300), using a vertical rod (verge) with pallets engaging a crown wheel; enabled the first weight-driven mechanical clocks.
- ****Foliot**** — A primitive balance bar with adjustable weights used as the oscillator in early verge clocks before the balance spring; not a harmonic oscillator, resulting in poor accuracy (~hours/day).
- ****Fusee**** — A cone-shaped pulley with a spiral groove, wound by a chain from the mainspring barrel; equalizes torque as the spring unwinds (15th–18th century).
- ****Remontoire**** — A small secondary power source (spring/weight) rewound frequently by the main drive, isolating the escapement from drive-train friction variations; invented by Bürgi (1584).
- ****Anchor escapement**** — A pendulum escapement (Clement, 1670) shaped like a ship’s anchor; reduces swing angle and recoil vs. Huygens’ crown escapement, improving accuracy.
- ****Hairspring (balance spring)**** — A fine spiral spring (Huygens/Hooke, 1675) attached to the balance wheel, making it a harmonic oscillator; enabled accurate portable watches.
- ****Marine chronometer**** — A high-precision spring-driven clock (Harrison, mid-18th c.) compensated for temperature and motion, accurate enough (<10 s/day) for celestial navigation at sea.
- ****Q (quality factor)**** — Dimensionless parameter = resonant frequency / energy loss rate; higher Q means sharper resonance and higher potential timekeeping precision.
- ****Caesium standard**** — The primary atomic clock definition of the SI second: 9,192,631,770 cycles of the hyperfine transition of caesium-133 atoms.
- ****Synchronous (slave) clock**** — A clock without a precision oscillator that counts AC power-line cycles (50/60 Hz) or receives synchronization pulses from a master clock/time signal.

## Debates and open questions
- **Origin of water clocks**: "Where and when they first existed is not known and is perhaps unknowable" (source); earliest firm evidence is 16th century BC (Babylon/Egypt), but some authors claim 4000 BC in India/China.
- **Inventor of spring-driven clocks**: Often erroneously credited to Peter Henlein c. 1511; earliest surviving example is c. 1430 (Phillip the Good).
- **Inventor of rack-and-snail striking**: 20th-century misconception attributed it to Edward Barlow; source states it was introduced in the 17th century, while Barlow invented a repeating mechanism *using* it. The repeating clock itself (1676) is credited to either Daniel Quare or Barlow.
- **Reliability of early astronomical clocks**: Wallingford’s (1336) and Dondi’s (1364) clocks "probably adjusted manually every day to compensate for errors caused by wear and imprecise manufacture"; their true accuracy is unknown.
- **Transfer of Chinese escapement technology**: The source states the Chinese escapement "spread west and was the source for Western escapement technology," but the mechanism of this transfer (trade routes, translations) is not detailed.
- **Atomic clock supremacy**: As of 2013, ytterbium clocks lead stability (<2×10⁻¹⁸); the source implies ongoing competition among atomic species (caesium, ytterbium, etc.) for the primary standard.