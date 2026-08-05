# Architectural Inquiry: Canonical Knowledge

[Home](../../../../README.md) › [Project Index](../../../../PROJECT_INDEX.md) › [AI](../../README.md) › [Architectural Research](../README.md) › [Canonical Knowledge](README.md) › Architectural Inquiry: Canonical Knowledge

> **Status:** Draft
> **Owner:** CRA Architecture Team
> **Applies To:** Architectural research supporting the Canonical Representation Architecture
> **Last Reviewed:** 2026-08-05
> **Review Frequency:** On Change

## Executive Position

The phrase **Canonical Knowledge** should not denote a special kind of document, record, assertion, graph, or data structure. It should denote an **architectural role assigned to preserved meaning within a defined governance scope**.

Canonicality is not an intrinsic property of knowledge. It is a status conferred by an architecture that declares:

1. which meaning must be preserved,
2. which identity that meaning possesses,
3. within what scope it is controlling,
4. how its provenance and epistemic condition are recorded,
5. and which representations may be regenerated, replaced, or discarded without changing it.

The central distinction is therefore not between "canonical files" and "non-canonical files." It is between:

- **knowledge-bearing content that the architecture commits to preserve**, and
- **representations through which that content is expressed, used, navigated, published, indexed, or inferred**.

A practical complication must be acknowledged immediately: knowledge cannot be stored or communicated without some representation. "Representation-independent" therefore cannot mean "existing without representation." It must mean that **no particular representation defines the identity or architectural primacy of the knowledge**.

---

# 1. Meaning of Canonical Knowledge

In a representation-independent architecture, **Canonical Knowledge** should mean:

> A governed, identity-bearing body of meaning that an identified authority has designated as the preserved semantic basis from which representations may be produced, evaluated, or reconstructed within an explicitly defined scope.

Several parts of this definition are deliberate.

### Governed

Canonicality must arise through an accountable rule, authority, or process. Something is not canonical merely because it exists, is widely copied, appears official, or is stored in a particular repository.

### Identity-bearing

The knowledge must remain recognizable as the same architectural subject across changes in wording, serialization, file location, publication form, interface, and technology.

### Body of meaning

Canonical knowledge may include observations, assertions, definitions, relationships, competing interpretations, decisions, constraints, uncertainty, and historical states. It is not limited to individual propositions.

### Designated

Canonicality is conferred. It is not discovered merely by examining content.

### Preserved semantic basis

The architecture commits to retaining the distinctions necessary to preserve the knowledge's meaning and status.

### Within an explicitly defined scope

Canonicality is never absolute by default. It applies within some bounded jurisdiction, such as:

- a repository,
- a project,
- an organization,
- a standard,
- a legal regime,
- a scientific investigation,
- a historical archive,
- a version,
- a time interval,
- or a declared subject domain.

### Representations may be produced, evaluated, or reconstructed

Canonical knowledge acts as the basis against which representations are considered faithful, incomplete, transformed, obsolete, or derived.

---

# 2. Essential Properties

Something qualifies as canonical knowledge only when it possesses the following properties.

## 2.1 Stable identity

It must have an identity that survives representational change.

This does not require a particular identifier format. It requires that the architecture can determine whether two manifestations refer to:

- the same knowledge,
- different versions of the same knowledge,
- different knowledge,
- or a derivation from existing knowledge.

Without identity, preservation becomes indistinguishable from copying text.

## 2.2 Preserved semantic content

There must be identifiable meaning that the architecture intends to preserve.

The exact wording, layout, serialization, encoding, and storage location may change, but the architecture must be capable of determining whether an alteration changes the knowledge itself.

## 2.3 Explicit scope

The domain within which the knowledge is canonical must be stated or determinable.

A claim may be canonical for:

- one project but not another,
- one historical period but not the present,
- one jurisdiction but not another,
- one model version but not later versions,
- one interpretive school but not all schools.

A declaration of canonicality without scope is structurally ambiguous.

## 2.4 Provenance

The architecture must preserve enough information to explain where the knowledge came from or how it entered canonical status.

Provenance may identify:

- an observer,
- an author,
- a governing body,
- a source system,
- an experiment,
- a decision process,
- an imported standard,
- or an earlier knowledge object.

Provenance does not guarantee truth. It establishes origin and accountability.

## 2.5 Epistemic or normative status

The architecture must preserve what kind of commitment is being recorded.

Examples include:

- observed,
- reported,
- inferred,
- hypothesized,
- disputed,
- accepted,
- approved,
- required,
- prohibited,
- superseded,
- retracted,
- historically believed,
- or unknown.

Without status, a hypothesis may be mistaken for a fact, a historical claim for a current claim, or a recommendation for a requirement.

