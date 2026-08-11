[Home](../../README.md) › [Project Index](../../PROJECT_INDEX.md) › [Development](README.md) › CRA Adoption Roadmap

> **Status:** Maintained
> **Owner:** Architecture Team
> **Applies To:** CRA program evolution after foundational specifications
> **Last Reviewed:** 2026-08-12
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

**Status:** **Phase 1 complete** (2026-08-10, `technique-palm-muting`). **Phase 2 complete** (2026-08-11, `technique-left-hand-muting` + identity registry).

**When:** Prefer learning by doing over additional specifications.

**Approach:** Apply CRA-0001–0003 to a reference repository (ELS, EGLS, or another CRA adopter). Capture gaps as [Watch Items](../Architecture/Watch_Items/README.md) or [ADRs](../Architecture/ADRs/README.md).

**Outcome:** [CRA Adoption Report EGLS-001](EGLS_Adoption/CRA_Adoption_Report_EGLS-001.md) · [Genesis Inventory](EGLS_Adoption/Genesis_Document_Inventory.md) · [ADR-0001](../Architecture/ADRs/ADR-0001-egls-identifier-alignment.md) · [ADR-0002](../Architecture/ADRs/ADR-0002-egls-production-identity-model.md) · [ADR-0003](../Architecture/ADRs/ADR-0003-discovery-and-retrieval-separation.md)

## Parallel Architectural Workstream

The Options above are **mutually exclusive strategic alternatives** for the next substantive work path. They are not the only architectural activity the program may pursue in parallel.

### Knowledge Interaction/Evolution Workstream

**Status:** Active (2026-08-12)

**Purpose:** Preserve and structure architectural discoveries from [AI Canonical Knowledge Interaction and Evolution](../Architecture/Discovery_Records/AI_Canonical_Knowledge_Interaction_and_Evolution.md) and bridge them to future normative work without prematurely chartering specifications.

**Approach:** Maintain [Knowledge Interaction/Evolution Workstream](Knowledge_Interaction_Evolution_Workstream.md) as the primary living document mapping discoveries to architectural questions, candidate workstreams, dependencies, and [Watch Items](../Architecture/Watch_Items/README.md) (AWI-0001–AWI-0004).

**Relationship to Options A–D:** This workstream **informs** future selection among Options A–D and subsequent normative chartering. It does not replace or compete with those strategic paths. For example, candidate workstream analysis for canonical relationships overlaps Option B; knowledge evolution analysis may inform Option A (CRA-0004 Evidence Promotion candidate) if that path is later selected.

**Outcome:** [Knowledge Interaction/Evolution Workstream](Knowledge_Interaction_Evolution_Workstream.md) · [Discovery Records](../Architecture/Discovery_Records/README.md) · [AWI-0001](../Architecture/Watch_Items/AWI-0001-knowledge-evolution-and-canonicalization.md)–[AWI-0004](../Architecture/Watch_Items/AWI-0004-cross-authority-canonical-knowledge.md)

## Deferred Program Operations

Non-blocking infrastructure to mature over time:

| Area | Location | Status |
|---|---|---|
| Governance policy | [docs/Governance/](../Governance/README.md) | Deferred |
| Adoption guides | [docs/Development/](../Development/README.md) | Minimal |
| Architecture decisions | [ARCHITECTURE_DECISIONS.md](../../ARCHITECTURE_DECISIONS.md) | ADR-0001–0003 |

## How to Proceed

1. Complete stabilization and [Glossary](../Reference/Glossary.md) (foundational vocabulary).
2. Run an adoption exercise (Option D) or begin CRA-0004 planning (Option A) based on active project needs.
3. Record concrete choices in ADRs as implementation decisions arise.

## Related Documents

- [PROJECT_INDEX.md](../../PROJECT_INDEX.md)
- [Knowledge Interaction/Evolution Workstream](Knowledge_Interaction_Evolution_Workstream.md)
- [Glossary](../Reference/Glossary.md)
- [Project Charter](../../PROJECT_CHARTER.md)
