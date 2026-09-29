# Case Study 001: The Decision Environment

## Status

**Working case study for AADAG v0.2 Decision Classification**

This case study tests AADAG against a published AI-agentic decision intelligence architecture rather than a hypothetical example. It is intended to expose weaknesses, ambiguity, and unnecessary complexity in AADAG while the framework is still being developed.

This case study began while several v0.2 concepts were still being refined. The terminology below has been aligned to the released v0.2 framework while preserving the development questions the case study was designed to test.

## Source architecture

This case study is based on:

Alper Murat, Ratna Babu Chinnam, Satyendra Rana, Stephen H. Rapp, Kurt Hansen, Todd A. Richman, and James E. Bechtel, **“From Concept to Execution: An AI-Agentic Decision Intelligence Framework for Product Planning and Concept Development,”** presented at the 2025 NDIA Michigan Chapter Ground Vehicle Systems Engineering and Technology Symposium and published as SAE Technical Paper 2025-01-0455.

DOI: 10.4271/2025-01-0455

A public-release version of the paper is available through the 2025 GVSETS proceedings. The paper is marked Distribution Statement A, approved for public release with unlimited distribution.

## Why this is a useful AADAG test

The proposed architecture uses Large Language Models and agentic workflows to support product planning and concept development. It captures and refines stakeholder intent, synthesizes engineering and market information, performs analytical tasks, supports trade-space exploration, and orchestrates downstream workflow.

That creates a useful governance question for AADAG:

> **An AI system may be capable of participating in a decision. How much influence should it actually be permitted to have over that decision?**

The paper provides the decision environment. AADAG is being tested as a governance layer over that environment.

## Test method

AADAG treats the AI-influenced decision as the primary unit of governance.

For each decision point identified in the architecture, the case study asks the current v0.2 core governance questions:

1. **Decision:** What decision is AI helping us make?
2. **Consequence:** What happens if the decision is wrong?
3. **Influence:** How much influence does AI have over the outcome?
4. **Human Authority:** What authority do people retain over the decision or decision process?
5. **Basis:** What information, criteria, need, or reasoning supports the decision?
6. **Accountability:** Who owns the decision and its consequences, and who authorized AI to have its assigned level of influence?
7. **Review:** How can the decision be challenged, corrected, or reversed?

The first pass intentionally does not add new AADAG categories. If the current framework cannot describe a decision cleanly, that failure will be documented rather than hidden by changing the model.

## Candidate decision points

The following decision points are derived from functions described in the source architecture. They are starting points for analysis, not claims that the authors delegate final authority for each decision to AI.

| # | Decision point | AI activity | Initial AADAG question |
|---|---|---|---|
| 1 | Interpret stakeholder intent | Analyze and refine stakeholder input | When does clarification become interpretation that materially changes intent? |
| 2 | Identify ambiguity or bias in requirements | Analyze stakeholder statements and requirements | Can AI flag a concern, resolve it, or only present it for human judgment? |
| 3 | Structure or refine requirements | Transform unstructured information into decision-ready artifacts | When does structuring information begin to alter the requirement itself? |
| 4 | Prioritize product features or requirements | Synthesize stakeholder, engineering, and market information | Is AI informing prioritization, recommending an order, or establishing the working priority? |
| 5 | Assess alternatives in the trade space | Combine performance, cost, risk, and contextual information | How much influence should AI have over eliminating or favoring alternatives? |
| 6 | Generate or evaluate scenarios | Support scenario simulation and causal analysis | What happens when an AI-generated scenario becomes evidence for a consequential decision? |
| 7 | Assess or communicate risk | Analyze information and produce risk-related outputs | Who determines whether the risk assessment is sufficient to proceed? |
| 8 | Recommend strategic adjustments | Use changing information to suggest changes in direction | At what consequence level must a recommendation receive explicit human approval? |
| 9 | Produce decision outputs for downstream systems | Export outputs such as prioritized features or risk-adjusted estimates | When does a recommendation become an operational action because another system consumes it? |
| 10 | Advance the workflow to the next analytical stage | Orchestrate chained AI-driven processes | Who has authority to let the agent continue without a human checkpoint? |

## First AADAG observation

The architecture highlights a distinction between **technical capability** and **decision authority**.

An agent may be technically capable of interpreting information, ranking alternatives, recommending action, updating a knowledge structure, or passing an output into another enterprise system. Technical capability alone does not establish whether that degree of influence is appropriate for a particular decision.

> **Capability does not grant authority.**

AADAG attempts to make that authority question explicit by classifying the decision, its potential consequences, and the influence given to AI.

## Consequence analysis

AADAG v0.2 uses the following working consequence levels:

