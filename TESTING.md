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

Tests looked for fields that became unclear or redundant, missing governance information, contradictions between the Decision Path and Decision Inventory, accountability gaps as AI influence increased, unnecessary documentation burden, and behavior when information was incomplete.

## Scenario 1: Privileged production access

### Scenario

AI evaluates a request for privileged administrator access to a production financial system and recommends approving or denying the request. A designated access approver makes the final decision.

### Assessment

**Decision:** Should this employee receive privileged administrator access to the production financial system?

**Consequence:** C3 Significant

**AI Influence:** Recommend

**Human Authority:** A designated access approver accepts, rejects, or modifies the recommendation before access is granted.

### Result

The Decision Path produced a concise governance view and expanded into the full Decision Inventory without requiring the original assessment to be reinterpreted.

### Finding

The Decision Path can function as a concise representation of the larger inventory. Further testing is needed before defining when a concise assessment is sufficient.

## Scenario 2: Employee training information

### Scenario

AI analyzes optional employee training activity and surfaces courses that may be relevant to an employee's role. It does not recommend a course or enroll the employee.

### Assessment

**Decision:** What potentially relevant training information should be surfaced to the employee?

**Consequence:** C1 Limited

**AI Influence:** Inform

**Human Authority:** The employee decides whether the information is useful and whether to act on it.

### Result

The Decision Path remained useful with little assessment overhead. The full nine-field inventory remained workable but felt comparatively formal for the low-consequence use case.

### Finding

Assessment depth may need to be proportional to the governance need. Future testing should determine when the Decision Path is sufficient, when the full Decision Inventory should be documented, and when deeper analysis is warranted.

## Scenario 3: Fraud account restriction

### Scenario

AI evaluates account activity for suspected fraud and establishes a temporary restriction that will take effect unless an authorized fraud analyst intervenes during a defined review period.

### Assessment

**Decision:** Should access to this customer's account be temporarily restricted pending fraud verification?

**Consequence:** C3 Significant

**AI Influence:** Presume

**Human Authority:** Authorized fraud personnel can review, stop, or override the restriction before it takes effect.

### Result

The inventory remained usable when no case-by-case human approval was required to initiate the outcome.

### Finding

Decision ownership depends on the organization's defined accountability structure. AADAG should identify the accountable role rather than prescribe the same owner for every organization. Decision Owner and Authorizing Authority remain distinct because the roles may differ.

## Scenario 4: Automated endpoint isolation

### Scenario

An AI-enabled security system monitors a production environment. When defined indicators show an endpoint is actively compromised, AI can isolate the endpoint immediately without case-by-case human approval. Authorized security personnel can investigate, restore connectivity, or suspend the AI's isolation authority.

### Assessment

**Decision:** Should this endpoint be isolated from the network because of suspected active compromise?

**Consequence:** C3 Significant

**AI Influence:** Decide

**Human Authority:** Authorized security personnel establish operating rules and limits, monitor actions, restore connectivity, and modify or suspend the AI's decision authority.

### Result

Human Authority and Decision Owner remained meaningful even when no person approved the individual decision before it occurred.

### Finding

Human accountability can exist at the governance and process level when AI operates at Decide. AADAG can distinguish ownership of the decision outcome from authorization of AI's decision-making authority.

## Failure reconstruction test

The endpoint-isolation scenario was extended with an incorrect AI decision. A legitimate administrative process was mistaken for compromise, the endpoint was isolated, and a production service was disrupted before authorized personnel restored connectivity.

### Result

The Decision Inventory provided a structured way to identify what decision was made, who could be affected, the consequence classification, the authority AI had, the authority humans retained, who owned the decision, who authorized the AI's influence, the basis intended to support the decision, and how the outcome could be reviewed or corrected.

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

**Decision:** Unresolved pending clarification of what organizational decision follows a flag

**Consequence:** CU Undetermined

**AI Influence:** Undetermined pending clarification of the workflow

**Human Authority:** Undetermined pending clarification of the workflow

### Result

AADAG did not require an assessor to invent answers when information was unavailable. CU represented unresolved consequence, while other inventory fields could be recorded as unknown, unresolved, or to be determined.

### Finding

AADAG can expose missing governance information and identify questions that must be answered before classification can be completed. CU remains specific to consequence classification. Separate undetermined classifications were not added for other fields.

## Overall findings

The v0.2 end-to-end tests did not identify a structural issue requiring redesign of the Decision Path or nine-field Decision Inventory.

Continued development should test the Decision Path as a distilled view of a completed assessment, determine how assessment depth should scale with governance need, prefer Human Authority terminology where it more clearly describes retained human control, explore decision-instance traceability as part of safeguard mapping, and continue testing CU and incomplete-information scenarios during field testing.

These findings do not establish universal thresholds or safeguard requirements. Those questions remain subject to later development and field testing.

