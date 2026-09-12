# Flash memory

Flash memory is a non-volatile electronic storage medium. It retains data without power, can be electrically erased and reprogrammed, and forms the basis of SSDs, USB flash drives, memory cards, and smartphone storage.

## The floating-gate cell

Every flash cell is a MOSFET, a transistor switched on and off by a gate, with a second "floating gate" buried in the insulating oxide between the control gate and the silicon channel. The floating gate is fully surrounded by insulator, so any electrons pushed onto it stay trapped. Their charge shifts the transistor's threshold voltage, the minimum gate voltage needed to turn the channel on. Programming pushes electrons onto the floating gate by Fowler–Nordheim tunneling, a quantum effect that lets electrons pass through thin insulator under a strong field, raising the threshold; erasing pulls them back off, lowering it. To read the cell, the controller applies a voltage between the two threshold states; whether current flows tells it whether the bit is 0 or 1.

Each program/erase cycle stresses the thin tunnel oxide at roughly ten million volts per centimetre. Over time the oxide traps electrons and develops defects, eventually leaking charge and causing data loss. This wear is the physical reason flash has limited endurance, typically a few thousand to a hundred thousand program/erase cycles per block depending on cell type.

Storing more than one bit per cell works by holding the floating gate charge at several precise intermediate levels. Single-level cells (SLC) hold one bit; multi-level cells (MLC) hold two; triple-level cells (TLC) hold three; quad-level cells (QLC) hold four. Each additional bit narrows the voltage gap between states, making the cell more sensitive to oxide wear and charge leakage, which is why endurance and retention fall as bits per cell rise.

## NOR versus NAND

Flash comes in two architectures named after the logic gates their cell wiring resembles.

NOR flash connects each cell between a bit line and ground in parallel, like a CMOS NOR gate's pull-down transistors. This allows random access at byte or word granularity, fast reads, and execute-in-place, in which a processor runs code directly from the chip without copying it to RAM first. Its drawbacks are a larger cell (roughly 10 F², where F is the smallest lithographic feature size, versus 4 F² for NAND) and slower bulk writes. NOR is therefore used for boot ROM, BIOS, and firmware that must run directly from the chip.

NAND flash connects cells in series within a string, like transistors stacked in a CMOS NAND gate. To read one cell the controller reads the whole string and drives the unselected cells hard on. This sacrifices true random access but shrinks the cell area by about 40%, and external address and data buses can be replaced by a serial command interface, so NAND packs far more storage into the same silicon. NAND dominates where capacity and cost per bit matter most: SSDs, memory cards, USB sticks, and smartphone storage.

Both types erase only whole blocks at once, and erasing resets every bit in the block to 1. Programming can only push bits from 1 to 0. To overwrite, the controller must erase the whole block first, which is why every NAND device includes a flash translation layer that maps logical addresses to physical blocks and spreads writes around to level out wear.

## The move to three dimensions

Around 2007, planar shrinking reached its economic floor near 15–16 nm. The breakthrough was 3D V-NAND: instead of shrinking cells, manufacturers stack them vertically, often dozens to over two hundred layers tall, with charge held in a thin silicon nitride film rather than a polysilicon floating gate. Charge-trap cells are mechanically simpler and can be made thinner, and stacking them in concentric cylinders around a vertical channel packs bits into the third dimension without further lithography shrinks. Samsung commercialized a 24-layer V-NAND in 2013; by 2019 it was producing 96-layer chips, and by 2025 devices were reaching 232 layers. Die stacking inside a single package, using through-silicon vias that pass vertical wires through a silicon die, now lets a single chip-sized package hold a terabyte or more.

## Endurance and reliability in practice

Three related mechanisms limit flash lifetime. Program/erase cycling wears the tunnel oxide until a block can no longer hold its charge. Data retention degrades, with charge loss roughly doubling for every 10 °C of temperature rise, so a chip rated for ten years at 25 °C may hold data for only about a year at 85 °C. Read disturb occurs because the high voltages used to read one NAND cell can weakly program neighbouring cells; after hundreds of thousands of reads, an adjacent cell can flip. Controllers counter all three with wear leveling, bad-block management, error-correcting codes such as BCH and LDPC, and periodic refresh. The TRIM command lets the operating system tell the SSD which pages are no longer in use, letting the controller erase them in advance and improving both performance and wear.

Raw SLC NAND endurance is roughly 50,000–100,000 cycles per block; MLC around 5,000–10,000; TLC around 1,000; QLC as low as 100–1,000. Through wear leveling and over-provisioning, real SSDs usually outlast the host device. As of late 2025 Samsung leads NAND production at about 30% of the market, followed by SK Hynix, Kioxia, Micron, YMTC, and Western Digital.
