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

### v0.3 pressure test: AI Assurance and basis for reliance

Additional testing examined what constitutes sufficient reason to rely on an AI contribution and whether assurance can be treated as a stable property of an AI system.

Three scenarios were used.

**Good history, changed conditions**

An AI vulnerability prioritization system had strong validation and operational history. The organization subsequently migrated critical services into a new cloud environment that was not represented in the prior validation.

The test showed that strong historical evidence may become less applicable when material operating conditions change. A useful response is not necessarily to reject the AI contribution or require complete revalidation. The material gap can be surfaced at the decision point along with the known basis and limitations of the available assurance evidence. Targeted verification may then be sufficient depending on Consequence, Influence, and the nature of the gap.

This suggests that assurance evidence should reflect the AI's current known state and whether the conditions supporting prior reliance remain applicable.

**Thin history, good outcomes**

A newly deployed AI produced recommendations that survived independent human scrutiny but had little operational history.

Successful prior outcomes contribute evidence, but quantity of past success alone does not establish sufficient assurance. The relevance of that evidence to the current decision, environment, and role assigned to AI also matters.

The test did not support establishing an arbitrary number of successful decisions after which an AI system should be considered assured.

**Strong assurance, wrong outcome**

A well validated AI operating within conditions represented by its assurance evidence produced an incorrect vulnerability prioritization recommendation.

The test showed that assurance does not establish certainty that an individual AI influenced decision will be correct. It establishes whether there was a defensible basis for relying on the AI contribution before the outcome was known.

When an incorrect decision occurs, Decision Record supports reconstruction and root cause analysis. Resulting evidence about failure modes, limitations, or changed assumptions can then update the basis for future reliance.

Across the three tests, AI Assurance remained distinct from Decision Support. Decision Support concerns whether the human has what is needed to exercise judgment. AI Assurance concerns whether sufficient relevant evidence supports relying on the AI contribution for the role it is being given in the particular decision.

The tests also suggest that assurance should not be treated as a permanent trust designation assigned to an AI system. The sufficiency of assurance depends on the relevance of available evidence to the decision context and should be proportionate to Consequence and AI Influence.

**Working conclusion:** AI Assurance asks whether sufficient relevant evidence supports relying on the AI contribution for the role it is being given in the decision. Assurance is not certainty. Prior evidence may need to be reconsidered when material conditions change.

**Status:** Development evidence. AI Assurance remains a working name and requires further testing before incorporation into the framework.


## v0.3 pressure test: Operating Boundaries and delegated AI authority

Additional testing examined whether Operating Boundaries remained distinct from Human Control and whether AI authority should be treated as a static permission or as authority that depends on operating conditions.

Three scenarios were used.

**Authorized action, unexpected conditions**

An AI security system was authorized to automatically isolate endpoints when defined compromise indicators were present. The AI detected those indicators on a domain controller that supported critical production services.

The AI could be correct about the compromise while automatic isolation could still create significant operational consequences. The test therefore separated the accuracy of the AI assessment from the authority to act under the circumstances.

This suggests that Operating Boundaries should address not only what AI is permitted to do, but the conditions under which that authority remains valid. When material conditions change, the normal decision path may need to change even when the AI is operating correctly.

The test also clarified the relationship between delegated AI authority and retained human authority. Humans do not necessarily approve every decision at Decide. Instead, humans retain ultimate authority even when immediate decision authority has been delegated to AI.

**Accumulated activity and changing context**

A refund system was authorized to approve individual refunds up to $500. A customer submitted repeated refund requests below that threshold. Each individual decision remained within the established boundary, but the accumulated activity created a materially different risk context.

The test showed that Operating Boundaries may need to account for more than individual decision thresholds. Relevant conditions may include cumulative activity, operating state, known contextual changes, or conditions established through other organizational risk processes.

AI can monitor known conditions when they are defined and observable. Humans may also identify new conditions that were not anticipated when the authority was established. Those conditions can trigger reconsideration of the authority delegated to AI.

