[Home](../../README.md) › [Project Index](../../PROJECT_INDEX.md) › [Reference](README.md) › Glossary

> **Status:** Maintained
> **Owner:** Architecture Team
> **Applies To:** Controlled vocabulary for the Canonical Representation Architecture
> **Last Reviewed:** 2026-08-10
> **Review Frequency:** On Change

# CRA Controlled Vocabulary — Glossary

## Purpose

This glossary indexes **normative terms** defined in CRA specifications. It is a reference index, not a fourth normative specification. When a definition here conflicts with a specification, the specification governs.

Terms are traced to their authoritative source. Do not treat this document as introducing new normative requirements.

## How to Use

- **Adopters:** Use this glossary for consistent terminology across implementations and documentation.
- **Authors:** Add entries when new terms are normatively defined in CRA specifications; do not define terms here before they appear in a spec.

## Terms from CRA-0001 — Foundational Architectural Principles

| Term | Summary | Source |
|---|---|---|
| **Canonical Knowledge** | Governed, scope-bounded semantic content whose identity and preservation an architecture commits to across representational change — not any particular file, format, index, or derived artifact. | [CRA-0001 §Canonical Knowledge](../Specifications/CRA-0001.md#canonical-knowledge) |
| **Canonical Artifact** | The smallest governed unit of Canonical Knowledge within a scope; the unit to which identity, governance designation, preservation obligations, and relationships apply. | [CRA-0001 §Canonical Artifact](../Specifications/CRA-0001.md#canonical-artifact) |
| **Derived Representation** | Any encoding, publication, index, navigation view, inference product, or other artifact produced from Canonical Knowledge for storage, presentation, search, consumption, or reasoning. | [CRA-0001 §Derived Representation](../Specifications/CRA-0001.md#derived-representation) |
| **Scope** | A declared boundary within which canonical designation applies and within which preservation and governance obligations are meaningful. | [CRA-0001 §Scope](../Specifications/CRA-0001.md#scope) |
| **Governance Designation** | An explicit act by a defined authority or governance process that confers canonical status on content within a scope. | [CRA-0001 §Governance Designation](../Specifications/CRA-0001.md#governance-designation) |

## Terms from CRA-0002 — Identity Model

| Term | Summary | Source |
|---|---|---|
| **Canonical Identifier** | A stable, scope-qualified name assigned to a canonical artifact at governance designation time, independent of physical location, repository structure, filename, publication format, and storage technology. | [CRA-0002 §Canonical Identifier](../Specifications/CRA-0002.md#canonical-identifier) |
| **Organizational Locator** | Any address, path, URL, filename, commit reference, database key, index position, or other mechanism that locates a canonical artifact or its derived representation; architecturally distinct from a canonical identifier. | [CRA-0002 §Organizational Locator](../Specifications/CRA-0002.md#organizational-locator) |
| **Identity Binding** | The governed association between a canonical identifier and a canonical artifact within a scope, established at designation time and maintained across representational change. | [CRA-0002 §Identity Binding](../Specifications/CRA-0002.md#identity-binding) |
| **Identity Equivalence** | The determination that two manifestations refer to the same canonical artifact under CRA-0002 equivalence rules. | [CRA-0002 §Identity Equivalence](../Specifications/CRA-0002.md#identity-equivalence) |
| **Version** | A governed state of a canonical artifact at a point in time; the canonical identifier persists across versions. | [CRA-0002 §Version](../Specifications/CRA-0002.md#version) |
| **Lineage** | The ordered history of versions and governance events (amendment, supersession, split, merge) associated with a canonical identifier within a scope. | [CRA-0002 §Lineage](../Specifications/CRA-0002.md#lineage) |
| **Supersession** | A governed relationship in which a later version or canonical artifact replaces the authoritative standing of an earlier version or artifact without erasing identity or referential integrity of the superseded state. | [CRA-0002 §Supersession](../Specifications/CRA-0002.md#supersession) |

## Terms from CRA-0003 — Representation Fidelity

| Term | Summary | Source |
|---|---|---|
| **Committed Distinction** | A semantic, epistemic, relational, or structural commitment that scope governance treats as irreducible for a given canonical artifact and version. | [CRA-0003 §Committed Distinction](../Specifications/CRA-0003.md#committed-distinction) |
| **Derivation** | The production of a derived representation from one or more canonical artifacts, versions, or other derived representations governed within a scope. | [CRA-0003 §Derivation](../Specifications/CRA-0003.md#derivation) |
| **Representation Fidelity** | The degree to which a derived representation preserves all committed distinctions required by scope governance for the canonical artifact and version it expresses. | [CRA-0003 §Representation Fidelity](../Specifications/CRA-0003.md#representation-fidelity) |
| **Fidelity Reference** | The canonical artifact and version against which a derived representation's fidelity is evaluated; MUST be the designated canonical source, not another derived representation. | [CRA-0003 §Fidelity Reference](../Specifications/CRA-0003.md#fidelity-reference) |
| **Regeneration** | The replacement of a derived representation by a newly produced derived representation intended to express the same canonical artifact and version. | [CRA-0003 §Regeneration](../Specifications/CRA-0003.md#regeneration) |

## Derived Qualifiers (CRA-0003)

These qualifiers apply to derived representations and are defined within the Representation Fidelity term:

| Term | Summary | Source |
|---|---|---|
| **Fidelity-preserving** (derived representation) | A derived representation that preserves all committed distinctions required by scope governance for its fidelity reference. | [CRA-0003 §Representation Fidelity](../Specifications/CRA-0003.md#representation-fidelity) |
| **Lossy** (derived representation) | A derived representation that omits or alters one or more committed distinctions relative to its fidelity reference. | [CRA-0003 §Representation Fidelity](../Specifications/CRA-0003.md#representation-fidelity) |

## Change Types (CRA-0002 and CRA-0003)

| Term | Summary | Source |
|---|---|---|
| **Representational change** | Change affecting only encoding, format, publication channel, or organizational locator without governed semantic change; identity and version unchanged. | [CRA-0002 §Versioning](../Specifications/CRA-0002.md#representational-change-versus-semantic-change); [CRA-0003 §Derivation and Change Classification](../Specifications/CRA-0003.md#derivation-and-change-classification) |
| **Semantic change** | Governed change to committed semantic content; requires new version or lineage event per CRA-0002 IM-5. | [CRA-0002 §Versioning](../Specifications/CRA-0002.md#representational-change-versus-semantic-change); [CRA-0003 §RF-5](../Specifications/CRA-0003.md#rf-5--semantic-change-and-versioning) |

## Lineage Events (CRA-0002)

| Term | Summary | Source |
|---|---|---|
| **Amendment** | Creation of a new version with governed semantic change. | [CRA-0002 §Lineage events](../Specifications/CRA-0002.md#lineage-events) |
| **Split** | One canonical artifact becomes two or more distinct canonical artifacts. | [CRA-0002 §Lineage events](../Specifications/CRA-0002.md#lineage-events) |
| **Merge** | Two or more canonical artifacts are governed as a single canonical artifact or equivalence class. | [CRA-0002 §Lineage events](../Specifications/CRA-0002.md#lineage-events) |

## Maintenance

Update this glossary when CRA specifications add, revise, or deprecate normative terms. Each entry MUST trace to an authoritative specification section.

## Related Documents

- [CRA-0001 — Foundational Architectural Principles](../Specifications/CRA-0001.md)
- [CRA-0002 — Identity Model](../Specifications/CRA-0002.md)
- [CRA-0003 — Representation Fidelity](../Specifications/CRA-0003.md)
- [Reference domain](README.md)
