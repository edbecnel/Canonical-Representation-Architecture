# Architectural Inquiry: Canonical Knowledge

[Home](../../../../README.md) › [Project Index](../../../../PROJECT_INDEX.md) › [AI](../../README.md) › [Architectural Research](../README.md) › [Canonical Knowledge](README.md) › Architectural Inquiry: Canonical Knowledge

> **Status:** Draft
> **Owner:** CRA Architecture Team
> **Applies To:** Architectural research supporting the Canonical Representation Architecture
> **Last Reviewed:** 2026-08-05
> **Review Frequency:** On Change

*Representation-Independent Definition*

---

## 1. What should "Canonical Knowledge" mean in a representation‑independent architecture?

**Canonical Knowledge** is the *minimal, stable set of distinguishable entities and their observable properties* that are required to account for the *full historical record of evidence* relevant to a given domain, **independent of any particular encoding, organization, or interpretation**.

It is not the *truth* about the domain, but the *invariant trace* of all primary observations, measurements, and attested events that any valid representation must be able to reproduce or explain. It acts as the **conceptual zero‑point** for consistency checking, version reconciliation, and derivation tracing, without dictating how that trace is stored, queried, or presented.

---

## 2. Essential properties of Canonical Knowledge

- **Evidentiary anchoring** – Every item is directly or transitively traceable to a primary observation, measurement, or attested act (human or sensor).  
- **Identity persistence** – Each entity has a globally stable identifier that survives format changes, schema migrations, and retractions.  
- **Minimality** – No element is included that can be fully derived from other canonical elements without loss of evidential provenance.  
- **Temporal ordering** – Each item bears a precise, immutable timestamp (or interval) of when the underlying evidence was collected or attested.  
- **Provenance links** – Each item records its source, method, and any known confounders, without interpreting those links.  
- **Completeness w.r.t. evidence** – The set is closed under the requirement that no recorded observation is discarded; supersession is handled by adding new items, not deleting old ones.  

---

## 3. Commonly associated properties to exclude

- **Truth** (not essential – see Q6)  
- **Immutability** (items can be retracted by adding new evidence, but the original item remains)  
- **Consistency** (competing observations can coexist)  
- **Uniqueness** (same entity may have contradictory properties from different sources)  
- **Human‑readability** (may be a binary blob if that is the only original evidence)  
- **Normalization** (does not enforce a single data model)  
- **Authority** (authoritativeness is a derived annotation, not a prerequisite)  

---

## 4. Distinctions

| Concept | Relation to Canonical Knowledge |
|--------|--------------------------------|
| **Canonical data** | A *specific serialization* (e.g., JSON, RDF, binary) of canonical knowledge; one of many possible encodings. |
| **Canonical documents** | A *published snapshot* of canonical knowledge at a given time, often with editorial choices (order, highlighting). |
| **Authoritative sources** | *Trust‑ranked origins* of canonical items; authority is metadata, not part of the item itself. |
| **Semantic assertions** | *Interpretive claims* (e.g., “X causes Y”) derived from canonical observations; they can be false even if observations are true. |
| **Derived representations** | Any aggregation, summary, index, or visualisation that *transforms* canonical items – they are not canonical because they lose provenance or add interpretation. |

---

## 5. Can it contain uncertainty, disagreement, incomplete observations, etc.?

**Yes, necessarily.**  
Canonical knowledge is a *record of what was observed*, not a *filtered consensus*.  
- Uncertainty is stored as a measured precision or confidence interval attached to the observation.  
- Disagreement is stored as two separate observations from different sources/methods.  
- Incomplete observations are stored as partial records (missing fields are absent, not filled with defaults).  
- Superseded claims are retained and linked to their successors via “replaces” relationships, so that historical derivations remain reproducible.

---

## 6. Is it necessarily true or authoritative within a scope?

**Neither.** It is *factual about the evidence*, not about the domain.  
An observation of “pressure = 101 kPa” is canonical if the sensor recorded it; it may be inaccurate. Authoritativeness is a *second‑order attribute* assigned by a governance process, not intrinsic to the knowledge itself. Scope is defined by the *boundary of evidence ingestion* (e.g., “all temperature readings from station X between 2000–2020”).

---

## 7. Fundamental composition

Canonical knowledge consists of **attested records** – elementary tuples:  
`(entity_id, property, value, time, method, source, confidence, context_id)`  

This is more fundamental than “meaning” (which is interpretive), “assertions” (which are relational), or “concepts” (which are classifications). The core is *observed state* of an identifiable subject at a known moment, with known method.

---

## 8. Minimum information that must survive

- **Unique entity identifiers** (universal, not context‑dependent)  
- **Property names** (what was measured/attested)  
- **Values** (with their native units/type)  
- **Temporal anchors** (time of observation)  
- **Method identifiers** (how the value was obtained)  
- **Source identifiers** (who/which device produced it)  
- **Context identifiers** (experiment, deployment, project)  
- **Retraction/supersession links** (if any)  

All ordering, grouping, hierarchies, and formatting are removable.

---

