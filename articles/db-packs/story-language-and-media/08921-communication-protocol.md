# Communication protocol

A communication protocol is a system of rules that lets two or more computing entities exchange information. It defines the rules, syntax, semantics, and synchronization of communication, including how to recover from errors. Protocols are to communication what algorithms are to computation. Most networks use several protocols together as a **protocol suite**, which, when implemented in software, becomes a **protocol stack** where each layer solves a distinct class of problem.

## Origins and growth

The term entered modern data communication in 1967 in a memorandum for the NPL Data Communications Network, directed by Donald Davies at the UK National Physical Laboratory. In 1969 Bob Kahn wrote the 1822 protocol for the ARPANET, and in 1970 Steve Crocker, Jon Postel, and others deployed the Network Control Program, an early example of protocol layering. Louis Pouzin's CYCLADES network in the early 1970s pioneered the end-to-end principle, putting reliability in the hosts rather than the network, which influenced TCP. Bob Metcalfe's work at Xerox PARC produced Ethernet and the PARC Universal Packet.

Research by Kahn and Vint Cerf led to the Transmission Control Program, specified in RFC 675 in December 1974. It was split into TCP and IP, installed on SATNET in 1982 and the ARPANET in January 1983, and by 1989 the full TCP/IP suite was documented in RFCs 1122 and 1123. ISO published the OSI reference model in 1984. Through the late 1980s and early 1990s the field polarized over TCP/IP versus OSI; TCP/IP won, and the IETF's principle of "rough consensus and running code" became the dominant standardization style.

## Message encoding

Protocols can be text-based, with human-readable ASCII or UTF-8 lines terminated by newline (FTP, SMTP, early HTTP, finger), or binary, using all byte values. Text is easier to debug; binary is denser and faster for machines to parse. HTTP/2, HTTP/3, and EbXML use binary formats.

## What a protocol must specify

A working protocol addresses recurring problems. **Data format**: messages are bitstrings split into a header (control information) and a payload (the actual data); messages longer than the maximum transmission unit are fragmented. **Addressing**: sender and receiver identifiers in the header, with an addressing scheme that may include broadcast addresses. **Address mapping**: translating between schemes, such as IP to Ethernet MAC. **Routing**: forwarding through intermediary systems. **Error detection**: a CRC in each packet lets the receiver detect corruption. **Acknowledgements**: receivers confirm receipt for connection-oriented communication. **Timeouts and retries**: senders retransmit if no acknowledgement arrives, up to a retry limit. **Direction of information flow**: media access control governs who transmits on half-duplex or shared media, including handling collisions. **Sequence control**: sequence numbers let receivers reassemble, deduplicate, and request retransmission of fragments. **Flow control** prevents a fast sender from overwhelming a slow receiver. **Queueing** uses FIFO buffers, sometimes with priorities.

## Protocol suites and layering

A network transmission is handled not by one protocol but by a cooperating set, organized by function in a **layering scheme**. The two dominant schemes are the **TCP/IP model**, used on the Internet and connectionless at the network layer, and the **OSI model**, originally connection-oriented and later extended to connectionless services. OSI has seven layers, from bottom to top: physical, data link, network, transport, session, presentation, application. TCP/IP collapses these into roughly four: link, internet, transport, application.

To send a message, each layer hands its data to the layer below, adding its own header in a process called encapsulation. On reception, each layer strips its header and passes the remainder upward. Message flow diagrams show vertical flows inside one system and horizontal flows between systems at the same layer. **Strict layering** keeps each layer ignorant of others' internals, but real systems sometimes break it for performance, and layering has been criticized for forcing the same function, such as error recovery, to be implemented in more than one layer.

## Standards and standardization

Protocols can become **de facto standards** through market dominance, which can lock out competitors; IBM's BSC protocol spawned over 50 incompatible variants. Formal standards come from organizations including ISO, ITU, IEEE, the IETF (which maintains Internet protocols), and the W3C (web). The IETF's "rough consensus and running code" process differs from ISO's committee-driven draft progression, and multiple uncoordinated bodies defining the same protocol can produce incompatible interpretations.

## Wire image and ossification

The **wire image** of a protocol is everything an outside observer can infer from on-the-wire messages, including unencrypted metadata and timing. The IETF declared in 2014 that large-scale surveillance of the wire image is an attack, and protocol design now deliberately hides signals from intermediaries. **Protocol ossification** is the loss of evolvability that happens when middleboxes such as firewalls, NATs, and load balancers make assumptions about a protocol's wire image and drop or block messages they do not recognize, violating the end-to-end principle. Ossification is why TCP and UDP remain the only practical Internet transport choices, and why QUIC was the first IETF transport designed with explicit anti-ossification properties.

Source: adapted from "Communication protocol" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Communication_protocol
