# Computer network

A computer network is a group of communicating computers and peripherals, called hosts, that exchange data through agreed-upon rules, called communication protocols, carried over physical media and directed by networking hardware. The arrangement of hosts and links is the network topology. Today nearly every computer belongs to some network, from the global Internet to embedded systems in appliances, because most useful applications assume a connection.

## What a network is made of

Every network combines the same ingredients: hosts, the computers, phones, servers, and peripherals that originate or consume data; network addresses, numeric identifiers such as IP and MAC addresses that let hardware locate a host, with memorable hostnames translated to addresses by a name service like DNS; transmission media, the physical carriers of bits, including copper cable, optical fiber, and radio waves; networking hardware, including NICs, hubs, switches, routers, modems, and firewalls; and protocols, the rules for formatting and exchanging messages.

A protocol stack organizes these rules in layers, where each layer builds on the one below. In the dominant stack, TCP/IP, the physical layer moves raw bits, the link layer (Ethernet, Wi-Fi) carries frames between adjacent devices, the network layer (IP) routes packets across many links, the transport layer (TCP) ensures reliable delivery between programs, and the application layer (HTTP for the web, SMTP for email) provides the user-visible service.

## How data moves: packets

Modern networks use packet switching rather than circuit switching. A packet is a formatted bundle with control information, including source and destination addresses, sequencing, and error checks, in a header, and the user payload in between. Messages longer than the link's maximum transmission unit (MTU) are split into multiple packets and reassembled at the destination.

Packet switching lets many users share a link efficiently. When one user is silent, others' packets fill the gap, and a packet that hits a busy link is queued and forwarded later. Packets are independent of any single path, so the network can route around failures.

## The hardware

A network interface controller (NIC) connects a host to the medium. Each Ethernet NIC carries a globally unique 48-bit MAC address, with the first half identifying the manufacturer under IEEE oversight. A repeater cleans and retransmits signals; a hub repeats to every port but has been largely replaced by switches. A bridge or switch reads the destination MAC address in each frame and forwards it only out the correct port, learning which MAC sits where by watching source addresses. A router forwards packets between different networks using a routing table, exploiting the fact that IP addresses are structured so one entry can represent a group of nearby destinations. A modem (modulator-demodulator) converts digital data into an analog signal for media not built for digital traffic, such as telephone or cable lines. A firewall enforces access rules between a trusted internal network and an untrusted external one.

## Topology and scale

Topology, the pattern of interconnections, strongly affects reliability and cost. A bus shares one medium; a star concentrates connections through a central switch; a ring passes traffic node to node; a mesh offers many redundant paths, making the network robust but expensive. An overlay network is a virtual topology built on top of another network; the Internet itself began as an overlay on the telephone system.

Networks are classified by extent: a personal area network (PAN) reaches roughly 10 meters, often via Bluetooth or USB; a local area network (LAN) covers a building or campus, typically Ethernet or Wi-Fi; a campus area network (CAN) links several LANs; a metropolitan area network (MAN) covers a city; a wide area network (WAN) covers a country or continent and relies on leased carrier links. The Internet is the largest internetwork, networks stitched together by routers using the Border Gateway Protocol (BGP).

## How we got here

The first computer network was demonstrated in 1940, when George Stibitz used a teletype at Dartmouth to operate his Complex Number Calculator at Bell Labs. The SAGE system in the late 1950s became the first network to use a commercial modem.

The decisive step was packet switching, independently invented in the 1960s by Paul Baran in the United States and Donald Davies in the UK. Baran focused on adaptive routing of message blocks across a distributed network; Davies designed a hierarchical system with high-speed routers and the end-to-end principle, the idea that reliability belongs to the hosts, not the network. The NPL network in the UK pioneered a working implementation in 1968–69.

J. C. R. Licklider's early-1960s memos on an "Intergalactic Computer Network" inspired the ARPANET, which connected its first four nodes in 1969 at 50 kbit/s. In 1973, Robert Metcalfe and David Boggs at Xerox PARC described Ethernet, a local-area network inspired by the ALOHAnet packet radio system at the University of Hawaii; Peter Kirstein at UCL that same year connected the ARPANET to British academic networks, the first international heterogeneous network. In 1974, Vint Cerf and Bob Kahn published the TCP/IP design and coined "Internet" as shorthand for internetworking. Ethernet scaled from 2.94 Mbit/s to 10 Mbit/s in 1980, then 100 Mbit/s in 1995 and 1 Gbit/s by 1998, and this continuous scaling is why Ethernet still dominates. The NSFNET, launched in 1986, gave the U.S. a research backbone, and as embedded systems proliferated, networks spread into factories, cars, and everyday objects, giving rise to the Internet of Things.

## Performance, congestion, and security

Three quantities define how a network feels: throughput, useful bits delivered per second; latency, delay from sender to receiver, made up of processing, queuing, transmission, and propagation components; and jitter, variation in delay. When traffic exceeds a link's capacity, queues grow and packets are dropped, a state called congestion. Aggressive retransmission can lock a network into a low-throughput equilibrium called congestive collapse. Modern networks avoid this with congestion control such as TCP's window reduction and Wi-Fi's exponential backoff, and sometimes with quality-of-service priority queues for critical traffic.

Security is layered in. Firewalls filter traffic at network boundaries. End-to-end encryption, used by HTTPS, PGP, and similar systems, ensures that only the two communicating parties can read a message, so intermediaries cannot read or tamper with it; it does not hide traffic analysis or protect against compromise of the endpoints themselves. The SSL/TLS protocol, introduced by Netscape in the mid-1990s for e-commerce, established the certificate-based handshake that HTTPS still uses to authenticate servers and negotiate a per-session encryption key.
