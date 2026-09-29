# NEXUS Competency Questions

## Overview

Competency questions (CQs) define the knowledge requirements that the NEXUS ontology is designed to represent and query.

They provide a practical way to evaluate whether the ontology contains the concepts, relationships, and semantic structures needed to address clinically and computationally relevant questions in neurodegenerative disease research.

The NEXUS ontology includes competency questions spanning clinical presentation, diagnosis, cognition, biomarkers, anatomy, disease progression, artificial intelligence, explainability, clinical decision support, and patient safety.

The questions below provide a public-facing representation of the NEXUS competency-question framework. They are aligned with the conceptual structure of NEXUS v1.0 while avoiding reproduction of the complete ontology implementation.

---

## CQ1 — Representation of Neurodegenerative Diseases

**Question**

Which diseases are represented as neurodegenerative diseases within NEXUS?

**Purpose**

This question verifies whether NEXUS can organize specific diseases under the broader concept of neurodegenerative disease.

**Key concepts**

- `nexus:NeurodegenerativeDisease`
- `nexus:AlzheimerDisease`
- `nexus:ParkinsonDisease`
- `nexus:FrontotemporalDementia`
- `nexus:LewyBodyDementia`
- `nexus:HuntingtonDisease`

**Representative semantic structure**

```text
NeurodegenerativeDisease
│
├── AlzheimerDisease
├── ParkinsonDisease
├── FrontotemporalDementia
├── LewyBodyDementia
└── HuntingtonDisease




CQ2 — Disease-Associated Symptoms


Question


Which symptoms and clinical findings can be associated with a neurodegenerative disease?


Purpose


This question evaluates whether the ontology can connect disease concepts with their clinically observable manifestations.


Key concepts




Disease


Neurodegenerative disease


Symptom


Clinical finding




Representative relationship


Disease
   │
   └── hasSymptom ──► Symptom




CQ3 — Biomarkers of Alzheimer Disease


Question


Which biomarkers can be associated with Alzheimer disease?


Purpose


This question examines whether disease concepts can be semantically connected to relevant biological biomarkers.


Key concepts




Alzheimer disease


Biomarker


Amyloid beta


Phosphorylated tau




Representative relationships


AlzheimerDisease
      │
      ├── hasProteinBiomarker ──► AmyloidBeta
      │
      └── hasProteinBiomarker ──► PhosphorylatedTau




CQ4 — Genetic Biomarkers


Question


Which genetic biomarkers are represented within NEXUS?


Purpose


This question evaluates the representation of genetic information relevant to neurodegenerative disease research.


Representative concepts




nexus:APOE


nexus:LRRK2


nexus:GBA


nexus:MAPT




These concepts are represented within the broader biomarker and biological-entity hierarchy.



CQ5 — Anatomical Associations


Question


Which anatomical structures or brain regions can be associated with a neurodegenerative disease?


Purpose


This question evaluates whether NEXUS can connect disease knowledge with relevant anatomical structures.


Representative example


ParkinsonDisease
      │
      └── affectsBrainRegion ──► SubstantiaNigra



Key concepts




Anatomical entity


Brain region


Substantia nigra


Hippocampus


Amygdala


Basal ganglia


Cerebellum


Brainstem


Cortical regions





CQ6 — Disease Stages


Question


Which stages of disease progression can be represented in NEXUS?


Purpose


This question evaluates whether the ontology can represent the longitudinal organization of neurodegenerative disease.


Represented stages




Preclinical


Prodromal


Mild


Moderate


Severe




Representative hierarchy


DiseaseStage
│
├── PreclinicalStage
├── ProdromalStage
├── MildStage
├── ModerateStage
└── SevereStage




CQ7 — Temporal Ordering of Disease Stages


Question


How can the temporal ordering of disease stages be represented?


Purpose


This question examines whether NEXUS can represent relationships between successive stages of disease progression.


Representative relationships


PreclinicalStage
        │
        └── precedes ──► ProdromalStage
                              │
                              └── precedes ──► MildStage
                                                   │
                                                   └── precedes ──► ModerateStage
                                                                        │
                                                                        └── precedes ──► SevereStage




CQ8 — Disease Progression


Question


How can disease progression, clinical transitions, and biomarker trajectories be represented?


Purpose


This question evaluates whether NEXUS can represent disease progression as a temporal and clinically meaningful process rather than only as a static disease classification.


Key concepts




Disease progression


Clinical transition


Biomarker trajectory


Disease stage


Biomarker




Representative conceptual structure


Disease
   │
   └── hasProgression ──► DiseaseProgression
                              │
                              ├── hasStartingStage ──► DiseaseStage
                              │
                              └── hasEndingStage ────► DiseaseStage




CQ9 — Clinical Assessment and Diagnosis


Question


How can clinical assessments be connected with diseases and diagnostic information?


Purpose


This question evaluates whether NEXUS can represent the relationship between clinical assessment, disease evaluation, and diagnosis.


Key concepts




Clinical assessment


Disease


Diagnosis


Differential diagnosis




Representative relationships


ClinicalAssessment
      │
      ├── assessesDisease ──► Disease
      │
      └── resultsInDiagnosis ──► Diagnosis
                                      │
                                      └── diagnosesDisease ──► Disease




CQ10 — Cognitive Assessment


Question


Which cognitive functions can be represented and assessed within NEXUS?


Purpose


This question evaluates the representation of cognitive dimensions that are relevant to neurodegenerative disease.


Representative concepts




Memory function


Attention function


Executive function


Language function


Visuospatial function




Representative relationship


ClinicalAssessment
      │
      └── assessesCognitiveFunction ──► CognitiveFunction




CQ11 — AI-Based Prediction


Question


Which types of artificial intelligence models can be represented for disease-related prediction?


Purpose


This question evaluates the representation of computational models used for predictive and analytical tasks.


Key concepts




AI model


Predictive model


Classification model


Prediction


Risk prediction




Representative structure


AIModel
   │
   ├── PredictiveModel
   │
   └── ClassificationModel




CQ12 — Knowledge-Graph-Based AI


Question


Which AI models can use knowledge graphs as part of their computational or semantic representation?


Purpose


This question evaluates the connection between AI models and structured biomedical knowledge.


Representative relationship


AIModel
   │
   └── usesKnowledgeGraph ──► KnowledgeGraph




CQ13 — Explainability of AI Outputs


Question


What explanatory information can accompany an AI-generated model output?


Purpose


This question evaluates whether NEXUS can represent explainability information associated with computational outputs.


Key concepts




Model output


Explainability report


Feature importance


Confidence score


Model interpretation




Representative structure


ModelOutput
      │
      ├── hasExplanation ──► ExplainabilityReport
      │
      ├── hasFeatureImportance ──► FeatureImportance
      │
      └── hasConfidenceScore ──► ConfidenceScore




CQ14 — Clinical Recommendations


Question


How can a clinical decision-support system provide a clinical recommendation?


Purpose


This question evaluates the semantic connection between computational decision support and clinical recommendations.


Representative relationship


ClinicalDecisionSupportSystem
      │
      └── providesClinicalRecommendation
                    │
                    ▼
          ClinicalRecommendation




CQ15 — Risk Prediction in Clinical Decision Support


Question


How can a clinical decision-support system provide a risk prediction?


Purpose


This question evaluates whether predictive outputs can be explicitly represented as part of a clinical decision-support process.


Representative relationship


ClinicalDecisionSupportSystem
      │
      └── providesRiskPrediction
                    │
                    ▼
              RiskPrediction




CQ16 — Safety Constraints


Question


Which safety constraints can be associated with or applied to a clinical recommendation?


Purpose


This question addresses the representation of safety-related constraints within AI-enabled clinical decision support.


Representative relationship


SafetyConstraint
      │
      └── constrainsRecommendation
                    │
                    ▼
          ClinicalRecommendation




CQ17 — Human Oversight


Question


How can human oversight be represented within an AI-enabled clinical decision-support process?


Purpose


This question evaluates whether NEXUS can explicitly represent human involvement in AI-supported clinical decision making.


Key concepts




Clinical decision-support system


Human oversight


Clinical recommendation


AI model




Representative relationship


ClinicalDecisionSupportSystem
      │
      └── hasHumanOversight ──► HumanOversight




CQ18 — Auditability


Question


Which information generated during clinical decision support can be represented in an audit trail?


Purpose


This question evaluates the representation of traceability and auditability.


Representative concepts




Audit trail


Clinical recommendation


Model output


CDSS output




Representative relationships


ClinicalDecisionSupportSystem
      │
      └── hasAuditTrail ──► AuditTrail
                                │
                                ├── recordsRecommendation
                                │
                                └── recordsModelOutput




CQ19 — Evidence and Provenance


Question


What evidence or provenance information can support a clinical recommendation?


Purpose


This question addresses the semantic representation of supporting evidence and provenance associated with clinical knowledge and recommendations.


Relevant concepts




Evidence


Knowledge source


Provenance


Clinical recommendation




This competency question provides a foundation for future extensions involving evidence provenance and traceable knowledge sources.



CQ20 — AI Contribution to Clinical Recommendations


Question


Which AI model or model output contributed to a clinical recommendation?


Purpose


This question evaluates whether computational contributions can be connected to downstream clinical recommendations.


Representative conceptual pathway


AIModel
   │
   └── generatesClinicalPrediction
                │
                ▼
          ModelOutput
                │
                ▼
    ClinicalRecommendation



This type of relationship supports traceability between computational processing and clinical decision-support outputs.



CQ21 — Clinical Risk


Question


Which clinical risks can be addressed by a clinical recommendation?


Purpose


This question evaluates whether recommendations can be connected to the clinical risks they are intended to address.


Representative relationship


ClinicalRecommendation
      │
      └── addressesClinicalRisk
                    │
                    ▼
              ClinicalRisk




CQ22 — Multimodal Clinical Information


Question


Which types of clinical and biological information can be integrated by an AI model?


Purpose


This question evaluates the ability to represent heterogeneous information sources that may contribute to computational analysis.


Potential information domains




Clinical information


Clinical findings


Biomarkers


Genetic information


Imaging findings


Cognitive assessments


Anatomical information




Representative conceptual pathway


Clinical Information ──┐
Biomarkers ────────────┤
Genetic Information ───┤
Imaging Information ───┼──► AI Model
Cognitive Information ─┤
Anatomical Information ┘




CQ23 — Clinical Case Representation


Question


How can a clinical case be represented in terms of disease, disease stage, and clinical course?


Purpose


This question evaluates whether NEXUS can support structured representation of patient-level or case-level clinical knowledge.


Relevant concepts




Clinical case


Disease


Disease stage


Disease course


Clinical finding


Clinical assessment




This competency question is particularly relevant to future integration with longitudinal clinical datasets.



CQ24 — Biomarker-Aware AI


Question


How can disease-associated biomarkers be connected to an AI model and its output?


Purpose


This question evaluates the semantic pathway from biological information to computational analysis and resulting model output.


Representative conceptual pathway


Biomarker
    │
    ▼
Model Input
    │
    ▼
AI Model
    │
    ▼
Model Output



This structure can support future integration of biomarker-driven machine-learning and knowledge-graph workflows.



CQ25 — Traceable AI-Supported Clinical Decision Making


Question


Can an AI-supported clinical decision be represented as a traceable chain from computational model to clinical recommendation, human oversight, and audit information?


Purpose


This question brings together several major NEXUS domains: artificial intelligence, explainability, clinical decision support, human oversight, and patient safety.


Representative semantic pathway


AI Model
   │
   ▼
Model Output
   │
   ▼
Explainability Report
   │
   ▼
Clinical Recommendation
   │
   ▼
Human Oversight
   │
   ▼
Audit Trail



This competency question represents one of the broader architectural goals of NEXUS: connecting computational outputs with interpretable and traceable clinical decision-support concepts.



Competency Questions and SPARQL


Selected competency questions are demonstrated through SPARQL queries provided in the sparql/ directory.


The current public examples include queries addressing:




neurodegenerative disease classification;


disease-associated biomarkers;


anatomical associations;


disease-stage progression;


AI and explainability concepts;


clinical decision-support and safety relationships.




The SPARQL examples are designed to demonstrate how NEXUS concepts and relationships can be queried using semantic-web technologies.



Scope of the Public Competency-Question Set


The competency questions presented here are intended to document the semantic requirements addressed by NEXUS without reproducing the complete ontology implementation.


The complete NEXUS ontology contains additional classes, properties, restrictions, axioms, annotations, and semantic relationships.


The authoritative ontology release is available through BioPortal:


https://bioportal.bioontology.org/ontologies/NEXUS



Scientific Interpretation


Competency questions describe what an ontology is designed to represent and query. They should not be interpreted as evidence of clinical validation or predictive performance.


NEXUS provides a semantic and knowledge-representation foundation for neurodegenerative disease research. Clinical prediction, diagnosis, treatment recommendation, and patient-outcome performance would require separate empirical validation using appropriate datasets, clinical evaluation, and prospective or retrospective studies.
