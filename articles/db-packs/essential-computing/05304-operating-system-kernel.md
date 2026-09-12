# Operating system kernel

A kernel is the always-running core program of an operating system. It is one of the first programs loaded at startup, after the bootloader, and it stays resident in memory for the entire session. The kernel manages the processor, memory, and devices, and gives applications safe, shared access to them. Without a kernel, each program would have to drive the hardware directly, as early computers did in the 1950s and 1960s, and as some embedded systems and game consoles still do.

## Kernel space and user space

The kernel and applications run in two strictly separated areas of memory, kernel space and user space. The CPU switches between a restricted user mode for applications and a privileged supervisor mode for the kernel. When a process needs a privileged service, such as reading from disk or sending a network packet, it makes a system call, usually routed through a C library like Glibc or the Windows API. The call traps into the kernel, the kernel performs the action, and control returns to the application. This split stops a misbehaving application from corrupting the kernel and stops two applications from overwriting each other's memory. Even kernels that share an address space with applications enforce the boundary through hardware memory protection.

## Memory management

The kernel gives every process its own private virtual addresses, even when physical RAM cannot hold all of them. The memory management unit (MMU) translates those virtual addresses to physical addresses on the fly, so two processes can use the same address and see different data. The same mechanism divides memory into the kernel area and the application area, which is why the kernel/user split is nearly universal in general-purpose systems.

Virtual addressing also enables demand paging. When a program touches a page that is not in RAM, the CPU raises a fault. The kernel writes some other inactive page out to disk if needed, loads the requested page, and resumes the program. The program gets the illusion of a memory space larger than the physical RAM, at the cost of slower access to paged-out data.

## Processes, IPC, and device access

The kernel defines a protected address space, called an execution domain, for each running program and mediates every access to shared resources inside that domain. It also provides primitives for synchronization and inter-process communication (IPC), so cooperating programs can share data without interfering, and performs context switching, saving the state of one running thread and restoring another, which is what lets a single CPU appear to run many programs at once.

Processes rarely control hardware directly. The kernel talks to each device through a device driver, a program that translates the kernel's generic requests into device-specific commands. To display a character, an application asks the kernel, the kernel forwards the request to the display driver, and the driver plots the pixel. The kernel maintains a list of available devices, fixed at build time on embedded systems, user-configured on older PCs, or detected at boot by scanning buses like PCI and USB (plug and play) on modern systems. The same pattern applies to keyboards, mice, disk drives, printers, network adapters, and sound cards.

## System calls

A system call is the formal interface between a process and the kernel. Hardware offers a few ways to cross the protection boundary: an interrupt, a call gate, a dedicated syscall instruction, or a memory-based queue. Interrupts and call gates dominate because they work on common hardware, including older x86 CPUs. Each kernel exposes its own set of system calls, including basics like `open`, `read`, `write`, `close`, and `wait`, reached through a C library or API. Every privileged operation, from file I/O to process creation to network communication, ultimately goes through a system call.

## Kernel design choices

Three decisions define a kernel: how much runs in privileged mode, how the kernel talks to the rest of the system, and how protection is enforced.

In a monolithic kernel, all operating system services (drivers, file systems, network stack, scheduler, memory management) run in the same address space in supervisor mode. The Linux, FreeBSD, AIX, HP-UX, and Solaris kernels are monolithic, and most support loadable modules inserted at runtime. The advantage is speed, since subsystems share memory instead of sending messages. The disadvantage is a large trusted computing base, so a bug in a driver can crash the whole system.

In a microkernel, only a small set of primitives stays in kernel space: IPC, basic scheduling, basic memory handling, and basic I/O. Everything else, including file systems, drivers, networking, and the full scheduler, runs as ordinary user-space servers that exchange messages through the kernel. MINIX 3, QNX, and GNU Hurd are microkernels. The L4 family showed microkernels can match monolithic speed with careful design. The benefits are modularity and fault isolation: one crashing server does not bring down the system, and updates do not require a reboot. The historical cost was performance, since 1980s and early 1990s microkernels paid for message passing and extra context switches.

Hybrid kernels mix the two ideas. They keep a microkernel-like core but place performance-critical services, like the network stack or file system, back in kernel space. The Windows NT family uses a hybrid kernel influenced by the Mach microkernel. macOS uses XNU, which combines FreeBSD's monolithic kernel with Mach. The Linux kernel is often described as monolithic and modular because of its loadable modules.

## Protection

Protection has two flavors: fault tolerance (preventing accidental crashes) and security (preventing malicious behavior). Conventional kernels enforce both together through hierarchical protection domains, the kernel/user mode split, which mixes the underlying protection mechanism with a specific security policy. Capability-based systems keep them separate: the kernel hands applications opaque handles, like file handles, that grant only the operations the application is allowed to perform, and the kernel checks every use. Most commercial CPUs lack hardware support for capabilities, so the CHERI project is adding it. Language-based protection pushes enforcement into a trusted compiler that produces only verifiable code, removing the need to switch address spaces at runtime; JX and Microsoft's Singularity used this approach. Without kernel-level isolation, application-level security policies rest on weak ground, because a flawed driver in supervisor mode can read or corrupt anything those policies are meant to guard.
