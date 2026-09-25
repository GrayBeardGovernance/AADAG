# AADAG v0.2 Validation Record

## Purpose

This record documents the end-to-end testing performed during development of AADAG v0.2 Decision Classification.

The goal was to pressure-test the framework as written, identify ambiguity or unnecessary complexity, and determine whether the Decision Path and Decision Inventory remained useful across different consequence and AI influence conditions.

Testing was exploratory rather than a formal validation study. Findings that require broader evidence or field testing are carried forward rather than treated as settled conclusions.

## Test method

Each scenario was evaluated using the AADAG Decision Path:

> **Decision → Consequence → Influence → Human Authority**

Where appropriate, the scenario was then expanded into the nine-field Decision Inventory:

1. Decision
2. Affected Parties
3. Consequence
4. AI Influence
5. Human Authority
6. Decision Owner
7. Authorizing Authority
8. Basis
9. Review / Recourse

Tests looked for:

- fields that became unclear or redundant
- missing governance information
- contradictions between the Decision Path and Decision Inventory
- accountability gaps as AI influence increased
- unnecessary documentation burden
- behavior when information was incomplete

## Scenario 1: Privileged production access

### Scenario

AI evaluates a request for privileged administrator access to a production financial system and recommends approving or denying the request. A designated access approver makes the final decision.

### Assessment

- **Decision:** Should this employee receive privileged administrator access to the production financial system?
- **Consequence:** C3 Significant
- **AI Influence:** Recommend
- **Human Authority:** A designated access approver accepts, rejects, or modifies the recommendation before access is granted.

### Result

The Decision Path produced a concise governance view and expanded into the full Decision Inventory without requiring the original assessment to be reinterpreted.

### Finding

The Decision Path can function as a concise representation of the larger inventory. Further testing is needed before defining when a concise assessment is sufficient.

## Scenario 2: Employee training information

### Scenario

AI analyzes optional employee training activity and surfaces courses that may be relevant to an employee's role. It does not recommend a course or enroll the employee.

### Assessment

- **Decision:** What potentially relevant training information should be surfaced to the employee?
- **Consequence:** C1 Limited
- **AI Influence:** Inform
- **Human Authority:** The employee decides whether the information is useful and whether to act on it.

### Result

The Decision Path remained useful with little assessment overhead. The full nine-field inventory remained workable but felt comparatively formal for the low-consequence use case.

### Finding

Assessment depth may need to be proportional to the governance need. Future testing should determine when the Decision Path is sufficient, when the full Decision Inventory should be documented, and when deeper analysis is warranted.

## Scenario 3: Fraud account restriction

### Scenario

AI evaluates account activity for suspected fraud and establishes a temporary restriction that will take effect unless an authorized fraud analyst intervenes during a defined review period.

### Assessment

- **Decision:** Should access to this customer's account be temporarily restricted pending fraud verification?
- **Consequence:** C3 Significant
- **AI Influence:** Presume
- **Human Authority:** Authorized fraud personnel can review, stop, or override the restriction before it takes effect.

### Result

The inventory remained usable when no case-by-case human approval was required to initiate the outcome.

### Finding

Decision ownership depends on the organization's defined accountability structure. AADAG should identify the accountable role rather than prescribe the same owner for every organization. Decision Owner and Authorizing Authority remain distinct because the roles may differ.

## Scenario 4: Automated endpoint isolation

### Scenario

An AI-enabled security system monitors a production environment. When defined indicators show an endpoint is actively compromised, AI can isolate the endpoint immediately without case-by-case human approval. Authorized security personnel can investigate, restore connectivity, or suspend the AI's isolation authority.

### Assessment

- **Decision:** Should this endpoint be isolated from the network because of suspected active compromise?
- **Consequence:** C3 Significant
- **AI Influence:** Decide
- **Human Authority:** Authorized security personnel establish operating rules and limits, monitor actions, restore connectivity, and modify or suspend the AI's decision authority.

### Result

Human Authority and Decision Owner remained meaningful even when no person approved the individual decision before it occurred.

### Finding

Human accountability can exist at the governance and process level when AI operates at Decide. AADAG can distinguish ownership of the decision outcome from authorization of AI's decision-making authority.

## Failure reconstruction test

The endpoint-isolation scenario was extended with an incorrect AI decision. A legitimate administrative process was mistaken for compromise, the endpoint was isolated, and a production service was disrupted before authorized personnel restored connectivity.

### Result

The Decision Inventory provided a structured way to identify:

- what decision was made
- who could be affected
- the consequence classification
- the authority AI had
- the authority humans retained
- who owned the decision
- who authorized the AI's influence
- the basis intended to support the decision
- how the outcome could be reviewed or corrected

### Accountability finding

When an AI-influenced decision fails, the Decision Inventory provides a structured governance record for reconstructing what happened, what authority AI had, what authority humans retained, who owned the outcome, who authorized the AI's influence, and what supported the decision.

The test also exposed a boundary. The inventory describes the governance arrangement and decision basis, but it does not necessarily record the detailed evidence of an individual decision instance.

### Safeguard finding