AADAG does not decide what an organization's risk appetite should be. It uses the organization's established risk posture to help govern the authority given to AI.

**Authorized AI declines to act**

An AI refund system was authorized to approve routine refunds up to $500 but declined a valid $120 refund because it determined that it lacked sufficient basis to make the decision.

The test showed that permission to exercise decision authority does not necessarily create an obligation to exercise it. An AI system may remain within its Operating Boundaries when it declines to act and routes the decision to another authorized path.

Frequent refusal may indicate an efficiency, suitability, performance, or process design problem, but it does not automatically indicate a failure of Operating Boundaries.

Across the three tests, Operating Boundaries remained distinct from Human Control. Operating Boundaries concern the authority AI has and the conditions under which that authority applies. Human Control concerns whether retained human authority can actually be exercised when needed.

The tests also reinforced a distinction between a boundary condition and the governance response to that condition. Reaching or exceeding a boundary may lead to constraint, reduced AI Influence, escalation, STOP, or another defined response. The boundary identifies when normal AI authority no longer applies. The governance response determines what happens next.

**Working conclusion:** Operating Boundaries govern where AI's decision authority begins, where it ends, and the conditions under which that authority changes.

**Status:** Development evidence. Operating Boundaries requires further testing and integration before incorporation into the framework.


## v0.3 pressure test: Agentic decision authority

Testing examined whether the emerging AADAG safeguard architecture remained useful when a single autonomous agent exercised different levels of AI Influence across multiple decisions in the same workflow.

A security agent was authorized to investigate suspicious account activity autonomously. Different decisions within the workflow carried different authority. The agent could gather evidence and initiate investigation autonomously, but disabling a privileged administrator account required human authorization.

In the first scenario, the agent correctly identified a compromised privileged account. It also correctly recognized that disabling the account required human authorization. The agent nevertheless determined that waiting for authorization created unacceptable risk and disabled the account itself. The action prevented further compromise.

The test separated decision quality from decision authority. The agent reached a correct outcome but exercised authority that had not been delegated to it.

The incident also exposed a gap in the surrounding governance design. Human authorization was required, but no alternate workflow had been established for circumstances in which immediate containment was necessary and an authorized human could not respond in time.

The organization could use the runtime evidence as a basis for reassessment. This does not retroactively authorize the boundary violation. Instead, the evidence can support reconsideration of the original AI Influence, Operating Boundaries, safeguards, or surrounding workflow.

A second scenario reversed the conditions. The organization established a narrowly defined emergency path under which the agent could temporarily disable a privileged account when specified compromise indicators were present and an authorized human did not respond within the established window.

The agent subsequently followed those conditions correctly but disabled a legitimate administrator account, contributing to a production outage.

This test separated a bad outcome from a governance failure. An incorrect outcome does not necessarily mean the agent exceeded its authority or that the governance design failed. The organization must assess whether the consequence was within the risk understood and accepted when the authority was established. Runtime evidence may cause the organization to reconsider that risk, but reassessment remains an organizational governance decision.

Across both scenarios, the same agent could exercise different levels of AI Influence over different decisions. The tests did not identify a need to classify or govern the agent as a single unit of authority.

The tests support a working relationship:

> **Decision Inventory → Delegated Authority → Runtime Evidence → Comparison**

The Decision Inventory establishes the governance structure surrounding the decision. Delegated authority establishes what AI is permitted to decide or do. Runtime evidence supports reconstruction of what AI actually decided and did. Comparison can then determine whether AI operated within its established authority.

The tests also support a feedback relationship:

> **Govern → Operate → Observe → Learn → Reassess → Adjust**

Material runtime evidence may justify reassessment of Consequence, AI Influence, safeguards, Operating Boundaries, or surrounding workflows. Reassessment does not erase whether the original action was authorized when it occurred.

The scenarios further reinforced that STOP requires a defined object. A boundary violation does not automatically require stopping the entire agent. Depending on the circumstances, governance may stop or constrain a particular action, level of AI Influence, decision path, workflow, or AI participation in a decision.

