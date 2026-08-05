# Architectural Inquiry: Canonical Knowledge

[Home](../../../../README.md) › [Project Index](../../../../PROJECT_INDEX.md) › [AI](../../README.md) › [Architectural Research](../README.md) › [Canonical Knowledge](README.md) › Architectural Inquiry: Canonical Knowledge

> **Status:** Draft
> **Owner:** CRA Architecture Team
> **Applies To:** Architectural research supporting the Canonical Representation Architecture
> **Last Reviewed:** 2026-08-05
> **Review Frequency:** On Change

**Independent Review for Canonical Representation Architecture (CRA)**
**Model:** GitHub Copilot (Claude Sonnet 5)
**Date:** 2026-08-05

# Canonical Knowledge: An Architectural Definition

## 1. What "Canonical Knowledge" Should Mean

In a representation-independent architecture, **canonical knowledge is the smallest set of claims about the world that all valid representations of a given subject must agree with, and from which those representations can be regenerated or validated, but to which no representation is reducible.**

It is not a format, a store, or a document. It is a *constraint structure* — a reference against which representations are checked for fidelity, and from which new representations can be legitimately derived. Canonicity is a relationship between an artifact and the space of things it could have been expressed as, not a property of the artifact itself.

The key architectural move: canonical knowledge is defined by its **invariance under representation change**, not by its format, authority, or medium.

## 2. Required Properties

Something qualifies as canonical knowledge only if it has:

- **Representation-independence** — it survives translation across formats, languages, media, and systems without loss of identity.
- **Referential stability** — it can be pointed to, cited, or invoked consistently over time, even as its expression changes.
- **Generative sufficiency** — other valid representations can be derived from it (a document, a graph node, a search result), even if none currently exist.
- **Scope-boundedness** — it declares (explicitly or by convention) the domain and conditions under which it holds. Canonicity without scope is meaningless.
- **Discernibility from its expressions** — there must be a real difference between "the knowledge" and "a rendering of the knowledge." If no such difference can be articulated, what you have is a document, not knowledge.

## 3. Properties Commonly but Wrongly Associated

- **Truth** — canonical ≠ true. It can be canonically wrong (a superseded scientific model can be canonical *within its historical scope*).
- **Immutability** — canonical knowledge can be versioned, corrected, or amended. What must be stable is *identity and traceability*, not content.
- **Singularity** — there can be multiple canonical knowledge items that disagree, if their scopes differ or are explicitly framed as competing.
- **Completeness** — canonical knowledge can be a fragment. A single verified fact is canonical without being a whole account.
- **Institutional authority** — authority is a social/organizational property; canonicity is a structural one. A source can be authoritative without being canonical (e.g., "the best current estimate") and canonical without being singularly authoritative (e.g., a formally agreed-upon working definition that everyone knows is provisional).
- **Formality** — canonical knowledge need not be expressed in formal logic, RDF triples, or structured schema. Formality is an implementation choice.

## 4. Distinguishing Adjacent Concepts

| Concept | What it actually is |
|---|---|
| **Canonical knowledge** | The stable referent that representations are validated against |
| **Canonical data** | A canonical *value* within a data model (e.g., "the canonical spelling is X") — narrower, syntactic, system-scoped |
| **Canonical documents** | A privileged *artifact* chosen as the reference instance among duplicates — an editorial/version-control concept, not an epistemic one |
| **Authoritative sources** | An origin trusted by convention or institutional mandate — a *social* property, orthogonal to canonicity |
| **Semantic assertions** | Structured claims (usually machine-readable) that *encode* knowledge in one particular formalism — a representation, not the knowledge itself |
| **Derived representations** | Anything generated from canonical knowledge for a purpose — documents, UIs, indexes, embeddings, summaries |

The common error is collapsing these into one axis ("more formal = more canonical"). They are actually independent axes: stability, privilege-among-duplicates, social trust, formal encoding, and purpose-built projection are four different things.

## 5. Can Canonical Knowledge Contain Uncertainty, Disagreement, Incompleteness?

Yes — and this is where most naive definitions collapse.

- **Uncertainty**: A canonical claim can be "the measured value is 6.674×10⁻¹¹ ± 0.001×10⁻¹¹." The uncertainty is *part of* the canonical content, not a defect in it.
- **Disagreement**: Two competing interpretations can both be canonical if the architecture treats "unresolved scientific dispute" as itself the canonical state. The canonical knowledge is not "answer A" or "answer B" — it is "the dispute exists, with these positions, as of this scope."
- **Incomplete observations**: A partial dataset can be canonical *as a partial dataset* — canonicity doesn't require the observation to be finished, only that its boundaries and status are stable and declared.
- **Historically superseded claims**: These remain canonical *within their historical scope*. "Ptolemaic astronomy held that..." is permanently canonical as a historical claim, even though it is false as a claim about planetary motion. Superseding a claim doesn't destroy its canonicity — it adds a new canonical claim about supersession.