| Level | Classification | Working meaning |
|---|---|---|
| CU | Undetermined | Consequence cannot yet be classified with sufficient confidence. |
| C0 | Negligible | No meaningful adverse effect. |
| C1 | Limited | Minor disruption or inconvenience that can be corrected routinely. |
| C2 | Moderate | Meaningful adverse effects requiring deliberate corrective action. |
| C3 | Significant | Substantial harm or persistent effects involving people, resources, security, opportunity, reputation, or mission outcomes. |
| C4 | Critical | Potential lasting harm involving life, safety, fundamental rights, major loss, critical security interests, or essential mission functions. |

The case study will not assign consequence based solely on the software function. The same AI capability may participate in decisions with very different consequences depending on context.

For example, an AI-generated prioritization used for an internal brainstorming exercise may carry relatively low consequence. The same mechanism used to remove a safety requirement from further consideration could carry substantially greater consequence.

This is one of the central hypotheses being tested:

> **The decision context matters more than the mere presence of the AI capability.**

## Influence analysis

AADAG v0.2 uses four AI Influence levels:

**Inform**  
AI provides information, analysis, or context for consideration. The human evaluates the information and retains responsibility for determining what action, if any, to take. AI may identify, summarize, analyze, prioritize, or flag information without leaving this level, provided it does not propose a decision or action.

**Recommend**  
AI proposes a decision, action, or ranked set of options for human consideration. The human retains authority to accept, reject, or modify the recommendation, and human action is required for it to become the decision.

**Presume**  
AI establishes a default decision or action that will take effect unless a human intervenes. A human retains the authority and opportunity to change or override the outcome before it takes effect.

**Decide**  
AI selects or executes a decision without requiring case-by-case human approval. Human authority is exercised through the rules, limits, oversight, and ability to modify or stop the AI's decision-making authority.

The source architecture is particularly useful for testing the boundary between these categories because outputs can move directly between analytical stages and into downstream enterprise systems.

A key question is whether influence should be assessed only at the point an AI produces an output, or across the full chain of downstream decisions affected by that output.

## Human checkpoints

A human-in-the-loop control is only meaningful if the human has enough information, authority, time, and practical ability to change the outcome.

For this case study, the presence of a human checkpoint will therefore not automatically be treated as sufficient governance.

AADAG will ask:

**Why is the checkpoint located there?**

**What decision is the human actually approving?**

**Can the human reject or modify the AI output?**

**What happens if the human does nothing?**

**Does the workflow continue automatically?**

**Who owns the outcome after approval?**

This may help determine whether AADAG consequence and influence classifications can provide a repeatable basis for deciding where meaningful human authority is required.

## Delegation question and v0.2 resolution

This case study originally tested whether delegation should become a distinct governance concept or whether it duplicated the Influence classification.

The v0.2 development process resolved that question. **Delegation is the organizational authorization granting AI a defined level of influence over a decision.** It is an accountability mechanism rather than a separate classification scale.

**Influence** describes how AI participates in the decision and the authority it has over the outcome.

**Delegation** identifies the organizational act and authority that permitted AI to operate at that level of influence.

The agentic architecture makes the distinction visible. A system may possess the technical capability to perform an action while the organization chooses whether that capability is permitted at a particular decision point.

This case study therefore tests whether the authorizing authority and assigned Influence level remain identifiable as decisions move through an agentic workflow.

## Accountability question

Traceability can show what happened in an AI-driven workflow. It does not by itself establish who possessed authority to make the decision.

AADAG therefore separates two questions:

**What did the system do?**

**Who owned the authority and consequences of the decision?**

This distinction will be tested throughout the case study.

## What would count as a successful test?

AADAG does not need to produce a perfect numerical answer.

The test is useful if the framework can consistently:

* identify the actual decision being governed;
* distinguish low-consequence uses from consequential uses of the same AI capability;
* describe AI influence without ambiguity;
* identify where meaningful human authority is required;
* expose unclear ownership or delegation;
* identify decisions whose consequences remain undetermined; and
* do this without creating a heavyweight assessment process.

## What would count as a failure?

The case study should also record where AADAG breaks.

Potential failure signals include:

* consequence levels that cannot be assigned consistently;
* influence categories that overlap or leave gaps;
* human-authority requirements that cannot be derived from the classification;
* delegation or authorization information that cannot be identified clearly;
* different reviewers reaching radically different classifications from the same facts; or
* an assessment process that becomes too complicated for routine organizational use.

Those outcomes would be development findings, not reasons to hide the test.

## Next pass

The next step is to take each of the ten candidate decision points individually and assign:

**Decision → Consequence → Influence → Human Authority**

Each assignment should include a short rationale and any uncertainty encountered.

The framework should remain unchanged during the first pass. Problems found during the exercise will be collected and evaluated after the full architecture has been tested.

## Working takeaway

> **Capability does not grant authority.**

Agentic AI makes it increasingly possible for systems to participate in, recommend, advance, and execute decisions. AADAG is being developed to help organizations decide how much of that influence is appropriate for a particular decision and what human authority must remain when the consequences increase.
