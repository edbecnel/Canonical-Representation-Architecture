# ADR-0001 — EGLS Identifier Alignment with CRA-0002

[Home](../../../README.md) › [Project Index](../../../PROJECT_INDEX.md) › [Architecture](../README.md) › [ADRs](README.md) › ADR-0001

> **Status:** Accepted
> **Date:** 2026-08-10
> **Owner:** Architecture Team

## Context

EGLS is the first CRA reference adopter implementing governed canonical artifacts per [CRA-0002 — Identity Model](../../Specifications/CRA-0002.md). EGLS already defines stable `id` fields in [CANONICAL_METADATA_FIELD_REFERENCE](https://github.com/edbecnel/Electric-Guitar-Learning-System/blob/main/docs/standards/CANONICAL_METADATA_FIELD_REFERENCE.md) using the format `{type}-{descriptive-slug}`.

The CRA adoption exercise for `technique-palm-muting` requires an explicit decision on how EGLS identifiers relate to CRA canonical identifiers.

## Decision

Within the **EGLS repository scope**, EGLS Knowledge Object `id` values (for example, `technique-palm-muting`) SHALL serve as **canonical identifiers** per CRA-0002 IM-1, provided they satisfy the EGLS identifier requirements (unique, stable, independent of filename).

**Organizational locators** — Markdown file paths (for example, `02_Technique/Palm_Muting.md`) — are NOT canonical identifiers. Renaming or relocating files MUST NOT change the `id` field without a governed lineage event.

CRA does not mandate a global identifier format beyond the CRA-0002 syntax profile. EGLS `{type}-{slug}` ids are an acceptable encoding within EGLS scope.

## Consequences

### Positive

- EGLS adopters need no parallel identity system; existing metadata standards satisfy CRA-0002 at the identity-model level.
- First concrete CRA adoption artifact demonstrates technology-independent identity binding.

### Negative

- EGLS ids are human-readable slugs, not opaque UUIDs; CRA-0002 permits this but other adopters may choose different encodings.
- Cross-repository identity federation remains out of scope (CRA-0002 deferred topic).

## Related Documents

- [CRA-0002 — Identity Model](../../Specifications/CRA-0002.md)
- [CRA Adoption Report EGLS-001](../../Development/EGLS_Adoption/CRA_Adoption_Report_EGLS-001.md)
- [Genesis Document Inventory](../../Development/EGLS_Adoption/Genesis_Document_Inventory.md)
