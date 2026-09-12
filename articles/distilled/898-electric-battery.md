# Electric battery

## Overview
An electric battery is a device consisting of one or more electrochemical cells that converts stored chemical energy directly into electrical energy via redox reactions. When discharging, electrons flow from the negative terminal (anode) through an external circuit to the positive terminal (cathode), powering connected devices. Batteries are classified as primary (single-use, irreversible reactions) or secondary (rechargeable, reversible reactions via applied current). While batteries have lower specific energy than fuels like gasoline, the higher efficiency of electric motors offsets this in applications such as electric vehicles. Demand grew 30% annually from 2010–2018, driven by transport electrification and grid storage.

## Timeline
- **1749** — Benjamin Franklin coins the term "battery" for linked Leyden jar capacitors.
- **1800** — Alessandro Volta invents the voltaic pile, the first electrochemical battery (copper/zinc/brine).
- **1834** — Michael Faraday shows electrode corrosion is an unavoidable consequence of operation, not a nuisance.
- **1836** — John Frederic Daniell invents the Daniell cell, the first practical, steady-current source for telegraphy.
- **Late 19th c.** — Invention of dry cells (paste electrolyte) enables portable electrical devices.
- **1859 (implied)** — Lead–acid battery invented (oldest rechargeable type); widely adopted for automotive SLI use.
- **1991 (context)** — Commercial lithium-ion batteries emerge; dominate portable electronics and later EVs.
- **2010–2018** — Global battery demand grows 30% annually, reaching 180 GWh.
- **2017** — World's largest battery (129 MWh) installed in South Australia by Tesla.
- **2022** — EU agrees to mandate user-replaceable batteries in appliances from 2026.
- **2024** — Prototype EV battery demonstrates 10%–80% charge in 5 minutes.

## Body

### Chemistry and Principles
A battery comprises voltaic cells, each containing two half-cells connected by a conductive electrolyte. In a half-cell, metal atoms oxidize (lose electrons) at the anode; cations reduce (gain electrons) at the cathode. Electrons flow externally; ions flow internally through the electrolyte (or a separator if electrolytes differ) to balance charge. The cell's electromotive force (emf, in volts) equals the difference between the half-cells' reduction potentials. The terminal voltage under load is lower than the open-circuit voltage due to internal resistance; it exceeds open-circuit voltage during charging. Voltage is chemistry-dependent: alkaline/zinc-carbon ≈ 1.5 V; NiCd/NiMH ≈ 1.2 V; lithium ≥ 3 V. Capacity (ampere-hours, A·h) scales with electrode mass. Peukert’s law describes the inverse relationship between discharge current and realized capacity in lead-acid batteries ($t = Q_P / I^k$, $k \approx 1.3$). The C-rate normalizes charge/discharge current to the theoretical 1-hour capacity current; lower C-rates yield higher usable capacity and longer cycle life.

### Historical Development
Franklin’s 1749 "battery" of Leyden jars stored static charge. Volta’s 1800 pile produced steady current but he misattributed the voltage to contact tension rather than chemical reaction. Early wet cells (liquid electrolyte) were fragile, leak-prone, and unsuitable for portable use. The Daniell cell (1836) stabilized voltage for telegraph networks. The late-19th-century dry cell (paste electrolyte) enabled portable devices. Vacuum tube era used wet "A" batteries (filament) and dry "B" batteries (plate voltage). Computational modeling now accelerates materials discovery via high-throughput screening and atomistic simulation, replacing trial-and-error.

### Types and Composition
**Primary (disposable):** Zinc-carbon, alkaline. Higher energy density but poor high-drain performance (<75 Ω load). Not reliably rechargeable.
**Secondary (rechargeable):**
- *Lead–acid:* Low cost, high surge current (450 A peak for auto SLI), heavy, liquid electrolyte (hydrogen risk), ~6-year auto life. Deep-cycle variants have thicker plates for longevity. VRLA (valve-regulated) types—Gel and AGM—immobilize electrolyte to prevent leakage.
- *Nickel-based:* NiCd (1,000 cycles, memory effect, toxic Cd), NiMH (higher capacity, less memory effect, low-self-discharge variants).
- *Lithium-ion (Li-ion):* Highest energy density, dominates portable/EV market. Solid-state variants (e.g., Goodenough 2017 prototype) promise 3× energy density, sodium electrolytes, faster charging, longer life.
- *Emerging:* Lithium-sulfur (solar flight), sugar-based enzymatic (Sony), nanoball (100× discharge rate), USB-rechargeable, smart packs with management systems.

