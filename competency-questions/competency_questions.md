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
CQ3 — Alzheimer disease biomarkers
Question
Which biomarkers are associated with Alzheimer disease?
Relevant concepts
Alzheimer disease
Biomarker
Amyloid beta
Phosphorylated tau
Core relationship
AlzheimerDisease
        |
        +---- hasProteinBiomarker ----> AmyloidBeta
        |
        +---- hasProteinBiomarker ----> PhosphorylatedTau
CQ4 — Genetic biomarkers
Question
Which genetic biomarkers are represented in NEXUS?
Examples include:
APOE
LRRK2
GBA
MAPT
CQ5 — Brain regions and Parkinson disease
Question
Which brain regions are associated with Parkinson disease?
A representative NEXUS relationship is:
ParkinsonDisease
        |
        +---- affectsBrainRegion ----> SubstantiaNigra
CQ6 — Disease stages
Question
Which disease stages are represented?
The public subset includes:
Preclinical
Prodromal
Mild
Moderate
Severe
CQ7 — Temporal ordering
Question
Which disease stages precede another disease stage?
Representative relationships include:
Preclinical → precedes → Prodromal
Prodromal → precedes → Mild
Mild → precedes → Moderate
Moderate → precedes → Severe
CQ8 — Disease progression
Question
How can disease progression and biomarker trajectories be represented?
Relevant concepts include:
Disease progression
Clinical transition
Biomarker trajectory
Disease stage
Biomarker
CQ9 — Clinical assessment
Question
Which clinical assessments can support disease assessment and diagnosis?
Relevant concepts include:
Clinical assessment
Disease
Diagnosis
Cognitive function
CQ10 — Cognitive assessment
Question
Which cognitive functions can be represented or assessed?
Examples include:
Memory
Attention
Executive function
Language
Visuospatial function
CQ11 — AI prediction
Question
Which AI models can represent disease-related prediction?
Relevant concepts include:
AI model
Predictive model
Prediction
Risk prediction
CQ12 — Knowledge-graph-based AI
Question
Which AI models use knowledge graphs?
Core relationship:
AIModel → usesKnowledgeGraph → KnowledgeGraph
CQ13 — Explainability
Question
What explainability information can accompany an AI model output?
Relevant concepts include:
Model output
Explainability report
Feature importance
Confidence score
Model interpretation
CQ14 — Clinical recommendations
Question
Which clinical recommendations can be provided by a clinical decision-support system?
Core relationship:
ClinicalDecisionSupportSystem
        |
        +---- providesClinicalRecommendation
                         |
                         v
              ClinicalRecommendation
CQ15 — Risk prediction
Question
Which risk predictions can be provided by a clinical decision-support system?
Core relationship:
ClinicalDecisionSupportSystem
        |
        +---- providesRiskPrediction
                         |
                         v
                   RiskPrediction
CQ16 — Safety constraints
Question
Which safety constraints apply to a clinical recommendation?
Core relationship:
SafetyConstraint
        |
        +---- constrainsRecommendation
                         |
                         v
              ClinicalRecommendation
CQ17 — Human oversight
Question
Which recommendations can receive human oversight?
Core concepts:
Clinical decision-support system
Human oversight
Clinical recommendation
CQ18 — Auditability
Question
Which information can be recorded in an audit trail?
Examples include:
Clinical recommendations
Model outputs
Decision-support outputs
CQ19 — Evidence
Question
What evidence can support a clinical recommendation?
Relevant concepts include:
Evidence
Clinical recommendation
Knowledge source
Provenance
CQ20 — AI contribution to recommendations
Question
Which AI model generated information contributing to a clinical recommendation?
Relevant concepts include:
AI model
Model output
Clinical recommendation
Clinical decision-support system
CQ21 — Clinical risk
Question
Which clinical risks are addressed by a recommendation?
Core relationship:
ClinicalRecommendation
        |
        +---- addressesClinicalRisk
                         |
                         v
                   ClinicalRisk
CQ22 — Multimodal AI
Question
Which information modalities can be integrated by an AI model?
Potential modalities include:
Clinical information
Biomarkers
Imaging findings
Cognitive assessments
Genetic biomarkers
CQ23 — Clinical case
Question
What disease and disease stage are represented in a clinical case?
Relevant concepts include:
Clinical case
Disease
Disease stage
Disease course
CQ24 — Biomarker-aware AI
Question
Which AI models use disease-associated biomarkers?
Core conceptual pathway:
Biomarker
     ↓
Model Input
     ↓
AI Model
     ↓
Model Output
CQ25 — Traceable AI output
Question
Can an AI-generated output be traced through explainability, human oversight, and audit information?
A representative semantic pathway is:
AI Model
   ↓
Model Output
   ↓
Explainability Report
   ↓
Clinical Recommendation
   ↓
Human Oversight
   ↓
Audit Trail
