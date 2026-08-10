[Home](../../README.md) › [Project Index](../../PROJECT_INDEX.md) › [Development](README.md) › CRA Adoption Roadmap

> **Status:** Maintained
> **Owner:** Architecture Team
> **Applies To:** CRA program evolution after foundational specifications
> **Last Reviewed:** 2026-08-10
> **Review Frequency:** On Change

# CRA Adoption Roadmap

## Purpose

This document records recommended next steps after completion of the foundational normative trilogy (CRA-0001 through CRA-0003). It is **informative program guidance**, not a normative specification.

## Foundational Layer Complete

| Specification | Layer | Status |
|---|---|---|
| [CRA-0001](../Specifications/CRA-0001.md) | Principles (FP-1–FP-5) | Draft v1.0 |
| [CRA-0002](../Specifications/CRA-0002.md) | Identity (IM-1–IM-7) | Draft v1.0 |
| [CRA-0003](../Specifications/CRA-0003.md) | Fidelity (RF-1–RF-7) | Draft v1.0 |

[Canonical Knowledge Conclusions](../AI/Architectural_Research/Canonical_Knowledge/Conclusions.md) open questions #1–#4 are resolved. Open question **#5** (evidence artifacts) remains deferred.

## Recommended Next Substantive Work

Choose **one** path based on program need. Default recommendation: **Option D first, then Option A** if Electronics Learning System (ELS) or AI-Assisted Electrical Engineering Reasoning Framework (AERF) adoption is active.

### Option A — Evidence Promotion (CRA-0004 candidate)

**When:** ELS/AERF adoption is imminent and governed promotion rules are needed.

**Approach:** Lean research synthesis + normative CRA-0004 Draft v1.0 defining how primary evidence records become canonical knowledge within scope.

**Addresses:** Conclusions open question #5; CRA-0001 evidence artifacts deferral.

### Option B — Canonical Relationship Model

**When:** Adopters need FP-3 operationalized beyond navigation fidelity (RF-7).

**Approach:** Normative specification defining canonical relationships independent of navigation mechanisms.

### Option C — Validation Methodology

**When:** External adopters need conformance testing beyond the question-based conformance tables in CRA-0001–0003.

**Approach:** Normative specification defining evaluation procedures and validation methodology (tooling remains implementation-specific).

### Option D — Adoption Exercise (recommended first)

**When:** Prefer learning by doing over additional specifications.

**Approach:** Apply CRA-0001–0003 to a reference repository (ELS, EGLS, or another CRA adopter). Capture gaps as [Watch Items](../Architecture/Watch_Items/README.md) or [ADRs](../Architecture/ADRs/README.md).

**Outcome:** Concrete adoption evidence before normativizing domain-specific rules.

## Deferred Program Operations

Non-blocking infrastructure to mature over time:

| Area | Location | Status |
|---|---|---|
| Governance policy | [docs/Governance/](../Governance/README.md) | Deferred |
| Adoption guides | [docs/Development/](../Development/README.md) | Minimal |
| Architecture decisions | [ARCHITECTURE_DECISIONS.md](../../ARCHITECTURE_DECISIONS.md) | Empty index |

## How to Proceed

1. Complete stabilization and [Glossary](../Reference/Glossary.md) (foundational vocabulary).
2. Run an adoption exercise (Option D) or begin CRA-0004 planning (Option A) based on active project needs.
3. Record concrete choices in ADRs as implementation decisions arise.

## Related Documents

- [PROJECT_INDEX.md](../../PROJECT_INDEX.md)
- [Glossary](../Reference/Glossary.md)
- [Project Charter](../../PROJECT_CHARTER.md)
