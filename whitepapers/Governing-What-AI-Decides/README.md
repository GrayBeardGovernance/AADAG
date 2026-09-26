# Governing What AI Decides

## Moving Beyond Static Compliance to Decision-Centric Accountability

### AI Assisted Decision Accountability & Governance (AADAG)

**AADAG Working Paper 001**  
**Version 0.1.1 | September 2026**

**Edward Magno**  
Gray Beard Governance

---

## Working Paper Status

This paper documents the current development of the AI Assisted Decision Accountability & Governance (AADAG) framework. It reflects the decision classification model established in AADAG v0.2 and findings from pressure testing that are informing the development of v0.3.

AADAG remains under active development. The safeguard model described in this paper is not yet complete. Additional scenario testing and safeguard mapping will continue as v0.3 develops.

This paper will be updated as that work progresses.

---

## Executive Summary

Organizations are adopting artificial intelligence quickly, forcing governance programs to address new systems, new uses, and new forms of decision authority. AI inventories, model evaluations, risk documentation, and human review requirements have become part of that effort.

The AI Assisted Decision Accountability & Governance (AADAG) framework focuses on the decisions AI helps shape. It begins with a straightforward question: **What decision is AI actually helping us make?**

AADAG uses the individual decision as the starting point for governance. That means identifying the decision AI is influencing, determining what could happen if that decision is wrong, measuring how much influence AI has over the outcome, and documenting the people and authorities responsible for it.

AADAG v0.2 established the framework's decision classification foundation. Testing that foundation produced several findings that are now shaping v0.3. Human approval can lose its value when the reviewer lacks enough information or an independent basis to challenge an AI recommendation. An override can become ineffective when the person responsible for using it cannot act within the available decision window. At machine speed, individual human review can become impractical, moving human authority toward the boundaries that define what the system is allowed to decide.

These findings support the central rule guiding the next phase of AADAG:

> **As decision consequence and AI influence increase, the strength of evidence, oversight, traceability, intervention, and recourse must increase with them.**

AADAG provides a structure for applying that rule to an actual decision.

---

# 1. The Governance Problem

AI governance often begins with the technology. Organizations inventory AI systems, identify approved models, evaluate vendors, document model risks, establish acceptable use policies, and monitor technical performance.

AADAG adds the decision layer. A model may summarize information for an employee, identify which transaction deserves investigation, prioritize security alerts, recommend whether an applicant advances in a hiring process, or automatically isolate a compromised endpoint. These decisions have different consequences, different levels of AI influence, and different requirements for human authority.

AADAG begins by asking: **What decision is AI helping us make?** From there, the framework examines what happens if the decision is wrong, how much influence AI has over the outcome, who has authority over the decision, and what evidence and safeguards support that authority.

These questions establish the structure needed to govern the decision.

---

# 2. The AADAG Decision Model

AADAG v0.2 introduced a structured method for examining AI influenced decisions through consequence, influence, and accountability.

**Consequence** describes what could happen if the decision is wrong. **Influence** describes how much control AI has over the outcome. **Accountability** establishes who is responsible for authorizing, reviewing, challenging, and correcting the decision.

Consequence is classified before safeguards are considered. This establishes a baseline view of the potential impact of an incorrect decision. AI influence is then classified according to the authority AI has in producing the outcome. Accountability identifies the people and authorities responsible for the resulting decision environment.

Together, these dimensions establish the foundation for the AADAG Decision Inventory.

---

# 3. Decision Consequence

Decision consequence describes the potential impact of an incorrect AI influenced decision. AADAG v0.2 uses a working scale ranging from C0 through C4, with CU used when there is insufficient information to determine the consequence responsibly.

**CU — Undetermined:** The potential consequence of an incorrect decision cannot yet be determined with sufficient confidence. Additional information or analysis is required before assigning a consequence level.

**C0 — Negligible:** An incorrect decision has no meaningful adverse effect. Any resulting inconvenience is trivial and readily corrected.

**C1 — Limited:** An incorrect decision may cause minor disruption or inconvenience. Effects are identifiable and can be corrected through routine action.

