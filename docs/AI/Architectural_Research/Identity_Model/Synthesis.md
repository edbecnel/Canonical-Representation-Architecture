[Home](../../../../README.md) › [Project Index](../../../../PROJECT_INDEX.md) › [AI](../../README.md) › [Architectural Research](../README.md) › [Identity Model](README.md) › Synthesis

> **Status:** Maintained
> **Document Class:** Architectural Research
> **Owner:** CRA Architecture Team
> **Applies To:** Architectural research supporting CRA-0002
> **Last Reviewed:** 2026-08-10
> **Review Frequency:** On Change

# Identity Model — Research Synthesis

## Research Phase Status

The identity model inquiry is **complete** for CRA-0002 Draft v1.0.

This document is **informative, not normative**. Authority for identity requirements rests in **CRA-0002 — Identity Model**.

## Governing Question

Per [Architectural Evaluation Methodology](../Canonical_Knowledge/Architectural_Evaluation_Methodology.md), the governing question is:

> **What must identity be in order for CRA to preserve semantic integrity across representational change?**

CRA-0001 deferred identifier syntax, equivalence rules, and versioning mechanics to CRA-0002 while normativizing FP-2: each canonical artifact MUST retain stable semantic identity independent of physical organization. This synthesis records the engineering decisions that operationalize that principle.

## Sources Synthesized

| Source | Contribution |
|---|---|
| [CRA-0000](../../../../CRA-0000.md) §6.2, §7.2 | Identity independent of organization; SIP as specialized reference, not full CRA |
| [CRA-0001](../../../Specifications/CRA-0001.md) FP-2, canonical artifact, scope | Constitutional constraints CRA-0002 must satisfy |
| SIP Whitepaper Principle 2 | Semantic identity ≠ transport location; one identity, many locators |
| [Conclusions](../Canonical_Knowledge/Conclusions.md) open Q2 | Identity model scope: identifiers, equivalence, versioning |
| [Composer_2.5.md](../Canonical_Knowledge/Composer_2.5.md) §8–9 | Identity anchor, version structure, lineage, counterexamples |
| [ChatGPT_GPT-5.5.md](../Canonical_Knowledge/ChatGPT_GPT-5.5.md) §2.1 | Four-way equivalence determination |

## Convergence

All sources independently support the following identity themes:

| Theme | Summary | CRA relevance |
|---|---|---|
| **Identity ≠ location** | Paths, URLs, filenames, and storage keys are locators, not identity | Directly operationalizes FP-2 and SIP Principle 2 |
| **Stable identifier at designation** | Every canonical artifact needs an identity anchor assigned at governance time | Required for preservation across change |
| **Equivalence determination** | Architecture must distinguish same artifact, different version, different artifact, and derived representation | Without this, preservation is indistinguishable from copying |
| **Governed versioning** | Semantic change is recorded; silent overwrite is architectural failure | Supports FP-5 preservation obligation |
| **Persistent lineage** | Superseded states remain resolvable for historical references | Supports contracts, standards, and audit trails |
| **Scope qualification** | Identity is meaningful within a declared scope | Consistent with FP-4 |

## Chosen CRA Identity Architecture

The following decisions are recorded as engineering rationale for CRA-0002. Normative text appears in the specification.

### 1. Scope-qualified opaque identifiers

CRA adopts a **requirement profile**, not a mandated global string format.

- Identifiers MUST be opaque with respect to storage layout.
- Identifiers MUST be scope-qualified (identity within a declared scope).
- Identifiers SHOULD be immutable once assigned.
- Adopters MAY use UUIDs, namespaced codes, URIs, or other encodings that satisfy the profile.

**Rationale:** ChatGPT §2.1 notes that stable identity does not require a particular format; it requires determinable equivalence. Composer §8 lists the identity anchor as minimum survivable information. A format-agnostic profile keeps CRA technology-independent.

### 2. Organizational locators are explicitly not identity

Paths (`docs/specs/foo.md`), URLs, commit refs, database keys, and index positions are **organizational locators**. They MAY change without altering canonical identity when no governed semantic change occurs.

**Rationale:** CRA-0000 §6.2; SIP Principle 2; Composer counterexample §10.6.

### 3. Four-way equivalence determination

An adopter MUST be able to determine whether two manifestations refer to:

1. the **same canonical artifact** (same identity, same version),
2. a **different version** of the same canonical artifact,
3. a **different canonical artifact**, or
4. a **derived representation** of canonical knowledge.

**Rationale:** ChatGPT §2.1. This is the minimum decision surface for identity-aware preservation.

### 4. Persistent identity with governed version lineage

- **Identity** persists across versions of the same artifact.
- **Version** records committed semantic state at a point in time.
- **Supersession** changes authoritative standing without destroying referential integrity.
- **Representational change** (new encoding of the same version) is distinct from **semantic change** (new version or lineage event). Fidelity rules for the former belong in CRA-0003.

**Rationale:** Composer §8–9 examples (REQ-042, superseded specifications). FP-5 requires preservation across change without silent corruption.

### 5. Governed split, merge, and cross-artifact equivalence

Split, merge, or declaration that two artifacts share equivalence MUST require an explicit governance act within scope. Equivalence MUST NOT be inferred from representation similarity alone.

**Rationale:** FP-4 governed designation. Prevents accidental collapse of distinct canonical commitments.

## Explicit Non-Adoptions

The following approaches were considered and **rejected** for CRA normative identity:

| Approach | Why rejected |
|---|---|
| **SIP `@path` / `sipi:` syntax** | Internet semantic addressing overlay; specialized reference per CRA-0000 §7.2, not CRA's domain-independent identity model |
| **Content-addressing as identity** | Hash of representation conflates identity with encoding; violates FP-1 and FP-2 |
| **Git paths or commit SHAs as identity** | Organizational locators; identity would break on relocation |
| **DOI or stable URL as identity** | Locator that may outlive or diverge from semantic content; locators may change while identity persists |
| **Global cross-scope federation** | Out of scope for CRA-0002; scope-bounded identity per FP-4 |

SIP's architectural insight — semantic identity independent of transport location — is adopted. SIP's concrete syntax, federated resolvers, and internet discovery mechanics are not.

## Relationship to CRA-0001

CRA-0002 does not redefine CRA-0001 principles or the canonical artifact primitive. It provides the identity mechanics that FP-2 requires:

| CRA-0001 principle | CRA-0002 operationalization |
|---|---|
| FP-2 | Canonical identifiers, equivalence rules, relocation invariance |
| FP-4 | Governed versioning, split/merge acts |
| FP-5 | Lineage preservation, supersession without reference loss |

## Handoff to CRA-0002

**Status:** Complete (2026-08-10). Normative content is in [`CRA-0002 — Identity Model`](../../../Specifications/CRA-0002.md).

CRA-0002:

- defines canonical identifier requirements and the identifier syntax profile;
- normativizes equivalence determination (IM-3) and versioning semantics (IM-5, IM-6);
- defers representation fidelity and validation to CRA-0003.

This research directory remains available as engineering evidence. It does not derive normative authority.

## Related Documents

- [CRA-0002 — Identity Model](../../../Specifications/CRA-0002.md)
- [CRA-0001 — Foundational Architectural Principles](../../../Specifications/CRA-0001.md)
- [Canonical Knowledge Conclusions](../Canonical_Knowledge/Conclusions.md)
- [CRA-0000](../../../../CRA-0000.md)
