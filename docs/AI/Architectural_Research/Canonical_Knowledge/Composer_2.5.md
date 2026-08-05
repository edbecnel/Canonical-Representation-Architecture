# Architectural Inquiry: Canonical Knowledge

[Home](../../../../README.md) › [Project Index](../../../../PROJECT_INDEX.md) › [AI](../../README.md) › [Architectural Research](../README.md) › [Canonical Knowledge](README.md) › Architectural Inquiry: Canonical Knowledge

> **Status:** Draft
> **Owner:** CRA Architecture Team
> **Applies To:** Architectural research supporting the Canonical Representation Architecture
> **Last Reviewed:** 2026-08-05
> **Review Frequency:** On Change

**Independent Review for Canonical Representation Architecture (CRA)**  
**Model:** Composer 2.5  
**Date:** 2026-08-05

---

## Executive Position

CRA exists because engineering systems repeatedly fail at the same boundary: they treat a *particular encoding* as the thing worth preserving, then lose meaning, identity, or history when that encoding changes.

The term **Canonical Knowledge** names what must sit on the *other side* of that boundary—not a format, not a publication, not an index, and not a convenience copy labeled "source of truth."

This analysis proposes that canonical knowledge is best understood architecturally as:

> **The governed, identity-bearing semantic substrate that a scope commits to preserve as irreducible across representational change.**

"Canonical" here does not mean *true*, *complete*, *immutable*, or *universally authoritative*. It means **designated as the architectural reference against which representation fidelity, supersession, and recovery are judged within a declared scope**.

The phrase is workable, but only if CRA explicitly rejects two seductive errors:

1. **The substance error** — treating canonical knowledge as a special kind of artifact (a file, graph, or database row).
2. **The epistemic error** — treating canonical knowledge as that which is correct, settled, or consensus-approved.

Canonical knowledge may be wrong, disputed, incomplete, or historically superseded. Its canonicality is a **preservation and identity contract**, not a truth certificate.

---

## 1. What Should "Canonical Knowledge" Mean in a Representation-Independent Architecture?

In CRA, "representation-independent" cannot mean "without representation." Knowledge is always expressed somehow. It means:

**No particular representation is authoritative for identity, meaning, or architectural primacy.**

Canonical knowledge is therefore the **preservation target** that representations are obliged to express, not any one expression of it.

Architecturally, canonical knowledge is:

1. **The semantic content a scope has designated as worth preserving** when documents, indexes, interfaces, and storage technologies are replaced.
2. **The identity-bearing subjects** that must remain the same object across those replacements.
3. **The relational structure among those subjects** that exists independently of navigation, layout, or query convenience.
4. **The epistemic and historical record** of how those subjects entered canonical status, changed, conflicted, or were superseded.

Canonical knowledge is not *what you store*. It is **what the architecture refuses to lose silently** when storage changes.

This aligns with CRA-0000's discovery that canonical knowledge endures while representations evolve—but sharpens the claim: endurance is not a magical property of content. It is the result of an explicit architectural commitment applied to a bounded scope.

---

## 2. Essential Properties

Something qualifies as canonical knowledge only if it possesses **all** of the following properties within its governing scope.

### 2.1 Governed designation

Canonicality is conferred by an accountable process: a specification, charter, editorial rule, legal instrument, repository policy, or equivalent governance act. Content does not become canonical merely by age, popularity, central storage, or frequent citation.

### 2.2 Scope-bounded authority

Every canonical item belongs to an explicitly declared scope (project, standard body, archive, jurisdiction, investigation, product line, version line, etc.). Canonical authority is **local to that scope**, not universal.

### 2.3 Stable semantic identity

The item must remain recognizably the *same architectural subject* across encoding changes, relocations, republication, and tooling replacement. Identity must not depend on filename, URL, repository layout, or presentation order.

### 2.4 Preservation obligation

The architecture treats loss or silent alteration of the item as failure—not as an acceptable optimization. This distinguishes canonical knowledge from regenerable caches, indexes, and views.

### 2.5 Irreducibility within the scope

The item cannot be fully reconstructed from other artifacts in the system **without losing distinctions the scope has committed to preserve** (identity, wording, dispute structure, supersession history, epistemic status, or relational commitments). If removal causes no committed loss, the item was not canonical.

### 2.6 Explicit epistemic framing

The architecture preserves *what kind of claim* the item constitutes: observed, asserted, required, prohibited, inferred, disputed, provisional, superseded, retracted, etc. Canonical knowledge carries its epistemic condition; it is not reduced to bare facthood.

