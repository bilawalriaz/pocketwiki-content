# Industry Standard Architecture

Industry Standard Architecture (ISA) is the 16-bit internal expansion bus IBM introduced with the PC/AT in 1984 and that defined PC-compatible expansion through the early 1990s. It connects peripheral cards to the motherboard, supports bus mastering, and addresses only the first 16 MB of main memory. ISA is a superset of the 8-bit PC bus designed by Mark Dean's team at IBM in 1981 for the original IBM PC.

## Bus architecture

The 8-bit XT bus reused the physical connector and signal protocol of the I/O bus in the IBM System/23 Datamaster. It exposed 8 data lines and 20 address lines, with −5 V and ±12 V power rails for legacy MOS circuits. A single 8259 PIC provided eight prioritized interrupt lines, and four DMA channels came from an 8237: one was reserved for DRAM refresh, the others served the floppy and hard disk controllers and add-on cards.

The 16-bit AT bus added a second, shorter edge connector in line with the original XT socket, leaving the XT connector unchanged for backward compatibility. It added four address lines (to 24), eight data lines (to 16), a second cascaded 8259 PIC for more interrupts, and four 16-bit DMA channels. IBM called the AT bus the "I/O Channel." After the mid-1980s, manufacturers replaced the two sockets with a single 98-pin connector, almost always coloured black.

Device counts were limited by shared interrupts and DMA. The XT bus supports up to six cards using 8-bit IRQs and up to four cards using 8-bit DMA channels. The AT bus extends this to up to five 16-bit-irq cards and up to three 16-bit-dma cards at once.

The bus was synchronous with the CPU clock at first, so different clones ran it at 4.77 MHz, 6 MHz, 8 MHz, or sometimes 16–20 MHz, which caused timing problems for cards designed for slower clocks. Later chipsets decoupled ISA from the CPU clock and fixed it at 4, 6, or 8 MHz, capping throughput at about 8 MB/s for the 8-bit bus and 16 MB/s for the 16-bit bus. Mixing 8- and 16-bit cards was also constrained: the MEMCS16 line that selects 16-bit transfers was decoded only in 128 KB blocks, so cards of different widths could not share the same 128 KB region.

## Naming, rivals, and configuration

The bus was originally called the PC bus (8-bit) or AT bus (16-bit). "ISA" was coined in the late 1980s or early 1990s by clone makers, led by Compaq, as a retronym after IBM introduced its proprietary Micro Channel Architecture (MCA) in 1987 and tried to reclaim control of the PC platform. The term let rivals refer to the AT bus without using IBM's trademarks. Clones including the "Gang of Nine" answered MCA in 1988 with the 32-bit Extended ISA (EISA), followed by VESA Local Bus (VLB); both were backward compatible with AT/ISA.

ISA had no real plug-and-play support. Users typically set IRQ lines, I/O addresses, and DMA channels by hand for every new card. MCA eliminated this, and PCI later inherited the idea. ISA PnP eventually arrived through BIOS, hardware, and operating-system cooperation, but it matured late in ISA's life.

## Displacement by PCI

ISA was squeezed off motherboards as PCI spread. Mid-1990s boards carried roughly equal numbers of each slot; by the turn of the century a typical board had an AGP slot near the CPU, several PCI slots, and one or two ISA slots near the edge. Microsoft's PC-99 specification recommended removing ISA slots entirely. The LPC bus replaced ISA on the motherboard for floppy, serial, and other legacy I/O, since LPC looks like ISA to software and preserves the 16 MiB DMA limit inherited from the 80286. By late 2008 floppy disk drives and serial ports were disappearing, and vestigial ISA (then via LPC) was being phased out of chipsets.

## Derivatives that survived ISA

ATA (IDE) hard disks descend directly from the 16-bit ISA hardware on the IBM PC AT. An ISA hardcard combined a drive and controller on one card, which was awkward in an ISA slot, so the next generation moved both onto the drive bay and exposed only a simple interface card to ISA. ATA standardised that arrangement, kept ISA's 16-bit transfer size and IRQ/DMA signalling, and defined its own register set and command protocol. ATA was later moved to PCI and integrated into the chipset, reaching 133 MB/s in ATA-6. The XT-IDE (XTA) interface was an earlier 8-bit variant but remained uncommon. Other ISA derivatives include PCMCIA, CompactFlash, the PC/104 embedded bus, and Super I/O chips.

## Current use

ISA never disappeared completely. Industrial motherboards from IEI (2008, Core 2 Duo), ADEK (2013), MSI (2020, Skylake/Kaby Lake), and DFI (Coffee Lake) have exposed one or two ISA slots for legacy industrial and military cards. IEEE's P996 attempt to standardise ISA after 1985 never progressed past draft, so the bus survives as a de facto specification sustained by industrial users and the LPC software interface.
