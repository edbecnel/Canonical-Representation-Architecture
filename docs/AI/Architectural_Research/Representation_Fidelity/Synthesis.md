[Home](../../../../README.md) › [Project Index](../../../../PROJECT_INDEX.md) › [AI](../../README.md) › [Architectural Research](../README.md) › [Representation Fidelity](README.md) › Synthesis

> **Status:** Maintained
> **Document Class:** Architectural Research
> **Owner:** CRA Architecture Team
> **Applies To:** Architectural research supporting CRA-0003
> **Last Reviewed:** 2026-08-10
> **Review Frequency:** On Change

# Representation Fidelity — Research Synthesis

## Research Phase Status

The representation fidelity inquiry is **complete** for CRA-0003 Draft v1.0.

This document is **informative, not normative**. Authority for fidelity requirements rests in **CRA-0003 — Representation Fidelity**.

## Governing Question

Per [Architectural Evaluation Methodology](../Canonical_Knowledge/Architectural_Evaluation_Methodology.md), the governing question is:

> **What must representation fidelity be in order for CRA to preserve semantic integrity when derived representations are created, replaced, or discarded?**

CRA-0001 normativized FP-1 (separation of canonical and derived) and established a preservation and fidelity obligation within scope. CRA-0002 defined identity, versioning, and the representational/semantic change boundary without operationalizing fidelity. This synthesis records the engineering decisions that close that gap.

## Sources Synthesized

| Source | Contribution |
|---|---|
| [CRA-0001](../../../Specifications/CRA-0001.md) FP-1, FP-3, FP-5; Derived Representation | Constitutional constraints; fidelity obligation in Canonical Knowledge definition |
| [CRA-0002](../../../Specifications/CRA-0002.md) IM-3, representational/semantic change table | Interface point: derived representation as equivalence category; version boundary |
| [Conclusions](../Canonical_Knowledge/Conclusions.md) open Q3 | Fidelity rules scope |
| [Composer_2.5.md](../Canonical_Knowledge/Composer_2.5.md) §4, §8, §10, formal model | Distinction preservation; derived vs canonical; fidelity criterion; counterexamples |
| [Claude_Sonnet_GitHub_Copilot.md](../Canonical_Knowledge/Claude_Sonnet_GitHub_Copilot.md) §2 | Fidelity as evaluation against canonical distinctions |
| [Grok.md](../Canonical_Knowledge/Grok.md) §2–5 | Recoverability; canonical as reference beneath representations |
| [Claude_Sonnet_Web.md](../Canonical_Knowledge/Claude_Sonnet_Web.md) | Constraint structure; generativity test for derivation |

## Convergence

All sources independently support the following fidelity themes:

| Theme | Summary | CRA relevance |
|---|---|---|
| **Canonical as reference** | Fidelity is judged against canonical artifacts, not derived representations | Operationalizes FP-1 |
| **Distinction preservation** | Fidelity means preserving scope-committed distinctions; collapse is failure | Core of semantic integrity |
| **Derived regenerability** | Loss of a derived representation is acceptable if regeneration preserves committed distinctions | Enables replaceable carriers |
| **Recoverability** | Valid representations must permit recovery of canonical content to required fidelity | Supports FP-5 preservation |
| **Navigation as derived** | Navigation views are derived representations, not canonical relationships | Supports FP-3 at fidelity layer |
| **Lossy derivation is explicit** | Summaries, embeddings, and inference products are not fidelity-preserving unless scope says otherwise | Prevents silent canonical substitution |

## Chosen CRA Fidelity Architecture

The following decisions are recorded as engineering rationale for CRA-0003.

### 1. Fidelity is distinction preservation within scope

Representation fidelity means a derived representation preserves all **committed distinctions** that scope governance requires for a given canonical artifact and version.

A committed distinction is any semantic, epistemic, relational, or structural commitment that scope policy treats as irreducible — including dispute structure, supersession markers, epistemic status, and exact wording when scope requires it.

