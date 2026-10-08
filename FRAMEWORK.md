# AI-Assisted Decision Accountability & Governance (AADAG)

## Purpose

AADAG provides a practical way to govern AI according to the decisions it influences and the consequences of getting those decisions wrong.

The **AI-influenced decision** is the primary unit of governance.

## The governance object

AADAG begins with a decision inventory. The inventory records:

- which decisions AI affects
- who could be affected if a decision is wrong
- the consequence of an incorrect decision
- how much influence AI has over the decision
- what authority people retain
- who owns the decision
- who authorized AI's level of influence
- the basis supporting the decision process
- how the decision can be challenged, corrected, or reversed.

A tool inventory remains useful supporting evidence. The decision inventory connects that technology to its real-world use and consequences.

### Decision inventory template

The v0.2 decision inventory uses nine fields:

| Field | Question |
|---|---|
| **Decision** | What decision is AI helping make? |
| **Affected Parties** | Who could be affected if the decision is wrong? |
| **Consequence** | CU, C0, C1, C2, C3, or C4 |
| **AI Influence** | Inform, Recommend, Presume, or Decide |
| **Human Authority** | What authority do people retain over the decision or decision process? |
| **Decision Owner** | Who is accountable for the decision and its outcomes? |
| **Authorizing Authority** | Who authorized this level of AI influence? |
| **Basis** | What information, criteria, need, or reasoning supports the decision? |
| **Review / Recourse** | How can the decision be challenged, corrected, or reversed? |

The Decision Inventory was pressure-tested across Inform, Recommend, Presume, and Decide influence levels, along with failure reconstruction and an incomplete-information scenario. The fields are intended to remain concise. Basis may reference supporting information rather than reproduce documentation inside the inventory.

## Core questions

For each AI-influenced decision, ask:

1. **Decision:** What decision is AI helping us make?
2. **Affected Parties:** Who could be affected if the decision is wrong?
3. **Consequence:** What happens if the decision is wrong?
4. **AI Influence:** How much influence does AI have over the outcome?
5. **Human Authority:** What authority do people retain over the decision or decision process?
6. **Decision Owner:** Who is accountable for the decision and its outcomes?
7. **Authorizing Authority:** Who authorized this level of AI influence?
8. **Basis:** What information, criteria, need, or reasoning supports the decision?
9. **Review / Recourse:** How can the decision be challenged, corrected, or reversed?

## Initial assessment model

AADAG uses three working dimensions established in v0.1. Decision classification was refined in v0.2, with safeguard mapping continuing in later development.

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

### 3. Safeguard Mapping

AADAG applies safeguards according to the consequence of an incorrect decision and the level of influence AI has over that decision.

> **Consequence establishes how much governance a decision warrants. AI Influence determines how that governance should be applied.**

Safeguards should be proportionate to the decision being governed. Higher consequence may require greater rigor, but greater AI Influence does not automatically require every safeguard to become stronger. The safeguards that matter most, and how they are applied, depend on the role AI has in the decision.

AADAG uses five safeguard concerns:

#### Decision Support

Decision Support addresses whether the people involved in a decision have the information needed to exercise their role.

This may include the information AI provides, the basis supporting a recommendation, known limitations or uncertainty, relevant evidence, and other information material to the decision.

Decision Support does not require every possible piece of information to be available. The information required depends on the decision, the authority being exercised, and the organization's established requirements.

#### AI Assurance

AI Assurance addresses whether sufficient relevant evidence supports relying on AI for the role it has been given in the decision.

Relevant evidence may include testing, validation, observed performance, suitability for the decision environment, reliability of supporting data, and operational experience.

Assurance is not certainty. Evidence that supported reliance on AI under one set of conditions may become less applicable when the system, data, decision environment, or other material conditions change.

#### Human Control

Human Control addresses whether retained human authority can actually be exercised when needed.

The presence of a human role alone does not establish Human Control. The person must have the authority and practical ability to exercise the role assigned to them within the conditions and decision window in which that authority matters.

As AI Influence increases, Human Control may move from case-level approval toward governing the authority delegated to AI, including the ability to constrain, modify, suspend, or withdraw that authority.

#### Decision Record

Decision Record addresses whether a decision and the relevant events surrounding it can be reconstructed.

The record should be proportionate to the decision and may include the outcome, information or evidence used, AI contribution, human action, exceptions, changes in authority, and resulting actions where those details are material.

Decision Record supports accountability, review, correction, investigation, and later reassessment. It should not require documentation that provides no meaningful governance value.

#### Operating Boundaries

Operating Boundaries establish where AI's decision authority begins, where it ends, and the conditions under which that authority changes.