### 2.7 Distinction integrity

The architecture preserves the distinctions the scope treats as meaningful: what is separate must not be collapsed; what is equivalent under scope rules must not be duplicated without record. This is the operational core of "semantic integrity" in CRA.

---

## 3. Commonly Associated but Non-Essential Properties

These properties are often expected of "canonical" material but must **not** define canonical knowledge:

| Associated property | Why it is non-essential |
|---------------------|-------------------------|
| **Truth** | A scope may canonically preserve incorrect, outdated, or contested claims for audit, legal, or historical reasons. |
| **Completeness** | Canonical knowledge may deliberately omit derivable detail; completeness is a scope policy, not a prerequisite. |
| **Immutability** | Supersession, amendment, and retraction are normal; what must persist is **traceability**, not frozen text. |
| **Single interpretation** | Competing readings may coexist as first-class canonical structure. |
| **Universal authority** | Canonicality is always scope-relative. |
| **Human readability** | Canonical content may be opaque to humans if the scope's commitment is to preserve exact machine-origin artifacts (hashes, instrument dumps). |
| **Central physical location** | Canonicality is not "the copy in `/canonical/`." |
| **Normative correctness** | "Canonical" in mathematics and theology implies standard or approved forms; CRA uses a third sense: **preservation reference**. |
| **Absence of derivation** | Some canonical items are authored syntheses (principles, standards, definitions). What matters is governed irreducibility, not whether a human or sensor originated every byte. |
| **Semantic normalization** | Canonical knowledge need not be stored in one unified ontology or schema. |

---

## 4. Distinctions Among Related Concepts

| Concept | Architectural role | Relation to canonical knowledge |
|---------|-------------------|----------------------------------|
| **Canonical knowledge** | Governed, identity-bearing semantic substrate a scope commits to preserve as irreducible. | **Primary preservation target** in CRA. |
| **Canonical data** | A particular serialized encoding of content (JSON, RDF, SQL rows, protobuf). | **One representation** among many; canonical only if the scope mistakenly equates format with knowledge—a known anti-pattern. |
| **Canonical documents** | Human-facing documentary forms chosen as publication or authoring vehicles. | **Representations**; may carry canonical knowledge but are not identical to it. A PDF of a standard is not the standard's canonical identity. |
| **Authoritative sources** | Agents or instruments trusted within a scope to originate or approve content. | **Provenance and governance inputs**; authority explains *why* something was designated, not *what* canonicality consists of. |
| **Semantic assertions** | Statements that something is the case, often in subject–predicate form. | **Constituents** of canonical knowledge, not synonymous with it. A graph of assertions is a derived projection unless the scope canonically commits to that graph as substrate (unusual and usually inadvisable). |
| **Derived representations** | Indexes, layouts, summaries, embeddings, APIs, UI views, navigation trees, compiled artifacts. | **Regenerable from canonical knowledge** (in principle) subject to fidelity rules; loss of a derived representation is acceptable if regeneration preserves all committed distinctions. |

**Operational rule of thumb:**

- If deleting it and rebuilding from everything else **violates a preservation commitment**, it is canonical (or contains canonical structure not captured elsewhere).
- If deleting it only costs convenience or performance, it is derived.

---

## 5. Uncertainty, Disagreement, Supersession, and Incompleteness

**Yes—canonical knowledge not only *can* contain these; in realistic systems it often *must*.**

| Condition | Architectural treatment |
|-----------|-------------------------|
| **Uncertainty** | Preserve as explicit epistemic state (confidence, interval, "unknown", "under review"), not as silent absence or default values. |
| **Disagreement** | Preserve competing canonical commitments with identity and provenance intact; do not flatten to a single winner unless the scope's governance explicitly resolves the conflict. |
| **Competing interpretations** | Preserve interpretive variants as distinct canonical subjects or as structured dispute records linked to a shared base subject. |
| **Incomplete observations** | Preserve partial records; incompleteness is information, not a trigger to infer unstated values into the canonical layer. |
| **Historically superseded claims** | Retain prior states in lineage; supersession is a **relationship**, not deletion. Future readers must see what was once canonical, what replaced it, and when. |

CRA's goal is **semantic integrity across evolution**, not **semantic cleanliness**. A pristine but dishonest archive that hides superseded or disputed states fails architecturally even if every remaining sentence is "true."

---

## 6. Truth vs. Scope-Bound Authority

Canonical knowledge is **not necessarily true**.

It is **authoritative within an explicitly defined scope** for purposes of:

