[Home](../../README.md) › [Project Index](../../PROJECT_INDEX.md) › [Development](README.md) › Knowledge Interaction/Evolution Workstream

> **Status:** Maintained
> **Owner:** Architecture Team
> **Applies To:** CRA program evolution — knowledge interaction and controlled evolution
> **Last Reviewed:** 2026-08-22
> **Review Frequency:** On Change

# Knowledge Interaction/Evolution Workstream

## Purpose

This document is the **primary living bridge** between the preserved discovery records and future CRA architectural work:

- [AI Canonical Knowledge Interaction and Evolution](../Architecture/Discovery_Records/AI_Canonical_Knowledge_Interaction_and_Evolution.md) — second-wave discovery
- [Pragmatic Canonicality and Delegated Authority](../Architecture/Discovery_Records/Pragmatic_Canonicality_and_Delegated_Authority.md) — third-wave discovery

It is **informative program guidance**, not a normative specification. It maps discoveries to architectural questions, candidate workstreams, dependencies, and potential outcomes without prematurely converting hypotheses into CRA structure.

## Source Discovery Records

- [AI Canonical Knowledge Interaction and Evolution](../Architecture/Discovery_Records/AI_Canonical_Knowledge_Interaction_and_Evolution.md) — Architectural Discovery Record (Permanent Historical Record)
- [Pragmatic Canonicality and Delegated Authority](../Architecture/Discovery_Records/Pragmatic_Canonicality_and_Delegated_Authority.md) — Architectural Discovery Record (Candidate Architectural Position)

The discovery record bodies are preserved as historical reasoning. This workstream may refine, reject, or supersede their hypotheses; it must not rewrite discovery records in place.

## Workstream Flow

```text
Discovery
    ↓
Architectural Questions
    ↓
Candidate Workstreams
    ↓
Dependencies
    ↓
Research / Validation Needed
    ↓
Potential Normative Outcomes
```

Potential normative outcomes are **illustrative**. A candidate workstream may produce zero, one, or multiple specifications, ADRs, handbook guidance, or Watch Item resolutions. Workstreams are **not** predetermined specification boundaries.

## Relationship to Existing CRA Foundation

This workstream builds on the foundational trilogy without modifying it normatively in this integration pass:

| Existing artifact | Relevance |
|---|---|
| [CRA-0001](../Specifications/CRA-0001.md) FP-1–FP-5 | Constitutional principles; evaluation baseline for foundational questions |
| [CRA-0002](../Specifications/CRA-0002.md) | Identity, lineage, supersession — relevant to knowledge evolution |
| [CRA-0003](../Specifications/CRA-0003.md) RF-7 | Navigation as derived representation — relevant to traversal |
| [CRA Adoption Roadmap](CRA_Adoption_Roadmap.md) Options A–D | Mutually exclusive strategic paths for next substantive work; this workstream runs in parallel and informs future path selection |

## Architectural Questions Extracted from Discovery

The following questions require workstream evaluation. They are drawn from discovery §§2–28 and §33.

### Consumption and Traversal

1. Must CRA explicitly require that canonical knowledge be traversable, or is this already entailed by FP-3 and existing obligations?
2. How do purpose-specific traversals (learning paths, answers, recommendations) relate to derived representations under FP-1?
3. What architectural boundary separates CRA's traversal enablement from consumer-prescribed journeys?

### Knowledge Evolution

4. Should knowledge gaps be first-class canonical entities, managed artifacts, implementation metadata, or something else?
5. What is the architectural relationship between candidate knowledge and canonical knowledge?
6. What constitutes a canonicalization policy at the architectural level (without prescribing a detailed schema)?
7. How should re-evaluation of existing canonical knowledge be triggered and governed?
8. How does controlled evolution interact with CRA-0002 lineage and supersession?

### Applicability and Epistemic Modeling

9. Are canonicality and applicability distinct architectural properties?
10. Are context and applicability distinct architectural concepts?
11. How does applicability relate to scope, relationships, qualification, epistemic status, and canonical assertions?
12. How should uncertainty, subjective knowledge, contested knowledge, and legitimate alternatives be represented?
13. When can applicability not be deterministically encoded?

### AI Interaction

