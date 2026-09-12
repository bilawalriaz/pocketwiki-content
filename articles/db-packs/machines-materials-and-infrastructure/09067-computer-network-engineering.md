# Computer network engineering

Computer network engineering is the discipline that designs, builds, and runs the systems that move data between devices. Those systems are partly physical, the cables, antennas, routers, and switches that carry electrical or optical signals, and partly logical, the protocols and services that decide what those signals mean and where they go. The engineer's job is to make data flow quickly, safely, and reliably across a few metres (a LAN), across a continent (a WAN), or over the public Internet.

The field originated in the 1960s with ARPANET, which pioneered packet switching and reliable data transmission across a distributed network. The decisive shift came with standardisation of TCP/IP: once every device agreed on the same addressing and transport rules, heterogeneous computers could exchange packets, and routers could forward them without inspecting their contents. That interoperability is the technical basis of the modern Internet.

## How a network is built

A working network has two layers of design. The physical layer determines what carries the bits: copper twisted-pair Ethernet for short indoor links, fibre-optic cable for long backbones and data centres, or radio waves where cables are impractical. Fibre dominates long distances because it is fast and immune to electrical interference. Wi-Fi (IEEE 802.11) is the standard indoor wireless technology and uses the 2.4 GHz band for broader coverage or the 5 GHz band for higher speed and less interference. Cellular generations 3G, 4G, and 5G add wide-area wireless, with 5G using millimetre-wave frequencies to deliver higher data rates and lower latency for applications such as IoT and autonomous systems.

Sitting on the physical layer is the logical topology, which decides how packets travel between devices. In a star topology every device connects to a central switch, simple to manage but vulnerable to a single point of failure. In a mesh topology every device connects to several others, redundant and reliable but more expensive. Large networks use a hierarchical model split into core, distribution, and access tiers, which scales better than flat designs.

Network devices do the actual work of moving and protecting traffic. Switches connect devices on the same LAN. Routers connect different networks and choose the path each packet takes. Wireless access points extend coverage; cellular base stations and repeaters cover wide areas. Firewalls and network controllers enforce policy and segment traffic.

## Protocols

Hardware is useless without agreed rules. The TCP/IP suite is the foundation: the Internet Protocol (IP) handles addressing and routing between networks, while TCP guarantees that a byte stream arrives intact and in order. Above this baseline, specialised protocols solve narrower problems:

| Concern | Representative protocols |
|---|---|
| Dynamic routing inside one organisation | OSPF, EIGRP |
| Traffic engineering | MPLS, Segment Routing |
| Overlay networks across data centres | VXLAN, NVGRE |
| Encryption in transit | IPsec, TLS |
| Real-time media | RTP, WebRTC, QUIC |

## Security

Firewalls filter traffic at network boundaries; next-generation firewalls add deep packet inspection so they can act on application-layer data. Encryption protocols (IPsec and TLS) protect data in transit, and VPNs create encrypted tunnels over public networks for remote access. Intrusion detection and prevention systems (IDS/IPS), SIEM platforms, and endpoint detection and response (EDR) software watch for attacks. Network segmentation using VLANs and subnets isolates sensitive systems so a breach in one segment does not spread to the rest.

## Performance and optimisation

Modern networks carry far more than email: they stream video, run distributed databases, and connect IoT devices. Quality of Service (QoS) prioritises latency-sensitive traffic. In 5G, network slicing carves the physical network into virtual lanes with guaranteed bandwidth or latency. Software-defined networking (SDN) replaces manual device configuration with a central controller that programs the network as software, and network function virtualization (NFV) replaces dedicated appliances such as firewalls and load balancers with software on standard servers. Edge computing moves processing close to users to cut latency. Multipath TCP spreads a single connection over several links at once, raising available throughput. Cloud platforms add overlay networks (VXLAN, GRE) that run virtual networks on shared hardware, Infrastructure as Code to automate deployment, and content delivery networks that cache content near users.

## Where the field is heading

AI and machine learning are increasingly used inside network management: predicting congestion, detecting anomalies, and, with software-defined control planes, rerouting around faults automatically. Quantum networking is moving from theory to early experiments; quantum key distribution aims to make intercepted keys detectable, a property classical key exchange lacks. Low-Earth-orbit satellite constellations such as Starlink extend Internet access to places cables and cell towers do not reach, and the planned 6G standard is expected to push mobile data rates and latency further while requiring new approaches to spectrum use, energy efficiency, and infrastructure sustainability.
