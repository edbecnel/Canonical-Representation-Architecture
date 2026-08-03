# ASR Bootstrap Report

[Home](README.md) › ASR Bootstrap Report

> **Status:** Maintained
> **Owner:** Architecture Team
> **Applies To:** Architecture Specification Repository bootstrap tracking
> **Last Reviewed:** 2026-08-03

## Purpose

Record the outcome of the Canonical Representation Architecture (CRA) Architecture Specification Repository bootstrap per the EDF [Architecture Specification Repository Bootstrap Procedure](https://github.com/edbecnel/Engineering-Documentation-Framework/blob/main/docs/Development/Repository_Bootstrap/Architecture_Specification_Repository/Bootstrap_Procedure.md).

## Bootstrap Summary

| Field | Value |
|---|---|
| **Repository** | Canonical Representation Architecture |
| **EDF profile** | `core` |
| **Bootstrap procedure** | Architecture Specification Repository Bootstrap Procedure |
| **Started** | 2026-08-03 |
| **Completed** | 2026-08-03 |
| **Performed by** | Human-directed AI-assisted bootstrap |

## Steps Completed

| Step | Status | Notes |
|---|---|---|
| Inspect repository | Complete | 1 commit, `CRA-0000.md` at root, no EDF structure |
| Preserve historical artifacts | Complete | `CRA-0000.md` not relocated or modified |
| Confirm ASR intent | Complete | CRA is an Architecture Specification Repository |
| Apply EDF Core | Complete | `adopt-edf.sh bootstrap --profile core` |
| Apply ASR guidance | Complete | Domain READMEs populated; Watch_Items and Governance created |
| Map existing documents | Complete | `CRA-0000` mapped at root; logical domain `docs/Architecture/` |
| Create missing bootstrap artifacts | Complete | README, identity docs, domain READMEs |
| Record deferred items | Complete | See Deferred Artifacts below |
| Validate | Complete | Framework Advisor run with `profile: core` |
| Report gaps | Complete | See Gaps and Feedback sections |

## Document Mappings

| Original path | New path | Document type | Normative? | Notes |
|---|---|---|---|---|
| `CRA-0000.md` | `CRA-0000.md` (preserved) | Architectural Discovery Record | No | Permanent historical foundation; repository began with this document. Logical domain: `docs/Architecture/`. Relocation deferred as explicit evolution decision. |

## Deferred Artifacts

| Artifact | Reason deferred | Target date |
|---|---|---|
| `CRA-0001` and subsequent normative specs | Awaiting post-bootstrap architectural development in `docs/Specifications/` | TBD |
| Repository-wide controlled vocabulary / glossary (`docs/Reference/Glossary.md`) | Vocabulary should emerge from foundational specifications, not premature bootstrap standardization. CRA terminology will largely be established by `CRA-0001` and subsequent specs. | After `CRA-0001` |
| Foundational principles document(s) | Recommended early; derive from discovery record over time | TBD |
| Full governance policy set | Maturity-dependent | TBD |
| ADRs | None yet; `docs/Architecture/ADRs/` prepared | TBD |
| `CHANGELOG.md` | Framework Advisor recommended root file; not required at bootstrap | TBD |
| Reference implementation | Optional; non-canonical; not applicable now | N/A |
| `CRA-0000` relocation | Preserved at root as historical foundation; any future move is an explicit repository evolution decision | N/A |

## Gaps Requiring Human Decision

- [ ] License selection for the CRA repository (`README.md` placeholder)
- [ ] Timing and scope of `CRA-0001` as first normative specification
- [ ] Whether to pursue Navigable-tier conformance remediation for remaining Framework Advisor advisories

## Framework Advisor Results

| Metric | Score | Date | Report path |
|---|---|---|---|
| Overall | 65% | 2026-08-03 | `reports/conformance/framework-advisor-20260803-183920.txt` |
| Structure | 97% | 2026-08-03 | `reports/conformance/framework-advisor-20260803-183920.txt` |
| Navigation | 97% | 2026-08-03 | `reports/conformance/framework-advisor-20260803-183920.txt` |
| AI | 10% | 2026-08-03 | `reports/conformance/framework-advisor-20260803-183920.txt` |
| Governance | 57% | 2026-08-03 | `reports/conformance/framework-advisor-20260803-183920.txt` |

All scores meet the EDF **Bootstrap** tier targets (Overall ≥ 50%, Structure ≥ 80%, Navigation ≥ 40%, AI ≥ 10%, Governance ≥ 20%).

**Known intentional advisories:**

- `CRA-0000.md` and `ASR_BOOTSTRAP_REPORT.md` listed under "Markdown outside canonical locations" — `CRA-0000` preserved at root per Historical Preservation Principle; bootstrap report at root per EDF ASR template
- Low AI and Governance scores expected at bootstrap tier
- Missing software profile directories not penalized under `profile: core`

## Feedback for EDF

1. **Watch_Items not in Core `required_dirs`** — ASR Validation Checklist requires `docs/Architecture/Watch_Items/README.md`, but `edf_profile.sh` Core dirs do not include `Watch_Items/`; must be created manually.
2. **Governance README not generated** — `generate_documentation_skeleton.sh` creates `docs/Governance/` directory but no `README.md`; ASR checklist requires it.
3. **Generic skeleton prose** — `docs/Architecture/README.md` and `docs/Specifications/README.md` templates use software-oriented default text; ASR adopters must populate post-bootstrap.
4. **Root `README.md` not generated** — skeleton creates `PROJECT_INDEX` template but not `README.md`; ASR and general Bootstrap both require manual creation.
5. **Metadata format divergence** — `CRA-0000` uses table metadata; EDF `Document_Metadata_Standard` uses blockquote format. Historical records should retain pre-bootstrap metadata without reformatting.
6. **`ASR_BOOTSTRAP_REPORT.md` template links** — template references EDF-internal paths that do not exist in adopting repos; use external GitHub links or EDF-clone-only references.
7. **Historical preservation guidance** — Bootstrap Procedure and Playbook should codify: bootstrap adapts to existing repository organization; relocation of discovery records requires compelling justification and is never mandatory.

## Related Documents

- [Validation Checklist (EDF)](https://github.com/edbecnel/Engineering-Documentation-Framework/blob/main/docs/Development/Repository_Bootstrap/Architecture_Specification_Repository/Validation_Checklist.md)
- [PROJECT_INDEX.md](PROJECT_INDEX.md)
- [CRA-0000.md](CRA-0000.md)