- identity assignment,
- preservation priority,
- representation fidelity testing,
- supersession and amendment rules,
- and downstream derivation policy.

Truth is an external evaluation. Canonicality is an **internal architectural status**.

Example: A product standard may canonically specify a bolt torque value later found empirically unsafe. The value remains canonical *as the governing requirement within that standard's scope* until amended; it does not become non-canonical merely by being false in the physical world.

Conversely, a true statement found in a wiki footnote is **not** canonical knowledge unless the relevant scope designates it as such.

---

## 7. Fundamental Composition

Canonical knowledge is not primarily "meaning," "assertions," "relationships," "concepts," or "observations" in isolation.

It is more fundamental to treat it as **governed semantic commitments bound to stable identities**:

```text
Canonical Knowledge ≈ { (Identity, Commitment, EpistemicStatus, Provenance, Scope) }
                      + canonical relationships among identities
```

Where:

- **Identity** — what architectural subject this is, independent of representation.
- **Commitment** — what the scope holds about that subject (content at the granularity the scope requires).
- **EpistemicStatus** — observed, required, disputed, superseded, etc.
- **Provenance** — origin, steward, approval path, instrument, or derivation lineage *as committed*.
- **Scope** — where this designation is valid.

Individual categories (assertions, concepts, observations) are **views** over this substrate:

- A **concept** is an identity cluster with definitional commitments.
- An **assertion** is a commitment with propositional form.
- A **relationship** is a typed commitment linking two or more identities.
- An **observation** is a commitment whose epistemic status is tied to a method and time.

No single view is sufficient alone. A graph of assertions without identity, scope, and epistemic framing is a derived representation, not canonical knowledge.

---

## 8. Minimum Information That Must Survive Representation Removal

When all implementation-specific representations are stripped away, the following must remain recoverable for every canonical subject in scope:

1. **Identity anchor** — stable identifier and identity equivalence rules.
2. **Committed semantic content** — at the granularity defined by scope policy (not necessarily maximal).
3. **Epistemic status** — including uncertainty, dispute, and supersession markers.
4. **Temporal and version structure** — what state was canonical when; amendment lineage.
5. **Provenance of designation** — who or what process conferred canonical status and under which rule.
6. **Scope boundary** — where the commitment applies and where it does not.
7. **Canonical relationships** — typed links among identities that the scope treats as part of the preserved substrate (dependency, supersedes, contradicts, defines, requires, etc.).
8. **Integrity constraints** — invariants the scope commits to (e.g., "exact hash preserved", "both readings retained", "numeric tolerance recorded").

What may be removed without violating canonicality:

- sort order, typography, section numbering tied to one document form,
- navigation hierarchies,
- search indexes,
- cached aggregates,
- presentation markup,
- storage paths,
- interface labels,
- any material fully derivable under scope rules **without collapsing committed distinctions**.

---

## 9. Concrete Examples

1. **CRA-0000 as an architectural discovery record** — A governed artifact with stable document identity, committed historical narrative, and explicit status as permanent historical record within the CRA scope. Its canonicality lies in the designated preservation of specific architectural claims and their lineage, not in any one Markdown file encoding.

2. **Versioned engineering requirement REQ-042** — Including its current text, superseded revisions, approval provenance, and "deprecated" epistemic status. The requirement remains canonical through revision because identity persists across states.

3. **Dual canonical measurements of the same phenomenon** — Two conflicting sensor readings both designated canonical within an investigation scope, linked by a `conflicts-with` relationship and separate method provenance—not merged into a single averaged "truth."

4. **A constitutional architectural principle** — e.g., "Identity is independent of organization," stated as a governed commitment with scope "CRA," independent of whether it appears in HTML, PDF, or a future interface.

5. **Legal clause identity CL-7.3** — Exact committed text (or exact committed hash of text), amendment history, and jurisdictional scope—preserved even when published formats change.

6. **A deliberately retained obsolete specification** — Marked `superseded-by: SPEC-12`, kept canonical so contracts referencing the old identity remain interpretable.

---

## 10. Counterexamples

These often *look* canonical but are **representations, indexes, projections, or derived artifacts**:

1. **Rendered PDF of a specification** — Publication snapshot; may omit machine-readable structure, dispute records, or amendment graph present in the canonical substrate.

2. **Full-text search index** — Inverted index optimized for retrieval; loses epistemic framing, identity equivalence, and amendment lineage unless redundantly stored (which would duplicate, not replace, canonical knowledge).

