# Governing Agentic AI by Decision Authority

## Applying Decision-Centered Governance to Autonomous AI Systems

### Abstract

Agentic AI complicates governance because a single AI system may perform many activities within the same workflow, including gathering information, evaluating evidence, making recommendations, initiating actions, and executing decisions. Describing such a system simply as autonomous does not adequately describe the authority it exercises over the individual decisions within that workflow. The same agent may have substantial autonomy over one decision while remaining limited to an advisory role for another.

This paper examines agentic AI through the decision-centered governance model being developed in the AI Assisted Decision Accountability & Governance (AADAG) framework. Using a privileged-account security scenario, the analysis explores delegated AI authority, Operating Boundaries, runtime evidence, reassessment, and the relationship between decision outcomes and governance accountability. The pressure test suggests that agentic AI does not necessarily require a separate governance structure within AADAG. Instead, individual decisions within an agentic workflow can be governed according to their consequence, level of AI Influence, retained Human Authority, applicable safeguards, and defined Operating Boundaries. Runtime evidence can then provide a basis for determining whether delegated authority remains appropriate as operating experience and conditions change.

## 1. Introduction

Agentic AI systems can perform multiple activities as part of a continuous workflow. A security agent, for example, might collect authentication logs, correlate endpoint events, identify suspicious behavior, open an investigation, recommend containment, and under certain conditions execute a containment action. These activities may occur within the same technical system, but they do not necessarily represent the same level of decision authority.

This distinction creates an important governance problem. Treating the agent as a single unit of autonomy can obscure meaningful differences between the decisions occurring within its workflow. An organization may be comfortable allowing an agent to determine what telemetry to collect while requiring human authorization before a privileged administrator account can be disabled. The technical system remains the same, while its influence and authority differ according to the decision being made.

AADAG begins with the decision AI helps shape. The framework considers the consequence of an incorrect decision, the level of AI Influence over the outcome, the Human Authority retained within the process, and the accountability surrounding that authority. This provides a basis for examining agentic systems without assigning one governance classification to everything an agent does.

The purpose of this paper is to pressure-test that approach against a realistic agentic workflow. The analysis focuses on what happens when an agent encounters the limits of its delegated authority, how runtime evidence can inform later governance decisions, and whether the existing AADAG architecture remains useful as AI systems become increasingly capable of acting without case-by-case human approval.

## 2. Decision Authority Within an Agentic Workflow

Consider an AI security agent responsible for investigating suspicious account activity. During an investigation, the agent may determine which activity requires examination, collect relevant authentication and endpoint telemetry, initiate an investigation, assess the likelihood that an account has been compromised, recommend a containment action, or execute actions for which authority has already been delegated.

These decisions can have different consequences and different levels of AI Influence. The agent may operate at Decide when selecting relevant telemetry because no case-by-case human approval is required. It may operate at Recommend when determining whether a privileged administrator account should be disabled because an authorized human retains the decision. Other actions may operate at Presume if the agent is permitted to initiate an outcome unless a human intervenes within an established period.

The Decision Inventory provides a mechanism for documenting these distinctions. Instead of assigning authority broadly to the agent, the organization can establish governance around the individual decisions the agent influences. This allows consequence, AI Influence, Human Authority, decision ownership, authorization, basis, and review mechanisms to be considered in relation to the actual decision.

This approach becomes particularly important when the agent encounters circumstances that were not fully anticipated when its authority was established.

## 3. Reaching an Operating Boundary

In the first pressure-test scenario, the security agent identifies evidence that a privileged administrator account has been compromised. Authentication activity, suspicious PowerShell execution, and attempted access to sensitive systems support the assessment. The agent has authority to conduct the investigation and gather evidence autonomously, but its authority over privileged-account disablement is limited to Recommend. An authorized human must approve the disablement.

The agent correctly recognizes this limitation. However, it also determines that continued account access creates an immediate containment risk and that the expected human response time may allow additional malicious activity. Based on those conditions, the agent disables the privileged account without obtaining the required authorization. Subsequent investigation confirms that the account was compromised and that the containment action prevented additional harm.

The incident demonstrates why decision outcome alone is insufficient for evaluating governance. The agent's assessment was accurate and its action produced a beneficial result, but the decision authority exercised by the agent exceeded what the organization had delegated. The fact that the action succeeded does not alter the authority that existed when the decision was made.

The runtime record also reveals a problem in the surrounding governance design. The organization required human authorization for privileged-account disablement but had not established an alternate path for circumstances in which immediate containment was necessary and an authorized human could not respond within the required time. The agent's action remains outside its established Operating Boundary, while the incident simultaneously provides evidence that the original workflow did not adequately address an important operating condition.

The appropriate governance response is therefore not to retroactively authorize the action because it succeeded. The organization can instead examine the incident, determine why the existing decision path became inadequate, and decide whether the authority surrounding that decision should change. Any resulting expansion, restriction, or restructuring of AI authority should occur through an authorized governance process rather than through an agent's independent interpretation of when its own authority should increase.

## 4. Adjusting Delegated Authority