## v0.3 exploratory finding: Candidate sourcing

An AI system may remain at the **Inform** influence level while materially shaping the options available to a human decision maker.

In the candidate-sourcing scenario, AI filtered a pool of 2,000 potential candidates to 50 candidates normally reviewed by the recruiter. The recruiter retained authority over whom to contact, but that authority was exercised primarily over the candidate set surfaced by AI.

Influence classification alone may not fully determine safeguard needs. Safeguard assessment may also need to consider whether AI materially limits, filters, or shapes the options available to the human decision maker.

**Status:** Exploratory. Requires additional pressure testing before incorporation into the framework.

## v0.3 exploratory finding: Filtering and retained human authority

A second Inform-level pressure test examined routine news monitoring. AI filtered thousands of articles to a small set for an analyst, materially shaping the information available for review. The decision was treated as C1 Limited because an incorrect filtering decision in the tested scenario would have only limited consequences.

The test showed that substantial AI filtering alone does not necessarily justify strong safeguards. The consequence of the decision remains important in determining how rigorously the filtering should be governed.

Where AI materially shapes the information or options available to a human decision maker, safeguards should provide a means appropriate to the consequence level for the human to examine, challenge, or move beyond the AI-selected information.

This refines the candidate-sourcing finding. AI Influence describes how AI participates in the decision, while safeguard design may also need to consider whether AI's role affects the human's practical ability to exercise retained authority.

**Status:** Exploratory. Requires additional pressure testing before incorporation into the framework.

## v0.3 pressure test: Meaningful human review

A manufacturing company uses AI to analyze sensor readings, maintenance history, operating conditions, and inspection records for production equipment. The AI recommends that Machine 14 be taken offline for immediate maintenance. A maintenance supervisor must accept or reject the recommendation before anything happens.

Taking the machine offline could halt a production line for several hours. Ignoring a correct recommendation could allow equipment damage or create a safety hazard. The decision was classified C3 Significant with AI at Recommend and the maintenance supervisor retaining authority to accept, reject, or modify the recommendation.

The test examined whether requiring human review is sufficient as a safeguard for a higher-consequence Recommend-level decision. A supervisor could technically review an AI recommendation while lacking enough information to evaluate it independently.

Requiring human approval does not by itself establish meaningful human control. Human review is meaningful only when the reviewer has sufficient information and authority to independently accept, reject, or modify the AI-influenced outcome. The information required should be proportionate to the consequence of an incorrect decision. Higher-consequence decisions may require stronger supporting information, reviewer qualifications or authority, and evidence that review occurred.

This finding connects **Basis**, **Human Authority**, and safeguard rigor without requiring AI systems to expose internal reasoning as a universal safeguard.

**Status:** Exploratory. Requires additional pressure testing before incorporation into the framework.

## v0.3 pressure test: Practical opportunity to override

A payment processor uses AI to evaluate transactions for fraud. When the AI determines that a transaction is likely fraudulent, it places a temporary hold on the transaction. A fraud analyst has 15 minutes to override the hold before the transaction is blocked.

The decision was classified C2 Moderate with AI at Presume and a fraud analyst retaining override authority. The test examined whether providing an override mechanism is sufficient as a safeguard.

Assume the analyst has a functioning override control and sufficient information to evaluate the transaction. During the 15-minute intervention window, however, three analysts receive 600 alerts requiring potential review. The authority to override exists and the technical mechanism works, but many decisions may take effect because analysts lack the operational capacity to review them before the intervention window closes.

An override mechanism alone does not establish meaningful human control. An override is meaningful only when a human has a practical opportunity to exercise it before the AI-established outcome takes effect. Practical opportunity may depend on sufficient time, notice, access, information, and operational capacity. The rigor required should be proportionate to the consequence of an incorrect decision.

This supports a broader principle emerging across Inform, Recommend, and Presume: retained human authority must be practically exercisable rather than existing only as formal authority or a technical control.

**Status:** Exploratory. Requires additional pressure testing before incorporation into the framework.

## v0.3 pressure test: Governing Decide authority

A large automated warehouse uses AI to route autonomous material-handling vehicles through the facility. The AI continuously decides which route each vehicle should take based on congestion, worker locations, blocked aisles, delivery priorities, and other vehicle movements. Individual routing decisions occur without case-by-case human approval.

The decision was classified C4 Critical with AI at Decide. Humans establish operating boundaries, monitor the system, modify its authority, and can suspend autonomous operation.

The test examined whether defined operating boundaries and documented accountability are sufficient safeguards for a high-consequence Decide-level process. A temporary construction barrier altered an aisle. The AI began making routing decisions that remained within its original authorization but created a hazardous interaction near the changed work area. No individual decision necessarily violated the established rules. The conditions that supported the original authorization had changed.

