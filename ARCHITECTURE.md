# Architecture

## Five-Layer MDIP Architecture

MDIP is organized as a five-layer manufacturing intelligence architecture that supports evidence capture, workflow governance, future analytics, and decision support while maintaining controlled access to implementation-sensitive logic.

1. Industrial data acquisition  
   Structured intake of production, quality, and supporting records from common industrial sources.

2. Workflow orchestration  
   Validation, staging, lifecycle progression, and review-aware operational movement of records.

3. PSPP-aligned relational governance  
   Process-Structure-Property-Performance aligned data organization with traceable entity relationships.

4. Analytics and AI-assisted reasoning  
   Planned statistical, predictive, and retrieval-augmented intelligence layers for engineering insight.

5. Industrial decision support  
   Compliance review, traceability retrieval, reporting, and evidence-backed operational decisions.

## Simplified Block Diagram

```text
+--------------------------------------------------------------+
| Layer 5: Industrial Decision Support                         |
| Reporting | Review | Traceability | Governance Actions       |
+--------------------------------------------------------------+
| Layer 4: Analytics and AI-Assisted Reasoning                 |
| SPC | Reliability | ML Prediction | RAG/SLM Intelligence     |
+--------------------------------------------------------------+
| Layer 3: PSPP-Aligned Relational Governance                  |
| Material | Batch | Process | Inspection | Documents | Audit  |
+--------------------------------------------------------------+
| Layer 2: Workflow Orchestration                              |
| Ingestion | Validation | Lifecycle | Compliance | Approval   |
+--------------------------------------------------------------+
| Layer 1: Industrial Data Acquisition                         |
| CSV/XLSX | Logs | Quality Records | Supporting Documents     |
+--------------------------------------------------------------+
```

## Data Flow

```text
Fragmented records
    -> ingestion/validation
    -> PSPP relational governance
    -> compliance/analytics/AI
    -> decision support
```

## Architectural Interpretation

The architecture is meant to convert disconnected manufacturing evidence into a governed, reviewable, and eventually intelligence-enabled operational system. The lower layers focus on reliable intake and control of industrial records. The middle governance layer links those records relationally so traceability and compliance become practical rather than manual. The upper layers support interpretation, reporting, and future decision intelligence through analytics and AI-assisted reasoning.

## Repository Boundary Note

The actual backend code for this architecture is private and is not included in this showcase repository. This document is intended to communicate the system structure and maturity at a public, reviewer-friendly level only.
