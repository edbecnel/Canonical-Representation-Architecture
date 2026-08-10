# ADR-0003 — Discovery and Retrieval Separation

[Home](../../../README.md) › [Project Index](../../../PROJECT_INDEX.md) › [Architecture](../README.md) › [ADRs](README.md) › ADR-0003

> **Status:** Accepted
> **Date:** 2026-08-10
> **Owner:** Architecture Team

## Context

Users need to find canonical Knowledge Objects by description (for example, "guitar muting"), metadata, tags, or semantic and contextual paths — not only by a known canonical identifier or file path.

[CRA-0001 — Foundational Architectural Principles](../../Specifications/CRA-0001.md) defines **Derived Representations** to include indexes and navigation views produced for search, presentation, and consumption (FP-1). FP-3 requires that navigation and browse hierarchies are derived views of relationships, not authoritative definitions of canonical knowledge.

[CRA-0002 — Identity Model](../../Specifications/CRA-0002.md) defines **organizational locators** as retrieval addresses for a known artifact and requires a registry or equivalent mechanism that binds canonical identifiers to canonical artifacts within each scope. A canonical identifier is not proof of network location or retrievability.

[ADR-0002](ADR-0002-egls-production-identity-model.md) records the production retrieval model (opaque identifier, scope, organizational locators) for EGLS but does not address discovery.

Conflating discovery inputs (search queries, semantic paths, topic descriptions) with organizational locators or canonical identity violates CRA FP-1, FP-3, and IM-2. The [Semantic Identity Protocol (SIP)](../../../CRA-0000.md) explored semantic addressing as an informative reference (CRA-0000 §7.2); semantic and contextual paths may aid discovery but must not substitute for registry binding.

This ADR is a **CRA program-level** decision. [Electric Guitar Learning System (EGLS)](https://github.com/edbecnel/Electric-Guitar-Learning-System) serves as the reference example.

## Decision

1. **Discovery layer** (derived, non-authoritative): search indexes, metadata queries, tag or topic filters, and semantic or contextual paths MAY return **candidate** canonical identifiers. Discovery results MUST NOT be treated as canonical identity or as authoritative relationship definitions (CRA FP-3).

2. **Resolution layer** (authoritative binding): a registry or equivalent mechanism per CRA-0002 Architectural Obligations confirms that a candidate identifier refers to a governed canonical artifact within scope.

3. **Retrieval layer** (organizational locators): one or more organizational locators (file path, scope-qualified path, URL, or other storage address) fetch the canonical encoding. Per [ADR-0002](ADR-0002-egls-production-identity-model.md).

4. **Lookup flow:** discovery query → candidate identifiers → registry resolution → locator retrieval → content. A direct canonical identifier or known organizational locator MAY skip the discovery step.

5. **Semantic and contextual paths** (for example, `egls:technique/muting`): classified as discovery or derived navigation projections unless explicitly governed as organizational locators. They MUST resolve to a canonical identifier before retrieval and are NOT substitutes for registry binding.

6. **EGLS example:** a query for "guitar muting" MAY match metadata or tags (`muting`, `technique_family: muting`) or a future search index, yielding candidate `technique-palm-muting` → registry binding → locator `02_Technique/Palm_Muting.md` → Markdown encoding.

7. **Implementation is deferred.** Trigger: introduction of a discovery index or authoring of a second governed Knowledge Object requiring cross-object lookup. Governed semantic path vocabulary may align with [CRA Adoption Roadmap Option B — Canonical Relationship Model](../../Development/CRA_Adoption_Roadmap.md).

## Consequences

### Positive

- Clear separation aligns with CRA-0001 and CRA-0002 without conflating search with identity.
- Supports human search, metadata filtering, and AI retrieval without path-as-identity failure modes.
- Search indexes remain rebuildable derived representations per EGLS delivery architecture.

### Negative

- EGLS-001 has no discovery index; tags in `technique-palm-muting` front matter are minimal hooks only.
- Semantic path vocabulary is not yet defined for EGLS.
- A canonical relationship model (Roadmap Option B) may be required before semantic paths are governed beyond informal discovery.

## Related Documents

- [ADR-0001 — EGLS Identifier Alignment](ADR-0001-egls-identifier-alignment.md)
- [ADR-0002 — EGLS Production Identity Model](ADR-0002-egls-production-identity-model.md)
- [CRA-0001 — Foundational Architectural Principles](../../Specifications/CRA-0001.md)
- [CRA-0002 — Identity Model](../../Specifications/CRA-0002.md)
- [CRA Adoption Report EGLS-001](../../Development/EGLS_Adoption/CRA_Adoption_Report_EGLS-001.md)
- [CRA Adoption Roadmap — Option B](../../Development/CRA_Adoption_Roadmap.md)