**C2 — Moderate:** An incorrect decision may cause meaningful adverse effects requiring deliberate corrective action.

**C3 — Significant:** An incorrect decision may cause substantial harm involving people, rights, access, finances, security, opportunity, reputation, or mission outcomes. Correction may require significant intervention and some effects may persist.

**C4 — Critical:** An incorrect decision may cause lasting harm involving life, safety, fundamental rights, major financial or material loss, critical security interests, or essential mission functions. Effective correction may be difficult or impossible.

The classification question is direct: **What could happen if this decision is wrong?**

Safeguards are evaluated later in the process. Keeping them out of the initial consequence classification establishes a consistent baseline for determining how much governance the decision requires.

CU addresses cases where that baseline cannot yet be established. During framework testing, CU proved useful because it recorded uncertainty without forcing a consequence classification. Missing information could then be identified and investigated as part of the governance process.

---

# 4. AI Influence

AI Influence describes how much authority AI has over the outcome. AADAG uses four influence levels: Inform, Recommend, Presume, and Decide.

The v0.2 influence model defines the four levels as follows:

**Inform:** AI provides information, analysis, or context for consideration. The human evaluates the information and retains responsibility for determining what action, if any, to take. AI may identify, summarize, analyze, prioritize, or flag information without leaving this level, provided it does not propose a decision or action.

**Recommend:** AI proposes a decision, action, or ranked set of options for human consideration. The human retains authority to accept, reject, or modify the recommendation, and human action is required for it to become the decision.

**Presume:** AI establishes a default decision or action that will take effect unless a human intervenes. A human retains the authority and opportunity to change or override the outcome before it takes effect.

**Decide:** AI selects or executes a decision without requiring case-by-case human approval. Human authority is exercised through the rules, limits, oversight, and ability to modify or stop the AI's decision-making authority.

These definitions and boundaries are the current v0.2 working influence model.

---

# 5. The Consequence × Influence Matrix

The two classifications can be viewed together to identify where an AI influenced decision sits within the AADAG model.

| Consequence | Inform | Recommend | Presume | Decide |
| --- | :---: | :---: | :---: | :---: |
| **C4 Critical** | C4 / Inform | C4 / Recommend | C4 / Presume | C4 / Decide |
| **C3 Significant** | C3 / Inform | C3 / Recommend | C3 / Presume | C3 / Decide |
| **C2 Moderate** | C2 / Inform | C2 / Recommend | C2 / Presume | C2 / Decide |
| **C1 Limited** | C1 / Inform | C1 / Recommend | C1 / Presume | C1 / Decide |
| **C0 Negligible** | C0 / Inform | C0 / Recommend | C0 / Presume | C0 / Decide |

CU remains outside the matrix because it represents an unresolved consequence classification. A CU decision requires additional information before its position in the matrix can be established.

The matrix does not currently assign a fixed safeguard package to each cell. That work is the focus of AADAG v0.3.

Its current purpose is to establish the two conditions that determine the starting point for safeguard analysis: **how consequential the decision is and how much authority AI has over the outcome.**

---

# 6. The Decision Inventory

The Decision Inventory documents the structure surrounding an AI influenced decision. It connects the consequence and influence classifications to the people, authority, evidence, and review mechanisms involved in making that decision.

The v0.2 Decision Inventory contains nine fields:

| Field | Governance Question |
| --- | --- |
| Decision | What decision is AI helping make? |
| Affected Parties | Who could be affected if the decision is wrong? |
| Consequence | CU, C0, C1, C2, C3, or C4 |
| AI Influence | Inform, Recommend, Presume, or Decide |
| Human Authority | What authority do people retain over the decision or decision process? |
| Decision Owner | Who is accountable for the decision and its outcomes? |
| Authorizing Authority | Who authorized this level of AI influence? |
| Basis | What information, criteria, need, or reasoning supports the decision? |
| Review / Recourse | How can the decision be challenged, corrected, or reversed? |

The inventory creates a record of decision authority. As AI influence increases, that record establishes who authorized the AI's role, what authority was delegated, and what mechanisms exist to review the resulting decisions.

