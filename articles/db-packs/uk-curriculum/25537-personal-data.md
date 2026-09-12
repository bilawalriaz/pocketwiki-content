# Personal data

Personal data is any information relating to an identified or identifiable natural person. Identifiers may be direct (name, national ID, biometric) or indirect (location data, online identifier, or combinations like gender, ZIP code, and birth date that together single out an individual). In 1990, 87% of Americans were uniquely identifiable by those three attributes alone. The key is the link to a person: the word "red" is not personal data, but "favorite color: red" in a user record is.

## Two regulatory philosophies

**United States: sectoral, prescriptive PII.**  
"Personally identifiable information" (PII) is defined in statutes for specific domains. NIST SP 800-122 lists items that distinguish or trace identity (Social Security number, passport, biometrics) and items linkable to a person (medical, financial, employment records). California’s breach law (SB 1386) defines "personal information" narrowly: a name plus one additional element (e.g., SSN, driver’s license). A name alone or an SSN alone is not "personal information" under SB 1386, though both are PII under federal OMB guidance. HIPAA protects health data; the Privacy Act of 1974 governs federal agencies; other sectors have separate rules. No single federal law covers the private sector comprehensively. Internationally, "PII" is deprecated in favor of "personal data" or "personal information."

**European Union: principles-based, expansive personal data.**  
The GDPR defines personal data as "any information relating to an identified or identifiable natural person," including indirect identification via identifiers like name, ID number, location data, online identifier, or factors specific to physical, physiological, genetic, mental, economic, cultural, or social identity. An IP address can be personal data. The GDPR applies to processing of EU residents' data regardless of processor location, establishes lawful bases, data-subject rights (access, rectification, erasure, portability, objection), and heavy fines. The UK GDPR mirrors this regime.

Other jurisdictions align with the EU model: Australia’s Privacy Act covers "reasonably identifiable" individuals; Canada’s PIPEDA governs private-sector processing; Switzerland requires express consent for virtually any processing; New Zealand sets twelve privacy principles.

## How identifiability works

Direct identifiers (full name, national ID, biometric template) uniquely point to one person. Quasi-identifiers (age, gender, postcode, occupation) do not, but their combination rapidly narrows the field. De-identification is difficult: removing names while leaving birth date, ZIP code, and gender often leaves individuals re-identifiable. The GDPR treats pseudonymised data—where direct identifiers are replaced but re-identification remains possible—as personal data. Anonymous data, where re-identification is no longer feasible by any party using reasonable means, falls outside the regime.

Sensitive personal data (GDPR "special categories")—racial/ethnic origin, political opinions, religious beliefs, trade-union membership, genetic/biometric data, health data, sex life/orientation—receives stricter processing conditions. The UK and Australia treat health data similarly. U.S. law handles sensitivity contextually: HIPAA protects health data; the OMB notes not all PII is "sensitive," and context determines safeguards.

## Risks and exploitation

Personal data fuels identity theft, financial fraud, stalking, and doxing (public release of private details to harass or endanger). A Social Security number, date of birth, and name enable account takeover and credit fraud. A 2019 UK mobile-operator breach allowed hijacking of a customer’s phone number and mailbox. Data brokers aggregate public records, social-media activity, purchase histories, and geolocation into profiles sold for marketing, background checks, and risk scoring; Acxiom claims data on 2.5 billion people. The U.S. lacks a federal broker-regulation law; the GDPR subjects brokers to its full regime.

Surveillance capitalism describes the systemic extraction and commodification of behavioral data. Consumers typically have imperfect information about when their data is collected, for what purposes, and with what consequences. Economic models show privacy’s market impact is context-dependent: protection can improve or degrade efficiency depending on information asymmetry, price discrimination, and two-sided market dynamics.

## Forensic and protective uses

In criminal forensics, PII establishes identity: fingerprints, DNA, handwriting, glove prints, IP addresses. Criminals counter with masks, gloves, proxy servers, and handwriting avoidance. Wearing gloves during a crime can itself be an inchoate offense in many jurisdictions. Witness-protection programs, domestic-violence shelters, and intelligence agencies enforce strict PII controls to protect physical safety.

## Emerging responses

Personal-information-removal services automate takedown requests to data brokers, though coverage is incomplete and jurisdictionally limited. The EU–US Data Privacy Framework (2023) restores transatlantic data flows after the Privacy Shield’s invalidation. Some theorists propose data-ownership markets where individuals sell their data directly; others argue for stronger collective governance. The GDPR’s "right to be forgotten" and California’s CCPA/CPRA deletion rights give individuals legal leverage, but enforcement remains uneven.

The definition of personal data expands as new identifiers—device fingerprints, behavioral biometrics, inferred attributes—enter the ecosystem. The boundary between "anonymous" and "pseudonymous" shifts with advances in re-identification techniques. Regulatory convergence is slow; operational compliance still requires mapping each jurisdiction’s scope, sensitive-data categories, lawful bases, and subject-rights procedures.
