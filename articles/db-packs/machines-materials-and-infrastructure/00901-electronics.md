# Electronics

Electronics is the engineering discipline that designs devices which control electrons and other charged particles to process information and energy. A **semiconductor** is a material whose electrical conductivity sits between that of a metal and an insulator, and it is the foundation of modern electronics. The single most manufactured device in history is the **MOSFET** (metal-oxide-semiconductor field-effect transistor): an estimated 13 sextillion were produced between 1960 and 2018. The semiconductor industry that produces them generated more than $481 billion in sales in 2018.

## How electronic systems are built

A circuit groups **active** components, which control current flow and can amplify signals (transistors, diodes), and **passive** components, which store or dissipate energy but cannot add to it (resistors, capacitors, inductors). Today these are almost always soldered onto **printed circuit boards (PCBs)**, typically made of fibreglass laminate (FR-4 or FR-2), using either through-hole mounting or surface-mount technology. Early electronics used point-to-point wiring on wooden breadboards, then cordwood construction and wire wrapping.

The breakthrough that made modern electronics possible was the **integrated circuit (IC)**, independently invented by Jack Kilby and Robert Noyce, which fabricates entire circuits from one block of semiconductor. Component counts per chip then grew through named stages: **SSI** (small-scale integration) in the early 1960s, **MSI** (medium-scale integration) in the late 1960s, and eventually **VLSI** (very-large-scale integration), which produced commercial processors containing a billion transistors by 2008.

## Two kinds of signal

Electronic circuits split into two functional families. **Analog circuits** process signals whose voltage or current varies continuously; they powered early radio transmitters and receivers and remain common in signal-front-end stages. **Digital circuits** represent information with two discrete levels, labelled 0 and 1 (or Low and High), and manipulate those levels using **Boolean algebra** (logical AND, OR, NOT). The logic gate is the digital building block, and large ICs stack millions of them into adders, flip-flops, registers, counters, multiplexers, and Schmitt triggers, and into memory chips, microprocessors, microcontrollers, ASICs, DSPs, FPGAs, and systems-on-chip. Many modern devices are **hybrid**: an analog front-end receives the signal, a digital back-end processes it. A few circuits, such as voltage comparators and overdriven transistor amplifiers, mix linear and non-linear behaviour, so the boundary between analog and digital is not always sharp.

## The road to the transistor

| Year | Milestone |
|------|-----------|
| 1874 | Karl Ferdinand Braun builds the crystal detector, the first semiconductor device. |
| 1897 | J. J. Thomson identifies the electron. |
| Early 1900s | Ambrose Fleming invents the diode; Lee De Forest invents the triode. These vacuum tubes, also called **thermionic valves**, control current by influencing individual electrons in a vacuum and made radio, television, radar, and long-distance telephony practical. |
| 1947 | John Bardeen and Walter Houser Brattain build the first working point-contact transistor at Bell Labs. |
| 1955 | The IBM 608 becomes the first all-transistorised commercial calculator, using over 3,000 germanium transistors. Thomas J. Watson Jr. then ordered all future IBM products to use transistors. |
| 1955–1960 | Bell Labs invents the MOSFET, the first compact transistor suited to mass production. |

Vacuum tubes continued to dominate microwave and high-power uses until the mid-1980s, after which solid-state devices took over. The MOSFET's combination of scalability, low power draw, low cost, and high component density is what made billion-transistor chips possible.

## Designing circuits

Modern electronic design balances function, reliability, lifetime, and disposal. Physical laboratory testing is still important, but engineers increasingly rely on simulation packages such as CircuitLogix, Multisim, and PSpice, and on **electronic design automation (EDA)** tools (schematic capture and PCB layout) such as NI Multisim, Cadence ORCAD, EAGLE, Mentor PADS, Altium, LabCentre Proteus, gEDA, and KiCad.

Every circuit must also manage two unavoidable physical effects. **Heat** from resistive losses has to be removed by conduction, convection, or radiation, typically with heat sinks, fans, or liquid cooling, or the device fails. **Electronic noise**, unwanted electrical disturbance superimposed on a signal, is present in every circuit; some forms, such as shot noise, are fundamental quantum effects that cannot be removed at all, only reduced by lowering temperature.

## Where the industry is built

Electronics manufacturing is now heavily concentrated in East Asia. Japanese firms such as Sony and Hitachi undercut U.S. producers in the 1960s with cheaper, high-quality goods, and the United States regained leadership in semiconductor design and assembly by the 1980s. Microchip mass-production began shifting to East Asia in the 1970s, accelerated by cheap labour and rising technical skill, and by 2022 Taiwan had become the world's leading source of advanced semiconductors, followed by South Korea, the United States, Japan, Singapore, and China, with further fabrication in the Netherlands, Southeast Asia, South America, and Israel. The U.S. share of global semiconductor manufacturing capacity fell from 37% in 1990 to 12% in 2022, and Intel Corporation lost its manufacturing lead to Taiwan Semiconductor Manufacturing Company (TSMC), a shift that has raised concerns about supply-chain resilience and national security.
