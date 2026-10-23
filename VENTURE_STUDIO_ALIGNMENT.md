# IndusDatum | IIT Madras Venture Studio — Research and Pilot Alignment

**Project:** Manufacturing Data Intelligence Platform (MDIP)  
**Initial application:** MDIP-SR — Scrap Reduction  
**Target segment:** Indian Tier-2 and Tier-3 automotive-component manufacturing MSMEs  
**Document status:** Public research-alignment note | October 2026

> **Institutional status:** This document explains a *proposed* research and venture alignment with the Wadhwani School of Data Science and AI (WSAI), IIT Madras. It does not imply an existing IIT Madras collaboration, faculty commitment, access to institutional datasets, endorsement, or an agreed industrial pilot.

## 1. Industrial problem and focused application

In smaller automotive-component manufacturing facilities, material-lot information, production logs, process conditions, inspection results, and scrap/rework records may reside in spreadsheets, machine exports, paper records, or disconnected enterprise systems. Quality Engineers must often reconstruct a rejected batch's history before they can investigate contributing factors. This can delay corrective action and make earlier identification of quality risk difficult.

**IndusDatum's proposed initial user** is the **Quality Engineer**, with Quality Managers and Production/Process Engineers as supporting users. The intended economic buyer is the factory owner, Managing Director, or an authorized Plant Head, subject to customer discovery.

MDIP-SR is intended to help these teams move from fragmented records and retrospective rejection analysis toward **traceable, stage-specific scrap-risk assessment**. It is designed to complement existing ERP, MES, and QMS systems rather than assume their replacement.

## 2. What exists today, and what remains proposed

| Layer | Current evidence / status | Next validation requirement |
| --- | --- | --- |
| **MDIP data foundation** | Private Python/FastAPI, PostgreSQL, and SQLAlchemy backend with CSV/XLSX ingestion, validation, relational traceability, controlled access, audit, and workflow foundations; public architecture documentation is available here. | Test data onboarding and operational suitability with a manufacturing partner. |
| **MDIP-SR application** | Early workflows and testing with **controlled synthetic manufacturing data** for batches, inspections, defects, dispositions, and quality indicators. | Acquire representative industrial records and establish an actionable scrap-risk use case. |
| **Predictive ML** | Statistical and ML techniques have been explored in the preceding FDIP research; **no production-grade MDIP-SR scrap-risk model has been trained or validated**. | Develop and compare rule-based/statistical baselines with interpretable ML using real, appropriately labelled manufacturing data. |
| **Public demonstrations** | Streamlit interfaces illustrate research and platform concepts. | Verify operational requirements, data connections, engineering usefulness, and production deployment separately. |

The existing backend implementation is **not** published in this showcase repository. Private source access, if appropriate, is considered only through a controlled technical-review process.

## 3. Specific IIT Madras / WSAI research alignment

### A. Walmart Centre for Tech Excellence — manufacturing MSME adoption