## 9. Concrete examples

1. **CO₂ concentration** = 421 ppm at Mauna Loa, 2026‑08‑05 12:00 UTC, instrument S/N 42, calibration date 2026‑01‑01.  
2. **Patient X** temperature = 38.2°C, 2026‑08‑05 07:23, ear thermometer model T2, nurse ID 107.  
3. **Star Y** radial velocity = +12.4 km/s, 2026‑08‑04 23:11, spectrograph SP‑1, reduction pipeline v3.  
4. **Contract C** clause 7 text hash = SHA256:…, signed by party A on 2025‑01‑15, notary N.  
5. **Satellite S** position (x,y,z) = (…), GPS timestamp, receiver R, fix type “DGPS”.

---

## 10. Counterexamples (representation‑derived)

1. **Search index** – an inverted file that loses time and provenance.  
2. **Knowledge graph triple** (“X locatedIn Y”) – an interpretation that may conflate observation with inference.  
3. **PDF document** – a formatted snapshot that omits measurement errors and raw timestamps.  
4. **Average temperature** – a derived aggregate that discards individual sensor readings.  
5. **API JSON response** – a projection that orders fields and may default missing values.  
6. **AI embedding** – a numerical vector that is non‑invertible and untraceable.  
7. **Ontology class** – a classification that imposes a worldview (e.g., “mammal”) not present in raw data.

---

## 11. Inverted architecture: representations as primary

**Design**: Every representation (document, graph, index, model) is stored as the source of truth. Canonical knowledge is *continuously derived* by running reconciliation algorithms that extract common entities, resolve identities, and detect contradictions, producing a “canonical view” on‑the‑fly.

**Viability**: **Partially viable** – it works for near‑real‑time systems with low consistency requirements (e.g., search engines).  
**Consequences**:  
- Canonical knowledge becomes *non‑deterministic* (depends on reconciliation order and heuristics).  
- Historical reproducibility fails because derived canonical items are not persistent.  
- Provenance is weakened because the derivation logic is not captured in the canonical record itself.  
- This architecture privileges *current use* over *evidential fidelity* – acceptable for discovery, unacceptable for audit/forensics.

---

## 12. Ambiguities and hidden assumptions

- **“Canonical”** implies *normative* or *standard* in many fields – we must explicitly decouple from that.  
- **“Knowledge”** suggests *justified true belief* – we substitute *recorded evidence*.  
- Assumes a clear boundary of what constitutes an “observation” (e.g., is a textual statement “the sky is blue” an observation or an interpretation?).  
- Assumes stable entity identity across time – in practice, identity resolution is itself an interpretation.  
- Implicitly privileges *temporal* ordering over *causal* or *logical* ordering.

---

## 13. Recommendation

**Replace** “Canonical Knowledge” with **“Evidential Core”** or **“Primary Observation Record”** to avoid normative baggage.  
If retention is mandatory, **refine** it with a permanent qualifier: *“Canonical Knowledge (Evidential)”* to signal its limited scope.  

Divide into two concepts:  
- **Canonical Evidence** – raw attested observations.  
- **Canonical Interpretation** – agreed‑upon derived facts (scope‑bound, versioned) – which is what most people mean by “canonical” and should be treated as a separate architectural layer.

---

## 14. Final definitions and test

**Concise definition**  
> Canonical knowledge is the immutable, minimal set of timestamped, source‑attributed observations that constitute the primary evidence for a domain, independent of any representation or interpretation.

**Expanded formal definition**  
> A set *C* of tuples (*e, p, v, t, m, s, c, r*) where:  
> - *e* = globally unique entity identifier,  
> - *p* = property name from a stable vocabulary (not necessarily formal),  
> - *v* = value (primitive or hash for large binaries),  
> - *t* = observation time (or interval),  
> - *m* = method identifier (instrument, protocol, human),  
> - *s* = source identifier,  
> - *c* = context identifier (project, experiment),  
> - *r* = set of identifiers of tuples that this one replaces/retracts (optional).  
> *C* is closed under the rule that no tuple may be deleted; additions may link to prior tuples.

**Qualification test**  
An artifact *A* is canonical knowledge iff:  
1. Every element in *A* is traceable to an original observation without data‑loss (i.e., all units, confidences, and timestamps are preserved).  
2. Removing *A* and regenerating it from all other artifacts in the system would lose at least one observation or provenance fact.  
3. *A* does not contain any field that is a function (average, max, classification, link) of other elements in *A* unless that function is explicitly recorded as a separate observation with its own timestamp and method.

**Strongest objection to this proposal**  
> By excluding all interpretation and synthesis, “canonical knowledge” becomes a pile of raw sensor readings and textual attestations that is practically unusable for decision‑making. It pushes all semantic enrichment into derived layers, but without a shared interpretation framework, those layers will diverge, and the “canonical” core will be ignored in practice. The architecture risks producing a pristine but inert archive that no one queries directly, thereby defeating its purpose as a reference point.

---

## Parent

- [Canonical Knowledge](README.md)

*End of architectural inquiry.*