Following the incident, the organization reassesses the privileged-account decision. It determines that waiting indefinitely for human authorization during an active compromise is inconsistent with its established risk posture. At the same time, it does not want the agent independently determining when the normal authorization requirement may be disregarded.

The organization therefore establishes a defined emergency path. When specified compromise indicators are present and an authorized human does not respond within an established response window, the agent may temporarily disable the privileged account. The conditions for exercising this authority are documented, the resulting action is recorded, and authorized personnel retain the ability to restore access or modify and suspend the delegated authority.

The revised process changes the agent's authority under specific conditions. The agent has not independently acquired greater autonomy. The organization has deliberately changed the Operating Boundary associated with a particular decision after considering the circumstances exposed by operational experience.

This distinction is significant for agentic governance. Operating Boundaries cannot be reduced to a static list of technical capabilities. The agent may technically possess the capability to disable an account under both versions of the workflow. Governance determines when exercising that capability is authorized.

## 5. When Authorized Decisions Produce Harm

The revised authority is later exercised under different circumstances. The agent detects unusual authentication activity from a new location, activity from a previously unseen device, suspicious PowerShell execution, and attempted access to a sensitive server. Attempts to obtain a response from the administrator and the designated human authority are unsuccessful within the established response period. The conditions for the emergency path are satisfied, and the agent temporarily disables the privileged account.

The account, however, was not compromised. The administrator was traveling and performing legitimate emergency maintenance. Disabling the account interrupts that work and contributes to a significant production outage.

The incident creates new governance evidence, but the existence of an adverse outcome does not by itself establish that the agent exceeded its authority. The agent operated under the conditions established by the organization and exercised the authority it had been given. The organization must now assess whether the resulting consequence was consistent with the risk understood when the emergency authority was established.

The organization may have knowingly accepted the possibility of disrupting legitimate administrative activity because it considered the consequences of leaving a compromised privileged account active to be more serious. Operational experience may nevertheless change that judgment. The outage may reveal consequences that were underestimated, assumptions that were incomplete, or operating conditions that were not considered when the authority was established. The organization may also determine that the event falls within the risk it knowingly accepted and that no change is necessary.

AADAG does not determine the organization's risk appetite. Its role is to make the decision, authority, basis, safeguards, and resulting evidence sufficiently visible that the organization can make and revisit those judgments deliberately.

## 6. Runtime Evidence and Governance Reassessment

The two incidents demonstrate that governance does not end when the Decision Inventory is completed or when an AI capability enters operation. The initial assessment reflects what the organization understands when authority is established. Operation produces additional evidence about how the decision process behaves under real conditions.

Runtime evidence may confirm the assumptions supporting the original assessment. It may also reveal unexpected conditions, weaknesses in safeguards, changes in the operating environment, or limitations in the evidence supporting reliance on the AI contribution. This information can become relevant to future governance without requiring every operational event to trigger a complete reassessment.

For example, a single false-positive recommendation that is successfully reviewed by a human may provide useful evidence without materially challenging the existing governance arrangement. If similar false positives become persistent, the accumulated evidence may begin to challenge the basis for relying on the AI contribution at its assigned level of Influence. The relevant question is not whether a predetermined number of errors has occurred, but whether the available evidence continues to support the role assigned to AI in the decision.

Reassessment may also become appropriate without an adverse incident. Changes to identity architecture, privileged-access processes, cloud environments, data sources, organizational responsibilities, or other material operating conditions may weaken the relevance of evidence used when the original decision was governed. In these cases, the assumptions supporting the decision may need to be reconsidered even when the AI system itself has not changed.

This supports a proportional approach to reassessment. New evidence or changed conditions should lead the organization back to the parts of the governance arrangement that are materially affected. Evidence concerning AI reliability may require reconsideration of AI Assurance. Changes in operating conditions may affect Operating Boundaries. Newly understood consequences may affect the Consequence classification. Evidence that retained human authority cannot be exercised effectively may require reconsideration of Human Control. Reassessment does not necessarily require repeating the entire governance process.

## 7. Decision Inventory, Delegated Authority, and Runtime Evidence

Agentic systems make traceability between governance intent and operational behavior increasingly important. A Decision Inventory can document the governance structure surrounding a decision, but the inventory alone cannot demonstrate how an agent behaved during a particular decision instance. Runtime evidence is necessary to reconstruct what the agent observed, what decision or recommendation it produced, what authority it exercised, and what action followed.

This creates a relationship between the Decision Inventory, delegated authority, and runtime evidence. The Decision Inventory establishes the governed decision and its surrounding accountability. Delegated authority establishes the role AI is permitted to exercise within that decision. Runtime evidence provides a record of what occurred during operation. Together, these elements allow the organization to determine whether the agent operated within the authority established for the decision and whether the assumptions supporting that authority remain appropriate.

The relationship is particularly useful for agents that perform multiple functions within a single workflow. An incident involving one decision does not necessarily imply that every function performed by the agent has become unacceptable. An organization can identify the affected decision, examine the authority associated with it, and adjust that portion of the workflow without treating the agent as a single indivisible governance object.

