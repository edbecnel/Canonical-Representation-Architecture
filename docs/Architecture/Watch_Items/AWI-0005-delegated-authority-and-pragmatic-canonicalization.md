# AWI-0005 — Delegated Authority and Pragmatic Canonicalization

[Home](../../../README.md) › [Project Index](../../../PROJECT_INDEX.md) › [Architecture](../../README.md) › [Watch Items](README.md) › AWI-0005

> **Status:** Open
> **Date:** 2026-08-22
> **Owner:** Architecture Team

## Summary

Open architectural questions concerning delegated canonical authority, pragmatic canonicalization trade-offs, and the separation of canonicalization rigor from canonical status.

## Scope

This Watch Item consolidates the following related concerns from [Pragmatic Canonicality and Delegated Authority](../../Discovery_Records/Pragmatic_Canonicality_and_Delegated_Authority.md):

- **Delegated canonical authority** — governing authority → canonicalization authority → designation chain
- **Automated delegated authority** — including AI exercising authority only within delegated scope
- **Pragmatic canonicalization** — deliberate trade-offs between rigor, cost, speed, risk, and usefulness
- **Rigor as governance metadata** — verification level recorded via provenance and policy, not as a property of canonicality itself
- **Economic practicality** — architectural constraints on canonicalization cost and latency
- **Delegation chain provenance** — recoverable authority, delegated authority, scope, method, and policy

## Why Watch, Not Specification Now

- Delegation architecture not explicit in CRA-0001 FP-4
- Pragmatic canonicalization and variable rigor modes require CKES experimental validation
- Technology-independent delegation and canonicalization role taxonomy not finalized
- Overlaps AWI-0001 (canonicalization policy), AWI-0003 (AI authority), and AWI-0004 (cross-authority)

## Foundational Questions for CRA-0001 Evaluation

Does FP-4 (Scope-Bounded Governed Designation) already entail that canonical authority may be delegated to another actor or mechanism, or does CRA need an explicit delegation architecture?

Does CRA-0001's recoverable designation requirement (FP-4) suffice for delegated authority provenance, or does a separate provenance metadata specification become necessary?

**CRA-0001 must not be modified normatively until evaluated.**

## Candidate Workstream

[Knowledge Interaction/Evolution Workstream](../../../Development/Knowledge_Interaction_Evolution_Workstream.md) — **Knowledge Evolution and Canonicalization** and **AI Interaction**

## Related Documents

- [Pragmatic Canonicality and Delegated Authority](../../Discovery_Records/Pragmatic_Canonicality_and_Delegated_Authority.md) §§9–13, 15–17
- [CRA-0001](../../../Specifications/CRA-0001.md) FP-4
- [AWI-0001](AWI-0001-knowledge-evolution-and-canonicalization.md) — canonicalization policy
- [AWI-0003](AWI-0003-ai-assisted-knowledge-evaluation.md) — AI-assisted canonicalization
- [CKES — Pragmatic Canonicalization Research and Validation](https://github.com/edbecnel/Canonical-Knowledge-Engineering-System/blob/main/docs/Development/Pragmatic_Canonicalization_Research_and_Validation.md)
- [CKES CRA Findings Report](https://github.com/edbecnel/Canonical-Knowledge-Engineering-System/blob/main/docs/Development/CRA_Findings_Report.md)
