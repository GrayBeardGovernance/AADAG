# AADAG Reference: ISO/IEC 42001:2023 Crosswalk

**Version 0.1 | October 2026**  
**Gray Beard Governance**  
**Status: Draft for Review**

## 1. Purpose

This document correlates the AI Assisted Decision Accountability & Governance (AADAG) framework v0.3 with selected requirements and controls of ISO/IEC 42001:2023.

AADAG and ISO/IEC 42001 serve different but complementary purposes. ISO/IEC 42001 addresses organizational AI management systems. AADAG provides a decision centered methodology for assessing consequences, AI influence, human authority, and appropriate safeguards.

This crosswalk does not modify AADAG, establish equivalence between the two frameworks, or demonstrate ISO/IEC 42001 compliance.

## 2. Mapping Method

Correlations are evaluated using three classifications:

- **Direct conceptual alignment:** AADAG explicitly addresses a relevant governance concern.
- **Partial alignment:** AADAG addresses a portion of the concern, but does not provide the full organizational or technical process.
- **Outside scope:** The ISO requirement addresses responsibilities not covered by AADAG's intended methodology.

Alignment describes conceptual relevance, not evidence that an organization has implemented a control.

## 3. Preliminary ISO Crosswalk

| ISO reference | Relevant AADAG component | Correlation |
| --- | --- | --- |
| 6.1.2, AI risk assessment | Decision Inventory, Consequence Classification | Partial |
| 6.1.3, AI risk treatment | Five Safeguard Families, Operating Boundaries | Partial |
| 6.1.4, AI system impact assessment | Affected Parties, Consequence Classification | Partial |
| 8.1, Operational planning and control | Human Authority, Operating Boundaries, STOP | Partial |
| 8.2, AI risk assessment | Decision reassessment and documented classification | Partial |
| 8.3, AI risk treatment | Safeguard Mapping | Partial |
| 8.4, AI system impact assessment | Decision consequences and affected parties | Partial |
| A.3.2, AI roles and responsibilities | Decision Owner, Authorizing Authority, Human Authority | Direct conceptual |
| A.5.2, AI system impact assessment process | Decision Inventory and Consequence Classification | Partial |
| A.5.3, Documentation of impact assessments | Decision Inventory, Basis, Review / Recourse | Partial |
| A.5.4, Impacts on individuals or groups | Affected Parties, Consequence Classification | Partial |
| A.5.5, Societal impacts | Affected Parties, Consequence Classification | Partial |
| A.6.2.4, Verification and validation | AI Assurance | Partial |
| A.6.2.6, Operation and monitoring | Operating Boundaries, Human Control | Partial |
| A.6.2.8, Recording of event logs | Decision Record | Partial |
| A.9.2, Responsible use processes | Human Authority, Safeguard Mapping | Partial |
| A.9.4, Intended use | Decision definition, AI Influence, Operating Boundaries | Partial |

All mappings are provisional pending final source verification and detailed interpretation.

## 4. Where AADAG Provides Additional Decision Level Structure

AADAG distinguishes four levels of AI influence: Inform, Recommend, Presume, and Decide.

It also establishes consequence classifications from CU through C4 and uses consequence and influence together to guide safeguard assessment.

This provides a structured method for examining the degree of authority exercised by AI and determining where human intervention may be appropriate.

AADAG's STOP outcome, Human Control, and Operating Boundaries further support examination of when delegated AI decision authority should be constrained, redirected, or suspended.

These features should be presented as AADAG's own methodology, not as requirements imposed by ISO/IEC 42001.

## 5. Traceability and the Decision Lifecycle

AADAG's Decision Record safeguard addresses reconstruction of decisions and resulting outcomes.

Potential applications include documenting:

- The basis for a decision
- The authority under which AI acted
- Relevant operating conditions
- Actions taken and their outcomes
- Human intervention, review, and recourse

Execution time revalidation, confirmed outcomes, and post execution exception handling are areas for further AADAG pressure testing. They should not be represented as fully implemented capabilities of v0.3.

## 6. ISO Requirements Outside AADAG's Intended Scope

AADAG does not independently establish a complete organizational AI management system.

Examples of responsibilities outside its intended scope include:

- Organization wide AI policy and management system objectives
- Resource allocation and competence management
- Formal internal audit programs
- Management review processes
- Comprehensive AI data lifecycle management
- Supplier and third party management
- Organization-wide continual improvement programs

These are scope distinctions, not automatically AADAG deficiencies.

## 7. Limitations

This document is an independent correlation of governance concepts.

It is not endorsed by ISO or IEC, is not a certification guide, and does not replace the official ISO/IEC 42001:2023 standard.

AADAG v0.3 remains a development framework that has undergone scenario pressure testing but has not been independently field validated.

## 8. References

1. ISO/IEC 42001:2023, *Information technology — Artificial intelligence — Management system*. https://www.iso.org/standard/42001
2. Gray Beard Governance, *AADAG Framework v0.3*. https://github.com/GrayBeardGovernance/AADAG/blob/main/FRAMEWORK.md
3. Gray Beard Governance, *AADAG Development Testing Record*. https://github.com/GrayBeardGovernance/AADAG/blob/main/TESTING.md

**Document status:** Draft v0.1. Not approved for publication.
