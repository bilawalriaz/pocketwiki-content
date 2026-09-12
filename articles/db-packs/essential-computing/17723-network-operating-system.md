# Network operating system

A network operating system (NOS) is a specialised operating system for a network device such as a router, switch, or firewall. The term once described any operating system that gave a personal computer the ability to join a local area network (LAN), share files, and use shared printers. That older meaning is now mostly historical because mainstream desktop and server operating systems already ship with a built-in network stack and act as clients or servers in a client–server model.

## Core responsibilities

A NOS manages the activity that makes a packet-switched network useful. Its key functions are creating and managing user accounts, controlling who can reach shared resources such as files and printers, letting devices communicate, monitoring network performance, resolving problems as they appear, and managing resources so the network stays efficient and secure.

## How the term shifted

Packet-switched networks first appeared to share expensive hardware such as a mainframe, a printer, or a large hard disk. In that era a network operating system was simply an operating system for a computer that had been given networking capability, allowing PCs to act as clients of a server that handed out shared resources such as printers. Those limited client–server setups were then overtaken by peer-to-peer networks, in which every connected machine has equal status and offers its own files and resources to the others.

In the 1980s the need to connect dissimilar machines grew, and the number of networked devices rose rapidly. The Internet protocol suite (TCP/IP) became almost universal because it supported multi-vendor interoperability and could route packets globally instead of being confined to a single building. After that point, both general-purpose computer operating systems and the firmware inside network devices converged on Internet protocols.

## Network device operating systems

Today the label "network operating system" most often refers to the software embedded in routers and hardware firewalls that performs the work at layer 3 of the network model, the layer that decides how packets are forwarded between networks.

These systems fall into three groups. Proprietary NOSes ship from one vendor and run only on its hardware: Cisco IOS, IOS XE, IOS XR, and NX-OS on Cisco routers, switches, and Nexus and ASR platforms; Junos OS on Juniper Networks devices; ExtremeXOS on Extreme Networks switches; FTOS on Force10 Ethernet switches; ZyNOS on ZyXEL devices; RouterOS on MikroTik hardware; and Dell Networking OS on Dell switches, where DNOS9 is NetBSD-based and OS10 uses the Linux kernel.

Unix-like and Linux-based NOSes use a general-purpose kernel as their foundation. FreeBSD, NetBSD, OpenBSD, and Linux all serve this role. Cumulus Linux runs the full Linux TCP/IP stack on switches, Extensible Operating System (EOS) uses an unmodified Linux kernel on Arista switches, SONiC is a Linux-based NOS developed by Microsoft, and DD-WRT ports the Linux kernel to wireless routers and access points such as the Linksys WRT54G.

Open-source systems aimed at routing and security include OpenBSD, which ships its own implementations of BGP, RPKI, OSPF, MPLS, VXLAN, and other IETF-standardised protocols along with the PF firewall; OpenWrt for routing IP packets on embedded devices; pfSense and its fork OPNsense, both built around PF; VyOS, a fork of the Vyatta routing suite; IPFire, a firewall distribution; and ONOS, a Linux Foundation project for software-defined networking aimed at communications service providers that need scalability, high performance, and high availability.

Source: adapted from "Network operating system" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Network_operating_system