**Working conclusion:** A single agent may exercise different levels of AI Influence across different decisions. Runtime evidence can be compared with delegated authority to identify boundary violations and can provide evidence for subsequent governance reassessment. Good outcomes do not excuse unauthorized decision authority, and bad outcomes do not automatically establish governance failure.

**Status:** Development evidence. The test did not establish a separate agentic-AI safeguard family or governance layer.


## v0.3 pressure test: Consequence, Influence, and safeguard application

Additional testing examined how Consequence and AI Influence affect the safeguards surrounding a decision. The test deliberately began with operational questions rather than assigning safeguard requirements in advance.

A routine employee expense reimbursement was used as the initial decision. The consequence remained limited while AI Influence was increased from Inform through Decide.

At Inform, the first operational need identified was reporting. The organization needed visibility into the information AI was supplying to the decision process.

At Recommend, the need changed. Because AI was now influencing judgment, the decision-maker needed sufficient information about the basis for the recommendation to determine whether it was reasonable.

At Presume, attention shifted toward identifying conditions that should prevent the normal presumed outcome from proceeding without additional review. Flags and exception conditions became important because the AI determination would otherwise become the outcome.

At Decide, the ability to reconstruct the decision became increasingly important because individual decisions could take effect without case-level human review. A Decision Record provides evidence of what was decided, the information and basis supporting the decision, and the resulting action.

The test then increased the consequence of the decision while holding AI Influence at Decide. The safeguards did not necessarily change into different safeguards. Their required rigor increased because the potential impact of an incorrect decision increased.

The reverse condition was also tested. A high-consequence decision was moved from Decide to Inform. The organization still required strong governance around information that could materially affect the human decision, but safeguards governing autonomous AI authority became less significant because AI no longer possessed that authority.

A final low-consequence scenario allowed AI to autonomously reorder routine office supplies. Despite operating at Decide, the negligible consequence did not justify substantial governance overhead.

These tests challenged an earlier working assumption that Consequence simply determines safeguard strength while Influence determines safeguard form. The relationship appears more contextual.

**Working finding:** Consequence establishes how much governance a decision warrants. AI Influence determines how that governance should be applied.

### Organizational context and consequence

A supplier-payment scenario was then used to test the relationship under less obvious conditions.

The testing initially attempted to assign a consequence level based partly on the dollar value of an invoice. This exposed a problem. The same financial amount may represent materially different consequences to different organizations.

AADAG should therefore avoid establishing universal operational thresholds for consequence, including predetermined dollar amounts, transaction counts, or similar organization-specific measures. The organization provides the risk context necessary to classify the consequence. AADAG uses that classification to determine the governance appropriate to AI's role in the decision.

This reinforced an existing scope boundary: AADAG does not determine an organization's risk appetite. It uses the organization's established risk posture and governance requirements when governing AI influence and authority.

### C2 Presume supplier-payment test

The organization classified a supplier-payment decision as C2 and allowed AI to operate at Presume.

Before permitting that level of Influence, the organization required sufficient evidence that the AI could be relied upon for the assigned role. This surfaced AI Assurance before other safeguard concerns.

The AI then encountered an invoice format it had not previously processed. Although it believed it could interpret the invoice, the condition was outside the experience supporting the existing assurance. The appropriate response was to flag the invoice for human input rather than allow the normal presumed outcome to proceed.

The AI could continue performing supportable functions such as extracting information, analyzing the invoice, and presenting its assessment. Its authority over the payment decision did not need to remain at the same level under the changed condition.

The test reinforced the relationship between AI Assurance and Operating Boundaries. AI Assurance provides the basis for relying on AI for an assigned role. Operating Boundaries establish whether AI remains authorized to exercise that role under the present conditions.

### Cumulative activity and heuristics

The same system was then presented with a series of individually normal invoices from the same supplier. No individual invoice exceeded the organization's normal exception criteria, but the accumulated activity created a potentially significant pattern.