The [Walmart Centre for Tech Excellence](https://wsai.iitm.ac.in/research/walmart-centre-for-tech-excellence/) focuses on enabling MSME adoption of AI and IoT. Its emphasis on practical, accessible technologies matches IndusDatum's intended deployment environment, where firms may not have a fully integrated industrial data stack.

IIT Madras also announced a [29 July 2026 collaboration with FaMe TN](https://www.iitm.ac.in/ta/node/17945) to support AI-led digital transformation among Tamil Nadu MSMEs, including automotive, engineering, and fabrication manufacturers. **IndusDatum is not a participant in that agreement.** The initiative is cited here as relevant institutional context for a proposed MSME-focused use case.

**Potential interaction:** Explore mentorship on manufacturing use-case selection, MSME digital readiness, practical data onboarding, and pilot design.

### B. Robert Bosch Centre for Data Science and AI (RBCDSAI) — manufacturing analytics

[The Robert Bosch Centre for Data Science and AI](https://wsai.iitm.ac.in/research/rbcdsai/) identifies manufacturing analytics among its research activities. The [research interests of Prof. Raghunathan Rengaswamy](https://wsai.iitm.ac.in/faculty-and-management/raghunathan-rengaswamy/), including fault detection and diagnosis, are relevant to the proposed treatment of process deviations and quality outcomes. These are **research connections of interest**, not confirmed individual supervision or collaboration.

**Potential research problem:** Can engineering-informed, traceability-linked features derived from incomplete and heterogeneous factory records support a useful scrap-risk warning *before* the relevant downstream quality outcome?

**Proposed methods:** Begin with specification checks, conventional statistical monitoring, and logistic-regression baselines; evaluate suitable tree-based models only where data sufficiency permits. Use chronological validation, class-imbalance assessment, calibration, and human engineering review. Do not infer confirmed physical root cause from predictive associations alone.

### C. Centre for Responsible AI (CeRAI) — trustworthy decision support

The [Centre for Responsible AI (CeRAI)](https://wsai.iitm.ac.in/research/cerai/) provides complementary alignment around explainability, accountability, and responsible deployment. For MDIP-SR, the practical requirements are traceable prediction inputs, reviewable risk indicators, uncertainty disclosure, and preservation of authorized engineering decisions.

## 4. Proposed bounded industrial pilot

A feasible first pilot would focus on **one automotive-component manufacturer, one component family or production process, and one recurrent rejection/scrap category**:

1. **Agree on the problem and data rights:** Confirm the quality event, participating engineering roles, historical data access, confidentiality, ownership, and permitted uses.
2. **Build reliable genealogy:** Import available material, production, process, inspection, and disposition records; measure mapping quality and identify unavailable or ambiguous links.
3. **Validate engineering outcomes:** Review defect labels and scrap/rework classifications with plant engineers. Use only information available at the intended prediction stage to avoid data leakage.
4. **Establish baselines before advanced ML:** Compare specification rules, statistical quality-monitoring methods, and any subsequently trained ML approaches against later, unseen production outcomes.
5. **Evaluate operational value:** Assess traceability completeness, warning lead time, false-alert burden, engineering review effort, and scrap/rework cost where records permit. Quantified savings must be based on real pilot evidence, not synthetic estimates.

If historical records are insufficient for reliable prediction, the pilot should first demonstrate data quality, traceability, and retrospective quality analysis rather than force an unsupported ML result.

## 5. Potential research outputs and IP boundaries

Possible outputs include process-aware data mappings, validated defect taxonomies, engineering-specific feature-generation methods, model-evaluation protocols, and software improvements that could reduce onboarding effort across future deployments.

These are **proposed outputs**, not existing patents or an established competitive moat. Background technology and any jointly created research IP would require written terms governing ownership, licensing, publication, confidentiality, and commercial use. Customer manufacturing records would remain subject to the customer's contractual rights; cross-customer data pooling or model reuse would require explicit permission.

## 6. What IndusDatum contributes and seeks

**Existing contribution:** Materials-engineering and fatigue-reliability research; a peer-reviewed data-infrastructure publication; a public reproducibility repository; a private MDIP backend with a public architecture showcase; and early synthetic-data MDIP-SR work.

**Proposed Venture Studio benefit:** Specialist AI/ML mentorship, interdisciplinary research feedback, guidance on engineering-valid model assessment, MSME customer discovery, pilot design, and responsible commercialization. No specialist co-founder, industry pilot agreement, or IIT Madras research partnership is currently committed.

## 7. Evidence and demonstrations

- **MDIP public architecture showcase:** https://github.com/sreearravind/MDIP-Research-Showcase
- **MDIP Streamlit prototype demonstration:** https://mdipv10-fhp7vphy3y29eoypp8papppp.streamlit.app/
- **FDIP Streamlit research demonstration:** https://fatiguedbms-feo394nhh75ex5cfn6ua4t.streamlit.app/
- **FDIP dashboard source:** https://github.com/sreearravind/fatigue_DBMS
- **Published research / DOI:** [*Fatigue Data Infrastructure for Reliability Analytics: A Relational Database Framework for Traceable Fatigue Knowledge Integration*](https://doi.org/10.1007/s11665-026-14593-5), *Journal of Materials Engineering and Performance* (2026)
- **Research reproducibility repository:** https://github.com/sreearravind/Fatigue-Data-Infrastructure-for-Reliability-Analytics

**External engagement:** FDIP reached the final evaluation stage of the TCS–SASTRA Prototype-to-Go-to-Market initiative (not selected). MDIP-SR was shortlisted for the NASSCOM Future Forge Applied Research Bridge in response to AUMOVIO's automotive scrap-reduction challenge, followed by an industry discussion on 7 August 2026. Neither engagement represents a signed pilot, product endorsement, customer contract, or measured scrap-reduction result.

---

**Public disclosure note:** This document communicates research alignment, present development maturity, and proposed validation steps. It deliberately excludes private backend code, confidential data, credentials, and implementation-sensitive assets.
