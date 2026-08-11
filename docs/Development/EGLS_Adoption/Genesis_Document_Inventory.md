[Home](../../../README.md) › [Project Index](../../../PROJECT_INDEX.md) › [Development](../README.md) › EGLS Adoption › Genesis Document Inventory

> **Status:** Maintained
> **Document Class:** Adoption Exercise (informative)
> **Owner:** CRA Architecture Team
> **Applies To:** EGLS CRA adoption exercise
> **Last Reviewed:** 2026-08-11
> **Review Frequency:** On Change

# Genesis Document — Knowledge Object Inventory

## Purpose

This document inventories candidate Knowledge Objects extracted from the genesis curriculum document that informed EGLS and the broader CRA engineering path. It is **informative, not normative**.

## Source Document

| Field | Value |
|---|---|
| **Title** | Learning Electric Guitar — Guide for Casual Experience Acoustic Guitarists |
| **Location** | [`docs/Reference/Learning Electric Guitar - Guide for Casual Experience Acoustic Guitarists.docx`](../../Reference/Learning%20Electric%20Guitar%20-%20Guide%20for%20Casual%20Experience%20Acoustic%20Guitarists.docx) |
| **Scope** | CRA repository (provenance record); organizational locator, not canonical identity |
| **Content** | ~850 paragraphs; 8-phase electric guitar curriculum for experienced acoustic players |

## Selected First Sample

| Field | Value |
|---|---|
| **id** | `technique-palm-muting` |
| **EGLS type** | `technique` |
| **Source section** | Phase 2 §2.1 — Palm muting |
| **Implementation** | [Electric-Guitar-Learning-System `02_Technique/Palm_Muting.md`](https://github.com/edbecnel/Electric-Guitar-Learning-System/blob/main/02_Technique/Palm_Muting.md) |
| **Adoption report** | [CRA_Adoption_Report_EGLS-001.md](CRA_Adoption_Report_EGLS-001.md) |

## Candidate Inventory

| Priority | Section | Candidate object | EGLS `type` | Suggested `id` | Status |
|---|---|---|---|---|---|
| **1** | §2.1 | Palm muting | technique | `technique-palm-muting` | **Implemented** |
| **2** | §2.2–2.3 | Left-hand muting / stopping unused strings | technique | `technique-left-hand-muting` | **Implemented** (focused v1) |
| 3 | §2.4 | Muting during bends | technique | `technique-muting-during-bends` | Backlog |
| 4 | §2.4 | Practical Rule (muting) | reference | `reference-muting-practical-rule` | Backlog |
| 5 | §2.4 | Silent String Check drill | exercise | `exercise-silent-string-check` | Backlog |
| 6 | §2.4 | Bend, Release, Mute drill | exercise | `exercise-bend-release-mute` | Backlog |
| 7 | §3 | Bending and vibrato | technique | `technique-bending-vibrato` | Backlog |
| 8 | §4 | Slides, hammer-ons, pull-offs, legato | technique | `technique-legato` | Backlog |
| 9 | §5 | Power chord rhythm | technique | `technique-power-chord-rhythm` | Backlog |
| 10 | §6 | Blues and shuffle rhythm | technique | `technique-blues-shuffle-rhythm` | Backlog |
| 11 | §1 / §5 | Power chord root on 6th string | reference | `reference-power-chord-root-6th-string` | Backlog |
| 12 | §1 / §5 | Power chord root on 5th string | reference | `reference-power-chord-root-5th-string` | Backlog |
| 13 | §7 | Notes on 6th and 5th strings | fretboard-concept | `fretboard-concept-6th-5th-string-notes` | Backlog |
| 14 | §8 | CAGED as chord shapes | theory-concept | `theory-caged-chord-shapes` | Backlog |
| 15 | §9 | Minor pentatonic | scale | `scale-minor-pentatonic` | Backlog |
| 16 | §10 | Major pentatonic | scale | `scale-major-pentatonic` | Backlog |
| 17 | §11 | Chord tones | theory-concept | `theory-chord-tones` | Backlog |
| 18 | §12 | Six songs as course projects | learning-path | `learning-path-six-song-projects` | Backlog |
| 19 | §13 | Improvisation formula | theory-concept | `theory-improvisation-formula` | Backlog |
| 20 | End | Tone → Muting → Rhythm → … sequence | learning-path | `learning-path-electric-bridge-curriculum` | Backlog (meta) |

## Backlog Notes

- **Identity registry** introduced at [`10_Reference/knowledge_object_registry.yaml`](https://github.com/edbecnel/Electric-Guitar-Learning-System/blob/main/10_Reference/knowledge_object_registry.yaml) — binds opaque `canonical_id` (URN UUID), slug `id`, and organizational locators for both muting objects per ADR-0002.
- **Large sections** (§2.2–2.3 left-hand muting) may be split into additional Knowledge Objects per EGLS single-responsibility principle; current `technique-left-hand-muting` is a focused v1.
- **Learning Path** objects (`learning-path-*`) are composite; implement after foundational Techniques, References, and Scales exist.
- **Tab diagrams and ASCII notation** in the genesis document are **derived representations** of canonical technique content; preserve in Markdown as fidelity-preserving encodings per CRA-0003 RF-4.

## Related Documents

- [CRA_Adoption_Report_EGLS-001.md](CRA_Adoption_Report_EGLS-001.md)
- [CRA Adoption Roadmap](../CRA_Adoption_Roadmap.md)
- [CRA-0002 — Identity Model](../../Specifications/CRA-0002.md)
- [CRA-0003 — Representation Fidelity](../../Specifications/CRA-0003.md)