3. **Knowledge graph triple store built by automated extraction** — Inference-laden projection; conflates asserted, inferred, and navigational edges unless the scope explicitly canonizes the graph (generally a category error).

4. **Website table of contents / sidebar navigation** — Derived view of relationships for UX; not the canonical relationship set (CRA-0000 §6.3).

5. **AI-generated summary of a canonical document** — Lossy compression; non-invertible; fails irreducibility if treated as source.

6. **Git repository path `docs/specs/foo.md`** — Organizational locator; identity must not depend on it (SIP/CRA identity principle).

7. **Aggregated metric** (e.g., monthly average of daily canonical readings) — Derived unless the scope explicitly canonizes the aggregate as a committed reporting artifact with its own identity and provenance.

8. **"Single source of truth" database replica** — Often confused with canonical knowledge; frequently canonical *data* (one encoding) mistaken for the semantic substrate.

---

## 11. Inverted Architecture: Representations Primary, Canonical Knowledge Derived

### Description

Invert CRA's preservation hierarchy:

1. **Primary layer:** all artifacts that exist—documents, databases, logs, graphs, models, commits, messages—stored as peers.
2. **Reconciliation layer:** algorithms continuously cluster, deduplicate, infer entities, and rank authority.
3. **Canonical layer:** emergent "canonical view" computed on demand or periodically materialized as a cache.

In this architecture, canonical knowledge is **not preserved directly**; it is **the output of a derivation pipeline** applied to representations.

### Viability

**Partially viable** for specific problem classes:

- discovery systems (search, recommendation),
- low-audit consumer content,
- ephemeral collaboration where history is expendable.

**Not viable** as a general CRA substitute when the engineering goal includes:

- long-term auditability,
- legal or standards traceability,
- reproducible derivation across decades,
- explicit supersession and dispute preservation,
- cross-tool semantic interoperability with guaranteed identity.

### Consequences

| Area | Consequence |
|------|-------------|
| **Determinism** | Canonical output depends on reconciliation heuristics, model versions, and processing order. |
| **Historical fidelity** | Past "canonical views" may be unrecoverable if derivation logic or inputs change. |
| **Provenance** | The reconciliation algorithm becomes hidden authority; failures are hard to adjudicate. |
| **Identity** | Identities are inferred, not governed; merges and splits may occur silently. |
| **Governance** | Scope boundaries blur; "what is canonical" becomes whatever the latest job emitted. |
| **CRA alignment** | Directly contradicts CRA-0000 §6.1 and §8.5: representations evolve, but nothing stable is architecturally primary. |

**Conclusion:** Representation-primary architecture is a coherent design for **mutable views**, not for **preserved knowledge under evolving representation**. CRA's inversion test strengthens the case for a designated canonical substrate—not because representations are unimportant, but because they are **replaceable carriers**, not **preservation commitments**.

---

## 12. Ambiguities and Hidden Assumptions in "Canonical Knowledge"

### 12.1 Lexical tension in "canonical"

The word imports at least three lineages:

- **Mathematical:** canonical form = chosen representative of an equivalence class (**a representation**).
- **Institutional:** canonical = officially accepted list (**authority**).
- **CRA intended:** canonical = preservation reference (**neither necessarily a form nor globally approved**).

Without explicit disambiguation, practitioners will map CRA terminology to their nearest familiar meaning—usually "master copy" or "normalized database record."

### 12.2 "Knowledge" implies justified true belief

In epistemology, knowledge carries a truth condition. CRA uses "knowledge" in an engineering sense closer to **governed informational commitment**. The word encourages epistemic overloading.

### 12.3 Hidden assumption: a single layer suffices

Many systems implicitly assume one canonical tier (the repo, the database, the PDF). CRA requires **separation of concerns**:

- canonical substrate,
- canonical relationships (may be co-located but conceptually distinct from navigation),
- derived representations.

Collapsing these produces false confidence that the "main branch" or "official PDF" *is* the knowledge.

### 12.4 Hidden assumption: preservation equals stasis

"Preserve canonical knowledge" is often read as "prevent change." Architecturally, preservation means **prevent silent loss of committed distinctions across change**.

### 12.5 Hidden assumption: canonicality is binary

In practice, scopes may designate **degrees** or **partitions** of canonicality (constitutional vs. informational vs. illustrative). Binary thinking hides necessary gradations.

### 12.6 Hidden assumption: humans are the only designators

Instrument-generated records, automated compliance baselines, and machine-enforced constraints may enter canonical status through governed pipelines without human sentence-level authorship.

