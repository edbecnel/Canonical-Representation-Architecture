# ADR-0002 — EGLS Production Identity Model

[Home](../../../README.md) › [Project Index](../../../PROJECT_INDEX.md) › [Architecture](../README.md) › [ADRs](README.md) › ADR-0002

> **Status:** Accepted
> **Date:** 2026-08-10
> **Owner:** Architecture Team

## Context

[ADR-0001](ADR-0001-egls-identifier-alignment.md) established that EGLS Knowledge Object `id` values (for example, `technique-palm-muting`) serve as canonical identifiers within the EGLS-001 adoption exercise. That exercise intentionally used human-readable slugs and a single file-path locator to demonstrate CRA-0002 IM-1 and IM-2 without building a registry.

[CRA-0002 — Identity Model](../../Specifications/CRA-0002.md) permits opaque UUIDs, scope qualification, and multiple organizational locators (IM-2). The [CRA Adoption Report EGLS-001](../../Development/EGLS_Adoption/CRA_Adoption_Report_EGLS-001.md) records a gap: no identity registry file; identity is carried in per-object front matter only.

Production systems require an immutable opaque identifier, an explicit scope root, and retrieval via multiple path forms (folder paths, scope-qualified colon paths, URLs). This ADR records the target production model EGLS should adopt as its Knowledge Object corpus grows.

ADR-0001 remains valid for the EGLS-001 exercise. This ADR defines the forward-looking production architecture without requiring immediate implementation.

## Decision

1. Production EGLS identity SHALL use three architecturally distinct layers:
   - **Canonical identifier** — an opaque UUID (or URN equivalent) assigned at governance designation; immutable across relocation and reformatting
   - **Scope** — explicit scope qualification (for example, `egls` or the EGLS repository per CRA FP-4)
   - **Organizational locators** — one or more retrieval addresses for the canonical encoding; locators are NOT identity

2. Human-readable slugs (`{type}-{slug}`) MAY coexist as aliases alongside an opaque canonical identifier but SHALL NOT be the sole canonical identifier in production.

3. Organizational locators MAY take multiple equivalent forms for the same artifact:
   - Repository-relative file path (for example, `02_Technique/Palm_Muting.md`)
   - Scope-qualified path (for example, `egls:02_Technique/Palm_Muting`)
   - Network or storage URLs, database keys, or other locator mechanisms

4. Implementation is deferred. Trigger: introduction of an identity registry or authoring of a second governed Knowledge Object.

## Consequences

### Positive

- Aligns EGLS with CRA-0002 opacity and locator-separation requirements at scale.
- Supports multi-platform retrieval without identity churn when content is mirrored or republished.

### Negative

- EGLS-001 (`technique-palm-muting`) does not yet conform to the production model.
- Requires a registry file and metadata standard updates before implementation.
- A governed slug-to-UUID migration path must be defined when implementation begins.

## Related Documents

- [ADR-0001 — EGLS Identifier Alignment](ADR-0001-egls-identifier-alignment.md)
- [ADR-0003 — Discovery and Retrieval Separation](ADR-0003-discovery-and-retrieval-separation.md)
- [CRA-0002 — Identity Model](../../Specifications/CRA-0002.md)
- [CRA Adoption Report EGLS-001](../../Development/EGLS_Adoption/CRA_Adoption_Report_EGLS-001.md)
- [Genesis Document Inventory](../../Development/EGLS_Adoption/Genesis_Document_Inventory.md)
