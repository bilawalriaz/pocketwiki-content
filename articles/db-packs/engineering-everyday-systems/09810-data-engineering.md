# Data engineering

Data engineering is the software engineering discipline of building the systems that collect, store, and process data so that it can be analysed or fed into machine learning. The work centres on two problems: moving data cheaply through pipelines, and storing it so the right query can reach it cheaply later. Data engineers build that infrastructure; data scientists then run analysis and machine learning on the prepared data.

## A short history

The field's parent is *information engineering methodology* (IEM), created in the 1970s and 1980s to describe database design and software-supported data analysis. The Australian Clive Finkelstein, often called the "father" of IEM, co-authored an influential Savant Institute report with James Martin. From 1983 to 1987 Charles M. Richter, working with Finkelstein, helped revamp IEM and design the IEM software product (called "user data") that automated it.

In the early 2000s, data and data tools sat with the IT team, and other departments used the results with little overlap in skills. The early 2010s changed this. The internet drove a large increase in the *volume, velocity, and variety* of data, the label *big data* entered common use, and companies such as Facebook and Airbnb started using the job title *data engineer*. Major firms including Google, Facebook, Amazon, Apple, Microsoft, and Netflix moved away from traditional *ETL* (extract, transform, load) and storage techniques and created data engineering as a branch of software engineering focused on infrastructure, warehousing, data protection, cybersecurity, mining, modelling, processing, and metadata management. The shift was especially tied to *cloud computing*, and data began to be used by sales and marketing, not only IT.

## Compute: dataflow

High-performance data processing usually relies on *dataflow programming*. A computation is written as a *directed graph* (a dataflow graph): nodes are operations, edges are the data moving between them. Popular implementations include Apache Spark and TensorFlow (the latter aimed at deep learning). More recent systems such as Differential Dataflow and Timely Dataflow apply *incremental computing*, recomputing only the parts of a result that changed, which is more efficient when inputs update continuously.

## Storage: pick the form that fits the use

Storage choice follows from how the data will be used. Engineers also cut storage and processing cost through compression, partitioning, and archiving.

| Data and workload | Typical storage | Why |
| --- | --- | --- |
| Structured data with online transaction processing (OLTP) | Databases, originally *relational* with *ACID* transaction guarantees and *SQL* queries | ACID (atomicity, consistency, isolation, durability) keeps transactions correct |
| Structured data at very large scale, OLTP | *NoSQL* or *NewSQL* databases | NoSQL drops ACID to scale horizontally across many machines; NewSQL tries to keep ACID while scaling horizontally |
| Structured data with online analytical processing (OLAP), not transactions | *Data warehouses* | Scale up analysis, mining, and AI; data typically flows in from databases |
| Mixed structured, semi-structured, unstructured, and binary data | *Data lakes* | Centralised repository, on premises or in the cloud |
| Less structured data | *File systems* (hierarchical folders), *block storage* (fixed-size chunks, matching virtual hard drives or SSDs), or *object storage* (files addressed by metadata keys such as a UUID) | Match how the data is read and written |

## Managing many moving parts

A modern organisation runs many data processes across many storage systems. To keep this tractable, engineers use a *workflow management system* such as Apache Airflow, where each task is a node and the dependencies between tasks form a *directed acyclic graph* (DAG): a graph with no cycles, so the scheduler can run tasks in order and monitor them.

## Data modeling

Data modeling produces a *data model*, an abstract description of the data and the relationships between its parts, which then guides how the systems above are built.

## The data engineer

A data engineer is a software engineer who builds the big-data ETL pipelines that move data through an organisation and turn raw volume into something analysts and models can use. They care about production concerns: formats, resilience, scaling, and security. They usually come from a software engineering background and write Java, Python, Scala, or Rust, and are more familiar with databases, architecture, cloud computing, and Agile development than typical developers. A *data scientist*, by contrast, works on analysis, algorithms, statistics, and machine learning, drawing on the prepared data and infrastructure that the data engineer provides.
