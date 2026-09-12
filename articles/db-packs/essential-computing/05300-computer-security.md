# Computer security

Computer security (also cybersecurity or IT security) protects computer systems, networks, and data from unauthorized access, theft, damage, and disruption. It sits within information security, which also covers internal policies and non-digital controls. As societies depend more on systems including smartphones and Internet-of-things (IoT) devices, the consequences of failure extend into physical infrastructure: power grids, hospitals, financial markets, and election systems can all be crippled by one breach. Physical defenses such as locks still matter because an attacker with hands-on access can bypass software controls.

## Vulnerabilities and threats

A **vulnerability** is a flaw in software, hardware, or procedures that compromises security. Most known vulnerabilities are catalogued in the Common Vulnerabilities and Exposures (CVE) database; one with a working exploit is called exploitable. A **threat** is any party that might exploit a vulnerability. Defenders reduce the **attack surface** (the set of points an attacker can reach) through vulnerability management: scanning for known flaws, patching promptly, and running penetration tests where outside auditors attempt to break in.

## How attacks work

Malware is software written to harm systems. Viruses attach to programs and need a user to run them; worms self-replicate across networks without help; trojans disguise themselves as legitimate software; spyware, including keyloggers, silently harvests data; scareware manipulates users with fake warnings; ransomware encrypts files and demands payment.

Phishing and social engineering trick people into handing over credentials. Phishing uses fake emails or sites that mimic real ones; spear-phishing tailors the bait to a specific person. The FBI reported that business-email-compromise scams cost US firms more than $2 billion over roughly two years ending in early 2016.

Man-in-the-middle attacks intercept or alter communication between two parties who believe they are talking directly. Variants include IP spoofing, DNS spoofing (redirecting lookups to attacker-controlled servers), and SSL hijacking (presenting a fraudulent certificate to break encryption).

Denial-of-service (DoS) attacks make a service unavailable. Distributed DoS (DDoS) floods a target from many machines, often a hijacked botnet, making it much harder to block than a single-source attack.

Backdoors are hidden methods of bypassing authentication, inserted by attackers or left in by design. Eavesdropping silently intercepts unencrypted traffic on open networks and leaves no performance trace; a VPN or HTTPS is the standard defense. Physical-access attacks bypass software by booting from external media or installing keyloggers; disk encryption and the Trusted Platform Module (TPM) counter them. Side-channel attacks infer secrets from physical effects such as power draw, timing, or memory residue rather than from the data itself. Multi-vector polymorphic attacks, emerging around 2017, combine techniques and change their code as they spread, defeating signature-based antivirus.

## Core goals and defending systems

The **CIA triad**, confidentiality, integrity, and availability, is the foundational goal. Every countermeasure maps onto one or more of these properties.

A *countermeasure* is any action, device, or procedure that reduces a threat. Defense works best in layers (**defense in depth**), so breaching one control does not compromise everything.

Security by design builds protection in from the start: least privilege (every component has only the access it needs), fail-secure defaults, audit trails, and prompt disclosure of vulnerabilities to keep the exploit window short. Formal verification, including automated theorem proving, can mathematically prove critical code correct; the seL4 and PikeOS operating systems are rare real-world examples.

A firewall filters traffic between a trusted and an untrusted network using packet-filtering rules; it can be software or a physical appliance. An intrusion detection system (IDS) watches for attacks in progress and supports forensics. Authentication confirms identity; access control lists (ACLs) and role-based access control (RBAC) decide what a user can do. Two-factor authentication requires something the user knows (a password) plus something they have (a phone or token), so stolen credentials alone are insufficient. Hardware safeguards include TPMs, USB dongles, drive locks, and disabled unused ports; infected USB sticks plugged into a machine behind the firewall are the most common hardware threat.

No defense is perfect, so organizations prepare incident response plans with four phases: preparation, detection and analysis, containment, eradication and recovery, and post-incident review. Quick response limits damage. Attackers route through proxies and machines across jurisdictions, complicating attribution.

## The human element

People remain the weakest link. The Verizon 2020 Data Breach Investigations Report, covering 3,950 breaches, found 30% of incidents involved internal actors, and analysts estimate more than 90% of security incidents involve some form of human error: poor passwords, misdirected emails, or failure to spot a fake login page. Inoculation theory offers a defensive analogue to vaccination: pre-exposing people to simulated phishing attempts builds resistance to real ones.

Cyber hygiene, the routine of updating software, backing up data, using strong unique passwords, and restricting admin rights, gives any user a baseline. The Gordon-Loeb Model captures the underlying trade-off: an organization should typically spend only a small fraction of the expected loss from a breach, because early security spending eliminates the cheapest attacks and additional spending yields diminishing returns.

## Notable incidents

In 1988, the Morris Worm infected an Internet of about 60,000 machines and slowed most of them. In 2010, the Stuxnet worm reportedly destroyed almost one-fifth of Iran's nuclear centrifuges by reprogramming industrial controllers, a landmark attack on physical equipment generally attributed to Israel and the United States. The 2013 Target breach (around 40 million credit cards) and 2014 Home Depot breach (53–56 million) used unsophisticated malware that warnings could have stopped. The 2015 US Office of Personnel Management breach exposed roughly 21.5 million personnel records, including Social Security numbers and fingerprints, and is attributed to Chinese hackers. In June 2021, ransomware shut down the largest US fuel pipeline (Colonial Pipeline) and caused East Coast shortages.

## Governance

No global legal framework governs cybercrime; attackers exploit the gap by routing through jurisdictions that will not prosecute. Governments respond with national strategies and computer emergency response teams (CERTs). The European Union's GDPR, in force since 2018, requires data protection by design and by default. The United States built the NIST Cybersecurity Framework after a 2013 executive order, and Executive Order 14028 in 2021 tightened software standards for federal suppliers. Cybersecurity is now treated by militaries as a warfighting domain, with US Cyber Command (created 2009) and the UK's National Cyber Force (launched 2020) as examples. The field grows faster than the talent pool: 46% of organizations reported a problematic cybersecurity skills shortage in 2016, up from 28% in 2015.
```

Source: adapted from "Computer security" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Computer_security