14. What technology-independent roles does CRA need for AI-assisted consumption and evolution?
15. How should AI-assisted canonicalization be architecturally supported without requiring human approval of every candidate?
16. How should multiple independent evaluators participate without reducing evaluation to majority voting?
17. Is canonical authority independent of any particular reasoning agent, or is this already entailed by FP-4?

### Cross-Authority Knowledge

18. How should canonical knowledge maintained by different authorities interoperate?
19. How should trust, provenance, conflicting authorities, and external canonical references be handled?

### Consumer Transparency

20. How should a consuming system distinguish canonical knowledge from derived representations?
21. How should a system communicate when a response depends partly on canonical knowledge and partly on knowledge outside the canonical layer?

### Delegated Authority and Pragmatic Canonicalization

The following questions are drawn from [Pragmatic Canonicality and Delegated Authority](../Architecture/Discovery_Records/Pragmatic_Canonicality_and_Delegated_Authority.md) §§9–13 and §17.

22. Does FP-4 already entail that canonical authority may be delegated, or does CRA need an explicit delegation architecture?
23. How should the delegation chain (governing authority → canonicalization authority → designation) be represented and recovered?
24. How should canonicalization rigor be recorded separately from canonical status?
25. What architectural support does pragmatic canonicalization require beyond existing FP-4 recoverability?
26. What provenance metadata is sufficient for delegated and pragmatic canonicalization decisions?
27. How should economic and latency constraints on canonicalization be architecturally acknowledged without prescribing optimization algorithms?

## Foundational Questions for CRA-0001 Evaluation

These discoveries appear potentially foundational. **CRA-0001 must not be modified normatively until separately evaluated.**

| Question | Discovery reference | Evaluation needed |
|---|---|---|
| **Traversability** | §§3, 29.1–29.2 | Entailed by FP-3? New obligation? Lower-level spec only? |
| **Reasoning-agent independence of canonical authority** | §17, 29.8 | Entailed by FP-4 (Governance Designation)? Refinement of FP-4? New obligation? |
| **Canonicality ≠ universal applicability** | §§20–21, 29.11 | Wording negation sufficient, or distinct applicability architecture required? |
| **Context vs applicability** | §21 | Distinct concepts? Relationship to scope and relationships? |
| **Delegated canonical authority** | Pragmatic §§9–10, 17 | Entailed by FP-4? Refinement of FP-4? New obligation? |
| **Pragmatic canonicalization** | Pragmatic §§11–13, 17 | New architectural concept? Extension of canonicalization policy (AWI-0001)? |

## Candidate Principle Evaluation Matrix

The following maps §17 candidate principles from [Pragmatic Canonicality and Delegated Authority](../Architecture/Discovery_Records/Pragmatic_Canonicality_and_Delegated_Authority.md) to likely disposition and CKES experimental evidence. **CRA-0001 must not be modified normatively until this evaluation is completed.**

| Candidate principle | Likely disposition | Related Watch Item | CKES evidence (research doc §) |
|---|---|---|---|
| Canonicality is a governance property | Already largely normative in CRA-0001; evaluate informative cross-link only | [AWI-0002](../Architecture/Watch_Items/AWI-0002-applicability-and-epistemic-modeling.md) | — |
| Canonicality is scoped | Already normative (Scope, FP-4) | — | — |
| Canonical authority may be delegated | **New**; likely future extension of FP-4 or separate governance spec | [AWI-0005](../Architecture/Watch_Items/AWI-0005-delegated-authority-and-pragmatic-canonicalization.md) | §3, §18, §33 |
| Automated delegated authority is permissible | **New**; ties to technology-independent role model | [AWI-0003](../Architecture/Watch_Items/AWI-0003-ai-assisted-knowledge-evaluation.md), AWI-0005 | §3, §18, §24, §33 |
| Canonicalization rigor is governed | **New**; inform canonicalization policy work | [AWI-0001](../Architecture/Watch_Items/AWI-0001-knowledge-evolution-and-canonicalization.md), AWI-0005 | §§4–5, §10 |
| Pragmatic canonicalization is legitimate | **New**; requires CKES validation | AWI-0005 | §§4–5, §19–20, §35 Q4–Q14 |
| Canonical representation is evolvable | Partially normative via CRA-0002 supersession | AWI-0001 | §26–27 |
| Provenance supports correctability | Partially normative via FP-4 recoverability; may need provenance metadata spec | AWI-0001, AWI-0005 | §§8–10, §26 |

