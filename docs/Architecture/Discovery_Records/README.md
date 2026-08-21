# Discovery Records

[Home](../../../README.md) › [Project Index](../../../PROJECT_INDEX.md) › [Architecture](../README.md) › Discovery Records

> **Status:** Maintained
> **Owner:** Architecture Team
> **Applies To:** Non-normative architectural discovery records for CRA
> **Last Reviewed:** 2026-08-22
> **Review Frequency:** On Change

## Purpose

This directory holds **Architectural Discovery Records** — non-normative documents that preserve architectural reasoning, observations, examples, and open questions arising before or alongside normative specification work.

Discovery records are **not** normative specifications. They explain what was discovered and considered at a point in CRA's evolution. Later workstream plans, specifications, ADRs, and Watch Items may refine, reject, or supersede hypotheses recorded here **by reference**, without rewriting historical reasoning in place.

## Relationship to CRA-0000

[`CRA-0000.md`](../../../CRA-0000.md) remains at the repository root as the approved historical exception — the permanent founding discovery record. Subsequent discovery records belong under this directory per [`docs/Architecture/README.md`](../README.md).

## Identifier Convention

**No continuing serial identifier series is established for discovery records.**

- `CRA-0000` is a special-case founding identifier, separate from the normative `CRA-0001+` specification series.
- Additional discovery records use **descriptive filenames** until the program explicitly adopts a continuing discovery-record naming convention through governed repository/documentation decision.

## Authoritative Documents

| Document | Status |
|---|---|
| [AI Canonical Knowledge Interaction and Evolution](AI_Canonical_Knowledge_Interaction_and_Evolution.md) | Permanent Historical Record |
| [Pragmatic Canonicality and Delegated Authority](Pragmatic_Canonicality_and_Delegated_Authority.md) | Architectural Discovery / Candidate Architectural Position |

## What Belongs Here

- Architectural discoveries arising from engineering experience, adoption exercises, or directed analysis
- Practical examples and reasoning chains that inform future normative work
- Open questions explicitly deferred from specification

## What Does Not Belong Here

- Normative specifications — see [`docs/Specifications/`](../../Specifications/README.md)
- Multi-model architectural research with comparative synthesis — see [`docs/AI/Architectural_Research/`](../../AI/Architectural_Research/README.md)
- Architecture Decision Records — see [`docs/Architecture/ADRs/`](../ADRs/README.md)

## Navigation

- [Project Index](../../../PROJECT_INDEX.md)
- [Architecture](../README.md)
- [Knowledge Interaction/Evolution Workstream](../../Development/Knowledge_Interaction_Evolution_Workstream.md) — primary bridge from discovery to future architectural work

## Maintenance

Update this index when discovery records are created, moved, renamed, or retired. Do not rewrite historical discovery record bodies to match later architectural conclusions.