The unifying principle: canonicity attaches to **the claim together with its scope and status**, not to a bare proposition stripped of context.

## 6. Is Canonical Knowledge True, or Authoritative Within Scope?

Neither, strictly. It is **stable and scoped**, and truth/authority are separable properties that may or may not attach to it.

- Truth is a semantic property (does it correspond to reality).
- Authority is a social property (is it institutionally sanctioned).
- Canonicity is a structural property (is it the stable reference point representations converge on).

A definition that requires truth cannot handle superseded science. A definition that requires authority cannot handle emergent consensus (e.g., community-agreed terminology with no governing body) or intentionally multi-perspectival canonical records (e.g., "three eyewitness accounts, none reconciled, all canonical"). So: canonical knowledge is **authoritative only in the narrow sense that it is the agreed point of reference within its declared scope** — not authoritative in the sense of being correct or officially sanctioned.

## 7. What Does Canonical Knowledge Consist Of?

None of the listed options alone. It consists of something more fundamental: **a stabilized relationship between an identified subject, a claim about that subject, and the conditions (scope, time, uncertainty, provenance) under which the claim holds.**

Call this a **knowledge unit**: `⟨subject, claim, scope, status⟩`.

- Meaning is what the unit *is about*.
- Assertions are one way to *express* the unit.
- Relationships are structural features *within or between* units.
- Concepts are *subjects* the unit refers to.
- Recorded observations are *evidence* that may ground a unit.

Canonical knowledge is the unit itself — the thing that meaning, assertion, relationship, concept, and observation are all facets of, but none of which alone constitutes it.

## 8. Minimum Information That Must Survive Representation Removal

Strip away format, medium, language, structure, and encoding. What must remain for something to still be "the same canonical knowledge"?

1. **Identity** — a way to recognize this unit as the same one across representations (a durable reference, not necessarily a literal ID).
2. **The claim's content** — the proposition itself, independent of phrasing.
3. **Scope** — the domain/conditions under which the claim is asserted to hold.
4. **Status** — its epistemic state (settled, disputed, superseded, provisional, uncertain-with-bounds).
5. **Provenance linkage** — enough traceability to know where the claim came from, even if the specific citation format is discarded.

If any of these five is lost, what survives is no longer canonical knowledge — it's a decontextualized fact, indistinguishable from folklore.

## 9. Five Concrete Examples of Canonical Knowledge

1. The defined value of the speed of light in vacuum (299,792,458 m/s) — a fixed, scoped, stable reference, independent of which textbook, unit system, or language expresses it.
2. The fact, with its uncertainty and evidentiary status, that a named historical treaty was signed by specific parties on a specific date — independent of any single archive's transcription.
3. The current formally agreed taxonomic classification of a species, understood as provisional and revisable — the classification-as-claim, not the encyclopedia article about it.
4. A patient's confirmed diagnosis and its clinical basis, as a stable clinical fact — independent of which EHR system, form, or chart note expresses it.
5. The outcome and vote count of a specific certified election — the result-as-fact, independent of any news article, database row, or press release reporting it.

## 10. Five Counterexamples (Things That *Look* Canonical But Aren't)

1. **A Wikipedia article** — a derived, editable representation *about* canonical facts; it is a projection, not the knowledge.
2. **A "golden record" database row** — canonical *data* (a system-level deduplication artifact), not canonical knowledge; it resolves format conflicts, not epistemic ones.
3. **A knowledge graph triple** `(Paris, capitalOf, France)` — a semantic assertion in one formalism; the same knowledge survives even if RDF disappears tomorrow.
4. **A published PDF marked "official version"** — a canonical *document* by editorial convention (privileged among duplicates), not canonical knowledge itself.
5. **A search engine's top result / a citation index entry** — a derived ranking or index artifact reflecting relevance or popularity, not stability of claim.
6. *(bonus)* **An AI-generated summary of a topic**, however fluent or widely reused — an inference/derivation, however useful, not a stable reference point others should validate against.

## 11. Inverting the Definition: Representations as Primary

