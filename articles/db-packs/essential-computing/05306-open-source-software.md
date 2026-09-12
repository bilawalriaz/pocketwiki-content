# Open-source software

Open-source software (OSS) is software whose source code is publicly available under a licence that lets anyone use, study, modify, and redistribute it. The opposite is proprietary, or closed-source, software, where the source is kept secret and copying is forbidden. OSS is not a niche: a 2022 estimate found that 80–96% of the code inside today's commercial software is of open-source origin, and it underpins web servers, cloud platforms, supercomputers, mobile devices, AI, and the Internet of Things.

## What "open" actually means

The standard benchmark is the Open Source Definition (OSD), maintained by the Open Source Initiative (OSI), founded in 1998. The OSD sets out ten criteria; the key one is non-discrimination: the licence must grant the same rights to every person, group, and field of use, with no restriction on who may modify or redistribute the code or for what purpose. The OSD was derived from the Debian Free Software Guidelines, written mainly by Bruce Perens and Eric S. Raymond. The OSI publishes a list of approved licences but has no legal authority, so "open source" is often used loosely, which fuels a long-running community conflict.

A related term is free software, promoted by the Free Software Foundation (FSF) since 1985. The FSF insists "free" means *libre* (freedom), not *gratis* (no cost): "free as in free speech, not free beer." Free software guarantees four essential freedoms: run, study, adapt, and redistribute. Richard Stallman, who founded the FSF, argues that "open source" describes a development method while "free software" describes a social and ethical stance. The FSF treats free software as a subset of open source: a piece of DRM code can be open source, because the code is public, but it is not free software, because users are restricted. The combined acronym FOSS (or FLOSS) sidesteps the argument.

## Ownership and licensing

Authors always keep copyright; the licence grants rights to everyone else. Most open-source licences fall into two families. Permissive licences (BSD, MIT, Apache) let anyone take the code, modify it, and ship the result under almost any licence, even a proprietary one. Copyleft licences (GNU GPL, MPL, EPL) allow reuse only if derivative works are distributed under the same licence. Strong copyleft, like the GPL, applies this to the whole combined work; weak copyleft applies it only to the portion that was copied.

A 2008 US ruling, *Jacobson v. Katzer*, established that open-source licence terms, including attribution, are enforceable under copyright law, a precedent that applies to almost all later licences.

Some projects require contributors to sign a Contributor License Agreement (CLA) so that a single entity controls the project's copyright and can relicense it. Such relicensed projects are sometimes described, controversially, as proprietary even though they began as OSS.

## How OSS is built

Eric S. Raymond's 1997 essay *The Cathedral and the Bazaar* contrasts two models. The cathedral model, normal in commercial software, is centralised: a defined team plans, codes, and releases. The bazaar model is decentralised: many people, including users, contribute code, fixes, bug reports, and documentation on their own initiative, with frequent integration and early public releases. Its slogan is Linus's Law: "given enough eyeballs, all bugs are shallow." A typical project runs at least two parallel releases, a stable one and a feature-rich but buggier development one, and coordinates through issue trackers, mailing lists, and version control. Today almost every project uses Git, a distributed version control system, hosted on platforms such as GitHub or GitLab.

## Why people and companies use it

OSS offers lower and shared cost, the ability to customise software, auditable code, interoperability through open standards, and independence from a single vendor. Because the code survives even if the originating company disappears, users are not locked in. Contributors gain reputation, employable skills, and the ability to shape tools they rely on. Companies contribute for similar reasons and often build a service business around a product they give away.

There are real risks. Vulnerabilities in widely reused components, such as the 2021 Log4j flaw, can ripple through thousands of products. Maintenance and funding are persistent problems, which is why governments such as Germany, through the Sovereign Tech Fund since 2022, and the United States, through the National Science Foundation's POSE programme, now directly support critical OSS infrastructure, and why large companies are increasingly setting up Open Source Program Offices to manage their dependence on it.
