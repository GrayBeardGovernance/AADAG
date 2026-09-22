# Changelog

All notable changes to AADAG will be documented here.

## Unreleased

### Added

- Began development of v0.2 Decision Classification
- Added decision consequence levels: CU Undetermined, C0 Negligible, C1 Limited, C2 Moderate, C3 Significant, and C4 Critical
- Added guidance for documenting undetermined consequences
- Added nature, scope, duration, and reversibility as considerations when assessing decision consequence
- Added the consequence assignment rule based on the highest credible consequence to affected parties
- Added decision-type granularity guidance and an affected-party assessment sequence
- Added practical examples for C0 through C4
- Added known limitations for the consequence model
- Clarified that consequence classification is performed without relying on safeguards intended to control the consequence
- Added delegation as an accountability mechanism that identifies who authorized AI's defined level of influence over a decision
- Added a governance rule requiring the authority granting or changing AI influence to be identifiable and documented
- Added decision owner, authorized AI influence, and authorizing authority as accountability fields for the decision inventory
- Added the nine-field decision inventory template: Decision, Affected Parties, Consequence, AI Influence, Human Authority, Decision Owner, Authorizing Authority, Basis, and Review / Recourse
- Added Basis as the field for information, criteria, need, or reasoning supporting the decision
- Pressure-tested the decision inventory across C1 Recommend, C2 Recommend, C3 Presume, and C4 Decide scenarios
- Added TRACEABILITY.md to map concepts, versions, status, authoritative sources, and tracking items
- Added the AADAG Decision Path: **Decision → Consequence → Influence → Human Authority**
- Added initial alignment with the **NIST Artificial Intelligence Risk Management Framework (AI RMF 1.0)** and its GOVERN, MAP, MEASURE, and MANAGE functions
- Added TESTING.md as the v0.2 validation record covering Inform, Recommend, Presume, Decide, failure reconstruction, and incomplete-information scenarios
- Added validation findings for distilled assessment views, proportional assessment depth, accountability reconstruction, and decision-instance traceability

### Changed

- Clarified that v0.1 established the initial three-dimension assessment model while v0.2 refines decision classification
- Completed the v0.2 consequence model with level definitions, assignment rules, practical examples, and known limitations
- Updated Issue #1 and the roadmap so completion status matches the actual definition of done
- Resolved the v0.2 delegation exploration by placing delegation under accountability rather than creating a separate scoring dimension
- Updated the README to reflect active v0.2 development, current consequence-model status, and traceability documentation
- Reframed project language as direct affirmative statements
- Replaced contrast-based scope descriptions with positive commitments
- Simplified contribution and roadmap language
- Refined the AI influence model with definitions and boundaries for **Inform, Recommend, Presume, and Decide**
- Tested the AI influence model using a cybersecurity account-compromise scenario across all four influence levels
- Completed the v0.2 decision inventory design and marked the roadmap item complete
- Standardized the core governance question on **Human Authority** to match the Decision Path and Decision Inventory
- Updated README status and delegation language to match the completed v0.2 work

## [0.1.0] — 2026-09-02

### Added

- Public project foundation
- Decision-centered governance thesis
- Seven core assessment questions
- Initial consequence, influence, and safeguard model
- Ten framework principles
- Development roadmap
- Contribution guidance

### Status

Early public draft. Terminology and framework mechanics remain subject to change.
