[Home](../../../README.md) › [Project Index](../../../PROJECT_INDEX.md) › [Development](../README.md) › EGLS Adoption › CRA Adoption Report EGLS-001

> **Status:** Maintained
> **Document Class:** Adoption Exercise (informative)
> **Owner:** CRA Architecture Team
> **Applies To:** EGLS as CRA reference adopter
> **Last Reviewed:** 2026-08-11
> **Review Frequency:** On Change

# CRA Adoption Report — EGLS-001

## Summary

This report documents the first CRA adoption exercise: governing **`technique-palm-muting`** in the [Electric Guitar Learning System (EGLS)](https://github.com/edbecnel/Electric-Guitar-Learning-System) as a canonical Knowledge Object derived from the genesis curriculum Word document.

| Field | Value |
|---|---|
| **Adopter** | EGLS (CRA reference implementation per [CRA-0000](../../../CRA-0000.md) §7.3) |
| **Canonical artifact** | `technique-palm-muting` |
| **EGLS encoding** | [`02_Technique/Palm_Muting.md`](https://github.com/edbecnel/Electric-Guitar-Learning-System/blob/main/02_Technique/Palm_Muting.md) |
| **Genesis provenance** | [Genesis Document Inventory](Genesis_Document_Inventory.md) |
| **ADR** | [ADR-0001 — EGLS Identifier Alignment](../../Architecture/ADRs/ADR-0001-egls-identifier-alignment.md) |

## Genesis Document Role

The Word document [*Learning Electric Guitar — Guide for Casual Experience Acoustic Guitarists*](../../Reference/Learning%20Electric%20Guitar%20-%20Guide%20for%20Casual%20Experience%20Acoustic%20Guitarists.docx) is a **provenance record**, not a canonical artifact. It is an organizational locator in the CRA Reference domain.

Palm muting content was extracted from Phase 2 §2.1 and authored as a governed EGLS Knowledge Object with explicit `source` metadata. The Word file remains available for historical traceability; the Markdown Knowledge Object is the canonical encoding within EGLS scope.

## CRA-0001 Principles

| Principle | Application |
|---|---|
| FP-1 | Knowledge Object (canonical) is distinct from navigation links and future index entries (derived) |
| FP-2 | `id: technique-palm-muting` persists if file moves from `02_Technique/Palm_Muting.md` to another path |
| FP-3 | Cross-references use `id` (`technique-palm-muting` ↔ `technique-left-hand-muting`), not file paths |
| FP-4 | Designated `status: published` within EGLS scope by governance exercise |
| FP-5 | Provenance and epistemic content preserved in Markdown encoding |

## CRA-0002 Identity Model

| Requirement | Evidence | Met? |
|---|---|---|
| **IM-1** Identifier at designation | `id: technique-palm-muting` in front matter | Yes |
| **IM-2** Independent of locators | `id` ≠ `02_Technique/Palm_Muting.md` | Yes |
| **IM-3** Equivalence determination | Same artifact = same `id` + version; file is derived encoding | Yes |
| **IM-4** Relocation invariance | Renaming `Palm_Muting.md` would not change `id` | Yes (by design) |
| **IM-5** Governed semantic evolution | Future content changes require version/lineage metadata update | Yes (process defined) |
| **IM-6** Historical reference | N/A for v1.0 initial designation | N/A |
| **IM-7** Governed split/merge | Single object; no merge inferred | Yes |

### Identity vs locator demonstration

| Concept | Value |
|---|---|
| **Canonical identifier** | `technique-palm-muting` |
| **Organizational locator** | `02_Technique/Palm_Muting.md` (EGLS repo) |
| **Scope** | EGLS repository |

### Production identity model (informative)

This subsection describes a **target production shape** for EGLS identity. It is informative only and is **not implemented** in EGLS-001, which uses a scope-local slug and a single file-path locator.

Per [CRA-0002](../../Specifications/CRA-0002.md) IM-1 and IM-2, production identity separates three architecturally distinct layers:

1. **Canonical identifier** — an opaque UUID or URN equivalent, assigned at governance designation and immutable across relocation or reformatting
2. **Scope** — an explicit scope qualification (for example, `egls` or the EGLS repository per CRA FP-4)
3. **Organizational locators** — one or more retrieval addresses for the canonical encoding; locators are NOT identity

| Layer | Production example | EGLS-001 exercise |
|---|---|---|
| Canonical identifier | `urn:uuid:7f3a9c2e-...` | `technique-palm-muting` (slug) |
| Scope | `egls` | EGLS repository |
| Human alias | `technique-palm-muting` | same as identifier |
| Locators | `egls:02_Technique/Palm_Muting`, file path, URL | `02_Technique/Palm_Muting.md` only |

Organizational locators MAY take multiple equivalent forms for the same artifact: repository-relative file paths, scope-qualified colon paths (for example, `egls:02_Technique/Palm_Muting`), network URLs, or other storage keys. CRA permits multiple locators per artifact without affecting identity equivalence.

See [ADR-0002 — EGLS Production Identity Model](../../Architecture/ADRs/ADR-0002-egls-production-identity-model.md) for the accepted architectural decision. **Phase 2 (2026-08-11):** minimal identity registry implemented; see addendum below.

## Phase 2 Addendum (EGLS-002)

Second adoption increment: **`technique-left-hand-muting`** plus minimal identity registry.

| Field | Value |
|---|---|
| **Second canonical artifact** | `technique-left-hand-muting` |
| **EGLS encoding** | [`02_Technique/Left_Hand_Muting.md`](https://github.com/edbecnel/Electric-Guitar-Learning-System/blob/main/02_Technique/Left_Hand_Muting.md) |
| **Identity registry** | [`10_Reference/knowledge_object_registry.yaml`](https://github.com/edbecnel/Electric-Guitar-Learning-System/blob/main/10_Reference/knowledge_object_registry.yaml) |
| **Genesis provenance** | Phase 2 §2.2–2.3 (focused v1) |

### ADR-0002 registry demonstration

| Object | `canonical_id` | Slug `id` | Locators |
|---|---|---|---|
| Palm muting | `urn:uuid:184dd940-453f-4aeb-92cb-7d155a061006` | `technique-palm-muting` | `02_Technique/Palm_Muting.md`, `egls:02_Technique/Palm_Muting` |
| Left-hand muting | `urn:uuid:30543cfe-269e-403a-b78a-9c2584b9a232` | `technique-left-hand-muting` | `02_Technique/Left_Hand_Muting.md`, `egls:02_Technique/Left_Hand_Muting` |

Slug `id` values remain in Knowledge Object front matter; registry holds production UUID bindings per ADR-0002.

### ADR-0003 resolution layer

Registry serves as the **resolution** step between candidate slug identifiers and organizational locators. Registry `tags` provide hooks for a future discovery index; no full-text search index yet.

### FP-3 cross-reference

`technique-palm-muting` and `technique-left-hand-muting` reference each other by canonical `id`, not by file path.

## CRA-0003 Representation Fidelity

| Requirement                         | Evidence                                                                     | Met? |
| ----------------------------------- | ---------------------------------------------------------------------------- | ---- |
| **RF-1** Fidelity reference         | Tab example evaluated against Knowledge Object body, not vice versa          | Yes  |
| **RF-2** Distinction preservation   | Hand position, pinky-side edge, bridge placement preserved from genesis §2.1 | Yes  |
| **RF-3** Lossy boundaries           | One-line summary below is **lossy**; must not substitute for object          | Yes  |
| **RF-4** Representational change    | Reformatting Markdown layout does not change semantic version                | Yes  |
| **RF-5** Semantic change versioning | Substantive technique change would update `version` / lineage                | Yes  |
| **RF-6** Regeneration integrity     | Regenerated Markdown must preserve committed distinctions                    | Yes  |
| **RF-7** Navigation separation      | File path is not authoritative relationship definition                       | Yes  |

### Lossy derived representation (RF-3 example)

> *Palm muting shortens notes by resting your hand on the strings.*

This summary omits hand position (pinky-side edge, bridge placement), picking approach (downstrokes vs alternate), and distinction from left-hand muting. It is **lossy** and MUST NOT replace the canonical Knowledge Object.

### Fidelity-preserving derived representation (RF-4 example)

The ASCII tab diagram in the Knowledge Object body is a **fidelity-preserving** encoding of the genesis document's notation for the same version of the technique.

## Conformance Summary

EGLS can demonstrate CRA-0001 principles-level, CRA-0002 identity-level, and CRA-0003 fidelity-level conformance for two related technique artifacts and a minimal identity registry. Full repository-wide conformance is not claimed.

## Gaps and Watch Items

| Gap | Notes | Future action |
|---|---|---|
| Identity registry partial | Registry binds two objects; slug remains in front matter without `canonical_id` field | Add `canonical_id` to metadata standard when ready |
| No discovery index | Registry tags exist but no search index or semantic path vocabulary | See ADR-0003; implement when object count grows |
| `source` field not in EGLS field reference | Used for provenance in adoption exercise | Propose field in EGLS metadata standard |
| Version lineage not exercised | v1.0 initial designation only | Demonstrate on first semantic amendment |
| Evidence promotion | Not applicable to this guitar technique object | CRA-0004 candidate if AERF/ELS evidence workflow proceeds |

## Related Documents

- [Genesis Document Inventory](Genesis_Document_Inventory.md)
- [ADR-0001 — EGLS Identifier Alignment](../../Architecture/ADRs/ADR-0001-egls-identifier-alignment.md)
- [ADR-0002 — EGLS Production Identity Model](../../Architecture/ADRs/ADR-0002-egls-production-identity-model.md)
- [ADR-0003 — Discovery and Retrieval Separation](../../Architecture/ADRs/ADR-0003-discovery-and-retrieval-separation.md)
- [CRA-0001](../../Specifications/CRA-0001.md) · [CRA-0002](../../Specifications/CRA-0002.md) · [CRA-0003](../../Specifications/CRA-0003.md)