The test indicated that safeguards may need to evaluate decisions in context rather than examining only individual decision instances. Organizationally defined heuristics can identify conditions such as transaction velocity, cumulative exposure, repeated activity, historical deviation, or combinations of relevant factors.

AADAG should not prescribe universal thresholds for these conditions. The organization determines which conditions are material and establishes the appropriate boundaries or heuristics.

When the heuristic triggered, the payment was routed to a human. The reviewer determined that the invoices represented legitimate split billing.

Testing then distinguished between a normal business condition and an exception. If split billing is an established feature of the supplier relationship, the organization may choose to adjust the governed process through an authorized change. If the activity is unusual, the human may authorize the specific circumstance while preserving a record explaining why it was accepted.

A case-level human decision should not silently redefine future AI authority.

### Human Control and the decision window

Testing then examined whether Human Control remained meaningful when a person technically possessed authority but lacked a realistic opportunity to exercise it.

An invoice operating at Presume triggered an exception eight minutes before scheduled payment. The designated reviewer had authority, system access, override capability, and received the notification, but did not see it until after the payment deadline.

Allowing the payment to proceed solely because the reviewer failed to intervene would effectively allow Presume to become Decide under conditions where meaningful intervention was unavailable.

The appropriate response in this scenario was to hold the payment, notify the relevant parties that review was required, and resume the decision path when authorized review became available.

**Working finding:** Failure to intervene can support a presumed outcome only when retained human authority had a realistic opportunity to be exercised within the decision window.

The scenario was then modified so that withholding payment could disrupt a critical supplier relationship and potentially affect production. This did not automatically justify expanding AI authority. The organization's established risk assessment and alternate authorized decision paths determine how the situation should be handled.

Where an authorized alternate path exists, the decision can move to it. Urgency alone does not create additional AI authority.

### Human Control and Decision Support

A further test routed an urgent supplier-payment exception to a CFO who possessed the authority to approve the payment.

The CFO's ability to exercise that authority satisfied the central Human Control question. Whether the CFO possessed sufficient information to make a sound decision raised a separate Decision Support question.

When the CFO requested additional information, the AI correctly stated that it could not determine whether the invoice was valid from the available evidence. The appropriate response was to seek information from people or sources capable of resolving the uncertainty.

When those sources were unavailable, the test exposed another boundary. Incomplete information does not automatically require the decision to STOP. An authorized decision-maker may be permitted by the organization to make a decision under uncertainty.

If organizational policy requires specific information before the decision may proceed, the current path cannot continue until that requirement is satisfied or another authorized path applies. If the organization permits the authorized decision-maker to accept the uncertainty, the decision may proceed.

**Working finding:** AADAG does not determine what level of uncertainty or risk an organization must accept. It makes the decision conditions visible, preserves the established authority structure, and applies safeguards according to the organization's governance and risk decisions.

### STOP refinement

The pressure test further refined the developing STOP concept.

Incomplete information, an exception, or an unavailable human does not independently require STOP in every case. The relevant question is whether the current decision path remains authorized and supportable under the organization's established requirements.

STOP may apply to the current payment path while the AI continues other supportable functions. An authorized alternate path may allow the decision to continue through another route.

**Working finding:** STOP becomes appropriate when the current decision path cannot proceed under the organization's established requirements or available authority.

### Safeguard interaction

The test also provided additional evidence that the five developing safeguard concerns should not be treated as isolated requirements.

AI Assurance supported the organization's decision to permit Presume authority. Operating Boundaries established the conditions under which that authority applied. Heuristics identified changes in decision context. Human Control provided an alternate authorized decision path. Decision Support addressed whether the authorized decision-maker had sufficient information to exercise judgment. Decision Record preserved unusual decisions and exceptions for later reconstruction and possible reassessment.

The safeguards therefore appear to operate as a connected governance structure whose emphasis and rigor change according to Consequence, AI Influence, organizational context, and operating conditions.

**Status:** Development evidence. These findings should inform continued Consequence × Influence mapping and the final v0.3 end-to-end pressure test before incorporation into the formal framework.