## 2.6 Context sufficient to preserve meaning

The meaning must remain interpretable outside any accidental characteristics of its current representation.

Necessary context may include:

- applicable conditions,
- units,
- definitions,
- temporal bounds,
- jurisdiction,
- reference frame,
- interpretive assumptions,
- dependencies,
- or the meaning of related concepts.

Context is not optional metadata when its removal changes meaning.

## 2.7 Governed change

The architecture must distinguish between:

- correction,
- clarification,
- extension,
- replacement,
- supersession,
- retraction,
- reinterpretation,
- and representational re-expression.

A canonical knowledge object need not be immutable, but its evolution must be accountable.

## 2.8 Representation substitutability

No particular document, file, table, graph, database schema, or serialization may be essential merely because it currently carries the knowledge.

A representation may be indispensable operationally at a particular moment, but the knowledge remains architecturally distinct from it.

## 2.9 Preservation intent

The architecture must explicitly treat the meaning as something that should survive representational replacement.

Many meaningful things exist temporarily in applications, conversations, reports, and indexes. They do not become canonical knowledge unless the architecture commits to their preservation as part of its knowledge base.

---

# 3. Non-Essential Properties Commonly Confused with Canonicality

The following properties may be desirable, but they should not be part of the essential definition.

## 3.1 Truth

Canonical knowledge may contain errors, contested interpretations, outdated theories, incorrect measurements, or deliberate records of false claims.

Truth and canonicality are separate dimensions.

## 3.2 Completeness

A canonical record may be intentionally incomplete. It may preserve only what is currently known.

Requiring completeness would make canonicality impossible in any evolving domain.

## 3.3 Immutability

Canonical knowledge may evolve. What matters is controlled change and preserved lineage, not permanent stasis.

## 3.4 Universal authority

Canonical status is normally scoped. A project's canonical terminology need not bind another project.

## 3.5 Consensus

Canonical knowledge may preserve disagreement rather than eliminate it.

## 3.6 Formal semantics

Formal logic, ontologies, schemas, and machine-readable semantics may strengthen precision but are not prerequisites.

## 3.7 Machine readability

Human-maintained canonical knowledge is possible, although machine verification may be desirable.

## 3.8 Human readability

Some canonical knowledge may only be directly intelligible through specialized tools. Human readability is a design value, not an ontological requirement.

## 3.9 Atomicity

Canonical knowledge need not consist only of indivisible assertions. Some meanings exist only as structured wholes.

## 3.10 Storage in one place

Canonical knowledge may be distributed, replicated, federated, or partitioned.

## 3.11 One current version

Multiple versions may remain canonical within different temporal scopes.

## 3.12 Absence of contradiction

Contradictions may themselves be canonical knowledge when the disagreement is real and preservation-worthy.

## 3.13 Official publication

Publication is a representation and distribution act. It does not itself create canonicality.

## 3.14 Technical normalization

Canonical serialization, canonical ordering, and normalized data structures may reduce ambiguity, but they concern representations rather than knowledge itself.

---

# 4. Distinction from Adjacent Concepts

## 4.1 Canonical knowledge

Canonical knowledge is the governed semantic commitment the architecture intends to preserve.

It answers:

> What meaning, distinctions, context, and status must survive?

## 4.2 Canonical data

Canonical data is a designated data model or normalized data form used as the controlling interchange or storage representation.

It answers:

> Which data structure should systems treat as the standard form?

Canonical data is still a representation. It may carry canonical knowledge faithfully, partially, or incorrectly.

## 4.3 Canonical documents

A canonical document is a document designated as the controlling documentary expression for some purpose.

It answers:

> Which document governs when documentary versions conflict?

A canonical document is still a representation.

## 4.4 Authoritative sources

An authoritative source is an origin that has recognized standing to originate, attest, determine, or govern information within some scope.

Authority concerns **where knowledge comes from**, not **what is canonical**.

## 4.5 Semantic assertions

A semantic assertion is an expressed proposition.

Canonical knowledge may contain semantic assertions, but also definitions, observations, decisions, evidence, uncertainty, disagreements, and relationships among them.

## 4.6 Derived representations

Derived representations include:

- websites,
- books,
- search indexes,
- navigation trees,
- knowledge graphs,
- AI summaries,
- APIs,
- visualizations,
- reports,
- publications,
- embeddings,
- diagrams,
- and translated forms.

They are products derived from canonical knowledge, not canonical knowledge itself.

---

# 5. Can Canonical Knowledge Contain Uncertainty?

Yes.

Canonical knowledge may preserve:

- uncertainty,
- disagreement,
- competing interpretations,
- incomplete observations,
- superseded claims,
- rejected hypotheses,
- historical beliefs,
- conflicting evidence.

