# Operating system

An operating system (OS) is system software that manages a computer's hardware and software resources and provides common services to programs. It sits between applications and the bare hardware, deciding who gets the CPU, who gets memory, and how files, devices, and the network are accessed. Without an OS, every program would have to drive the hardware directly, and no two programs could safely share a machine.

## What an OS actually does

Three purposes define the job. First, the OS allocates limited resources between competing applications, giving each a fair share of CPU time and memory so one runaway program cannot monopolise the machine. Second, it isolates applications from each other, containing crashes and security breaches inside one program, while still allowing controlled communication between them. Third, it provides abstractions that hide messy hardware details, letting programmers work with files, virtual memory, and network sockets instead of raw disk sectors, RAM chips, and network cards.

The always-running core that enforces these jobs is the kernel. Programs running in user mode can only execute legal instructions; the kernel runs with unrestricted power. Everything else on the machine, system programs (such as a command shell) and applications (such as a browser), sits on top of the kernel. Most of an OS's code is not the kernel itself but the surrounding services.

## Mechanisms the OS uses

Interrupts are the OS's main way of reacting to events. A hardware or software signal forces the CPU to stop the current program, save its state, jump to a handler, and resume later. Pressing Control-C to kill a stuck command, a disk finishing a read, and a timer ticking all arrive as interrupts. Because I/O devices are far slower than the CPU, this asynchronous model lets the processor keep working on other tasks instead of waiting.

Processes and threads let several programs appear to run at once. A process owns its memory and resources; threads inside it share those resources and are cheaper to create. The kernel rapidly switches between them, saving each one's registers and program counter (a context switch) so they take turns. Modern systems use preemptive multitasking, where the kernel can interrupt a thread at any moment, replacing earlier cooperative schemes where a thread could hog the CPU indefinitely.

Virtual memory gives each program the illusion of a large, private, contiguous address space. The kernel maps virtual addresses to physical RAM and to disk, swapping rarely used pages out to storage. This both isolates programs from each other and lets the system run programs bigger than the installed RAM.

File systems translate human-readable names into blocks on disk. They handle directories, free-space tracking, caching, atomic writes (so a crash never leaves a file half-written), and checksums for corruption. They sit on top of storage hardware whose access times differ from RAM by orders of magnitude, so caching and prefetching matter greatly.

Device drivers are OS-specific translators that let the kernel talk to particular pieces of hardware without applications needing to know what hardware is present.

Security rests on the CIA triad: confidentiality, integrity, and availability. The kernel enforces isolation, checks authorisation on every request, and applies the principle of least privilege. Most OS code is written in C or C++, which lack bounds checking and so allow buffer-overflow attacks; hardening techniques such as address space layout randomization and control-flow integrity make such exploits harder.

## Varieties of operating system

General-purpose desktop and mobile OSs dominate everyday computing. As of late 2025, Android led web-connected usage with a 38% share, followed by Microsoft Windows (around 31–33%), iOS and iPadOS (15%), macOS (4–7%), and Linux (1%). Linux distributions dominate servers and supercomputers and number in the thousands.

Specialised classes serve narrower needs. Real-time operating systems guarantee that events are processed within strict deadlines; hard real-time systems used in manufacturing and avionics often have no protection between applications, trading isolation for timing precision. Embedded operating systems run inside appliances and internet-of-things devices, often in less than 10 kilobytes, and do not load user-installed software, so they need no inter-application protection. Library operating systems strip the OS down to libraries linked with a single application, producing a unikernel suited to cloud or embedded deployment, with faster system calls because there are no context switches. Hypervisors run virtual machines that emulate hardware, useful for research, portability, and running incompatible software on one host.

## A brief history

Late-1940s and 1950s computers were programmed directly with plugboards or punched cards; no operating system existed. Transistor-based mainframes of the mid-1950s still relied on professional operators, though rudimentary monitor systems such as FMS and IBSYS handled simple scheduling. In the 1960s, IBM's System/360 line shipped with OS/360, written in millions of lines of assembly and famous for thousands of bugs; it was also the first widely used OS to support multiprogramming, holding several jobs in memory so one could use the CPU while another waited for I/O.

MULTICS in the same era aimed to give hundreds of users simultaneous access to one large machine and is regarded as a precursor to cloud computing. UNIX descended from MULTICS as a single-user system; its source code being openly available spawned System V from AT&T and BSD from the University of California. IEEE's POSIX standard later made UNIX-like systems broadly compatible. MINIX, a stripped-down UNIX created in 1987 for teaching, inspired the commercially successful free-software project Linux. Since 2008, MINIX has run inside most Intel chips as a controller; Linux dominates data centres and powers Android smartphones.

The personal-computer era began around 1980. CP/M led microcomputers for about five years until IBM's 1981 choice of Microsoft Disk Operating System (MS-DOS) reshaped the market. Apple's 1984 Macintosh popularised the graphical user interface (GUI); Microsoft's Windows began as a GUI shell over MS-DOS and was later rewritten as the standalone Windows NT, borrowing so heavily from DEC's VAX/VMS that a large legal settlement followed. On mobile devices, Symbian OS gave way to BlackBerry OS (from 2002), then iOS (from 2007), and finally Android (from 2008), which combined a Linux kernel with the Bionic C library partly derived from BSD. Today UNIX-style systems, especially Linux, are most common on enterprise servers, while Windows remains popular on personal computers.
