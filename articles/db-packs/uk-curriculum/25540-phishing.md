# Phishing

Phishing is a form of social engineering—a manipulation technique that exploits human trust rather than technical vulnerabilities—to deceive people into revealing sensitive information such as passwords or financial details, or into installing malware like ransomware. The term, a deliberate misspelling of "fishing," appeared in the 1995 cracking toolkit AOHell, describing the use of lures to "fish" for data. It remains the most prevalent cybercrime globally, affecting the vast majority of organizations. Generative AI now enables attackers to craft highly convincing, automated, and hyper-targeted campaigns at unprecedented scale.

## Main Types

**Email phishing** delivers fraudulent messages in bulk, often mimicking banks, cloud providers, or streaming services. Stolen credentials are used for theft, malware installation, or further spear phishing; compromised accounts are sold on darknet markets.

**Spear phishing** targets specific individuals—often executives or finance staff—using personal or organizational details to build credibility. It frequently combines email, SMS, and calls to manufacture urgency. The Russian group Fancy Bear (GRU Unit 26165) used the domain `accounts-google.com` to spear phish over 1,800 Google accounts linked to Hillary Clinton’s 2016 campaign.

**Vishing (voice phishing)** uses VoIP and text-to-speech to automate calls spoofed from legitimate numbers, claiming account fraud. Victims are prompted to enter data or transferred to a live social engineer. It exploits higher trust in telephony versus email.

**Smishing (SMS phishing)** sends bait via text message, urging clicks, calls, or replies. Attackers impersonate governments, shippers, bosses, or "wrong numbers." Mobile browsers’ truncated URL display complicates link verification.

**Quishing (QR code phishing)** embeds malicious links in QR codes sent by email, social media, or physical stickers placed over legitimate codes (e.g., on parking meters). Scanning redirects to credential-harvesting sites. QR codes bypass email filters and receive less scrutiny than URLs. Attackers now combine quishing with browser-in-the-browser techniques to steal two-factor authentication (2FA) approvals.

**Man-in-the-Middle (MitM) phishing** intercepts live sessions between user and legitimate service, stealing session cookies and login tokens to bypass 2FA entirely. Tools like Evilginx—originally for penetration testing—act as a transparent proxy, passing traffic without storing passwords, evading detectors that look for credential storage. Attackers gain full account access for the session’s duration.

**Page hijacking** compromises legitimate sites via cross-site scripting or malicious iframes to load exploit kits, often paired with watering hole attacks on corporate targets.

## How Attacks Work

**Link manipulation** disguises malicious destinations. Subdomain tricks (e.g., `http://www.yourbank.example.com/` points to the attacker’s `example.com`, not `yourbank`) and deceptive display text are common. Internationalized domain names enable homograph attacks: `http://www.exаmple.com/` uses a Cyrillic `а` to mimic `example.com`, resolving to `xn--exmple-4nf.com`. Hovering to inspect URLs can be defeated by JavaScript redirects.

**Social engineering** creates urgency—threatening account closure—or impersonates trusted entities. Fake virus notifications or fabricated news articles lure clicks. Generative AI amplifies realism in text and images, improves targeting, and automates campaign production.

## Historical Evolution

- **1990s**: AOL warez community stole credit cards via instant messages impersonating staff; AOHell automated the process.
- **2000s**: Organized crime emerged. First payment-system attack (E-gold, 2001); first retail bank attack (2003). U.S. losses hit nearly $1B (1.2M users, 2004–2005). UK banking fraud losses doubled in 2005. Russian Business Network groups committed roughly half of thefts in 2006.
- **2010s**: High-profile breaches. RSA SecurID master keys stolen (2011). Target lost 110M records via phished subcontractor (2013). iCloud celebrity leaks (2014). ICANN administrative access compromised (2014). Fancy Bear hit Pentagon, White House, NATO, DNC, Bundestag, WADA (2015–2016). 76% of organizations attacked in 2017.
- **2020s**: Twitter breach (July 2020): a 17-year-old built a fake VPN portal, vished employees as helpdesk, seized high-profile accounts, and collected cryptocurrency. Phishing-as-a-Service (PhaaS) platforms like Darcula now let attackers clone trusted sites instantly.

## Defense

**Human layer**: Training teaches indicators—requests for credentials, URL/email mismatches, generic greetings, typos, urgency, unexpected attachments, poor graphics. Simulated campaigns test readiness. PayPal addresses users by username, but personalization alone doesn’t guarantee legitimacy; studies show it negligibly affects click rates. Educational games reduce disclosures.

**Technical layer**: Spam filters use machine learning and natural language processing to block phishing mail. Browsers (Chrome, Edge, Firefox, Safari, Opera) check URLs against real-time blocklists (Google Safe Browsing, Microsoft Defender SmartScreen, Netcraft, etc.). DNS filtering services block known malicious domains. Site owners alter logos to serve warnings when hotlinked.

**Authentication**: Multi-factor authentication (MFA) limits damage from stolen passwords but falls to MitM and session hijacking. WebAuthn/FIDO2 resists these by binding credentials to the legitimate domain. Dynamic image grids and security skins (user-chosen images overlaid by the browser) add mutual authentication, though adoption is limited.

**Monitoring and takedown**: Digital Risk Protection services (Netcraft, ZeroFox, Recorded Future) automate detection and removal of impersonating infrastructure. Individuals report to PhishTank, Google, or industry groups.

**Legal layer**: The U.S. FTC filed the first phishing suit in 2004. Brazil arrested a kingpin who stole $18–37M. UK Fraud Act 2006 criminalizes phishing kit possession (up to 10 years). Microsoft filed 117 U.S. lawsuits in 2005 and 129 mixed actions by 2006. The first U.S. jury conviction under CAN-SPAM (2007) yielded a 70-month sentence.

Phishing targets the human element, which technology alone cannot fully patch. As AI lowers the cost of sophistication and PhaaS commoditizes infrastructure, the gap between lure and legitimate communication narrows, making continuous vigilance and layered defense the only sustainable posture.