Consider an architecture where there is no canonical layer at all — only a network of representations that mutually constrain and correct each other (a "consensus mesh"). Canonical knowledge, in this inversion, is not stored anywhere; it is **an emergent equilibrium** computed on demand from the current state of all representations (e.g., a weighted convergence across sources, recalculated continuously, à la distributed version-control or Wikipedia's own revision-consensus model, or a blockchain-style ledger where "truth" is whatever the majority of nodes currently agree on).

**Is this viable?** Partially, and it's not actually a rejection of the original definition — it's a different *implementation strategy* for it. The five invariants (identity, content, scope, status, provenance) still have to exist *somewhere* — they just live in the aggregation algorithm and its history rather than in a designated record. So the inversion collapses back into the same requirement, relocated.

**Consequences of pursuing it anyway:**
- Canonicity becomes a moving target — recomputed rather than referenced, breaking stable citation (a serious problem for scientific, legal, and archival use).
- It requires the aggregation function itself to be canonical (its rules, weights, and thresholds) — an infinite regress unless *something* is fixed.
- It trades "who decides what's canonical" for "who controls the aggregation algorithm" — the governance problem doesn't disappear, it relocates and becomes less visible/auditable.
- It's genuinely useful for domains where consensus itself *is* the phenomenon of interest (e.g., tracking evolving scientific consensus, community-defined terminology) — there the *emergence* is the canonical thing, and the mesh's convergence history becomes the actual invariant.

So: viable as a *specialized* architecture for consensus-tracking domains, but not as a general replacement — it still needs a fixed point, it just moves where that fixed point sits.

## 12. Hidden Assumptions in the Phrase Itself

- **"Canonical" imports a religious/textual-criticism metaphor** (canon = the accepted books) — smuggling in connotations of institutional gatekeeping and closed lists that don't belong in a general architecture.
- **It implies singularity** ("the" canonical version), when multiplicity-with-declared-scope is often the correct model.
- **It conflates process and product** — "canonical" describes both an act of designation (a governance process) and an assumed intrinsic property of the resulting artifact, and people slide between the two without noticing.
- **It presumes a stable "knowledge" substrate exists prior to any representation**, which is philosophically contestable — some would argue knowledge is only ever accessible *through* representation, making "representation-independent knowledge" an idealization rather than an achievable engineering target. (This is directly relevant to §11.)
- **It implicitly assumes a reader/system that needs deduplication** — the entire concept is motivated by the practical problem of multiple competing representations; in a world with only one representation, "canonical" would be a vacuous term.

## 13. Retain, Refine, Replace, or Divide?

**Divide.** The single term "canonical knowledge" is being asked to do at least three jobs that should be architecturally separate:

1. **Knowledge identity** — the stable `⟨subject, claim, scope, status⟩` unit (§7–8). Keep this as the core concept — this is what deserves the name.
2. **Canonical designation** — the governance act of privileging one representation/document as the reference instance among duplicates. This should be called something like **"reference instance"** or **"designated representation,"** not knowledge.
3. **Authoritative provenance** — the social/institutional trust attached to a source. This should remain a separate metadata property (**"authority"** or **"trust level"**), attachable to any representation, orthogonal to canonicity.

Recommendation: retain **"canonical knowledge"** narrowly for (1), and introduce **"canonical representation"** or **"reference document"** for (2), keeping "authoritative" strictly for (3). This prevents the architecture from silently treating "the officially blessed PDF" as if it were epistemically equivalent to "the stable fact."

## 14. Final Deliverables

**Concise definition:**
> Canonical knowledge is the stable, scoped claim — independent of any particular format or document — that all valid representations of a subject must be traceable to and consistent with.

**Expanded formal definition:**
> Canonical knowledge is a unit `⟨subject, claim, scope, status, provenance⟩` such that: (a) its identity persists across arbitrary changes in format, medium, or encoding; (b) it declares the domain and conditions under which the claim is asserted to hold; (c) it declares its own epistemic status, including uncertainty, disagreement, or supersession, as intrinsic content rather than external metadata; (d) it is sufficient to generate or validate at least one representation, without being reducible to any single one; and (e) its truth-value and institutional authority are independent, separately-tracked properties, not preconditions of its canonicity.

**Qualification test** (an artifact X is canonical knowledge if and only if):
1. **Survival test** — Can X's identity and content be re-expressed in a wholly different format/medium without becoming "a different thing"? (If not: it's a document/data artifact.)
2. **Scope test** — Does X declare, explicitly or by clear convention, the conditions under which it holds? (If not: it's an unscoped assertion, not yet knowledge.)
3. **Generativity test** — Could a new, previously nonexistent representation be legitimately derived from X and checked against it? (If not: X is itself a derived representation of something else.)
4. **Non-reducibility test** — Is there at least one other valid representation of the same content that differs from X in form? (If X and "the knowledge" are the same object with no daylight between them, X is likely a canonical *document*, not canonical *knowledge*.)
5. **Status-bearing test** — Does X carry its own epistemic status (certain/uncertain/disputed/superseded) rather than presenting as flatly asserted fact? (Optional but strongly diagnostic — its absence often signals a representation masquerading as knowledge.)

An artifact passing 1–4 qualifies; failing any one demotes it to a representation, index, projection, or designation.

**Strongest objection to this proposal:**
> The claim that a scope- and status-bearing unit can exist "independent of any particular format" may be a category error: every attempt to state, store, compare, or transmit a knowledge unit *is itself* a representation (even `⟨subject, claim, scope, status, provenance⟩` is a schema — a representation choice). If there is no format-free way to even *express* the definition of canonical knowledge, then "representation-independence" is not an achievable property but a regulative ideal — useful for architecture (as a discipline: "treat representations as fungible, validate against a reference model") but not a literal ontological claim. Under this objection, the proposal should be understood as **"the representation that behaves as if it were representation-independent, by design constraint,"** rather than as knowledge that genuinely exists outside representation — a weaker but more defensible claim.