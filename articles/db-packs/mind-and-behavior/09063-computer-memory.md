# Computer memory

Computer memory is the working storage a computer uses to hold the data and program instructions it is actively using. The terms *main memory* and *primary storage* mean the same thing; *RAM* (random-access memory) is the most common label, though some historical forms of memory were not random-access. Main memory is fast but expensive and limited in capacity, while mass storage (disks, SSDs, tapes) is slower, cheaper, and much larger. Main memory also acts as a cache and write buffer for that larger storage, and operating systems automatically use any unused RAM to cache disk data.

Modern computer memory is built as **semiconductor memory**: memory cells made from MOS transistors and other components etched onto an integrated circuit. The cells are grouped into words of a fixed width (commonly 8, 16, 32, or 64 bits), and each word is located by a binary address, so an N-bit address can reach 2ᴺ words.

## Volatile and non-volatile memory

Semiconductor memory splits into two main kinds.

**Volatile memory** loses its contents when power is cut. The two important types are:

- **SRAM (static RAM)**. Each bit is held by a latch of about six transistors. It is fast, simple to interface, and keeps its value as long as power is on. It is used where speed matters more than density, chiefly for CPU cache and small embedded systems.
- **DRAM (dynamic RAM)**. Each bit is a single transistor controlling a tiny capacitor that stores a charge. The charge leaks away in milliseconds, so the memory must be constantly *refreshed*, which complicates its interface. Because each cell is one transistor and one capacitor, DRAM reaches far higher density and far lower cost per bit than SRAM, and it is the standard main memory of PCs and servers (as of 2021, over 90% of PC and server memory was the DDR4 SDRAM variant).

Both SRAM and DRAM are random-access: any cell can be read or written in roughly the same time.

**Non-volatile memory** keeps its data without power. The main families are:

- **ROM and its programmable relatives**: PROM (programmable once), EPROM (erasable with ultraviolet light, introduced by Intel in 1971), and EEPROM (electrically erasable, 1972).
- **Flash memory**, invented by Fujio Masuoka at Toshiba in the early 1980s. NOR flash was presented in 1984 and NAND flash in 1987; NAND became the basis of memory cards, USB drives, and SSDs.
- Older non-semiconductor media: magnetic hard disks, floppy disks, magnetic tape, optical discs (CD, DVD, Blu-ray), and the historical punched cards and paper tape.

A third category, **semi-volatile memory**, describes designs that retain data for some time after power loss but eventually lose it. It balances speed, cost, and endurance; an example is nvSRAM, which pairs SRAM with a small non-volatile backup on the same chip.

## How the cell works

The bit-storage trick differs by technology. In SRAM, cross-coupled transistors continuously reinforce the stored value. In DRAM (developed by Robert Dennard at IBM in 1966–67), a MOS transistor acts as a switch that writes a charge onto a capacitor; the presence or absence of charge represents 1 or 0. The Intel 1103, released in October 1970, was the first commercial single-transistor DRAM chip. In flash, each cell is a transistor with a *floating gate* that traps electrons, and the trapped charge changes the transistor's threshold voltage to represent the bit. Flash cells originally held one bit; multi-level cells later store multiple bits per cell by using more than two charge ranges.

## A short history

In the early 1940s, memory held only a few bytes; ENIAC used thousands of vacuum tubes to store 20 ten-digit numbers. Acoustic delay-line memory stored bits as sound pulses travelling through mercury, with quartz crystals at each end to read and write. Capacity topped out at a few thousand bits. The Williams tube (1946) was the first random-access memory, using electron beams in a cathode-ray tube, but was sensitive to environmental disturbance.

Magnetic-core memory, developed in the late 1940s and improved in the early 1950s, became the standard form of working memory because it was non-volatile. It dominated until the late 1960s, when semiconductor memory overtook it.

Semiconductor memory began with bipolar flip-flop cells in the early 1960s; the first commercial bipolar memory IC was IBM's SP95 in 1965. The MOSFET made dense, cheap memory cells practical: MOS memory was developed at Fairchild in 1964, silicon-gate MOS chips followed in 1968, and MOS memory displaced magnetic core in the early 1970s. SDRAM debuted with Samsung's KM48SL2000 in 1992, and later generations have continued to raise transfer rates while keeping the underlying DRAM cell.

## Memory management

The operating system, usually with help from a memory management unit (MMU) in the CPU, manages memory on behalf of running programs. Two ideas are central.

**Virtual memory** lets programs use addresses as if the computer had a single large, contiguous memory. The OS and MMU translate those addresses into real physical locations, keeping the most-used data in RAM and moving less-used pages to a swap file on disk. If programs together demand more memory than RAM can hold, the system spends most of its time shuttling pages back and forth, a condition called *thrashing*.

**Protected memory** gives each program its own private address range and stops it from reading or writing outside that range. A program that tries to access memory it does not own is terminated with a segmentation fault rather than corrupting another program or the OS. Without protection, a bug or a virus in one program can silently damage others.

Improper memory handling is a frequent source of bugs and security holes. A *memory leak* happens when a program requests memory and never releases it, so its usage grows until the system runs out. A *buffer overflow* happens when a program writes past the end of an allocated block, overwriting adjacent data; this is the basis of many software exploits.

Source: adapted from "Computer memory" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Computer_memory
