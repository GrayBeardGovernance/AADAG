# AI-Assisted Decision Accountability & Governance (AADAG)

## Purpose

AADAG provides a practical way to govern AI according to the decisions it influences and the consequences of getting those decisions wrong.

The **AI-influenced decision** is the primary unit of governance.

## The governance object

AADAG begins with a decision inventory. The inventory records:

- which decisions AI affects;
- how much authority the technology carries;
- who may be harmed by an incorrect decision;
- where human judgment is required; and
- who owns the outcome.

A tool inventory remains useful supporting evidence. The decision inventory connects that technology to its real-world use and consequences.

## Core questions

For each AI-influenced decision, ask:

1. **Decision:** What decision is AI helping us make?
2. **Consequence:** What happens if the decision is wrong?
3. **Influence:** How much influence does AI have over the outcome?
4. **Human role:** What judgment or authority must remain with a person?
5. **Evidence:** What information supports the decision, and can it be examined?
6. **Accountability:** Who owns the decision and its consequences?
7. **Review:** How can the decision be challenged, corrected, or reversed?

## Initial assessment model

AADAG v0.1 proposes three dimensions for further development.

### 1. Decision consequence

Decision consequence describes the potential impact of an incorrect AI-influenced decision.

Consequence is assessed by considering the nature, scope, duration, and reversibility of the potential harm. Assessment may include impacts to:

- people and communities;
- rights, eligibility, or access;
- safety and security;
- financial or material resources;
- reputation and opportunity; and
- mission or operational outcomes.

#### Consequence levels

AADAG uses the following consequence levels:

| Level | Classification | Definition |
|---|---|---|
| **CU** | **Undetermined** | The potential consequence of an incorrect decision cannot yet be determined with sufficient confidence. Additional information or analysis is required before assigning a consequence level. |
| **C0** | **Negligible** | An incorrect decision has no meaningful adverse effect. Any resulting inconvenience is trivial and readily corrected. |
| **C1** | **Limited** | An incorrect decision may cause minor disruption or inconvenience. Effects are identifiable and can be corrected through routine action. |
| **C2** | **Moderate** | An incorrect decision may cause meaningful adverse effects requiring deliberate corrective action. |
| **C3** | **Significant** | An incorrect decision may cause substantial harm involving people, rights, access, finances, security, opportunity, reputation, or mission outcomes. Correction may require significant intervention and some effects may persist. |
| **C4** | **Critical** | An incorrect decision may cause lasting harm involving life, safety, fundamental rights, major financial or material loss, critical security interests, or essential mission functions. Effective correction may be difficult or impossible. |

#### Undetermined consequences

An undetermined consequence is a valid assessment when available information does not support a reliable classification.

The uncertainty should be documented along with the information needed to complete the assessment.

### 2. AI influence

Identify the AI system's actual role:

- **Inform:** supplies information to a human;
- **Recommend:** proposes or ranks possible decisions;
- **Presume:** establishes a default that a human may override;
- **Decide:** makes or executes the decision with limited intervention.

These are working categories and will be tested during development.

### 3. Required safeguards

Safeguards should increase with both consequence and AI influence. Candidate safeguards include:

- named human ownership;
- documented decision criteria;
- source and evidence review;
- meaningful human review;
- logging and traceability;
- bias and performance evaluation;
- appeal or correction mechanisms;
- monitoring for changed conditions; and
- authority to suspend AI use.

## Central rule

**The greater the consequence and the greater the AI influence, the stronger the required evidence, oversight, traceability, and recourse.**

## Scope

AADAG provides a decision-governance layer that works alongside law, regulation, organizational policy, technical assurance, and vendor review.

It applies proportional governance to AI-assisted decisions according to their consequences and the influence given to AI. Human accountability requires meaningful authority, adequate information, and genuine control over the outcome.

## Development status

This is an early public draft. Decision classes, scoring, safeguard mappings, examples, and implementation guidance remain under development.
