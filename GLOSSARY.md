# AADAG Glossary

This glossary defines key terms used in AI Assisted Decision Accountability & Governance (AADAG).

The definitions are derived from the AADAG Framework. `FRAMEWORK.md` remains the authoritative source for framework definitions and mechanics.

## Affected Parties

The people, groups, organizations, or other parties that could be affected if an AI-influenced decision is wrong.

## AI Influence

The level of influence AI has over a decision.

AADAG defines four AI Influence levels: Inform, Recommend, Presume, and Decide.

## AI-Influenced Decision

A decision that AI helps shape through information, analysis, recommendations, defaults, or decision authority.

The AI-influenced decision is the primary unit of governance in AADAG.

## Authorizing Authority

The person or role that authorized the assigned level of AI influence over a decision.

## Basis

The information, criteria, need, or reasoning supporting a decision or decision process.

Basis may reference supporting information rather than reproduce the underlying documentation.

## Consequence

The potential impact of an incorrect AI-influenced decision.

AADAG assigns consequence according to the highest credible consequence to affected parties while considering the nature, scope, duration, and reversibility of the potential harm.

## Consequence Levels

AADAG uses six consequence classifications:

- **CU: Undetermined**
- **C0: Negligible**
- **C1: Limited**
- **C2: Moderate**
- **C3: Significant**
- **C4: Critical**

Detailed definitions and assignment rules are maintained in `FRAMEWORK.md`.

## Decide

An AI Influence level in which AI selects or executes a decision without requiring case-by-case human approval.

Human authority is exercised through rules, limits, oversight, and the ability to modify or stop the AI's decision-making authority.

## Decision

The specific decision AI is helping make.

## Decision Inventory

The structured record used by AADAG to describe an AI-influenced decision.

The Decision Inventory contains nine fields:

1. Decision
2. Affected Parties
3. Consequence
4. AI Influence
5. Human Authority
6. Decision Owner
7. Authorizing Authority
8. Basis
9. Review / Recourse

## Decision Owner

The person or role accountable for the decision and its outcomes, including when individual decisions occur without case-by-case human approval.

## Decision Path

The concise AADAG governance path:

**Decision → Consequence → Influence → Human Authority**

## Decision Type

A defined category of decision AI is helping make.

Consequence is assigned to a decision type rather than each individual decision instance. Separate decision types should be used when differences in purpose, affected parties, or potential outcomes would materially change the consequence classification.

## Delegation

The organizational authorization granting AI a defined level of influence over a decision.

Delegation identifies the organizational authority that authorized AI's influence. It is an accountability mechanism rather than a separate classification scale.

## Duration

How long the effects of an incorrect decision could persist.

Duration is one of the characteristics considered when assigning consequence.

## Human Authority

The authority people retain over a decision or decision process.

Human Authority may include approval, rejection, modification, intervention, override, oversight, or the authority to modify or stop AI decision-making authority.

## Inform

An AI Influence level in which AI provides information, analysis, or context for consideration.

AI may identify, summarize, analyze, prioritize, or flag information, provided it does not propose a decision or action.

## Nature

The kind of harm or adverse effect that could result from an incorrect decision.

Nature is one of the characteristics considered when assigning consequence.

## Presume

An AI Influence level in which AI establishes a default decision or action that will take effect unless a human intervenes.

A human retains the authority and opportunity to change or override the outcome before it takes effect.

## Recommend

An AI Influence level in which AI proposes a decision, action, or ranked set of options for human consideration.

Human action is required for the proposed outcome to become the decision.

## Review / Recourse

The means by which an AI-influenced decision can be challenged, corrected, or reversed.

## Reversibility

How easily the effects of an incorrect decision can be corrected or undone.

Reversibility is one of the characteristics considered when assigning consequence.

## Safeguard

A measure used to prevent an incorrect decision, reduce its effects, provide opportunities for intervention, or help correct an outcome.

Detailed safeguard selection and mapping are planned for AADAG v0.3.

## Scope

The extent of who or how many could be affected by an incorrect decision.

Scope is one of the characteristics considered when assigning consequence.

## Undetermined (CU)

The consequence classification used when the potential consequence of an incorrect decision cannot be determined with sufficient confidence.

Additional information or analysis is required before assigning another consequence level.