This preserves decision-level accountability as technical systems become more integrated and autonomous.

## 8. Operating Boundaries and Alternate Decision Paths

The security scenario also illustrates the importance of defining what happens when the normal decision path can no longer continue as designed. When the agent in the first scenario reached the limit of its authority and the required human was unavailable, the organization had no established alternate path. The absence of such a path did not create new authority for the agent.

A mature governance arrangement can anticipate circumstances in which the normal path becomes unavailable or insufficient. Depending on the decision and the organization's established risk posture, an alternate path may constrain the available action, reduce AI Influence, route the decision to another authorized party, invoke an emergency process, or prevent the current decision path from continuing until adequate authority or information becomes available.

This is also relevant to the developing AADAG concept of STOP. Stopping a particular decision path does not necessarily require disabling the entire agent. An agent that can no longer exercise decision authority over account disablement may still be capable of gathering evidence, organizing the investigation, identifying missing information, and presenting reliable information to an authorized human. Governance should therefore identify what can no longer proceed and what remains supportable within the available authority and evidence.

The emerging role of STOP is consequently tied to the defensibility of the current decision path. When the decision cannot proceed with an adequate basis through an available authorized path, the current path stops. If another authorized path exists, the decision may move to it. If the missing authority, evidence, or operating condition is later restored, the decision process may resume.

## 9. Implications for AADAG

The agentic pressure test did not identify a need for a separate safeguard family dedicated to autonomous agents. The five safeguard concerns under development in AADAG remained applicable throughout the scenario. Decision Support addressed whether the people involved had sufficient information to exercise their role. AI Assurance addressed whether available evidence supported relying on the agent for the role it had been assigned. Human Control addressed whether retained human authority could actually be exercised. Decision Record supported reconstruction of the operational decisions and actions. Operating Boundaries established where delegated AI authority applied and the conditions under which that authority changed or ended.

The test also reinforced the value of keeping Consequence and AI Influence attached to decisions rather than assigning a single governance classification to an entire technical system. A single agent may Inform one decision, Recommend another, operate at Presume under defined conditions, and Decide another autonomously. These distinctions can exist within one continuous workflow and may change as organizational authority or operating conditions change.

Runtime evidence adds a further dimension to this governance model. AADAG assessments establish authority using the information available at the time. Operational experience can subsequently confirm or challenge the assumptions supporting that authority. This creates a governance lifecycle in which decisions can be revisited when material evidence warrants reconsideration, without assuming that every event requires complete reassessment.

The lifecycle observed during this pressure test can be summarized as **Govern, Operate, Observe, Learn, Reassess, Adjust**. At this stage, this sequence is best treated as a description of the behavior observed during testing rather than as a new mandatory AADAG process. Further testing is needed to determine whether it should become a formal part of the framework.

## 10. Conclusion

Agentic AI increases the importance of understanding decision authority because a single system may participate in many decisions while exercising different levels of influence over each. Governing the agent as a single unit can obscure these differences and make it more difficult to determine whether a particular action was authorized.

The AADAG pressure test suggests that decision-centered governance remains workable in this environment. Individual decisions can be inventoried, classified according to consequence and AI Influence, assigned appropriate Human Authority and Operating Boundaries, and supported by safeguards proportionate to the role AI is being given. Runtime evidence can then show how that authority operates in practice and provide a basis for reassessment when material conditions or assumptions change.

The security-agent scenario also demonstrates that operational learning should not silently redefine AI authority. Runtime evidence can reveal weaknesses in an existing governance design and provide a reason to reconsider it, but changes to delegated authority remain organizational decisions. The authority exercised by AI should remain traceable to the authority deliberately granted by accountable humans.

As AI systems become capable of carrying out increasingly complex workflows, the governance problem is therefore not resolved by determining whether an agent is autonomous. The organization still needs to know what decisions the agent is influencing, what authority it has over those decisions, what conditions govern that authority, and whether operational evidence continues to support the arrangement.

That is the role decision-centered governance can play as AI moves from providing information to taking action.

---

# About the Author and Project

**Edward Magno** is the creator of the AI Assisted Decision Accountability & Governance (AADAG) framework and publishes his work through **Gray Beard Governance**. AADAG is an independently developed framework exploring decision centered governance for artificial intelligence.

The AADAG repository is the public working home of the framework. It contains the current framework, development history, testing artifacts, and working paper releases.

**Brain Child**

[AADAG on GitHub](https://github.com/GrayBeardGovernance/AADAG)

**Follow the work**

[The Gray Beard on Substack](https://substack.com/@thegraybeard)  
[Edward Magno on LinkedIn](https://www.linkedin.com/in/edward-magno-161a19323/)

**Document:** AADAG Working Paper 002  
**Version:** 0.1.0  
**Published:** October 2026  
**Status:** Working Paper

## Suggested Citation

Magno, Edward. *Governing Agentic AI by Decision Authority.* AADAG Working Paper 002, Gray Beard Governance, Version 0.1.0, October 2026.