At Decide, human control does not depend on case-by-case approval. It operates through governance of the authority delegated to AI. The organization must be able to detect material changes in operating conditions and modify or suspend AI decision authority when necessary.

For higher-consequence Decide processes, safeguards may therefore need to address defined authority, operating boundaries, monitoring, traceability, intervention capability, and identifiable accountability. Retained human authority remains practically exercisable, but at Decide that authority is exercised through governance, monitoring, modification, and suspension of delegated decision authority rather than approval of each individual decision.

**Status:** Exploratory. Requires synthesis and additional validation before incorporation into the framework.

# v0.3 safeguard architecture synthesis

Additional pressure testing was performed after the initial Inform, Recommend, Presume, and Decide scenarios. The purpose was to determine whether the emerging safeguard concepts remained useful as both AI Influence and decision consequence changed.

Five safeguard concerns continued to appear across the tests: Decision Support, AI Assurance, Human Control, Decision Record, and Operating Boundaries. AI Assurance remains a working name.

Decision Support addresses whether people have the information and context necessary to exercise their role in an AI-influenced decision. AI Assurance addresses whether there is sufficient reason to rely on the AI contribution for the decision being made. Human Control addresses whether retained human authority can actually be exercised. Decision Record addresses whether the decision and resulting outcome can be reconstructed when necessary. Operating Boundaries addresses what AI is permitted to do, under what conditions, and when that authority must change or end.

The five concerns remained distinct when tested against the same failure. If AI produces a bad recommendation, Decision Support asks whether the person had enough information to evaluate it. AI Assurance asks whether there was sufficient basis for relying on the AI in the first place. Human Control asks whether an authorized person could meaningfully intervene. Decision Record asks whether the decision can be reconstructed. Operating Boundaries asks whether AI was authorized to exercise that influence under those conditions.

Testing across Inform, Recommend, Presume, and Decide suggested that the safeguard concerns themselves remain relatively stable while their application changes with AI Influence. Inform places greater emphasis on what information is selected, presented, filtered, or omitted. Recommend requires enough information and authority for meaningful human judgment. Presume requires a practical opportunity to intervene before an AI-established outcome takes effect. At Decide, human control shifts away from case-by-case approval and toward governing the authority delegated to AI.

Testing also exposed a recurring issue that was not fully covered by the original four safeguard concepts. Human review, intervention, traceability, and operating limits do not establish that the AI contribution itself is sufficiently reliable for the decision environment. This appeared independently in candidate sourcing, the Machine 14 maintenance scenario, fraud intervention, and autonomous warehouse routing. That repeated finding is the basis for the fifth candidate safeguard, currently called AI Assurance.

A separate test held Recommend constant while consequence increased from C0 through C4. The five safeguard concerns remained usable throughout the range, but the required rigor changed substantially. At low consequence, some safeguards required little beyond ordinary operation. At higher consequence, stronger evidence, review, control, traceability, and operating limits became appropriate. This supports the working conclusion that consequence primarily affects safeguard rigor while Influence primarily affects safeguard form and emphasis.

Presume was then tested across the same consequence range. This exposed an important qualification. A stronger safeguard does not necessarily mean more documentation, more information, or more human intervention. In time-sensitive decisions, adding additional review can make the process less effective. Safeguard strength therefore needs to reflect whether the safeguard actually works within the consequence, Influence, operating conditions, and available decision window.

This also clarified Human Control. Human Control does not mean maximizing human involvement. It means that the human authority retained by the decision process can actually be exercised when it matters.

The tests also continued to surface STOP. When information or operating conditions required to support authorized AI influence are no longer present, the normal decision path may no longer be appropriate. STOP currently appears more useful as a possible governance outcome than as another safeguard family. Constraint, reduced AI Influence, escalation, safe-state operation, and STOP remain under development and have not been established as formal AADAG outcomes.

Two additional tests were used to challenge the emerging Consequence × Influence mapping.

A C3 Presume medication-order scenario showed that a nominal override does not necessarily make a process Presume in practice. If the pharmacist cannot reasonably exercise the override within the available time and workload, AI may effectively be exercising greater authority than the process documentation suggests. This supports classifying Influence according to how the decision process actually operates rather than according to the label assigned to the system.

A C4 Inform emergency-response scenario tested the opposite problem. AI organized and surfaced critical information but did not recommend or initiate an emergency action. Strong Decision Support, AI Assurance, and Decision Record were justified by the consequence, but maximum Human Control and Operating Boundaries were not. This supports keeping Consequence and Influence distinct. C4 does not automatically mean maximum safeguards everywhere.

Taken together, these tests provide strong support for continuing with the five-family safeguard architecture and a proportional Consequence × Influence model. The exact safeguard-strength scale, individual matrix assignments, the final name for AI Assurance, and the treatment of STOP remain open. These results are development evidence and have not yet been incorporated into FRAMEWORK.md.
