# AADAG

## AI Assisted Decision Accountability & Governance

> **Govern every decision AI helps shape.**

AADAG is an emerging, decision centered framework for governing how artificial intelligence influences consequential decisions.

AADAG begins with the decisions AI helps shape:

1. **What decision is AI helping us make?**
2. **How consequential is that decision if it is wrong?**
3. **How much influence does AI have over the outcome?**
4. **What human judgment, evidence, and accountability must remain?**

These questions reveal how AI affects people, resources, rights, access, safety, and institutional outcomes.

## Why this repository exists

This repository is the public working home of AADAG. Version 0.1 established the foundation. Development is now underway on version 0.2, Decision Classification.

AADAG is a practical framework in development, informed by risk management, cybersecurity governance, and real-world accountability.

## Decision consequence levels

AADAG v0.2 introduces a working consequence scale for classifying the potential impact of an incorrect AI influenced decision:

- **CU: Undetermined**
- **C0: Negligible**
- **C1: Limited**
- **C2: Moderate**
- **C3: Significant**
- **C4: Critical**

Full definitions are maintained in the [Framework](FRAMEWORK.md). The level names and core definitions are established as the current v0.2 working scale. Assignment rules, examples, and known limitations are still being developed.

## Alignment with the NIST AI Risk Management Framework

AADAG is designed to align with the principles of the **[NIST Artificial Intelligence Risk Management Framework (AI RMF 1.0)](https://www.nist.gov/publications/artificial-intelligence-risk-management-framework-ai-rmf-10)** and its four core functions: **GOVERN, MAP, MEASURE, and MANAGE**.

AADAG applies these principles at the decision level. It establishes the context and potential consequences of an AI influenced decision, identifies the degree of influence given to AI, establishes human accountability for the outcome, and provides a basis for applying governance and safeguards proportional to consequence.

The relationship can be viewed through the NIST AI RMF functions:

- **GOVERN:** AADAG identifies ownership, accountability, and the authority given to AI within a decision.
- **MAP:** AADAG identifies the decision being influenced, its context, affected parties, and the potential consequences if the decision is wrong.
- **MEASURE:** AADAG consequence and influence classifications provide context for determining what evidence, testing, and monitoring are appropriate.
- **MANAGE:** AADAG provides a structure for applying oversight, safeguards, review, and recourse according to the consequence and AI influence associated with a decision.

A more detailed NIST AI RMF crosswalk is planned as the framework develops.

## Current exploration: delegation

AADAG is currently exploring **delegation** as a way to describe the organizational choice to give AI influence over a decision.

The working distinction is simple:

- **Influence** describes how much AI affects a decision.
- **Delegation** describes how much decision influence people or organizations choose to give AI.

The idea is still being tested. The current question is whether delegation adds useful accountability to the framework without creating unnecessary complexity.

A working observation behind this exploration is:

> **The technology didn't necessarily change. Its influence did.**

## Start here

- [Framework](FRAMEWORK.md)
- [Principles](PRINCIPLES.md)
- [Roadmap](ROADMAP.md)
- [Traceability](TRACEABILITY.md)
- [Contributing](CONTRIBUTING.md)
- [Changelog](CHANGELOG.md)

## Current status

- **Version:** 0.2 Decision Classification
- **Status:** Active development
- **Completed:** Consequence level names and core definitions
- **In progress:** Consequence assignment guidance, AI influence refinement, delegation exploration, and practical examples
- **Maintainer:** Gray Beard Governance

## Short description

AADAG helps organizations classify the decisions AI influences, determine how much influence is appropriate, and assign safeguards and accountability in proportion to potential harm.

## Feedback

Constructive challenges are welcome. If a concept is unclear, incomplete, difficult to apply, or produces the wrong result, please open an issue.
