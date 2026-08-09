[Home](../../../../README.md) › [Project Index](../../../../PROJECT_INDEX.md) › [AI](../../README.md) › [Architectural Research](../README.md) › [Canonical Knowledge](README.md) › Comparative Analysis

> **Status:** Maintained
> **Document Class:** Architectural Research
> **Owner:** CRA Architecture Team
> **Applies To:** Architectural research supporting the Canonical Representation Architecture
> **Last Reviewed:** 2026-08-09
> **Review Frequency:** On Change

# Comparative Analysis — Canonical Knowledge

## Purpose

This document compares seven independent AI architectural reviews collected in response to [Prompt.md](Prompt.md). It identifies convergence, divergence, and implications for the Canonical Representation Architecture (CRA).

This analysis is **informative, not normative**. It does not adopt a definition. Normative principles belong in CRA-0001.

## CRA Context for This Analysis

CRA exists to address a recurring engineering failure: systems treat a particular encoding as the thing worth preserving, then lose meaning, identity, or history when representations change ([CRA-0000](../../../../CRA-0000.md), sections 2 and 6).

The research question was therefore evaluated against CRA's architectural purpose:

- preserve knowledge across evolving representations, formats, and technologies;
- maintain stable identity independent of physical organization;
- support derivation of multiple representations from a common source;
- govern what is authoritative within a scope without equating authority with truth.

Definitions that do not serve these objectives were noted but not selected here.

## Sources Compared

| Review | Model | Context |
|---|---|---|
| [ChatGPT_GPT-5.5.md](ChatGPT_GPT-5.5.md) | GPT-5.5 | Independent |
| [Gemini.md](Gemini.md) | Gemini | Independent |
| [Claude_Sonnet_Web.md](Claude_Sonnet_Web.md) | Claude Sonnet 5 | Independent |
| [Claude_Sonnet_GitHub_Copilot.md](Claude_Sonnet_GitHub_Copilot.md) | Claude Sonnet 4.6 | Repository context |
| [Grok.md](Grok.md) | Grok | Independent |
| [DeepSeek_R1.md](DeepSeek_R1.md) | DeepSeek R1 | Independent |
| [Composer_2.5.md](Composer_2.5.md) | Composer 2.5 | Independent |

## Convergence

All seven reviews independently supported the following architectural themes. Each theme aligns with observations already recorded in CRA-0000.

| Theme | Summary | CRA relevance |
|---|---|---|
| **Representation independence** | Canonical knowledge is not a file, document, database, graph, index, or publication. Representations are derived; they may change without changing the knowledge. | Directly supports CRA-0000 §6.1 |
| **Scope-bounded authority** | Canonicality is valid within a declared scope. It does not imply global truth, completeness, or consensus. | Supports governed adoption across domains |
| **Governed designation** | Something becomes canonical through architectural commitment and governance—not through popularity, storage location, or format longevity. | Required for multi-repository CRA adoption |
| **Stable identity** | The same knowledge must remain identifiable across reformatting, relocation, republication, and tooling change. | Directly supports CRA-0000 §6.2 |
| **Epistemic plurality** | Uncertainty, disagreement, competing interpretations, and superseded claims may be canonical. | Supports ELS/AERF-style evidence without premature closure |
| **Provenance and status** | Origin, authority, and epistemic condition must be preserved with the knowledge. | Required for governed promotion (e.g., hypothesis → canonical) |
| **Preservation obligation** | The architecture commits to preserving canonical knowledge; loss or silent corruption is architectural failure. | Core CRA preservation objective |
| **Invertibility test** | Architectures that make representations primary and knowledge derived are coherent but weaker for CRA's goals. | Validates CRA's direction |

## Divergence

The reviews disagreed on **how to name the primitive** and **what must survive** when all representations are removed. No adjudication is made here; CRA-0001 must decide.

| Topic | Variants observed | Implication for CRA |
|---|---|---|
| **Core primitive** | meaning; distinctions; intellectual content; evidentiary trace; semantic substrate; preservation contract | CRA-0001 must define the smallest unit that supports identity, derivation, and governance |
| **Term "canonical"** | retain with architectural redefinition; refine with scope qualifier; optional secondary terms (e.g., preservation substrate) | Term likely retained; definition must disambiguate from mathematical "canonical form" |
| **Evidence vs meaning** | some models emphasize primary observations; others emphasize governed semantic commitments | CRA must support both engineering documentation and evidence-heavy domains (e.g., electronics) |
| **Minimality** | what is the minimum recoverable content when representations are stripped? | Tied to identity model and derivation fidelity rules in CRA-0001 |
| **Relationships** | explicit graph of relations vs distinctions preserved across representations | Aligns with CRA-0000 §6.3 — relationships independent of navigation |

## Useful Inputs for CRA

The following inputs are worth carrying into normative work without treating any single review as authoritative:

- **Qualification tests** — several reviews proposed decision procedures (identity, scope, governance, recoverability, non-representation). CRA-0001 may adapt one as conformance guidance.
- **Counterexample catalogs** — PDFs, indexes, knowledge graphs, and AI-derived structures as derived artifacts, not canonical knowledge.
- **Terminology warnings** — avoid conflating canonical knowledge with canonical data, canonical documents, or authoritative sources.
- **Representation-independence clarification** — not representation-free; no single representation has architectural primacy ([ChatGPT_GPT-5.5.md](ChatGPT_GPT-5.5.md), [Composer_2.5.md](Composer_2.5.md)).
- **Scope pairing** — always pair "canonical" with an explicit scope in normative prose.

## Explicit Non-Outcomes

This comparative analysis does **not**:

- select a winning AI definition;
- establish normative CRA terminology;
- resolve primitive-unit or identity-model questions;
- replace [Architectural_Evaluation_Methodology.md](Architectural_Evaluation_Methodology.md) or [Conclusions.md](Conclusions.md).

## Related Documents

- [Prompt.md](Prompt.md)
- [Conclusions.md](Conclusions.md)
- [Architectural_Evaluation_Methodology.md](Architectural_Evaluation_Methodology.md)
- [CRA-0000](../../../../CRA-0000.md)
