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
6. **Accountability:** Who owns the decision and its consequences, and who authorized AI to have its assigned level of influence?
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

These labels, definitions, assignment rules, examples, and known limitations form the current v0.2 consequence model.

#### Consequence assignment

AADAG assigns a consequence level based on what could credibly happen if an AI-influenced decision is wrong.

**Assignment rule:** Assign the consequence level according to the highest credible consequence of an incorrect decision to affected parties. Consider the nature, scope, duration, and reversibility of the potential harm when determining that level.

Use the following sequence:

> **Define Decision Type → Identify Affected Parties → Identify Highest Credible Consequence → Consider Nature, Scope, Duration, and Reversibility → Assign Consequence Level**

1. **Define the decision type.** Identify the specific decision AI is helping make. Consequence is assigned to a defined decision type rather than each individual decision instance. The decision type should be specific enough that its credible consequences can be meaningfully assessed. Separate decision types should be defined when differences in purpose, affected parties, or potential outcomes would materially change the consequence classification.

2. **Identify affected parties.** Identify the people, groups, organizations, or other parties that could be affected if the decision is wrong. Consider consequence from the perspective of those affected, rather than solely from the perspective of the organization making or operating the decision.

3. **Identify the highest credible consequence.** Determine the highest consequence that could credibly result from an incorrect decision. A consequence should not be elevated simply because an extreme outcome can be imagined. There should be a reasonable connection between the incorrect decision and the potential consequence.

4. **Consider the characteristics of the consequence.** Consider nature, scope, duration, and reversibility when determining the appropriate level. Assess these characteristics based on the credible consequence of the incorrect decision without relying on safeguards intended to prevent, limit, or correct that consequence.

   - **Nature:** What kind of harm or adverse effect could occur?
   - **Scope:** Who or how many could be affected?
   - **Duration:** How long could the effects persist?
   - **Reversibility:** How easily could the effects be corrected or undone?

   These characteristics inform judgment rather than functioning as separate numerical scores.

5. **Assign the consequence level.** Assign the decision type to the consequence level that represents its highest credible consequence.

#### Treatment of safeguards

The initial consequence classification is made without relying on safeguards or mitigations intended to control the consequence.

Safeguards are evaluated separately. They may prevent an incorrect decision, reduce its effects, provide opportunities for intervention, or help correct an outcome.

This keeps two questions distinct:

- **Consequence:** What could credibly happen if this decision is wrong?
- **Safeguards:** What are we doing about it?

Detailed safeguard selection and mapping are addressed separately within AADAG.

#### Practical examples

The following examples illustrate the consequence levels. Classification depends on the defined decision type and its credible consequences.

- **C0 — Negligible:** AI selects the order in which optional internal training announcements appear on an employee portal. An incorrect decision causes only trivial inconvenience with no meaningful adverse effect.
- **C1 — Limited:** AI recommends an optional employee training course. An incorrect recommendation may waste a small amount of employee time and can be corrected through routine action.
- **C2 — Moderate:** AI determines whether an employee should be granted access to a routine business application based on role and authorization. An incorrect denial may prevent the employee from performing part of their job until deliberate administrative action restores access.
- **C3 — Significant:** AI temporarily restricts access to a customer's primary deposit account because activity is suspected to be fraudulent, pending verification. An incorrect restriction may prevent access to funds needed for housing, food, bills, transportation, or other important needs. Some resulting financial effects may persist after access is restored.
- **C4 — Critical:** AI influences whether a patient should receive an urgent medical intervention. An incorrect decision may credibly result in death, serious injury, or lasting harm.

A change in context may require a different decision type and consequence classification. For example, access to a routine business application and privileged access to a critical system should not automatically be treated as the same decision type when their credible consequences materially differ.

#### Known limitations

1. **Consequences depend on available context.** A classification is only as good as the information available when the assessment is performed. Unknown affected parties, uses, dependencies, or circumstances may reveal consequences that were not reasonably identifiable during the original assessment.

2. **Credibility requires judgment.** AADAG does not assign a numerical probability to every possible consequence. Determining whether a consequence is credible requires informed judgment and may produce disagreement between assessors.

3. **Individual outcomes can vary.** AADAG assigns consequence to a decision type, while the actual effect of an incorrect decision may differ between individual cases. The classification represents the highest credible consequence to affected parties rather than predicting the outcome of every individual instance.

4. **Context can change.** A classification can become outdated when the decision's purpose, affected population, operating environment, or potential outcomes materially change. Classification should be revisited when the decision materially changes.

5. **Consequence is not likelihood.** Consequence classification describes what could credibly happen if the decision is wrong. It does not by itself determine how likely the AI is to make that incorrect decision.

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

## Delegation and accountability

**Delegation** is the organizational authorization granting AI a defined level of influence over a decision.

The authority granting or changing AI's influence over a decision should be identifiable and documented.

Delegation does not create a separate classification scale. The AI Influence level identifies what AI is authorized to do. Delegation identifies the organizational authority that authorized it.

When an AI system's authorized influence changes, such as moving from Recommend to Presume, the change should be treated as a governance decision and the authorizing authority documented.

A decision inventory can capture this accountability through three fields:

- **Decision owner:** Who owns the decision and its consequences
- **Authorized AI influence:** Inform, Recommend, Presume, or Decide
- **Authorizing authority:** Who approved that level of influence

## Central rule

**The greater the consequence and the greater the AI influence, the stronger the required evidence, oversight, traceability, and recourse.**

## Scope

AADAG provides a decision-governance layer that works alongside law, regulation, organizational policy, technical assurance, and vendor review.

It applies proportional governance to AI-assisted decisions according to their consequences and the influence given to AI. Human accountability requires meaningful authority, adequate information, and genuine control over the outcome.

## Development status

AADAG v0.2 is an active development release focused on decision classification. The consequence model and AI influence model are established as current v0.2 working models. Delegation is incorporated as an accountability mechanism rather than a separate scoring dimension. Decision inventory mechanics and later safeguard mappings remain under development.