Detailed evidence for an individual decision instance is not added as a separate v0.2 inventory field. The v0.2 failure reconstruction test identified decision-instance traceability as a safeguard consideration carried forward into v0.3.

A completed inventory should make it possible to answer a central AADAG question: **Who authorized this system to influence this particular class of decision this much?**

---

# 7. Testing Method

AADAG v0.2 was subjected to exploratory scenario based pressure testing after the initial classification model was established. The purpose of this testing was to examine how the framework behaved when applied to different types of AI influenced decisions and to identify areas where the model required additional development.

The scenarios included fraud restrictions, insider risk decisions, endpoint isolation, privileged production access, employment related decisions, and autonomous operational systems. The scenarios varied in consequence, AI influence, decision speed, human involvement, and the authority granted to the AI system.

Each scenario was examined using the AADAG classification model and Decision Inventory. Testing focused on whether the decision could be identified clearly, whether consequence and influence could be classified, whether decision authority could be traced, and whether the stated human controls remained meaningful under the operating conditions of the scenario.

These exercises were exploratory framework tests. They were designed to pressure test the structure and expose weaknesses, ambiguities, and unanswered questions in AADAG. They should not be interpreted as empirical validation of the framework or as evidence of effectiveness in deployed organizations.

The testing produced several findings that directly influenced the development of v0.3.

---

# 8. Finding 1: Approval Is Not Necessarily Control

One pressure test, referred to during development as **Machine 14**, examined a high consequence AI recommendation requiring supervisory approval. The supervisor had final authority, and AI could not execute the decision independently.

The test examined the information and capability available to the supervisor when making that decision. A supervisor receiving information selected and framed by AI may have limited ability to independently evaluate the recommendation. The same issue arises when the reviewer cannot reconstruct how the recommendation was reached or lacks access to information that would support a different conclusion.

The supervisor retains formal approval authority under these conditions, while the practical ability to evaluate the recommendation depends on the information, time, authority, and independent basis available to the reviewer.

The individual pressure test produced an exploratory finding. Taken together with subsequent tests, it supports the following emerging v0.3 synthesis:

> **Finding 01 — Review Capability**  
> **Human review should be evaluated by capability, not presence.**

The testing identified several factors affecting that capability, including information available to the reviewer, authority to reject the recommendation, subject matter competence, time available for review, access to the decision basis, and an independent means of challenging the recommendation.

These factors provide measurable characteristics for evaluating human review within an AI influenced decision process.

---

# 9. Finding 2: The Practical Opportunity to Override

The fraud pressure test examined a system that could identify suspicious activity and initiate a restriction unless an analyst intervened. The analyst had authority to override the action.

The test introduced decision volume and timing into the scenario. An analyst handling a manageable number of cases could review the AI generated action and intervene when necessary. Increasing the volume to hundreds or thousands of machine generated actions within short decision windows changed the analyst's practical ability to exercise that authority.

The override remained available in the system. Its operational value depended on whether the analyst could use it before the decision took effect.

The individual pressure test produced an exploratory finding. Taken together with the surrounding tests, it supports the following emerging v0.3 synthesis:

> **Finding 02 — Practical Override**  
> **Human control must be operationally achievable within the decision window.**

Decision volume, staffing, response time, information availability, escalation paths, and the amount of time between the AI generated action and execution all affect the practical opportunity to intervene. These factors provide a basis for evaluating whether an override functions as an effective safeguard under actual operating conditions.

---

# 10. Finding 3: Governing Autonomous Velocity

The autonomous warehouse pressure test pushed AADAG to the upper end of both classification dimensions: **C4 consequence and Decide level AI influence**.

The environment involved autonomous decisions occurring at a speed and volume that made case level human approval impractical. Testing therefore focused on the authority surrounding those decisions and the operating conditions established for the autonomous system.

That authority can be expressed through operating boundaries, permitted decision classes, prohibited actions, thresholds, escalation conditions, monitoring requirements, drift detection, emergency suspension authority, recovery procedures, and authorization to resume operations.

At this level, human governance occurs at the boundary of the autonomous decision environment. The human governs the **decision authority granted to the machine**.

