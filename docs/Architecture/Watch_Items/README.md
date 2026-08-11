# Watch Items

[Home](../../../README.md) › [Project Index](../../../PROJECT_INDEX.md) › [Architecture](../README.md) › Watch Items

> **Status:** Maintained
> **Owner:** Architecture Team
> **Applies To:** Open architectural questions and deferred concerns
> **Last Reviewed:** 2026-08-12
> **Review Frequency:** On Change

## Purpose

This directory holds open architectural questions, deferred concerns, and items under observation. Watch items are **non-authoritative** until promoted to a normative specification, ADR, or other governed document.

## Naming Convention

Architectural Watch Items in this repository use the filename pattern:

```text
AWI-NNNN-descriptive-slug.md
```

For example: `AWI-0001-knowledge-evolution-and-canonicalization.md`

This is a **repository/documentation convention** for organizing open architectural concerns within the CRA program. It is **not** a normative CRA architectural requirement. Adopters are not required to use `AWI-*` identifiers in their own repositories.

Serial numbers (`NNNN`) are assigned sequentially within this repository, beginning at `0001`. When a Watch Item is resolved, promoted, or retired, update this index accordingly.

## Authoritative Documents

| Watch Item | Subject | Status |
|---|---|---|
| [AWI-0001](AWI-0001-knowledge-evolution-and-canonicalization.md) | Knowledge Evolution and Canonicalization | Open |
| [AWI-0002](AWI-0002-applicability-and-epistemic-modeling.md) | Applicability and Epistemic Modeling | Open |
| [AWI-0003](AWI-0003-ai-assisted-knowledge-evaluation.md) | AI-Assisted Knowledge Evaluation | Open |
| [AWI-0004](AWI-0004-cross-authority-canonical-knowledge.md) | Cross-Authority Canonical Knowledge | Open |

## What Belongs Here

- Open questions requiring further architectural analysis
- Deferred design concerns identified during specification development or discovery integration
- Items that may warrant future ADRs or normative specifications
- Consolidated concern areas that may later split into additional Watch Items as architecture matures

## Navigation

- [Project Index](../../../PROJECT_INDEX.md)
- [Architecture](../README.md)
- [Knowledge Interaction/Evolution Workstream](../../Development/Knowledge_Interaction_Evolution_Workstream.md)
- [Architecture Decision Records](../ADRs/README.md)

## Maintenance

Update this index when watch items are created, resolved, promoted, split, or retired.