Boundaries may reflect the decision being made, AI Influence, organizational policy, operating conditions, defined exceptions, cumulative activity, or other conditions the organization determines are material.

Operating Boundaries also govern the **context and timing of AI-generated information**. Information suitable for retrospective research or process improvement may be inappropriate to introduce as an operational recommendation during an active incident. Movement from research into operational use remains subject to the organization's established authorization, validation, and change-control requirements.

Reaching an Operating Boundary does not automatically require disabling the AI system. The affected decision or level of AI Influence may be constrained, routed to another authorized path, reduced, suspended, or stopped while other supportable AI functions continue.

#### 3.1 Consequence and Safeguard Rigor

Consequence determines the rigor warranted around an AI-influenced decision but does not prescribe a fixed set of controls.

AADAG does not define universal thresholds for financial value, transaction volume, confidence scores, error rates, or other organization-specific measures. The organization provides the risk context used to classify the decision and determine what level of governance is appropriate.

The consequence levels provide the following safeguard posture:

**C0 — Negligible**

Safeguards should remain minimal. Governance should not introduce meaningful overhead where an incorrect decision has no meaningful adverse effect. Basic operational practices may be sufficient.

**C1 — Limited**

Safeguards should provide basic visibility and accountability appropriate to AI's role. Errors should be identifiable and correctable through routine action without requiring substantial governance infrastructure.

**C2 — Moderate**

Safeguards should be deliberately defined for the decision. The organization should understand why AI is being relied upon, establish relevant boundaries and exceptions, preserve appropriate human authority, and maintain enough evidence to review or reconstruct material decisions.

**C3 — Significant**

Safeguards should provide strong and reliable governance over AI's role in the decision. Evidence supporting reliance on AI, operating boundaries, human authority, decision support, records, exception handling, and reassessment should be established with rigor appropriate to the potential harm.

**C4 — Critical**

Safeguards should receive the highest level of rigor appropriate to the organization's environment and established risk requirements. Delegated AI authority should have a strong supporting basis, clearly defined boundaries, reliable paths for exercising retained human authority, and sufficient evidence to reconstruct and reassess consequential decisions.

These levels describe increasing governance rigor rather than a mandatory control count. The same safeguard may be implemented very differently across consequence levels.

A Decision Record for a C1 decision, for example, may require only enough information to identify what occurred and correct an error. A C4 Decision Record may require substantially greater evidence because the organization must be able to reconstruct a decision whose effects could be lasting or irreversible.

Safeguards should also avoid unnecessary governance overhead. High AI Influence does not by itself justify extensive controls around a negligible-consequence decision.

#### 3.2 AI Influence and Safeguard Application

AI Influence determines how safeguards should be applied to the decision.

As AI moves from Inform through Decide, its role changes from supplying information to exercising decision authority. Safeguards should reflect that role rather than increase mechanically with each Influence level.

##### Inform

At Inform, AI provides information, analysis, context, prioritization, or flags without proposing or making the decision.

Safeguards should focus primarily on whether the AI contribution can be appropriately relied upon as an input to the human decision. Decision Support and AI Assurance may therefore carry substantial weight, particularly when the consequence of an incorrect decision is high.

Human Control is generally inherent at this level because the human retains decision authority. Operating Boundaries should ensure that AI remains within its informational role and does not begin recommending or taking action without authorization.

Decision Records should preserve AI's contribution when reconstruction of the decision warrants it.

##### Recommend

At Recommend, AI proposes a decision, action, or set of options while a human retains authority to determine the outcome.

Safeguards should allow the human to exercise judgment rather than simply accept the AI recommendation without a meaningful basis for doing so. Decision Support should provide enough information about the recommendation and its basis for the human to evaluate it at the rigor warranted by the consequence.

AI Assurance should support reliance on AI for the recommending role. Operating Boundaries should prevent a recommendation from becoming an action without the required human decision.

Decision Records should preserve the recommendation and resulting decision when those details are material to accountability or reconstruction.

##### Presume

At Presume, AI establishes an outcome that will take effect unless a human intervenes.

Safeguards should address the conditions under which the presumed outcome may proceed, the conditions requiring additional review, and whether retained human authority can realistically be exercised before the outcome takes effect.

Operating Boundaries may include exceptions, heuristics, cumulative activity, changed conditions, or other organization-defined triggers that alter the normal decision path.

Human Control requires more than assigning someone the ability to override the AI. The authorized person must have a realistic opportunity to exercise that authority within the relevant decision window.

> **Failure to intervene can support a presumed outcome only when retained human authority had a realistic opportunity to be exercised.**