## Candidate Workstreams

Five candidate workstreams group related architectural concerns. Names are descriptive; **no `CRA-NNNN` identifiers are assigned** until a normative specification is actually chartered.

### Candidate Workstream — Canonical Relationships

**Concerns:** Navigable knowledge space; relationship semantics; disagreement and alternatives as canonical knowledge; illustrative relationship distinctions (`requires`, `alternative-to`, `qualifies`, etc.).

**Dependencies:** FP-3; CRA-0003 RF-7; overlaps [Adoption Roadmap](CRA_Adoption_Roadmap.md) Option B (Canonical Relationship Model).

**Potential outcomes:** Normative specification(s); ADRs during adoption; Watch Item resolution.

### Candidate Workstream — Context, Applicability, and Epistemic Modeling

**Concerns:** Context vs applicability; canonicality vs applicability; subjective, conditional, and contested knowledge; uncertainty; epistemic status; applicability encoding limits.

**Dependencies:** CRA-0001 scope; likely informed by Canonical Relationships workstream.

**Potential outcomes:** Normative specification(s); possible CRA-0001 principle evaluation (separate decision); [AWI-0002](../Architecture/Watch_Items/AWI-0002-applicability-and-epistemic-modeling.md) resolution.

### Candidate Workstream — Knowledge Consumption and Traversal

**Concerns:** "CRA enables traversal; consuming systems prescribe journeys"; purpose-specific derived traversals; derived outputs (answers, lessons, paths) distinct from canonical knowledge.

**Dependencies:** FP-1; Canonical Relationships; Applicability modeling.

**Potential outcomes:** Normative specification(s) and/or adoption guidance.

### Candidate Workstream — Knowledge Evolution and Canonicalization

**Concerns:** Knowledge gaps; candidate knowledge; canonicalization lifecycle; canonicalization policy (architectural concept); re-evaluation; interaction with supersession.

**Dependencies:** FP-4; CRA-0002 lineage; evidence concepts; may relate to [Adoption Roadmap](CRA_Adoption_Roadmap.md) Option A (CRA-0004 Evidence Promotion candidate) when that path is selected.

**Potential outcomes:** Normative specification(s); [AWI-0001](../Architecture/Watch_Items/AWI-0001-knowledge-evolution-and-canonicalization.md) resolution.

### Candidate Workstream — AI Interaction

**Concerns:** AI as consumer and contributor; technology-independent roles; AI-assisted canonicalization; independent evaluation; reasoning vs authority.

**Dependencies:** Knowledge Evolution and Canonicalization workstream.

**Potential outcomes:** Normative specification(s); informative extensions to [AI domain](../AI/README.md); [AWI-0003](../Architecture/Watch_Items/AWI-0003-ai-assisted-knowledge-evaluation.md) resolution.

## Dependency Ordering (Analysis, Not Chartering)

```text
CRA-0001 through CRA-0003 (existing)
        ↓
Canonical Relationships
        ↓
Context, Applicability, and Epistemic Modeling
        ↓
Knowledge Consumption and Traversal
        ↓
Knowledge Evolution and Canonicalization
        ↓
AI Interaction

Optional parallel when roadmap Option A is selected:
CRA-0004 Evidence Promotion (candidate) → informs Evolution workstream
```

## Consolidated Watch Items

| Watch Item | Scope |
|---|---|
| [AWI-0001](../Architecture/Watch_Items/AWI-0001-knowledge-evolution-and-canonicalization.md) | Knowledge gaps, candidate knowledge, canonicalization policy, re-evaluation |
| [AWI-0002](../Architecture/Watch_Items/AWI-0002-applicability-and-epistemic-modeling.md) | Context vs applicability, epistemic status, contested knowledge |
| [AWI-0003](../Architecture/Watch_Items/AWI-0003-ai-assisted-knowledge-evaluation.md) | AI-assisted canonicalization, independent evaluation, evidence aggregation |
| [AWI-0004](../Architecture/Watch_Items/AWI-0004-cross-authority-canonical-knowledge.md) | Cross-repository authority, trust, external references |
| [AWI-0005](../Architecture/Watch_Items/AWI-0005-delegated-authority-and-pragmatic-canonicalization.md) | Delegated authority, pragmatic canonicalization, rigor vs status |

## Research / Validation Needed

