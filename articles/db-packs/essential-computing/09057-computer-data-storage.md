# Computer data storage

Computer data storage is the retention of digital data using recording media and electronic components, and is a core function of every computer. Almost all machines use a memory hierarchy: fast, volatile components near the CPU, called *memory*, and slower, persistent components farther away, called *storage*. Modern systems typically use hard disk drives (HDDs) or solid-state drives (SSDs) for the latter.

## How data is represented

Digital computers store everything as bits, each holding a 0 or 1. Text, numbers, images, audio, and video are encoded as bit patterns. A byte is 8 bits, the most common unit. Standards such as ASCII for text, JPEG for images, and MPEG-4 for video define how information maps onto bits. A memory cell stores one bit and is the fundamental building block of computer memory.

The dominant hardware design is the Von Neumann architecture, in which program instructions and data share the same memory. The CPU contains a control unit, which moves data between CPU and memory, and an arithmetic logic unit, which performs calculations. Because instructions live in memory, one machine can run many programs without rewiring.

## Primary, secondary, and tertiary storage

Primary storage, also called main memory, is directly accessed by the CPU. It includes processor registers (the fastest storage, holding a word of 32 or 64 bits), processor cache (an intermediate speed and capacity layer), and main RAM. Most primary storage uses DRAM, which is volatile. SRAM is faster and does not need refreshing, but is more expensive. Primary storage is byte-addressable: the CPU sends a memory address over an address bus, then reads or writes through a data bus. A memory management unit (MMU) translates virtual addresses into physical ones, enabling virtual memory. A small non-volatile region holds the BIOS, the boot program that loads the operating system from secondary storage into RAM.

Secondary storage is not directly accessed by the CPU. The computer moves data through input/output channels. It is non-volatile and far cheaper per byte than primary storage, so systems typically have two orders of magnitude more of it. Access times are measured in milliseconds, versus nanoseconds for primary storage. Secondary storage is block-addressable, so data is read and written in large contiguous blocks, reducing the mechanical seek time and rotational latency of HDDs. A file system organizes blocks into files and directories and stores metadata such as owner and permissions. Through virtual memory, the operating system pages least-used chunks of RAM to a swap file on secondary storage, treating disk as an extension of memory.

Tertiary storage uses robotic arms to mount and dismount removable media, such as tape cartridges, on demand. Access takes 5 to 60 seconds, making it suited to archiving rarely used data, including tape libraries, optical jukeboxes, and massive arrays of idle disks. It is also called nearline storage because it sits between online and offline. Offline storage is media physically disconnected from any computer, used for transport and disaster recovery.

## Characteristics and reliability

Storage technologies differ along several dimensions. Volatility is whether data survives without power: RAM is volatile, while HDDs, SSDs, optical discs, and flash are not. Mutability ranges from read/write (RAM, HDD, SSD) to write-once (CD-R, PROM) to read-only (CD-ROM, mask ROM). Access is random when any location takes roughly equal time, or sequential when data must be read in order, as on tape. SSDs consume less power than spinning disks; large caches and main memory can draw significant power. HDDs fail through head crashes; flash storage fails as its circuitry wears out from repeated writes.

Storage is unreliable, so redundancy is used to detect and correct errors. A cyclic redundancy check (CRC) detects bit flips, and RAID stores data across multiple disks so a single failure does not lose information. HDDs report health through S.M.A.R.T. diagnostics, though the accuracy of those predictions is disputed. Optical media are checked by counting correctable minor errors; rising counts signal deterioration.

## Network and cloud storage

When secondary or tertiary storage is accessed across a network, three models dominate. Direct-attached storage (DAS) is local disks with no network. Network-attached storage (NAS) exposes file-level access over a network using protocols such as NFS or SMB. A storage area network (SAN) is a specialized network, often using Fibre Channel, that provides block-level storage to other computers.

Cloud storage adds virtualization, elasticity, multi-tenancy, and metered usage. It is offered as object storage, where files are retrieved by ID and suit unstructured data; file storage, or shared folders; and block storage, which emulates physical disks. Deployment models include public, private, hybrid, and virtual private clouds, with trade-offs between control, cost, and security.

## Storage media

Semiconductor memory uses MOSFETs and MOS capacitors on integrated circuits. Volatile forms such as DRAM and SRAM dominate primary storage, while non-volatile flash memory, built on floating-gate transistors, is the basis of SSDs, USB drives, and memory cards, and has largely displaced HDDs in laptops and desktops. Magnetic storage records patterns of magnetization. HDDs remain common for high-capacity secondary storage, and magnetic tape serves tertiary and offline archival. Because altering magnetic fields causes no physical wear, magnetic media can be rewritten indefinitely, with lifespan limited mainly by mechanical parts. Optical storage uses a laser to read pits and lands on a disc, in read-only (CD, DVD, Blu-ray), write-once (CD-R, DVD-R, BD-R), and rewritable (CD-RW, DVD-RW, BD-RE) forms. Paper storage, including punched cards, paper tape, and barcodes, predates electronics and is still used for very-long-term archival, since paper can outlast magnetic media. Experimental media include phase-change memory, holographic storage in crystals or photopolymers, and DNA digital data storage, which encodes bits in nucleotide sequences and can hold enormous quantities in a small physical volume.

Source: adapted from "Computer data storage" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Computer_data_storage
