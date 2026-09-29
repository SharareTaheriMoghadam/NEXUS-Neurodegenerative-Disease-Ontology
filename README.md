# NEXUS: Neurodegenerative Disease Knowledge Ontology

## An Integrated Semantic Framework for Neurodegenerative Disease Knowledge

NEXUS is an ontology-oriented semantic framework developed to represent and connect heterogeneous knowledge related to neurodegenerative diseases.

The ontology brings together concepts from clinical medicine, cognitive function, disease characteristics, biological knowledge, brain anatomy, biomarkers, disease progression, artificial intelligence, explainability, clinical decision support, and patient safety within a common semantic structure.

The project was developed using ontology engineering principles and Protégé and is formally represented as a machine-readable ontology.

---

## Ontology

**Name:** NEXUS  
**Version:** 1.0  
**Domain:** Neurodegenerative disease knowledge representation  
**Development environment:** Protégé / OWL  
**Ontology repository:** BioPortal

### Official BioPortal record

The formal ontology is available through BioPortal:

https://bioportal.bioontology.org/ontologies/NEXUS

The complete ontology artifact is maintained through the formal ontology distribution rather than reproduced in this GitHub repository.

This repository provides selected public examples, competency questions, SPARQL queries, documentation, and demonstrations of the semantic structure.

---

## Scope

NEXUS was designed to provide an integrated semantic representation of heterogeneous neurodegenerative disease knowledge.

The ontology connects concepts across several major domains:

- Neurodegenerative diseases
- Clinical findings
- Symptoms
- Diagnosis
- Clinical assessment
- Cognitive functions
- Brain anatomy
- Biomarkers
- Genes
- Proteins
- Neuroimaging
- Disease stages
- Disease progression
- Clinical transitions
- Treatment
- Medication
- Artificial intelligence
- Machine learning
- Deep learning
- Predictive models
- Classification models
- Knowledge graphs
- Semantic reasoning
- Explainability
- Feature importance
- Risk prediction
- Clinical decision support
- Human oversight
- Patient safety
- Safety constraints
- Audit trails
- Confidence and transparency

The purpose is to provide a common semantic layer through which these heterogeneous concepts can be represented and related.

---

## Conceptual Motivation

Neurodegenerative disease information is distributed across multiple clinical, cognitive, biological, imaging, genetic, computational, and research resources.

Existing ontology and knowledge-representation approaches often focus on individual diseases, datasets, experimental paradigms, or particular biomedical domains.

NEXUS was developed as a broader semantic structure for connecting complementary concepts across these domains.

The ontology is therefore intended primarily as a knowledge-representation and interoperability foundation.

It is not itself a predictive clinical model.

---

## Major Semantic Domains

A simplified view of the NEXUS conceptual structure is:

```text
NEXUS
│
├── Clinical Domain
│   ├── Disease
│   ├── Symptom
│   ├── Clinical Finding
│   ├── Diagnosis
│   ├── Clinical Assessment
│   ├── Treatment
│   └── Medication
│
├── Cognitive Domain
│   ├── Cognitive Function
│   ├── Memory
│   ├── Attention
│   ├── Executive Function
│   └── Behavioural Function
│
├── Biological Domain
│   ├── Biomarker
│   ├── Protein
│   ├── Gene
│   └── Biological Process
│
├── Anatomical Domain
│   ├── Nervous System
│   ├── Brain Region
│   └── Specific Anatomical Structures
│
├── Temporal Domain
│   ├── Disease Stage
│   ├── Disease Progression
│   ├── Clinical Transition
│   └── Biomarker Trajectory
│
├── Artificial Intelligence Domain
│   ├── Artificial Intelligence
│   ├── Machine Learning
│   ├── Deep Learning
│   ├── Predictive Model
│   ├── Classification Model
│   ├── Knowledge Graph
│   └── Semantic Reasoner
│
├── Explainability Domain
│   ├── Explainability
│   ├── Feature Importance
│   ├── Explainability Report
│   └── Confidence Score
│
├── Clinical Decision Support
│   ├── CDSS
│   ├── Recommendation
│   └── Risk Prediction
│
└── Patient Safety
    ├── Patient Safety
    ├── Clinical Risk
    ├── Adverse Event
    ├── Near Miss
    ├── Safety Constraint
    ├── Human Oversight
    └── Audit Trail
