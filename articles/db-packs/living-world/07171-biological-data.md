# Biological data

Biological data is information derived from living organisms, including any compound or measurement that describes them. A vaccine or serum made from living cells counts as biological data, as does a DNA sequence, a protein structure, a microscopy image, or an entry in an electronic health record. Compared with most other data, biological data is unusually complex: a single protein can be represented as a one-dimensional amino acid sequence, a two-dimensional image, and a three-dimensional structure, and a useful record often combines several of these representations at once.

The field exists because genomics produces far more raw data than wet-lab biology can interpret by hand. Bioinformatics sits at the convergence of genomics, biotechnology, and information technology, and concentrates on storing, searching, and modelling biological information. Cheaper sequencing, larger storage, and faster processors have made it possible to manage and interpret this data, turning bioinformatics into a field that now underpins personalised and precision medicine.

## Forms and domains

Raw biological sequence data refers to DNA, RNA, and amino acids. Around that core sit several overlapping domains that extract and use the data:

- Omics, the high-throughput study of molecules in a cell, including genomics (DNA), transcriptomics and gene expression, proteomics (proteins), and metabolomics (metabolites).
- Bio-imaging and medical imaging, including neuro-imaging and brain-machine interfaces, which turn pictures of cells, tissues, or organs into measurable signals.
- Clinical and electronic health records, which link molecular measurements to individual patients.

These domains are heterogeneous. A single object such as a protein may carry sequential data (its amino acid string), geometric data (its folded shape), relational data (which other proteins it binds), and image data (a stained slide), and any analysis must reconcile all of them. The CATH database is one well-known resource built around this multi-layered view of protein structure.

## Machine learning on biological data

Because biological data is large, noisy, and high-dimensional, it became a target for data-intensive machine learning once enough compute was available.

- Deep learning (DL) uses layered neural networks that learn features directly from raw inputs. DL architectures that operate at the pixel level of microscopy images have identified mitosis in histological images of the breast and segmented nuclei in images of breast cancer cells.
- Reinforcement learning (RL) is a trial-and-error method, originally from behavioural psychology, in which an agent learns actions that maximise a reward signal. In omics, RL has predicted bacterial genomes and annotated biological sequences.

A typical pipeline starts from raw sequence data, extracts features, then runs downstream tasks such as gene-expression profiling, splicing-junction prediction, and protein-protein interaction evaluation.

## Security and privacy

Biohacking is an attack in which malicious DNA is synthesised and smuggled into a biological sample, for instance by contaminating lab coats, benches, or gloves, so that downstream sequencing pipelines execute attacker-controlled code or produce corrupted results. The same defences that block conventional code injection partially work here: comparing sequenced reads against expected reference material has been reported as up to 95% effective at detecting inserted malicious sequences.

A genome uniquely identifies a person and their blood relatives, so genomic data is personally identifying even when names are removed. Whether a sample counts as personal data, and is therefore protected under frameworks such as the European GDPR or the US HIPAA, or as physical matter outside such rules, varies by jurisdiction. The GDPR's Article 4(1) defines personal data as "any information relating to an identified or identifiable natural person", and this breadth is what makes genomic samples legally sensitive, though whether the GDPR applies to raw biological material is debated.

## Databases, errors, and sharing

Biomedical databases pool records from electronic health systems, decentralised federal genomic repositories, and large clinical studies, and now contain genomic data on millions of patients. Legal scholars have highlighted three recurring risks: the data may be incorrect or incomplete, it may carry systematic biases from researchers or from the biology itself, and it can be mined to support political, social, or economic agendas. A 2009 study in the Journal of Psychiatric Research that linked abortion to mental illness, later discredited in 2012 for serious methodological flaws, nevertheless drove several US states to pass mandatory pre-abortion counselling laws, an example of how flawed biomedical data can shape policy before it is corrected. EHR systems have also been manipulated by clinicians to inflate reported care for higher Medicare reimbursement.

Sharing biomedical data improves reproducibility and accelerates discovery, but runs into social and technical friction. A 2015 survey at the National Institutes of Health found that most clinicians and researchers regarded data sharing as important to their work yet rated their own expertise in it as low; sharing directly with other clinicians was common, but uploading data to public repositories was rare. Practical barriers include privacy laws such as HIPAA, reconciling different data formats and meanings across institutions, and meeting diverse confidentiality requirements while keeping data useful to outside researchers.

Source: adapted from "Biological data" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Biological_data
