# AI-Assisted Proposal Triage Tool — System Design

* **Candidate Name:** Arsalan Aftab Ali
* **Reference:** MATACS-TH-2026-02
* **Time Actually Spent:** 1 hour 20 mins

---

## AI Use and Guidelines

I used an AI assistant for roughly 50–60% of the workflow to structure the JSON extraction schemas, and refine the wording in `WRITEUP.md`, while I manually designed the core triage architecture, scoring rubric, and edge-case handling (such as catching Proposal B's unconfirmed subcontractor, Proposal C's prompt injection, and Proposal D's missing timeline). 

---

## How AI Tools Were Used

In accordance with the assessment guidelines, AI tools (Google Gemini) were used as a collaborative design and drafting partner during this assessment:
1. **Brainstorming & Edge-Case Verification:** Used to stress-test the separation of responsibilities between LLM extraction and deterministic rule-based scoring, ensuring edge cases in the sample set (Proposal B's unconfirmed subcontractor licence, Proposal C's prompt injection in Appendix C, and Proposal D's omitted timeline) were properly caught and categorized.
2. **Prompt Structuring & Schema Design:** Assisted in formatting the JSON extraction schema and refining the XML-tag isolation guardrails in `PROMPTS.md`.
3. **Drafting & Formatting:** Used to format the Mermaid flowchart syntax and refine `WRITEUP.md` for clarity and conciseness. 

---

---

## Repository Files & Deliverables

* **[`diagram/flow.png`](./diagram/flow.png)** — Process-flow diagram from PDF upload to ranked output, clearly distinguishing AI steps, deterministic rule-based steps, and human-in-the-loop checkpoints.
* **[`WRITEUP.md`](./writeup.md)** — Concise architectural write-up answering all five design questions (580 words; strictly under the 1,000-word limit).
* **[`PROMPTS.md`](./PROMPTS.md)** — Exact system and user prompts used for schema-driven fact extraction, prompt-injection detection, and one-line rationale generation.
* **[`ranking.json`](./ranking.json)** — Final evaluation output for sample proposals A–E following the strict JSON schema and status rules (`ranked`, `flagged`, `ineligible`).

---
