# AADAG Traceability

This file connects each major AADAG concept to the version where it entered development, its current status, and the repository location that defines or tracks it.

| Concept | Version | Status | Authoritative source | Tracking |
|---|---|---|---|---|
| Decision-centered governance thesis | v0.1 | Established foundation | README.md, FRAMEWORK.md, PRINCIPLES.md | v0.1 release history |
| Seven core governance questions | v0.1 foundation; v0.2 terminology refinement | Established foundation with Basis and Human Authority terminology aligned to the Decision Inventory | FRAMEWORK.md | v0.1 release history, v0.2 consistency audit |
| AADAG Decision Path: Decision → Consequence → Influence → Human Authority | v0.2 formalization of v0.1 core questions | Working model, end-to-end tested | README.md, TESTING.md | v0.2 development |
| NIST AI RMF 1.0 alignment | v0.2 | Initial alignment documented; detailed crosswalk and use case planned | README.md | ROADMAP.md Incubator |
| Three working assessment dimensions | v0.1 | Established foundation, refinement continues | FRAMEWORK.md | ROADMAP.md |
| Decision consequence scale | v0.2 | Level definitions, assignment rules, practical examples, and known limitations established as current working model | FRAMEWORK.md | Issue #1, ROADMAP.md |
| CU: Undetermined | v0.2 | Working level | FRAMEWORK.md | Issue #1 |
| C0: Negligible | v0.2 | Working level | FRAMEWORK.md | Issue #1 |
| C1: Limited | v0.2 | Working level | FRAMEWORK.md | Issue #1 |
| C2: Moderate | v0.2 | Working level | FRAMEWORK.md | Issue #1 |
| C3: Significant | v0.2 | Working level | FRAMEWORK.md | Issue #1 |
| C4: Critical | v0.2 | Working level | FRAMEWORK.md | Issue #1 |
| AI influence levels: Inform, Recommend, Presume, Decide | v0.1 concept; v0.2 refinement | Definitions and boundaries established as current working model | FRAMEWORK.md | Issue #3, ROADMAP.md |
| Delegation | v0.2 | Incorporated as an accountability mechanism, not a separate scoring dimension | FRAMEWORK.md | Issue #2, ROADMAP.md |
| Decision inventory | v0.2 | Nine-field template established and end-to-end tested across Inform, Recommend, Presume, Decide, failure reconstruction, and incomplete-information scenarios | FRAMEWORK.md | TESTING.md, ROADMAP.md |
| Safeguard mapping | v0.3.0 | Incorporated in the development release; consequence-rigor and AI Influence application guidance established; independent field validation outstanding | FRAMEWORK.md §3 | TESTING.md, ROADMAP.md |
| Five safeguard families: Decision Support, AI Assurance, Human Control, Decision Record, Operating Boundaries | v0.3.0 | Incorporated as five safeguard concerns; organization-specific implementations remain contextual | FRAMEWORK.md §3 | TESTING.md |
| Safeguard proportionality: consequence drives rigor; Influence changes form and emphasis | v0.3.0 | Incorporated as the central mapping rule | FRAMEWORK.md §3 | TESTING.md |
| Practical exercisability of Human Authority | v0.3.0 | Incorporated; human authority must be exercisable within the relevant decision window when retained | FRAMEWORK.md §3 | TESTING.md |
| Influence reflects actual operating authority | v0.3.0 | Incorporated into influence application: nominal review or override does not substitute for meaningful exercisable authority | FRAMEWORK.md §3 | TESTING.md |
| STOP for an unauthorized affected decision path | v0.3.0 | Incorporated as a path-level governance outcome when no authorized alternate path permits proceeding; not a sixth safeguard or blanket system shutdown | FRAMEWORK.md §3 | TESTING.md |
| Safeguard strength scale 0–4 | v0.3 | Exploratory implementation mechanism; labels and individual assignments not established | Not yet normative | TESTING.md |
| Field testing | v0.4 planned | Planned | ROADMAP.md | ROADMAP.md |
| Complete usable release | v1.0 planned | Planned | ROADMAP.md | ROADMAP.md |

## Current consequence scale

The consequence scale must remain identical anywhere it appears:

- **CU: Undetermined**
- **C0: Negligible**
- **C1: Limited**
- **C2: Moderate**
- **C3: Significant**
- **C4: Critical**

FRAMEWORK.md is the authoritative source for the definitions of these levels. README.md may summarize the scale but should not introduce alternate definitions.

## Version status

- **v0.1 Foundation:** published 2026-09-02
- **v0.2 Decision Classification:** published 2026-09-22
- **v0.3.0 Safeguard Mapping:** development release published 2026-10-08; not independently field-validated
- **v0.4 Field Testing:** planned
- **v1.0 Usable Release:** planned

## Traceability rule

A concept should not be described as complete in the roadmap while its tracking issue still lists required work as unfinished. Experimental concepts should remain clearly marked as exploratory until they are formally incorporated into FRAMEWORK.md as part of the assessment model.

## v0.3 release boundary

The framework owner incorporated the five safeguard families, consequence-based rigor, influence-specific application, meaningful human review, override/recourse, and path-level STOP guidance into FRAMEWORK.md for the v0.3.0 development release. FRAMEWORK.md is authoritative for the current model; TESTING.md remains the exploratory development evidence, not independent operational validation. Organization-specific acceptance criteria, authority assignments, and field validation remain outstanding. Concepts not incorporated in FRAMEWORK.md, including a numeric safeguard strength scale, remain exploratory.