Higher consequence and/or higher influence decisions may require sufficient decision traceability to reconstruct the information, criteria, AI output, and resulting action for an individual decision.

This is carried forward as a safeguard consideration rather than an additional Decision Inventory field.

## Scenario 5: Incomplete insider-risk use case

### Scenario

An organization proposes an AI feature that analyzes employee activity and flags possible insider risk. The initial description does not explain what data is used, what happens after a flag, how much authority AI has, or what review and recourse mechanisms exist.

### Assessment

- **Decision:** Unresolved pending clarification of what organizational decision follows a flag
- **Consequence:** CU Undetermined
- **AI Influence:** Undetermined pending clarification of the workflow
- **Human Authority:** Undetermined pending clarification of the workflow

### Result

AADAG did not require an assessor to invent answers when information was unavailable. CU represented unresolved consequence, while other inventory fields could be recorded as unknown, unresolved, or to be determined.

### Finding

AADAG can expose missing governance information and identify questions that must be answered before classification can be completed. CU remains specific to consequence classification. Separate undetermined classifications were not added for other fields.

## Overall findings

The v0.2 end-to-end tests did not identify a structural issue requiring redesign of the Decision Path or nine-field Decision Inventory.

The tests produced several items for continued development:

1. Test the Decision Path as a distilled view of a completed assessment.
2. Determine how assessment depth should scale with governance need.
3. Prefer Human Authority terminology where it more clearly describes retained human control.
4. Explore decision-instance traceability as part of safeguard mapping.
5. Continue testing CU and incomplete-information scenarios during field testing.

These findings do not establish universal thresholds or safeguard requirements. Those questions remain subject to later development and field testing.

## v0.3 exploratory finding: Candidate sourcing

An AI system may remain at the **Inform** influence level while materially shaping the options available to a human decision maker.

In the candidate-sourcing scenario, AI filtered a pool of 2,000 potential candidates to 50 candidates normally reviewed by the recruiter. The recruiter retained authority over whom to contact, but that authority was exercised primarily over the candidate set surfaced by AI.

**Finding:** Influence classification alone may not fully determine safeguard needs. Safeguard assessment may also need to consider whether AI materially limits, filters, or shapes the options available to the human decision maker.

**Status:** Exploratory. Requires additional pressure testing before incorporation into the framework.

## v0.3 exploratory finding: Filtering and retained human authority

A second Inform-level pressure test examined routine news monitoring. AI filtered thousands of articles to a small set for an analyst, materially shaping the information available for review. The decision was treated as C1 Limited because an incorrect filtering decision in the tested scenario would have only limited consequences.

The test showed that substantial AI filtering alone does not necessarily justify strong safeguards. The consequence of the decision remains important in determining how rigorously the filtering should be governed.

**Finding:** Where AI materially shapes the information or options available to a human decision maker, safeguards should provide a means appropriate to the consequence level for the human to examine, challenge, or move beyond the AI-selected information.

This refines the candidate-sourcing finding. AI Influence describes how AI participates in the decision, while safeguard design may also need to consider whether AI's role affects the human's practical ability to exercise retained authority.

**Status:** Exploratory. Requires additional pressure testing before incorporation into the framework.

## v0.3 pressure test: Meaningful human review

### Scenario

A manufacturing company uses AI to analyze sensor readings, maintenance history, operating conditions, and inspection records for production equipment.

The AI recommends that Machine 14 be taken offline for immediate maintenance. A maintenance supervisor must accept or reject the recommendation before anything happens.

Taking the machine offline could halt a production line for several hours. Ignoring a correct recommendation could allow equipment damage or create a safety hazard.

### Classification

- **Decision:** Should Machine 14 be taken offline for immediate maintenance?
- **Affected Parties:** Operators, maintenance personnel, the company, and potentially customers affected by disrupted production
- **Consequence:** C3 Significant
- **AI Influence:** Recommend
- **Human Authority:** A maintenance supervisor retains authority to accept, reject, or modify the recommendation

Distilled through the Decision Path:

> **Machine shutdown → C3 Significant → Recommend → Maintenance supervisor approval**

### What was tested

The test examined whether requiring human review is sufficient as a safeguard for a higher-consequence Recommend-level decision.

A supervisor could technically review an AI recommendation presented only as:

> Machine 14  
> Failure risk: HIGH  
> Recommendation: IMMEDIATE SHUTDOWN  
> ACCEPT / REJECT

The supervisor retains formal approval authority, but may lack sufficient information to independently evaluate the recommendation.

### Finding: Meaningful human review

Requiring human approval does not by itself establish meaningful human control. A reviewer may formally approve or reject an AI recommendation while lacking sufficient information to evaluate it independently.

**Finding:** Human review is meaningful only when the reviewer has sufficient information and authority to independently accept, reject, or modify the AI-influenced outcome.

The information required to support meaningful review should be proportionate to the consequence of an incorrect decision. Higher-consequence decisions may require stronger supporting information, reviewer qualifications or authority, and evidence that review occurred.

This finding connects **Basis**, **Human Authority**, and safeguard rigor without requiring AI systems to expose internal reasoning as a universal safeguard.

**Status:** Exploratory. Requires additional pressure testing before incorporation into the framework.