When that opportunity does not exist, Presume should not silently become Decide. The decision should follow another authorized path or wait until the organization's requirements for proceeding are satisfied.

##### Decide

At Decide, AI selects or executes the decision without requiring case-by-case human approval.

Safeguards should focus on the authority delegated to AI and the conditions under which that authority remains valid. AI Assurance should provide sufficient relevant evidence to support reliance on AI for the assigned decision role. Operating Boundaries should define where that authority applies and when it must change, route elsewhere, or cease.

Human Control at Decide does not require a person to approve every individual decision. Human authority is exercised through governance of the delegated authority, including the ability to constrain, modify, suspend, or withdraw it.

Decision Records become particularly important when individual decisions occur without prior human review because the organization must retain sufficient evidence to reconstruct material decisions and evaluate how the delegated authority was exercised.

#### 3.3 Safeguard Mapping — Application Guide (v0.3)

Use the nine-field Decision Inventory to define the decision and its accountable authority. Then apply two complementary assessments: **Consequence sets the required rigor; AI Influence determines how the five safeguards operate.** The following tables are application guidance, not 24 independent control sets or universal numeric thresholds.

| Consequence | Safeguard rigor and minimum expectation |
|---|---|
| **CU — Undetermined** | Identify missing consequence evidence and responsible reviewers. Do not treat CU as low risk or authorize a decision path whose required classification and approval remain unresolved. |
| **C0 — Negligible** | Use minimal, proportionate practices; avoid controls without meaningful governance value. |
| **C1 — Limited** | Establish basic visibility, identifiable responsibility, and routine error correction. |
| **C2 — Moderate** | Document relevant evidence, assigned authority, operating limits, exceptions, and a practical review or correction path. |
| **C3 — Significant** | Require strong, decision-relevant assurance; demonstrably effective human intervention where retained; dependable exception handling and reconstructable records. |
| **C4 — Critical** | Apply the highest justified rigor: robust evidence for reliance, explicit authority and boundaries, credible intervention or authorized alternate paths, and records sufficient for consequential investigation and recourse. |

| AI Influence | How safeguard application changes |
|---|---|
| **Inform** | Emphasize accurate and usable Decision Support, AI Assurance for informational reliance, limits on escalation into advice/action, and records where material. Humans interpret and decide. |
| **Recommend** | Provide evidence and uncertainty needed for independent human judgment; require the authorized human decision before implementation; retain the recommendation and disposition when material. |
| **Presume** | Define conditions for the default outcome, exception triggers, a realistic human override opportunity before effect, and evidence of whether the outcome proceeded or was changed. Without a meaningful opportunity to intervene, use an authorized alternate path rather than silently converting Presume to Decide. |
| **Decide** | Require documented delegated authority, fit-for-purpose assurance, explicit operating limits, runtime oversight and ability to constrain/suspend/withdraw authority, and reconstructable material decisions. Case-by-case human approval is not intrinsic to Decide. |

**Minimum evidence and authority expectations.** For each governed decision, the organization should identify (1) the basis for classifying consequence and AI Influence; (2) the evidence sufficient to rely on AI in that role, including material uncertainty and limitations; (3) the Decision Owner, Authorizing Authority, and retained Human Authority; (4) the applicable operating conditions and exception/STOP triggers; and (5) what must be recorded to enable proportionate review and recourse. The depth and form of evidence scale with consequence and operating context. **To be confirmed** documents an unresolved role; it is not authorization to proceed.

**Meaningful human review.** Where the organization retains case-level approval or intervention, the reviewer must have adequate decision-relevant information, appropriate authority, and a realistic opportunity to act in the applicable decision window. At Decide, review instead focuses on authorization, boundaries, performance, exceptions, and continuing suitability of delegated authority.

**Override and recourse.** Define who may challenge, correct, reverse, constrain, or suspend a decision or delegated AI authority, which outcomes are reversible, and what escalation or alternate authorized path applies when they are not. Record material overrides and their basis. Review/recourse expectations should reflect affected parties and the highest credible consequence.

**Proceed, redirect, or STOP.** The organization establishes the evidence, authority, and operating conditions required for a path to proceed. If a requirement fails, constrain or redirect the affected decision to an **already authorized** alternate path when available. If none permits it to proceed, **STOP that decision path**. Withholding an unsupported AI recommendation may coexist with continued authorized informational support and does not itself stop equipment, unrelated decisions, or established human authority.

**Scope and validation.** This v0.3 mapping consolidates exploratory framework pressure tests; it does not establish site-specific regulatory compliance, validate particular manufacturing procedures, or substitute for organizational acceptance criteria. Field testing and implementation templates are planned for later versions.

