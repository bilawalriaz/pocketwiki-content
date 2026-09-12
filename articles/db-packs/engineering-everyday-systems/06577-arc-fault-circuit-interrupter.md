# Arc-fault circuit interrupter

An arc-fault circuit interrupter (AFCI), called an arc-fault detection device (AFDD) in European standards, is a circuit breaker that opens a circuit when it detects the arcing that loose or damaged wiring produces. Those arcs can heat a connection enough to start a house fire, yet the current they draw is often too low or too erratic for an ordinary breaker to react to. A conventional breaker trips only on overloads and short circuits, so it ignores this hazard. An AFCI monitors the current continuously, recognises the high-frequency signature of a dangerous arc, and disconnects the circuit before the wiring burns.

## What an arc fault looks like electrically

Wire arcing produces current fluctuations at characteristic frequencies, usually around 100 kHz, that persist for more than a few milliseconds. The electronics inside an AFCI look for that fingerprint and must also reject harmless arcs, because normal operation of switches, plugs, and brushed motors creates brief arcs that should be ignored.

Two kinds of fault matter. A *parallel arc* runs between line and neutral, line and ground, or neutral and ground, often because insulation has worn through. A *series arc* happens when a single conductor is broken, loose, or has a high-resistance segment, so current has to jump across the gap. A combination-type AFCI detects both and still trips on overloads and short circuits like an ordinary breaker.

## Why the codes care

In the United States, arc faults are among the leading causes of residential electrical fires; over 40,000 US home fires a year are attributed to wiring problems, causing more than 350 deaths and 1,400 injuries. The US National Electrical Code has required AFCI protection on bedroom circuits since 1999 and expanded the requirement with each code cycle. By the 2014 NEC, most 15 A and 20 A branch circuits in dwellings need AFCI protection, covering kitchens, laundry areas, family rooms, dining rooms, living rooms, parlors, libraries, dens, bedrooms, sunrooms, recreation rooms, closets, hallways, and similar rooms, along with dormitory units. As of January 2008, only "combination type" AFCIs, defined by UL 1699, meet the NEC. The Canadian Electrical Code has required comparable protection on bedroom circuits since 2002 and broadened it in 2015.

Adoption is slower in 230 V and higher regions, because higher voltage and lower load currents change how an arc behaves and let existing breakers clear many faults before they become a fire risk. The UK Wiring Regulations (BS 7671:2018) mention AFDDs only as an optional measure for high fire-risk situations. The German VDE 0100-420 standard recommends them for sleeping accommodation, rooms built with combustible materials below fire-retardant grade, and places with irreplaceable goods. Australian rules do not require AFDDs. New Zealand requires AFDDs on final sub-circuits up to 20 A supplying locations with significant fire risk, irreplaceable items, certain historic buildings, and socket-outlets in school sleeping accommodation.

## Breaker or receptacle

Two forms are common. A combination-type AFCI breaker sits in the panel and protects the entire branch. An AFCI receptacle at the first outlet on a branch gives series-arc protection across the whole branch and parallel-arc protection from that outlet forward, and works on any panel, which suits modifications and extensions. Receptacles add a test and reset button at the point of use, though that convenience can encourage a casual reset without finding the underlying fault.

## Limits and false trips

AFCI sensitivity has a cost. Vacuum cleaners and some laser printers draw current that the breaker can mistake for arcing, and lightning produces similar profiles. AFCIs are also sensitive to radio-frequency energy in the 3–30 MHz band, which includes shortwave broadcasting, amateur radio, and citizens band radio; sensitivities and mitigations have been documented since 2013. An AFCI is built on a standard inverse-time breaker and adds no specific protection against glowing high-resistance connections, sustained overvoltage, or sustained undervoltage. An open neutral on a multiwire 120/240 V branch circuit can push one leg to roughly 240 V without an AFCI noticing, and a relay chattering on low voltage can still arc at its own contacts and start a fire, hazards the device is not designed to catch.
