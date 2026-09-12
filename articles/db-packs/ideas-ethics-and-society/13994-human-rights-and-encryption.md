# Human rights and encryption

Encryption is the mathematical scrambling of information so only intended parties can read it. It is foundational to a free, open, and trustworthy internet, and its availability shapes whether people can exercise two human rights: **freedom of expression** (Article 19 of the Universal Declaration of Human Rights and the International Covenant on Civil and Political Rights, ICCPR) and **privacy** (Article 17 ICCPR). Digital rights management in video games shows the reverse: encryption can lock purchased software so it stops working years later, eroding consumer rights.

## What encryption does

Encryption keeps messages confidential, proves who sent them (authenticity), and proves they were not altered (integrity). These properties let journalists protect sources, activists organize, and ordinary users browse without fear of interception. Since the 1970s, public-key cryptography has made encryption available outside nation-state intelligence agencies.

UN Special Rapporteur David Kaye told the Human Rights Council in June 2015 that encryption and anonymity "provide individuals with a means to protect their privacy, empowering them to browse, read, develop and share opinions and information without interference." The groups that depend on it most include journalists, civil society organizations, ethnic and religious minorities, LGBTQ+ people, persecuted activists, scholars, and artists.

## How it is deployed

- **Transport security (TLS/HTTPS)**: protects the connection between a user and a website against eavesdropping and man-in-the-middle attacks. It requires both the user's software and the service provider to implement it; users cannot enable it alone, and many providers implement it poorly.
- **End-to-end encryption**: scrambles messages so only sender and recipient can read them, not the service provider. Without it, messaging services could read all content.
- **At-rest encryption**: protects stored data on devices or cloud servers. Users must still trust the provider not to hand data to governments.
- **Anonymity tools (Tor, VPNs)**: hide who is communicating with whom, not just what is said. Tor routes traffic through volunteer proxies so no single relay sees both ends.
- **Obfuscation tools (e.g. TrackMeNot)**: generate fake signals to muddy user profiles, though some are vulnerable to filtering attacks.

Metadata (who contacted whom, when, and for how long) is often unencrypted. The Berkman Center notes that metadata "provides an enormous amount of surveillance data that was unavailable before [internet communication technologies] became widespread." Bitcoin is often called anonymous but only offers pseudonymity; protecting metadata requires anonymity tools used alongside encryption.

## The legal framework

Under Article 19(3) ICCPR, any limitation on freedom of expression must be provided by law, aimed at a legitimate goal such as national security or public order, and necessary and proportionate. Restrictions on cryptography most often invoke Article 19(3)(b), creating a tradeoff between individual protection from surveillance and state access for law enforcement.

International positions:

- **OECD (March 27, 1997)** set cryptography guidelines so national policies do not block trade. Principle 5 states that rights to privacy and secrecy of communications "should be respected in national cryptography policies."
- **UN Special Rapporteur** and **UNESCO** (Keystones Report, 2015) treat encryption as essential to freedom of expression and privacy.
- **ENISA and Europol** have rejected mandatory backdoors, joined by **Germany** and the **Netherlands**. Germany declared itself "Encryption Site No. 1" in a 2015 charter.

The UN's first Special Rapporteur on Privacy, Joe Cannataci, called privacy "an essential right which enables the achievement of an over-arching fundamental right to the free, unhindered development of one's personality." Restricting encryption therefore interferes with freedom of expression itself, because fear of surveillance distorts what people choose to say.

## National approaches

The United States has debated encryption since the 1990s "Crypto Wars," with CALEA requiring wiretap capability and export controls once treating strong crypto as munitions. The FBI-Apple dispute tested backdoor access. Germany gives encryption constitutional protection through the IT basic right and rejected bans in 1999. India lets the government set encryption rules under Section 84A of the IT (Amendment) Act 2008; a 2008 draft restricting mass-use products was withdrawn after backlash. Brazil passed Marco Civil in 2014 and a 2016 data protection law, but courts have repeatedly blocked WhatsApp over its end-to-end encryption.

Several states restrict or ban encryption outright. Tunisia's 2001 Telecommunication Code (Articles 9 and 87) bans encryption, with up to five years' prison for unauthorized use. Egypt's 2003 Telecommunication Regulation Law requires written consent from the NTRA, military, and national security authorities. Morocco requires licenses to import or export cryptographic technology under Law 53-05 (effective December 2007). Algeria has required authorization from ARPT since 2012. Ghana's proposed bill would allow interception on oral order from a public officer, with no judicial warrant. Nigeria has drafted a bill forcing phone companies to store all communications for three years and letting authorities demand decryption keys. South Africa does not prohibit use but regulates provision.

## Service providers as intermediaries

Service providers control which encryption is deployed by default. Cloud providers see all stored data; messaging services could read content unless end-to-end encryption is in place. Providers sit at the seam between users and states, making them both guardians and weak points. The unresolved question is jurisdiction: when a foreign service offers end-to-end encryption, which country's law-enforcement demands should it obey, and which human rights standards apply?

## UNESCO's framework

UNESCO's Internet Universality concept treats encryption as essential infrastructure. It considers interference with encryption especially severe when it weakens protections by key service providers, blocks vulnerable groups from accessing encryption, is justified only by theoretical risks, or uses informal arrangements that erode deployed security without accountability. Cryptographic standards expire as computing power grows, so continuous innovation and public education are necessary. Procedural guarantees matter too: transparency about who decided what, effective remedies, and legal certainty so people know when surveillance is lawful.

Source: adapted from "Human rights and encryption" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Human_rights_and_encryption
