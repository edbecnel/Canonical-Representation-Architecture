[Home](../../../../README.md) › [Project Index](../../../../PROJECT_INDEX.md) › [AI](../../README.md) › [Architectural Research](../README.md) › Canonical Knowledge

> **Status:** Maintained
> **Document Class:** Architectural Research
> **Owner:** CRA Architecture Team
> **Applies To:** Architectural research supporting the Canonical Representation Architecture
> **Last Reviewed:** 2026-08-09
> **Review Frequency:** On Change

**Research phase: Complete** (2026-08-09). See [Comparative_Analysis.md](Comparative_Analysis.md) and [Conclusions.md](Conclusions.md). Next normative work: **CRA-0001**.

# Canonical Knowledge Architectural Research

## Purpose

This directory contains the research artifacts produced while investigating one of the most fundamental concepts of the **Canonical Representation Architecture (CRA)**:

> **What is Canonical Knowledge?**

The objective of this research is **not** to determine the architecture by consensus among AI systems.

Instead, multiple independent Large Language Models (LLMs) are asked the same carefully constructed architectural question. Their responses are preserved as independent architectural reviews intended to expose:

- implicit assumptions,
- alternative viewpoints,
- recurring concepts,
- conflicting interpretations,
- potential weaknesses,
- terminology,
- examples,
- counterexamples,
- and questions that may not have been considered during the development of CRA.

The final architectural decisions remain the responsibility of the CRA engineering process and are documented only within the normative CRA specifications.

---

# Research Question

The investigation seeks to establish a rigorous, technology-independent definition of **Canonical Knowledge** suitable for use within the Canonical Representation Architecture.

This research precedes the authoring of **CRA-0001 – Foundational Architectural Principles**, since the definition of Canonical Knowledge is expected to influence one or more constitutional principles of the architecture.

---

# Methodology

Each participating AI model receives **exactly the same prompt**.

No model is shown another model's response.

Responses are preserved without modification except for formatting required for Markdown presentation.

After all responses have been collected, they are compared by human architectural review.

The objective is to identify:

- recurring concepts,
- independent convergence,
- significant disagreements,
- hidden assumptions,
- useful terminology,
- architectural implications,
- and unresolved questions.

Architectural decisions are **not** made by majority opinion.

Instead, the responses serve as independent engineering evidence that informs subsequent architectural reasoning.

---

# Research Artifacts

## Research Prompt

| Document             | Description                                                           |
| -------------------- | --------------------------------------------------------------------- |
| [[Prompt]] Prompt.md | The common research prompt presented to every participating AI model. |

---

## Independent AI Reviews

| AI Model      | Version     | Access Method            | Repository Context | Classification                   | Response                                                           |
| ------------- | ----------- | ------------------------ | ------------------ | -------------------------------- | ------------------------------------------------------------------ |
| ChatGPT       | GPT-5.5     | ChatGPT Web              | No                 | Independent Architectural Review | [[ChatGPT_GPT-5.5]] `ChatGPT_GPT-5.5.md`                           |
| Gemini        | _(version)_ | Gemini Web               | No                 | Independent Architectural Review | [[Gemini]] `Gemini.md`                                             |
| Claude Sonnet | 5           | Claude Web               | No                 | Independent Architectural Review | [[Claude_Sonnet_Web]] `Claude_Sonnet_Web.md`                       |
| Claude Sonnet | 4.6         | GitHub Copilot (VS Code) | Yes                | Contextual Architectural Review  | [[Claude_Sonnet_GitHub_Copilot]] `Claude_Sonnet_GitHub_Copilot.md` |
| Grok          | _(version)_ | Grok Web                 | No                 | Independent Architectural Review | [[Grok]] `Grok.md`                                                 |
| DeepSeek      | R1          | DeepSeek Web             | No                 | Independent Architectural Review | [[DeepSeek_R1]] `DeepSeek_R1.md`                                   |
| Composer      | 2.5         | Composer Web             | No                 | Independent Architectural Review | [[Composer_2.5]] `Composer_2.5.md`                                 |
*(Update the version information as appropriate when responses are collected.)*

---

## Comparative Analysis

| Document | Description |
|----------|-------------|
| [Comparative_Analysis.md](Comparative_Analysis.md) | Convergence, divergence, and CRA-relevant implications across independent AI reviews. |
| [Conclusions.md](Conclusions.md) | Working definition, candidate principles for CRA-0001, and open questions. |

---

# Engineering Principles

The following principles govern this research:

1. AI responses are treated as independent architectural reviews rather than authoritative sources.

2. No architectural decision is accepted solely because multiple AI systems agree.

3. Architectural conclusions must be supported by engineering reasoning, not model consensus.

4. Conflicting responses are often more valuable than agreement because they expose hidden assumptions and unexplored architectural questions.

5. This research documents the architectural discovery process and is therefore informative rather than normative.

---

# Relationship to CRA

The documents contained within this directory are **research artifacts**.

They are **not** normative architectural specifications.

Normative architectural decisions shall be documented only within the Canonical Representation Architecture specifications (for example, CRA-0001 and subsequent CRA documents).

Where appropriate, those specifications may reference the research conducted here, but they do not derive authority from it.

---

# Related Documents

- CRA-0000 — *The Discovery of the Canonical Representation Architecture*
- CRA-0001 — *Foundational Architectural Principles* (planned)
- `docs/AI/README.md`