# Network security

Network security is the set of policies, controls, processes and practices that prevent, detect and monitor unauthorised access, misuse, modification or denial of a computer network and the resources reachable through it. A network administrator gives each user an ID and password, or other authenticating information, that limits them to data and programs within their authority. The same principles apply to private networks inside an organisation and to public networks used for transactions, business and government communication.

## Authentication

Authentication is the entry point to a secure network. One-factor authentication uses only a password. Two-factor authentication adds something the user has, such as a security token or dongle, an ATM card, or a mobile phone. Three-factor authentication adds something the user is, such as a fingerprint or retinal scan. Each additional factor makes impersonation harder because an attacker must steal or forge more independent pieces of evidence.

## The defence stack

Once a user is authenticated, further layers protect the network. A firewall enforces access policies by deciding which services network users may reach, but it usually does not inspect the content of that traffic for malicious payloads. Anti-virus software and an Intrusion Prevention System (IPS) catch known malware such as worms and Trojans travelling over the network. An anomaly-based Intrusion Detection System (IDS) studies traffic patterns, for example with a tool like Wireshark, logs activity for audit, and in newer deployments applies unsupervised machine learning to full network traffic to spot active attackers, malicious insiders, or external attackers who have already compromised a user machine or account.

Encryption between two hosts preserves confidentiality and privacy during transit. Honeypots and honeynets form a deceptive layer. A honeypot is a decoy resource that looks vulnerable but is isolated and monitored; attacks against it are studied to learn new exploitation techniques and to tighten the security of the real network. A honeynet is a network of honeypots whose shared purpose is to attract attacks so the methods can be analysed. Honeypots also waste an attacker's time and draw attention away from legitimate servers.

## Security management

Security management scales with the situation. A home or small office may need only basic controls, while large businesses run advanced hardware and software to block hacking and spamming. Corporations run ongoing security verifications that also catch insider threats and email storms. The human element is usually the weakest link: a 2014 study found that employees often do not see themselves as part of their organisation's information security effort and frequently take actions that impede security changes.

The shift from centralised systems to cloud-based and hybrid work has made networks harder to monitor with traditional tools. A Broadcom survey reported that 65% of respondents rely on third-party network providers, which creates blind spots and reduces direct control over infrastructure, making advanced monitoring harder to apply.

## Types of attack

Attacks fall into two categories. A passive attack intercepts data in transit, usually without raising alerts, and may be impossible for the victim to notice. A wardriving attack can wirelessly capture the four-way handshake between an access point and a client and then crack the password offline, leaving the access point owner unaware.

An active attack sends commands against the network or its resources to disrupt normal operation, perform reconnaissance, or move laterally to reach other assets. Active attacks include eavesdropping, data modification, denial-of-service, DNS spoofing, man-in-the-middle, ARP poisoning, VLAN hopping, smurf attacks, buffer and heap overflows, format string attacks, SQL injection, phishing, cross-site scripting and CSRF. Passive techniques include wiretapping, port scanning, idle scans, encryption-based interception and traffic analysis.

Passively intercepted traffic can still be read if it is unencrypted, which is why transport-layer encryption is treated as a baseline control alongside firewalls and authentication.
