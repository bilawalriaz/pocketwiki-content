# Information security

Information security is the practice of protecting information by managing the risk that it will be accessed, changed, destroyed, or disrupted by unauthorised actors. It covers information in any form, including digital files, paper records, and tacit knowledge, and applies whether data is stored, processed, or transmitted.

## The CIA triad

The discipline is organised around three goals known as the CIA triad. **Confidentiality** means keeping information away from people who are not authorised to see it. **Integrity** means data cannot be modified in an unauthorised or undetected way and remains accurate and complete. **Availability** means information and the systems holding it are working when needed. The triad was formalised in the Anderson Report (1972) and the abbreviation was coined by Steve Lipner around 1986. Some practitioners extend it with authenticity, accountability, non-repudiation, and reliability (the debated Parkerian Hexad).

## Threats and risk

A **threat** is anything with potential to cause harm, a **vulnerability** is a weakness that could be exploited, and **risk** is the likelihood that a threat will use a vulnerability. When that happens, the impact is a loss of one or more CIA properties, plus possible financial, reputational, or human costs. Common threats include software attacks (viruses, worms, phishing, Trojan horses), identity theft, theft of intellectual property or equipment, sabotage, and information extortion (ransomware). The most vulnerable point in most systems is the human user.

Risk cannot be eliminated, so any programme leaves a **residual risk** to be accepted, mitigated, transferred (for example through insurance), or, in disputed cases, denied. The standard cycle is: identify assets and their value; conduct a threat assessment; conduct a vulnerability assessment; calculate impact; select proportional controls that balance productivity, cost, and asset value; then evaluate whether the controls actually work. Standards such as ISO/IEC 27001 and the U.S. NIST Cybersecurity Framework give organisations a structured way to run this cycle. Other widely used standards include the ISO/IEC 27000 family, Common Criteria (ISO/IEC 15408), IEC 62443 for industrial control systems, ISO/SAE 21434 for road vehicles, ETSI EN 303 645 for IoT, PCI DSS for cardholder data, the UK's Cyber Essentials, and Australia's Essential Eight. The Gordon–Loeb Model offers a mathematical way to decide how much to spend protecting a given asset.

## Controls and defence in depth

Controls are countermeasures that protect confidentiality, integrity, or availability. The **defense in depth** philosophy layers multiple, overlapping controls, including administrative (policies, training), logical (access permissions, encryption), and physical (locks, guards), so that no single failure exposes the data. Visualised as an onion, the data sits at the core, surrounded by application security, host security, network security, and people.

## Classification and access control

Because not all information is equally sensitive, organisations assign a **classification label** to each asset, for example Public/Sensitive/Private/Confidential in business, Unclassified up to Top Secret in government, or the colour-coded Traffic Light Protocol across sectors. Each label triggers a defined set of handling rules and controls.

Access is enforced through a three-step process. **Identification** is a claim of who someone is, typically a username. **Authentication** is verification of that claim, using something the user knows (password, PIN), has (token, card), or is (fingerprint, iris scan); two-factor authentication combines two of these. **Authorisation** decides what an authenticated user may do, such as read, write, or delete, based on policies, the user's role, the resource's classification, or the resource owner's discretion. The **need-to-know principle** restricts access to the minimum required for the job, even among staff with the same clearance. Authentication and authorisation attempts should be logged so an audit trail exists.

## Cryptography

**Cryptography** transforms readable information into an unreadable form (**encryption**) using a mathematical **key**, and reverses the process (**decryption**) for authorised holders. It protects data both in transit and at rest, and underpins stronger authentication, digital signatures, and non-repudiation. Older protocols such as Telnet, FTP, and WEP are being replaced by encrypted successors (SSH, WPA/WPA2). Poor implementation, short or weak keys, or careless key management can undermine the whole scheme, so peer-reviewed algorithms and well-managed public-key infrastructures are essential.

## Operations: change, incident, and continuity

Because change is itself a source of risk, formal **change management** processes (request, approve, plan, test, schedule, communicate, implement, document, review) reduce the chance that a routine update disrupts critical systems. **Incident response plans**, run by specialist teams, define how to detect, contain, and recover from breaches. **Business continuity management** ensures critical functions survive a major disruption; a related **disaster recovery plan** focuses specifically on restoring IT infrastructure afterwards.

## Laws, regulation, and people

Information security is shaped by regulation, including the UK Data Protection Act 1998, the EU Data Protection Directive, the Computer Misuse Act 1990, FERPA, HIPAA, GLBA, Sarbanes–Oxley Section 404, PCI DSS, and Canada's PIPEDA. U.S. Federal Sentencing Guidelines make corporate officers liable for failing to exercise due care and due diligence. Because the threat environment changes daily, no control remains effective without ongoing maintenance and review, and organisations must build a **security culture** spanning attitudes, awareness, communication, policy compliance, shared norms, and clear responsibility.
