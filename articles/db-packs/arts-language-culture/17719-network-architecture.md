# Network architecture

A network architecture is the design of a computer network: a framework that specifies the physical components, their functional organization and configuration, the operational principles and procedures, and the communication protocols used. In telecommunications, the specification can also describe the products and services delivered over the network and the rate and billing structures that compensate them.

## The Internet's architecture

The Internet is unusual in that its architecture is expressed predominantly through a protocol suite, the Internet protocol suite, rather than through a prescribed interconnection topology or hardware. The Internet does not depend on any specific link type or arrangement of nodes; any node that speaks the suite can participate. The same global Internet therefore runs across fibre, copper, radio, and satellite links at once.

## The OSI model and layered design

The Open Systems Interconnection (OSI) model codifies the concept of layered network architecture. It manages complexity by subdividing a communications system into abstraction layers. Each layer is a collection of similar functions that provides services to the layer above and receives services from the layer below. On every layer, an instance serves the instances above it and requests services from the one below.

The seven layers, top to bottom:

| # | Layer | Representative protocols and standards |
|---|---|---|
| 7 | Application | HTTP, FTP, DNS, SSH, SMTP, SNMP, DHCP, SIP, NTP |
| 6 | Presentation | MIME, TLS, ASCII, ASN.1 |
| 5 | Session | NetBIOS, PPTP, RTP, SOCKS |
| 4 | Transport | TCP, UDP, SCTP, QUIC |
| 3 | Network | IP (IPv4, IPv6), ICMP, IPsec, IGMP, IPX |
| 2 | Data link | Ethernet (IEEE 802 MAC), PPP, Frame Relay, ATM, HDLC, ARP |
| 1 | Physical | RS-232, SONET/SDH, DSL, USB, Bluetooth, IEEE 802 physical |

Higher layers deal with what users and programs see, such as web pages, files, and sessions. Lower layers deal with bits, voltages, and connectors. Because each layer only sees the service contract of its neighbour and not its implementation, a change in one layer (for example, a new physical medium) leaves the others untouched.

## Distributed computing and node-level architecture

In distributed computing, network architecture is also used to describe the structure of a distributed application, since the cooperating processes are themselves often called a network. The application architecture of the public switched telephone network (PSTN) has been termed the Intelligent Network, because call routing, billing, and service features are embedded in network nodes. At the opposite end of a continuum sits the dumb network, exemplified by the Internet, which keeps end-to-end intelligence in the hosts and treats the core as a transparent packet forwarder.

Peer-to-peer (P2P) services are a common contemporary instance. P2P networks usually implement an overlay network, a logical network built on top of an underlying physical or logical network, running across the participating nodes. These overlays may impose particular organizational structures on the nodes according to several distinct models, and that imposed structure is what practitioners call the P2P network architecture.

Source: adapted from "Network architecture" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Network_architecture
