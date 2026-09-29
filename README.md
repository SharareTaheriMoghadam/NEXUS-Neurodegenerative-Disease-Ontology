# NEXUS: Neurodegenerative Disease Knowledge Ontology

## Overview

NEXUS is an integrated ontology for representing and connecting knowledge related to neurodegenerative diseases across clinical, cognitive, biological, anatomical, temporal, artificial intelligence, explainability, clinical decision support, and patient-safety domains.

The ontology was developed to provide a structured semantic representation of neurodegenerative disease knowledge and to support interoperability between heterogeneous biomedical and computational concepts.

NEXUS is associated with the research manuscript:

> **An Integrated Semantic Framework and Ontology for Neurodegenerative Disease Knowledge: Linking Clinical, Cognitive, Biological, and Artificial Intelligence Domains**

**Authors**

- **Sharare Taheri Moghadam, PhD**
- **Md Shafiqur Rahman Jabin, PhD**

**Corresponding author:**  
Md Shafiqur Rahman Jabin  
Department of Medicine and Optometry  
Linnaeus University, Kalmar, Sweden  
Email: mdshafiqur.rahmanjabin@lnu.se

The associated manuscript is currently pre-published / under peer review.

---

## NEXUS Ontology

NEXUS integrates several major knowledge domains relevant to neurodegenerative disease research:

- Neurodegenerative diseases
- Clinical findings and symptoms
- Cognitive and behavioural concepts
- Diagnosis and clinical assessment
- Disease stages and progression
- Biomarkers
- Genes and proteins
- Brain and anatomical structures
- Imaging-related concepts
- Risk factors
- Treatment and medication concepts
- Artificial intelligence and machine learning
- Deep learning
- Predictive and classification models
- Explainability
- Feature importance
- Confidence and risk prediction
- Clinical decision support systems
- Human oversight
- Patient safety
- Temporal and disease-progression relationships

The ontology is designed as a semantic knowledge representation framework rather than as a validated clinical prediction system.

---

## BioPortal

The NEXUS ontology is available through the BioPortal ontology repository:

https://bioportal.bioontology.org/ontologies/NEXUS

The BioPortal version represents the authoritative ontology release.

This GitHub repository provides selected public-facing ontology representations, competency questions, and executable SPARQL examples for research, demonstration, and reproducibility purposes.

The GitHub repository intentionally does **not** reproduce the complete NEXUS ontology source.

---

## Repository Purpose

This repository is intended to provide a transparent research-facing representation of the NEXUS project while keeping the complete ontology implementation centralized through its authoritative ontology distribution.

The repository includes:

- A public ontology subset
- Core ontology classes and relationships
- Competency questions
- Example SPARQL queries
- Examples illustrating semantic relationships between clinical, biological, temporal, AI, explainability, and patient-safety concepts

The examples are designed to demonstrate the conceptual structure of NEXUS without reproducing the complete ontology implementation.

---

## Core Conceptual Domains

### Clinical Domain

NEXUS represents clinical concepts including:

- Neurodegenerative diseases
- Symptoms
- Clinical findings
- Diagnoses
- Clinical assessments
- Treatments
- Medications
- Laboratory findings
- Imaging findings
- Risk factors

### Biological Domain

The ontology represents biological knowledge including:

- Biomarkers
- Genes
- Proteins
- Anatomical entities
- Brain regions

Examples of represented biomarker and genetic concepts include:

- Tau protein
- Phosphorylated tau
- Alpha-synuclein
- Neurofilament light
- APOE
- LRRK2
- GBA
- MAPT

### Disease Progression

NEXUS represents temporal and progression-related concepts including:

- Disease stages
- Disease progression
- Clinical transitions
- Biomarker trajectories
- Disease timelines
- Precedes
- Follows
- Progresses-to relationships

### Artificial Intelligence

The ontology provides semantic representation for computational concepts including:

- Artificial intelligence
- Machine learning
- Deep learning
- Predictive models
- Classification models
- Recommendation engines
- Semantic reasoning
- Knowledge graphs
- Risk prediction
- Feature importance
- Explainability reports
- Confidence scores

### Clinical Decision Support and Patient Safety

NEXUS also connects computational concepts with clinical decision support and safety concepts, including:

- Clinical decision support systems
- Clinical recommendations
- Risk predictions
- Explainability
- Human oversight
- Safety constraints
- Audit trails
- Patient safety

---

## Disease Representation

The ontology includes a structured representation of neurodegenerative diseases, including:

- Alzheimer's disease
- Parkinson's disease
- Frontotemporal dementia
- Lewy body dementia
- Huntington's disease

Disease progression can be represented using stages such as:

- Preclinical
- Prodromal
- Mild
- Moderate
- Severe

The ontology also provides relationships for connecting diseases with clinical, biological, anatomical, diagnostic, and temporal concepts.

---

## Examples of Semantic Relationships

Examples of relationships represented within NEXUS include:

```text
Clinical Assessment
        |
        | assesses
        v
Disease
        |
        | associatedWith
        v
Clinical Finding
Disease
   |
   +---- associatedWith ----> Biomarker
   |
   +---- affects ------------> Anatomical Entity
   |
   +---- hasStage -----------> Disease Stage
   |
   +---- hasProgression -----> Disease Progression
Clinical Decision Support System
             |
             +---- uses ----> AI / ML / DL
             |
             +---- produces -> Risk Prediction
             |
             +---- produces -> Clinical Recommendation
             |
             +---- provides --> Explainability Report
             |
             +---- supports --> Human Oversight
             |
             +---- addresses -> Patient Safety