#### 3.4 Safeguards Working Together

The five safeguard concerns operate together. They should not be treated as independent requirements or a checklist that must be applied identically to every decision.

A condition identified by one safeguard may affect another. Evidence supporting AI Assurance may justify a particular level of AI Influence. Operating Boundaries determine where that authority applies. Decision Support provides information needed to exercise judgment. Human Control preserves the organization's ability to exercise retained authority. Decision Record provides evidence needed to reconstruct what occurred and support later review or reassessment.

The relative importance of each safeguard may change according to Consequence, AI Influence, organizational requirements, and operating conditions.

##### Changed Conditions

Safeguards should account for material changes in the conditions supporting the governed decision.

A change in data, operating environment, system behavior, affected population, decision context, or other material condition may weaken the basis supporting the current AI role without making every AI function unusable.

When this occurs, the organization should determine whether the existing AI Influence remains supportable under the established safeguards and Operating Boundaries.

AI authority may remain unchanged, become more constrained, move to a lower Influence level, route to another authorized decision path, or cease for the affected decision.

##### Alternate Decision Paths

A decision that cannot continue through its normal path does not necessarily have to stop entirely.

Operating Boundaries may route the decision to another person, process, Influence level, or authorized authority. The alternate path should operate within authority already established by the organization.

Urgency, inconvenience, or operational pressure does not itself expand AI authority.

A human decision made through an authorized alternate path also does not automatically expand future AI authority. A case-specific exception should remain an exception unless the organization deliberately changes the governed process.

##### STOP

STOP applies when the current decision path cannot proceed under the organization's established requirements or available authority.

STOP applies to the affected decision path rather than automatically requiring the AI system itself to be disabled. AI may continue performing other authorized and supportable functions while the affected decision is held, constrained, or routed elsewhere.

An exception, incomplete information, or unavailable human does not independently require STOP in every case. The organization determines what information, authority, and conditions are required for a decision to proceed.

Where another authorized path exists, the decision may move to that path. Where no authorized path permits the decision to continue, the current path stops.

Where material evidence cannot support a reliable AI recommendation, the AI may **withhold that recommendation**, communicate the uncertainty, and continue authorized informational support. Withholding an unsupported recommendation does not itself revoke a human's established authority or automatically trigger STOP; applicable procedures and authorized alternate paths govern what can proceed.

##### Runtime Evidence and Reassessment

Operation of the governed decision produces evidence about how the safeguards and delegated authority work in practice.

Runtime evidence may include exceptions, overrides, boundary conditions, repeated patterns, unexpected outcomes, performance changes, human interventions, or decisions that could not proceed through their expected path.

This evidence should inform reassessment when it indicates that the assumptions supporting the current governance may no longer hold.

Reassessment may result in no change. It may also result in changes to safeguards, Operating Boundaries, AI Influence, decision classification, or other parts of the governed process.

A successful outcome does not by itself establish that AI acted within its authorized authority. An unfavorable outcome does not by itself establish that governance failed. Reassessment should consider both the outcome and whether the decision occurred within the authority and conditions established by the organization.

## Delegation and accountability

**Delegation** is the organizational authorization granting AI a defined level of influence over a decision.

The authority granting or changing AI's influence over a decision should be identifiable and documented.

Delegation does not create a separate classification scale. The AI Influence level identifies what AI is authorized to do. Delegation identifies the organizational authority that authorized it.

When an AI system's authorized influence changes, such as moving from Recommend to Presume, the change should be treated as a governance decision and the authorizing authority documented.

The decision inventory captures this accountability through three fields:

- **Decision Owner:** Who is accountable for the decision and its outcomes
- **AI Influence:** Inform, Recommend, Presume, or Decide
- **Authorizing Authority:** Who approved that level of influence

## Central rule

**Consequence establishes how much governance a decision warrants. AI Influence determines how that governance should be applied.**

## Scope

AADAG provides a decision-governance layer that works alongside law, regulation, organizational policy, technical assurance, and vendor review.

It applies proportional governance to AI-assisted decisions according to their consequences and the influence given to AI. Human accountability requires that retained human authority remain meaningful and that delegated AI authority remain governable within the organization's established boundaries.

## Development status

AADAG v0.2 Decision Classification was released on September 22, 2026. AADAG v0.3.0 Safeguard Mapping was released on October 8, 2026 as a development release. The v0.3 application guide consolidates the five safeguard families, consequence-based rigor, influence-specific application, evidence, meaningful human review, recourse, and STOP. It has not been independently field-validated.