The individual pressure test produced an exploratory finding. Taken together with the surrounding tests, it supports the following emerging v0.3 synthesis:

> **Finding 03 — Autonomous Boundaries**  
> **When case level intervention becomes impractical, human control must move to the boundaries governing autonomous decision authority.**

For Decide level systems, those boundaries become a major part of the governance structure. They establish what the system may decide, the conditions under which it may operate, and the points at which human authority must intervene.

---

# 11. Toward Proportional Safeguards

The pressure tests gave us a clearer question for v0.3:

> **Given Consequence C0–C4 and Influence Inform–Decide, which safeguards are required, and how strong do they need to be?**

The tests identified several candidate safeguard characteristics that may help answer that question. Evidence needs to show how the decision was reached and provide enough information to reconstruct its basis. Authority establishes who permitted AI to operate at the assigned influence level and who remains responsible for that authority.

Review examines what the human reviewer can actually evaluate. This includes the information available, the time allowed, and the ability to challenge the AI generated result. Intervention addresses whether someone can stop or alter an outcome within the available decision window.

Traceability provides a record of what occurred during and after the decision. Recourse provides a path for an incorrect decision to be challenged, corrected, or reversed.

Boundary control becomes especially important at the Decide level. The organization needs defined and enforceable limits around what the system is authorized to decide, along with the conditions that trigger escalation, suspension, or human intervention.

These candidate characteristics are informing the development of AADAG v0.3 and remain subject to additional pressure testing and synthesis. They provide the structure for moving from a classified decision to the safeguards required to govern it.

---

# 12. The Principle of Proportional Governance

The testing performed so far supports the central rule guiding AADAG v0.3:

> **The greater the consequence and the greater the AI influence, the stronger the required evidence, oversight, traceability, intervention, and recourse.**

Safeguard requirements develop from the combined consequence and AI influence classification. Inform and Recommend decisions place greater emphasis on the quality of information available to the human decision maker and the person's ability to evaluate it. Presume decisions add greater requirements around intervention, timing, workload, and override capacity.

Decide level systems place greater emphasis on authorization boundaries, monitoring, suspension authority, traceability, and evidence of system behavior. These controls govern the authority delegated to the autonomous system and provide mechanisms for identifying and responding to conditions outside that authority.

The Consequence × Influence classification provides the basis for determining the governance requirements surrounding the decision. The safeguard model provides the structure for meeting those requirements.

---

# 13. What Comes Next

AADAG v0.2 established the classification structure for AI influenced decisions through consequence, influence, accountability, and the Decision Inventory. The pressure testing that followed produced three findings that are shaping safeguard development in v0.3.

> **Human review should be evaluated by capability, not presence.**

> **Human control must be operationally achievable within the decision window.**

> **When case level intervention becomes impractical, human control must move to the boundaries governing autonomous decision authority.**

The next development phase will map safeguards across the Consequence × Influence matrix and continue testing them against different decision environments. This work will establish the relationship among the decision being made, the consequence of getting it wrong, the authority given to AI, and the strength of governance required around that authority.

---

# About the Author and Project

**Edward Magno** is the creator of the AI Assisted Decision Accountability & Governance (AADAG) framework and publishes his work through **Gray Beard Governance**. AADAG is an independently developed framework exploring decision centered governance for artificial intelligence.

The AADAG repository is the public working home of the framework. It contains the current framework, development history, testing artifacts, and working paper releases.

**Project**

[AADAG on GitHub](https://github.com/GrayBeardGovernance/AADAG)

**Follow the work**

[The Gray Beard on Substack](https://substack.com/@thegraybeard)  
[Edward Magno on LinkedIn](https://www.linkedin.com/in/edward-magno-161a19323/)

**Document:** AADAG Working Paper 001  
**Version:** 0.1.1  
**Published:** September 2026  
**Status:** Working Paper

## Suggested Citation

Magno, Edward. *Governing What AI Decides: Moving Beyond Static Compliance to Decision-Centric Accountability.* AADAG Working Paper 001, Gray Beard Governance, Version 0.1.1, September 2026.
