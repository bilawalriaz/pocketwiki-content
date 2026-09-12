# Database

A database is an organized collection of data managed by a database management system (DBMS), software that lets users and applications store, retrieve, and update that data. The DBMS, the database itself, and the connected applications form a database system. In casual use "database" may mean any of these three; in strict use it means only the data.

Small databases fit on a file system; large ones run on computer clusters or cloud storage. Designing one means choosing a data model, picking storage structures, and deciding on query languages, security, and how to handle concurrent access and failures.

## Core operations

A DBMS provides four essential functions:

- **Data definition** — creating, modifying, and removing the structures (tables, indexes, schemas) that organize the data.
- **Updates** — inserting, modifying, and deleting individual data values.
- **Retrieval** — selecting data that matches specified criteria, usually through queries.
- **Administration** — registering users, enforcing security, monitoring performance, managing concurrent access, and recovering from corruption or crashes.

These map onto specialized language tasks: Data Definition Language (DDL), Data Manipulation Language (DML), Data Query Language (DQL), and Data Control Language (DCL). SQL is the dominant language that combines all four roles.

## The relational model

The dominant data model since the 1980s is the relational model, proposed by Edgar F. Codd at IBM in 1970. It organizes data into tables (relations) of rows (records) and columns (attributes). Each row is uniquely identified by a primary key, and relationships between tables are expressed by referencing those keys, not by physical disk addresses.

This replaced the earlier navigational databases (hierarchical and network models from the 1960s), which required applications to follow pointers from one record to another. Codd's insight was to make applications declare *what* data they wanted and let the DBMS figure out *how* to find it, using a query language grounded in mathematical logic. This separation enabled query optimization: the DBMS automatically rewriting queries into efficient execution plans.

Splitting data into multiple related tables so each fact is stored exactly once is called normalization, the practical discipline that keeps updates consistent.

A database exposes three layers: the **internal level** (physical storage), the **conceptual level** (a unified logical schema), and any number of **external levels** (custom-shaped views for different users). Changes at a lower layer, such as reorganizing storage, are invisible to higher layers, which is called data independence.

## ACID transactions

To keep data correct under concurrent use and crashes, databases group operations into transactions with four ideal properties, summarized as ACID:

- **Atomicity** — the transaction either completes entirely or has no effect.
- **Consistency** — the database moves from one valid state to another.
- **Isolation** — concurrent transactions don't interfere with each other.
- **Durability** — once committed, changes survive crashes.

These guarantees are why databases, not just files, are used for banking, reservations, and inventory: partial failures there would corrupt reality.

## Beyond relational: NoSQL and NewSQL

When applications needed to scale across many servers or store loosely structured data, the relational model's strict schemas and join operations became a bottleneck. In the 2000s, NoSQL databases emerged, collectively meaning "not only SQL." Common varieties include key-value stores (data indexed by a unique key, like a hash map), document stores (semi-structured documents, often JSON), and graph databases (nodes and edges optimized for relationship-heavy queries).

NoSQL systems typically relax some ACID guarantees for horizontal scalability, the ability to spread load across many machines. Under the CAP theorem, a distributed system can offer at most two of consistency, availability, and partition tolerance; many NoSQL systems relax consistency using eventual consistency, where replicas converge over time. NewSQL databases attempt a middle path: keeping SQL and ACID while matching NoSQL's horizontal scale.

## A brief history

Magnetic disks, available from the mid-1960s, replaced sequential tape and made shared interactive data possible. The 1960s brought navigational DBMS like IBM's IMS (hierarchical) and the CODASYL network model. Codd's 1970 relational paper sparked prototypes: IBM's System R, which produced SQL; Berkeley's INGRES; and the University of Michigan's MICRO. IBM shipped SQL/DS and Db2; Oracle, based on the System R papers, reached market in 1979. SQL became an ANSI standard in 1986 and an ISO standard in 1987.

The 1980s brought desktop databases like dBASE. The 1990s added object-oriented databases to bridge the gap between programming objects and relational tables. The 2000s saw NoSQL rise with web-scale companies, followed by NewSQL.

## What a database gives you

Compared with a filesystem, a database provides querying without writing custom code, concurrent access without corrupted writes, crash recovery without manual restoration, and security controls without separate files. The price is an extra software layer, the DBMS, between applications and storage, and the need to model data before using it. A user table, an address table, and a phone-number table, with relationships expressed by keys, illustrates the relational approach: every fact in one place, joins assembled on demand.