Targeted architectural research (multi-model or directed analysis) may be warranted **per candidate workstream** before normative authoring. Research is not required for all areas.

| Area | Research question | Priority |
|---|---|---|
| Applicability vs context | What must CRA distinguish architecturally? | High — blocks epistemic modeling |
| Knowledge gaps | Entity vs metadata vs derived diagnostic | High — blocks evolution architecture |
| Relationship model | Minimum semantic expressiveness for FP-3 | High — overlaps roadmap Option B |
| AI evaluation aggregation | Evidence model without majority voting | Medium — blocks AI interaction spec |
| Cross-authority knowledge | Trust and conflict boundaries | Lower — explicitly deferred in discovery §27 |

## Potential Normative Outcomes (Illustrative)

The following are **examples only**. Chartering decisions belong to future governed specification work.

- Normative specification for canonical relationships (related to roadmap Option B)
- Normative specification for context, applicability, and epistemic modeling
- Normative specification for knowledge consumption and traversal
- Normative specification for knowledge evolution and canonicalization
- Normative specification for AI interaction architecture
- [CRA-0004](CRA_Adoption_Roadmap.md) Evidence Promotion — **only if** roadmap Option A is selected; identifier already established in roadmap as candidate
- ADRs arising from adoption exercises
- Promotion or splitting of Watch Items

## Relationship to Adoption Roadmap

[CRA Adoption Roadmap](CRA_Adoption_Roadmap.md) Options A–D are **mutually exclusive strategic alternatives** for the next substantive work path ("choose one path based on program need").

This workstream is **not** a competing Option E. It is a **parallel architectural analysis track** that:

- preserves and structures discoveries from the AI knowledge interaction discovery record;
- informs future selection among Options A–D and subsequent normative chartering;
- may surface questions resolvable through adoption exercises (Option D) before specification.

## Cross-Repository Propagation (Future)

After relevant candidate workstreams produce chartered outcomes, propagate via separate adoption handoffs. No adopter repository changes are in scope for this workstream's initial integration.

| Concern | EGLS | ELS | CALS | Recipe Vault |
|---|---|---|---|---|
| Traversal / derived pathways | Learning paths, practice | Engineering paths | Culinary paths | Recipe-step explanations |
| Knowledge gaps | Missing technique detection | Analysis gaps | Ingredient/process gaps | Recipe-driven gaps |
| Candidate knowledge | Learner-use feedback | Analysis hypotheses | Workflow findings | Interpretation candidates |
| Canonicalization | Guitar authority policy | Evidence promotion | Culinary authority | Consumer, not authority |
| Applicability | Technique context | Circuit preconditions | Substitutions | Step applicability |
| Cross-authority refs | Electronics from ELS | — | — | CALS consumption |

## Items Intentionally Unresolved

- Discovery-record serial ID convention (descriptive filenames used until governed decision)
- Whether each candidate workstream becomes a spec, multiple specs, ADRs only, or remains guidance
- Specific relationship type taxonomy (discovery examples are illustrative)
- Commercial AI model names in normative architecture
- AI role name finalization
- Knowledge gap persistence layer (canonical vs implementation)
- Human review requirement triggers
- Mixed canonical/non-canonical provenance in AI responses
- All §33 open questions until corresponding workstream analysis

## Related Documents

- [AI Canonical Knowledge Interaction and Evolution](../Architecture/Discovery_Records/AI_Canonical_Knowledge_Interaction_and_Evolution.md)
- [Pragmatic Canonicality and Delegated Authority](../Architecture/Discovery_Records/Pragmatic_Canonicality_and_Delegated_Authority.md)
- [CKES — Pragmatic Canonicalization Research and Validation](https://github.com/edbecnel/Canonical-Knowledge-Engineering-System/blob/main/docs/Development/Pragmatic_Canonicalization_Research_and_Validation.md)
- [CKES CRA Findings Report](https://github.com/edbecnel/Canonical-Knowledge-Engineering-System/blob/main/docs/Development/CRA_Findings_Report.md)
- [Discovery Records](../Architecture/Discovery_Records/README.md)
- [CRA-0000](../../CRA-0000.md)
- [CRA Adoption Roadmap](CRA_Adoption_Roadmap.md)
- [Watch Items](../Architecture/Watch_Items/README.md)
- [PROJECT_INDEX.md](../../PROJECT_INDEX.md)