**Form factors:** Wet cells (flooded/vented), dry cells (paste), molten salt (high-temp), reserve batteries (activated by impact/water/assembly), button cells to grid-scale banks (129 MWh Tesla, 36 MWh China, 40 MW/7-min NiCd Fairbanks).

### Performance, Lifespan, and Endurance
Capacity is rated at 20-hour discharge (20 °C). Realized capacity falls with higher discharge rates, low temperature, age, and storage self-discharge. Self-discharge: primary 8–20%/year (room temp); NiCd 10%/day then 10%/month; modern NiMH/Li-ion much lower. Refrigeration slows side reactions but hurts low-temp performance (alkaline at 0 °C is 50% efficient at 250 mA). Cycle life: low-capacity NiMH ~1,000 cycles; high-capacity ~500; NiCd ~1,000; lead-acid degrades via sulfation/plate shedding—avoid <20% state-of-charge. Fast charging and overcharging accelerate degradation. "Endurance" = runtime per charge; "lifespan" = cycle count. Zamboni piles (1812) and Oxford Electric Bell (1840) demonstrate extreme calendar life at nanoamp currents.

### Hazards
**Explosion:** Caused by primary-cell recharging, short circuits, excessive charge rate (H₂/O₂ buildup), overcharging, or incineration. Li-ion: fast charging → dendrites → short circuit → thermal runaway. Jump-starting cars releases explosive hydrogen.
**Leakage:** Corrosive/toxic chemicals (e.g., zinc can breach) damage devices. Remove batteries for long-term storage.
**Ingestion:** Button cells cause tissue necrosis (NaOH generation at anode) if lodged in esophagus; perforation in 6 hours. Bittering agents added as deterrent.
**Disposal/Toxicity:** Lead, mercury, cadmium require recycling. US: 179,000 tons/year to landfill. Mercury-Containing and Rechargeable Battery Management Act (1996) bans Hg, mandates labeling/removability. EU Battery Directive mandates collection symbol, recycling targets, and (from 2026) user-replaceable design.

## Terms
- ****Anode**** — Electrode where oxidation occurs (electron loss); negative terminal during discharge.
- ****Cathode**** — Electrode where reduction occurs (electron gain); positive terminal during discharge.
- ****Electrolyte**** — Medium (liquid, paste, solid) allowing ion flow between half-cells to complete the circuit.
- ****EMF (Electromotive Force)**** — Open-circuit voltage of a cell (volts), determined by the difference in half-cell reduction potentials.
- ****Primary Battery**** — Single-use cell with irreversible chemistry; discarded when reactants are exhausted.
- ****Secondary Battery**** — Rechargeable cell; chemical reactions reversed by applied current to restore reactants.
- ****C-rate**** — Charge/discharge current normalized to the theoretical 1-hour capacity current (units h⁻¹).
- ****Peukert’s Law**** — Empirical relation $t = Q_P / I^k$ describing capacity reduction at high discharge rates (lead-acid).
- ****Self-Discharge**** — Capacity loss during storage due to parasitic side reactions consuming charge carriers.
- ****Thermal Runaway**** — Uncontrolled exothermic reaction chain (often in Li-ion) leading to fire/explosion.

## Debates and Open Questions
- **Solid-state commercialization:** Whether solid-state batteries (higher energy density, safety) can overcome manufacturing scale-up and interfacial stability challenges to replace liquid Li-ion.
- **Fast-charge limits:** Trade-offs between 5–10 minute charging targets and cycle life degradation / thermal management.
- **Grid storage chemistry:** Optimal chemistry for stationary storage (cost, cycle life, safety) vs. mobile (energy density)—e.g., sodium-ion, flow batteries, or repurposed EV packs.
- **Recycling economics:** Achieving closed-loop material recovery (Li, Co, Ni) at scale to meet regulatory mandates and reduce primary mining.
- **Resource constraints:** Long-term supply security for lithium, cobalt, nickel, and graphite amid exponential demand growth (2,600–3,562 GWh projected for 2030).
- **Safety vs. energy density:** Balancing higher voltage/capacity chemistries against flammability and thermal runaway risks in dense packs.

Source: adapted from "Electric battery" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Electric_battery
