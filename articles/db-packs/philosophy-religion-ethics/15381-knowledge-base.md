# Knowledge base

A knowledge base (KB) is a store of sentences written in a formal knowledge representation language, with interfaces for adding new sentences and for querying what is known. Those interfaces can use inference, so a program can derive facts that were never written down explicitly. The phrase first named one half of an expert system: facts about the world paired with a reasoning component that draws conclusions or flags inconsistencies.

## Why the term was needed

In the 1970s, "database" meant something specific: flat tables of strings and numbers, shared by many users, protected by transactions (the ACID properties: Atomicity, Consistency, Isolation, Durability), and built to hold huge, long-lived corporate data for years. A knowledge base was designed around different needs.

Early expert systems stored structured data as a web of objects pointing to other objects, organised as an ontology of classes, subclasses, and instances. They served one user reaching one answer at a time, such as a medical diagnosis, a molecule design, or an emergency response, and did not need transactions or years of persisted rows. Volume worked the other way too: representing general rules like "All humans are mortal" is the work of a knowledge base, while listing thousands of individual people with their ages and addresses is the work of a database. Feigenbaum's 1983 framing puts it plainly: a patient's record is a database; what was learned in medical school, the facts, predicates, and beliefs, is the knowledge base.

The split held only as long as expert systems stayed small and single-user. As they moved into corporate settings, they inherited the database concerns they had skipped: concurrent users, transactions, and persistence.

## How the two traditions converged

Two markets pushed KB and database features into the same product. From the AI and object-oriented communities, object-oriented databases such as Versant were built from scratch to support object semantics plus standard database services. From the established database world, vendors like Oracle added knowledge-base features such as class-subclass relations and rules into their existing systems. A clean separation no longer existed in practice.

## Documents, the Internet, and knowledge management

The Internet made hypertext and multimedia essential, and Web Content Management emerged to handle persistent, transactional document stores for corporate sites. Around the same time, knowledge management products (notably HCL Notes, formerly Lotus Notes) adopted "knowledge base" for human-facing repositories of manuals, procedures, policies, best practices, and reusable designs. The word now covered two ill-defined things: automated reasoning over formal sentences, and human reading of documents. Most real systems ended up doing some of both.

## Internal and external knowledge bases

Modern knowledge bases split by audience. Internal ones act like a corporate wiki for employees: onboarding, internal policies, and quick answers to staff questions. External ones face customers, prospects, or the public, and exist mainly to reduce support load and surface effective tips.

## Examples

Public, large-scale knowledge bases include Cyc, ConceptNet, DBpedia, YAGO, Wikidata, and Freebase, ranging from curated commonsense rules to structured extractions from web data.
