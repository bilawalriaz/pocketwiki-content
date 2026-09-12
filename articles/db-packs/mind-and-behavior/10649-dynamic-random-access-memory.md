# Dynamic random-access memory

Dynamic random-access memory (DRAM) stores each bit as an electrical charge in a microscopic capacitor, a tiny reservoir that holds electrons on two separated conductors. The charge leaks away in milliseconds, so every cell must be rewritten thousands of times each second. Cut power and the contents vanish within a fraction of a second, which is why DRAM is called volatile. This combination, one transistor plus one capacitor per bit plus a continuous refresh, is what makes DRAM simultaneously cheap, dense, and volatile, and it is why DRAM is the standard main memory of computers, graphics cards, and most digital devices.

## The 1T1C cell

A modern DRAM cell is a single MOS transistor guarding a single capacitor, the 1T1C cell. The transistor's gate connects to a horizontal **wordline** that runs across an entire row of cells. Its source connects to a vertical **bitline** shared with every other cell in the column. The capacitor's other terminal is tied to a fixed reference voltage, ground in older designs, or half the supply voltage in modern ones.

To **read** a cell, the controller precharges the bitline pair to a midpoint voltage, then drives the chosen wordline high. The transistor switches on and the cell's tiny capacitor shares its charge with the much larger bitline capacitance, nudging the bitline voltage up or down by only a few tens of millivolts. A **sense amplifier**, two cross-coupled inverters that latch onto a small difference, detects this nudge and amplifies it to a full logic 0 or 1. Reading is destructive: sharing charge empties the cell, so the amplifier immediately writes the value back. A **write** is similar. The row is opened and the bitline is forced to the desired voltage, which overwrites the capacitor.

Because the amplifier reads the entire open row at once, subsequent reads from other columns in the same row are much faster than the first.

The trade-off against SRAM is direct. SRAM uses four to six transistors per bit and never needs refreshing, so it is faster but takes far more silicon area per bit. DRAM uses one transistor and one capacitor, which lets engineers pack billions of cells onto a single chip at very low cost per bit, at the price of slower access and continuous refresh.

## Refresh

The JEDEC standard requires every row to be refreshed at least once every 64 ms. In a chip with 8,192 rows, that works out to one row every 7.8 µs. The DRAM can accept the row address from an external controller or generate it from an internal counter. Modern chips also support a **self-refresh** mode in which an on-chip timer refreshes rows autonomously, letting a system put the memory controller to sleep to save power.

Because the cell's charge takes time to decay, data can often be recovered for several minutes after power-off, especially at low temperatures. This **data remanence** is the basis of cold-boot attacks that extract encryption keys from RAM by rebooting a machine and dumping memory before it fades.

## Organisation and timing

Cells are arranged in a rectangular grid, typically 6–8 F² in area, where F is the smallest lithographic feature size. Rows are activated by the wordline; a column address then selects which bit of the latched row is delivered to the outside. The three classic control signals are **RAS** (row address strobe), **CAS** (column address strobe), and **WE** (write enable). To save pins, the address is multiplexed: the same pins first carry the row address, then the column address.

The most commonly quoted performance figure is the row-access time, t_RAC, the delay from asserting RAS to valid data. For a 50 ns asynchronous DRAM of the late 1990s, that was five clock cycles at 100 MHz, with successive bits in the same open row fetched every two cycles. Modern synchronous DRAM (SDRAM) expresses timing in clock cycles. DDR, DDR2, and DDR3 have multiplied the data transferred per internal access by two, four, and eight while keeping the internal core rate roughly constant at around 200 million accesses per second.

## History

The 1T1C cell was invented in 1966 by Robert Dennard at IBM, who realised that the same MOS process that built transistors could also build capacitors, and patented the idea in 1967 (US patent 3,387,286). Commercial MOS DRAM chips appeared in 1969, and the Intel 1103 of October 1970 became the first volume commercial DRAM. In 1973 Mostek introduced the MK4096 with multiplexed addressing, halving the pin count. Through the 1980s, Japanese manufacturers overtook American ones, and Gordon Moore withdrew Intel from DRAM in 1985. Samsung developed SDRAM, with the first commercial chip in 1992 and the first commercial DDR SDRAM in 1998. The market has since consolidated to three suppliers, Samsung, SK Hynix, and Micron, who in 2018 controlled most of the world's capacity.

## Variants

The asynchronous DRAM interface dominated until roughly 1997, when SDRAM took over. Successive DDR generations multiplied bandwidth, while specialised variants appeared for graphics: VRAM and WRAM added a second port for simultaneous read/write, SGRAM added block-write commands, and the GDDR family (now up to GDDR7) trades latency for raw bandwidth on GPUs. High-bandwidth memory (HBM) stacks multiple DRAM dies vertically to feed GPUs and accelerators. Pseudostatic RAM (PSRAM) and embedded DRAM (eDRAM) integrate refresh and control logic onto the chip, trading some density for ease of use in microcontrollers and game consoles. Error-correcting (ECC) DRAM adds parity and Hamming-code bits so that single-bit soft errors, mostly from cosmic-ray neutrons, can be detected and corrected.
