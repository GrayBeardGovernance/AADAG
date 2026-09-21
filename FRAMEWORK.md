# AI-Assisted Decision Accountability & Governance (AADAG)

## Purpose

AADAG provides a practical way to govern AI according to the decisions it influences and the consequences of getting those decisions wrong.

The **AI-influenced decision** is the primary unit of governance.

## The governance object

AADAG begins with a decision inventory. The inventory records:

- which decisions AI affects
- how much authority the technology carries
- who may be harmed by an incorrect decision
- where human judgment is required
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

AADAG uses three working dimensions established in v0.1 and being refined through v0.2 and later development.

### 1. Decision consequence

Decision consequence describes the potential impact of an incorrect AI-influenced decision.

Consequence is assessed by considering the nature, scope, duration, and reversibility of the potential harm. Assessment may include impacts to:

- people and communities
- rights, eligibility, or access
- safety and security
- financial or material resources
- reputation and opportunity
- mission or operational outcomes.

#### Consequence levels

AADAG v0.2 introduces the following working consequence levels:

| Level | Classification | Definition |
|---|---|---|
| **CU** | **Undetermined** | The potential consequence of an incorrect decision cannot yet be determined with sufficient confidence. Additional information or analysis is required before assigning a consequence level. |
| **C0** | **Negligible** | An incorrect decision has no meaningful adverse effect. Any resulting inconvenience is trivial and readily corrected. |
| **C1** | **Limited** | An incorrect decision may cause minor disruption or inconvenience. Effects are identifiable and can be corrected through routine action. |
| **C2** | **Moderate** | An incorrect decision may cause meaningful adverse effects requiring deliberate corrective action. |
| **C3** | **Significant** | An incorrect decision may cause substantial harm involving people, rights, access, finances, security, opportunity, reputation, or mission outcomes. Correction may require significant intervention and some effects may persist. |
| **C4** | **Critical** | An incorrect decision may cause lasting harm involving life, safety, fundamental rights, major financial or material loss, critical security interests, or essential mission functions. Effective correction may be difficult or impossible. |

These labels and definitions are the current v0.2 working scale. Assignment rules, examples, and known limitations remain under development.

#### Undetermined consequences

An undetermined consequence is a valid assessment when available information does not support a reliable classification.

The uncertainty should be documented along with the information needed to complete the assessment.

### 2. AI influence

AI influence describes how AI participates in a decision and how much decision authority remains with a human.

- **Inform:** AI provides information, analysis, or context for consideration. The human evaluates the information and retains responsibility for determining what action, if any, to take. AI may identify, summarize, analyze, prioritize, or flag information without leaving this level, provided it does not propose a decision or action.
- **Recommend:** AI proposes a decision, action, or ranked set of options for human consideration. The human retains authority to accept, reject, or modify the recommendation, and human action is required for it to become the decision.
- **Presume:** AI establishes a default decision or action that will take effect unless a human intervenes. A human retains the authority and opportunity to change or override the outcome before it takes effect.
- **Decide:** AI selects or executes a decision without requiring case-by-case human approval. Human authority is exercised through the rules, limits, oversight, and ability to modify or stop the AI's decision-making authority.

#### Influence boundaries

- **Inform → Recommend:** Inform may rank or prioritize information. Recommend proposes or ranks decisions or actions.
- **Recommend → Presume:** A recommendation requires human action to become the decision. Under Presume, human inaction allows the AI-established outcome to proceed.
- **Presume → Decide:** Under Presume, a human has the authority and opportunity to intervene before the outcome takes effect. Under Decide, the individual decision can occur without prior human intervention.

These definitions and boundaries are the current v0.2 working influence model.

AADAG is also exploring whether **delegation** adds a useful accountability concept alongside influence. Influence describes how much AI affects a decision. Delegation may describe the organizational choice to give AI that influence. This distinction is exploratory and is not yet a formal scoring dimension.

### 3. Required safeguards

Safeguards should increase with both consequence and AI influence. Candidate safeguards include:

- named human ownership
- documented decision criteria
- source and evidence review
- meaningful human review
- logging and traceability
- bias and performance evaluation
- appeal or correction mechanisms
- monitoring for changed conditions
- authority to suspend AI use.

Detailed safeguard mapping is planned for v0.3.

## Central rule

**The greater the consequence and the greater the AI influence, the stronger the required evidence, oversight, traceability, and recourse.**

## Scope

AADAG provides a decision-governance layer that works alongside law, regulation, organizational policy, technical assurance, and vendor review.

It applies proportional governance to AI-assisted decisions according to their consequences and the influence given to AI. Human accountability requires meaningful authority, adequate information, and genuine control over the outcome.

## Development status

AADAG v0.2 is an active development release focused on decision classification. The consequence labels and core definitions are established as the current working scale. Assignment rules, examples, delegation, decision inventory mechanics, and later safeguard mappings remain under development.