---

## 13. Terminology Recommendation

**Retain** the term **Canonical Knowledge** as the umbrella concept—it already anchors CRA-0000 and the project's vocabulary—but **divide and qualify** it in normative specifications.

Recommended conceptual split:

| Term | Purpose |
|------|---------|
| **Canonical Knowledge** | Umbrella: governed semantic substrate a scope commits to preserve. |
| **Canonical Subject** | Identity-bearing unit of preservation. |
| **Canonical Commitment** | Semantic content and constraints attached to a subject. |
| **Canonical Stewardship** | Governance, provenance, scope, and amendment rules. |
| **Canonical Relationship** | Typed inter-subject link in the preserved substrate. |
| **Derived Representation** | Regenerable expression, index, or interface. |

Add a persistent qualifier in early CRA specs until vocabulary stabilizes:

> **Canonical Knowledge (preservation sense)** — distinct from canonical *form* (math) and canonical *approval* (institutional).

Do **not** replace the term with "source of truth," "master data," or "golden record." Those terms smuggle in single-copy, single-interpretation, and database-centrism incompatible with CRA's scope-bound, dispute-tolerant model.

---

## 14. Definitions, Qualification Test, and Strongest Objection

### Concise proposed definition

> **Canonical knowledge** is the scope-governed, identity-bearing semantic substrate that an architecture commits to preserve as irreducible across representational change, independent of any particular encoding, publication, or interface.

### Expanded formal definition

Within a declared scope **S**, governed by rules **G**, canonical knowledge is the minimal set of elements **K** such that each element **k ∈ K** is a tuple:

```text
k = (id, σ, ε, π, ρ, χ)
```

where:

- **id** — stable canonical identity under **G**;
- **σ** — semantic commitment content at the granularity required by **G**;
- **ε** — epistemic status (including uncertainty, dispute, supersession, retraction);
- **π** — provenance and stewardship record sufficient to audit designation under **G**;
- **ρ** — canonical relationships to other identities in **K**;
- **χ** — scope marker binding **k** to **S**.

**K** satisfies:

1. **Designation:** every **k** is canonically designated under **G**;
2. **Irreducibility:** removing **k** from the system cannot be compensated by regenerating **σ** or **ρ** from derived representations without violating a preservation rule in **G**;
3. **Identity persistence:** transformations of representation must preserve **id** equivalence;
4. **Lineage integrity:** supersession and amendment append history unless **G** explicitly permits excision (rare, and itself a governed decision).

Derived representations **R** are mappings **f: K → artifact** such that loss of **r ∈ R** does not violate **G**, provided some **f** can be recomputed preserving all distinctions **G** requires.

### Qualification test

An artifact or structure **A** qualifies as canonical knowledge **iff** all of the following hold:

1. **Governance:** **A** is designated canonical under an explicit scope and rule set **G**.
2. **Identity:** **A** has stable identity not defined by storage path, format, or UI location.
3. **Irreducibility:** Deleting **A** and attempting reconstruction from all remaining derived artifacts would lose at least one distinction **G** commits to preserve (including dispute structure, superseded states, or exact committed content).
4. **Epistemic visibility:** **A** carries or references its epistemic status in a form recoverable without external guesswork.
5. **Fidelity criterion:** For every derived representation **r** claimed to express **A**, the architecture can test whether **r** preserves all distinctions **G** requires—using **A**, not **r**, as the reference.

If **A** fails any criterion, it is a representation, index, projection, or cache—possibly labeled "official," but not canonical knowledge in the CRA sense.

### Strongest objection to this proposal

> **By defining canonical knowledge as a governed semantic substrate rather than as concrete evidence or a single authoritative document, the architecture risks infinite abstraction with no operational anchor.** Scopes, identities, epistemic markers, and stewardship rules are themselves representations. Pushing "canonicality" into abstract commitments may produce specifications that are precise on paper but impossible to implement without secretly choosing one encoding as the real canonical store—thus collapsing back into the file/database fallacy the architecture rejects. Without a mandatory minimal concrete interchange form, "preservation substrate" becomes unfalsifiable: every implementation failure can be blamed on "incorrect derivation" rather than missing canonical content.

This objection is serious. It implies that CRA normative specs must eventually define **conformance tests and fidelity mappings**, not merely philosophical boundaries—but those mechanisms belong in implementation-adjacent standards, not in the definition of canonical knowledge itself.

---

## Parent

- [Canonical Knowledge](README.md)

*End of architectural inquiry.*