The architecture should preserve **what is known**, **what is believed**, **what is disputed**, and **how each is classified**.

---

# 6. Is Canonical Knowledge Necessarily True?

No.

Truth and canonicality are orthogonal.

Canonical knowledge is authoritative **within a declared scope** because the architecture has committed to preserving it—not because reality guarantees it is true.

---

# 7. What Does Canonical Knowledge Primarily Consist Of?

It should not be reduced to:

- meaning,
- assertions,
- relationships,
- concepts,
- observations,
- or facts.

Instead it consists of **preserved semantic commitments**.

Those commitments may take many forms while sharing the same architectural properties.

---

# 8. Minimum Information That Must Survive

If every implementation-specific representation disappears, the following must remain recoverable:

- identity,
- preserved meaning,
- scope,
- provenance,
- epistemic or normative status,
- temporal applicability,
- required context,
- meaning-bearing relationships.

Everything else is replaceable.

---

# 9. Examples of Canonical Knowledge

1. A normative architectural principle.
2. A scientific observation together with uncertainty.
3. A project decision and its rationale.
4. A disputed historical interpretation with both competing viewpoints preserved.
5. A terminology definition within a specification.
6. A legal rule together with its effective dates.
7. A known absence of evidence.
8. A requirement that governs a system.

---

# 10. Counterexamples

The following are **not** canonical knowledge:

1. A PDF designated "Master Copy."
2. A database.
3. A knowledge graph.
4. A search index.
5. A website.
6. An AI-generated summary.
7. An RDF or OWL serialization.
8. A normalized API payload.
9. A table of contents.
10. A dashboard.

All are representations or projections.

---

# 11. Inverted Architecture

An alternative architecture could make documents or representations primary.

In that architecture:

- documents become the preserved objects,
- meaning is reconstructed from documents,
- canonical knowledge becomes an inferred abstraction.

Such architectures are common in archives and records management.

Advantages:

- preserves original evidence,
- preserves original expression,
- avoids premature semantic interpretation.

Disadvantages:

- meaning must continually be reconstructed,
- semantic consistency is difficult,
- technology formats become preservation concerns,
- AI extraction becomes unavoidable.

Both architectures are viable.

They optimize for different preservation goals.

---

# 12. Hidden Assumptions

The phrase "Canonical Knowledge" hides numerous assumptions:

- that knowledge is true,
- that canonical means unique,
- that canonical means immutable,
- that authority is universal,
- that knowledge exists independently of representation,
- that all knowledge can be formalized,
- that there is only one valid interpretation,
- that preserving knowledge implies endorsing it.

None should be assumed.

---

# 13. Recommendation

Retain the term **Canonical Knowledge**, but define supporting concepts separately.

Recommended supporting concepts:

- Canonical Knowledge
- Canonical Knowledge Object
- Canonical Knowledge State
- Canonical Knowledge Commitment
- Authoritative Source
- Evidence Artifact
- Canonical Representation
- Derived Representation

This provides architectural precision while preserving intuitive terminology.

---

# 14. Final Definition

## Concise Definition

> Canonical Knowledge is the governed, scope-bounded meaning that an architecture commits to preserve independently of any particular representation.

## Expanded Definition

> Canonical Knowledge is the set of identity-bearing semantic commitments that a designated authority has admitted into a defined architectural scope for preservation and governance, together with the context, provenance, epistemic or normative status, temporal applicability, and meaning-bearing relationships necessary to preserve their meaning across changes in documents, formats, storage systems, publications, interfaces, and other representations. Canonical status establishes preservation authority within its declared scope; it does not imply truth, completeness, immutability, consensus, or universal authority.

## Qualification Test

A candidate qualifies as canonical knowledge only if all are true:

1. It possesses stable identity.
2. It preserves identifiable meaning.
3. Its scope is defined.
4. Canonical authority is identified.
5. Provenance is preserved.
6. Epistemic or normative status is preserved.
7. Necessary interpretive context survives.
8. Evolution is governed without losing identity.
9. Representations can change without changing the knowledge.
10. The architecture explicitly commits to preserving it.

If not, it is likely a representation, publication, index, or derived artifact.

## Strongest Objection

The strongest objection is that meaning cannot be fully separated from representation.

Language, notation, typography, ordering, structure, and medium frequently contribute to meaning.

Accordingly, representation-independent should not mean **representation-free**.

It should mean:

> **No single representation possesses architectural primacy over the knowledge it conveys.**

For this reason, a mature architecture should preserve both:

- canonical knowledge, and
- primary evidence artifacts,

allowing future interpretations while maintaining long-term semantic continuity.

## Parent

- [Canonical Knowledge](README.md)