**Rationale:** Composer §4, §89; Claude GitHub Copilot §2. Aligns with CRA's "semantic integrity" objective without requiring philosophical definitions of "meaning."

### 2. Canonical artifact is the fidelity reference

An adopter MUST evaluate derived representations against designated canonical artifacts (per CRA-0002 identity binding), not against other derived representations.

**Rationale:** FP-1; Grok recoverability property. Prevents derivation chains that cite derived artifacts as authoritative (hallucination loops per Gemini research).

### 3. Representational change versus semantic change (operationalized)

| Change | Canonical impact | Version impact | Fidelity impact |
|---|---|---|---|
| **Representational change** | Unchanged | Unchanged | New derived representation MUST be fidelity-preserving for the same version |
| **Semantic change** | Unchanged identity | New version per CRA-0002 IM-5 | Prior version remains reference for historical references; new version has its own fidelity obligations |

**Rationale:** CRA-0002 table; CRA-0003 operationalizes the fidelity column.

### 4. Regeneration policy

Derived representations MAY be discarded and regenerated provided regeneration is fidelity-preserving for the referenced canonical artifact and version.

An adopter MUST NOT treat regeneration as an opportunity to silently alter committed distinctions.

**Rationale:** Composer §4 derived representations table; operational rule of thumb (delete/rebuild test).

### 5. Lossy derivations are permitted but bounded

Lossy derived representations (summaries, embeddings, ranked indexes, inference products) MAY exist but MUST NOT be treated as canonical substitutes and MUST be identifiable as lossy relative to their source canonical artifact and version.

**Rationale:** Composer §10 counterexamples (AI summary, search index); Claude Web generativity test.

### 6. Navigation fidelity (FP-3 interface)

Navigation structures (TOCs, sidebars, browse hierarchies, hyperlink graphs) are derived representations of canonical relationships. They MUST NOT be treated as the authoritative definition of relationships among canonical artifacts.

**Rationale:** FP-3; CRA-0000 §6.3. CRA-0003 addresses fidelity of navigation as derived view, not relationship identity (full relationship model may emerge later).

## Explicit Non-Adoptions

| Approach | Why rejected |
|---|---|
| **Mandatory interchange format** | Implementation prescription; violates technology-independence |
| **Automated fidelity certification** | Validation tooling deferred |
| **Content-hash as fidelity proof** | Conflates encoding with semantic commitment |
| **Representation-primary recovery** | Inverted architecture; Grok and Composer invertibility critique |

## Relationship to CRA-0001 and CRA-0002

| Upstream spec | CRA-0003 operationalization |
|---|---|
| FP-1 | Canonical vs derived separation; fidelity reference direction |
| FP-3 | Navigation as derived representation subject to fidelity rules |
| FP-5 | Preservation across regeneration; no silent distinction loss |
| IM-3 category 4 | Defines "derived representation" for fidelity evaluation |
| IM-5 / versioning table | Semantic change triggers new version, not fidelity-only update |

## Handoff to CRA-0003

**Status:** Complete (2026-08-10). Normative content is in [`CRA-0003 — Representation Fidelity`](../../../Specifications/CRA-0003.md).

CRA-0003:

- defines representation fidelity, derivation, and committed distinctions;
- normativizes fidelity requirements RF-1 through RF-7;
- operationalizes the representational/semantic change boundary from CRA-0002;
- defers validation tooling, publication pipeline implementation, and full relationship model.

This research directory remains available as engineering evidence. It does not derive normative authority.

## Related Documents

- [CRA-0003 — Representation Fidelity](../../../Specifications/CRA-0003.md)
- [CRA-0002 — Identity Model](../../../Specifications/CRA-0002.md)
- [CRA-0001 — Foundational Architectural Principles](../../../Specifications/CRA-0001.md)
- [Canonical Knowledge Conclusions](../Canonical_Knowledge/Conclusions.md)
