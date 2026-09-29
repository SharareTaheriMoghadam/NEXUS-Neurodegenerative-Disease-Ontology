# NEXUS Competency Questions

NEXUS was designed around competency questions that identify the types of knowledge the ontology should be able to represent and query.

The complete NEXUS v1.0 ontology contains 25 competency questions. The questions below provide a public-facing selection corresponding to the ontology architecture.

---

## CQ1 — Neurodegenerative diseases

**Question**

Which diseases are classified as neurodegenerative diseases?

**Relevant concepts**

- `nexus:NeurodegenerativeDisease`
- `nexus:AlzheimerDisease`
- `nexus:ParkinsonDisease`
- `nexus:FrontotemporalDementia`
- `nexus:LewyBodyDementia`
- `nexus:HuntingtonDisease`

**Example query**

`../sparql/diseases_and_symptoms.rq`

---

## CQ2 — Disease symptoms

**Question**

Which symptoms are associated with a neurodegenerative disease?

**Relevant concepts**

- Disease
- Neurodegenerative disease
- Symptom
- Clinical finding

**Core relationship**

```text
Disease → hasSymptom → Symptom
