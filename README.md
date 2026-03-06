# AI Prompt Engineering — Prompting Under Governance

Governance-first · auditable · reproducible · human-accountable  
Built for **MBA / Master of Finance cohorts** and **professional finance / corporate finance / trading / research practitioners** who need disciplined prompt design under real institutional constraints.

---

## What this repository is

This repository is the governed home of **AI Prompt Engineering**: a Colab-first laboratory for designing, testing, and reviewing **prompts as operational contracts** rather than casual instructions.

The objective is not merely to get “better outputs.”  
The objective is to build **reviewable prompting systems** whose behavior can be inspected, reproduced, criticized, and improved under explicit control.

In professional environments, prompts are not harmless text. They are behavioral specifications. A prompt determines what the model is allowed to use, what it must refuse to invent, how uncertainty must be disclosed, how outputs must be structured, and when the system must stop instead of improvising. Once prompts are used in finance, corporate analysis, research workflows, committee materials, or decision-support pipelines, they stop being a convenience and become part of the control environment.

This repository therefore treats prompting as a governed discipline with explicit attention to:

- what information is included
- what information is excluded
- what the model is allowed to infer
- what must remain unresolved
- what structure the output must obey
- what artifacts must be produced for review
- what failure modes must be surfaced rather than hidden

An independent reviewer should be able to inspect a governed prompting run and answer:

- what prompt was used
- what constraints were imposed
- what evidence packet was provided
- what the model generated
- what assumptions appeared
- what open items remained unresolved
- what validations passed or failed
- whether the output should be advanced, revised, or rejected

This repository is intentionally explicit about limits:

- it does **not** claim that prompting alone creates truth
- it does **not** treat fluent narrative as evidence
- it does **not** assume structured output is automatically reliable
- it does **not** claim production readiness by default
- it does **not** promise decision quality, alpha, compliance sufficiency, or deployability

**Core premise:**  
**Capability ↑ ⇒ Risk ↑ ⇒ Controls ↑**

---

## Repository structure

This repository follows the structure shown in the current file tree:

- **/book/**  
  The book source and compiled materials. The book is the governing conceptual framework: principles, mechanisms, prompt patterns, failure modes, acceptance gates, and escalation logic.

- **/notebooks/**  
  The operational laboratories. These notebooks implement the book’s ideas in a deterministic, inspectable, artifact-producing workflow.

- **README.md**  
  The entry point to the repository and the high-level map for readers, reviewers, students, and practitioners.

---

## The book

The **/book/** directory contains the book materials for the Prompt Engineering project.  
The book serves as the conceptual and methodological anchor of the repository.

It explains:

- why prompts must be governed
- how prompts act as contracts
- how output structure reduces ambiguity
- how evidence packets should be bounded
- how prompt failure modes emerge
- how revision and promotion decisions should be made
- why “generation ≠ verification” remains a non-negotiable principle

The book is not separate from the notebooks.  
The book defines the discipline; the notebooks operationalize it.

---

## The notebooks

The **/notebooks/** directory contains the governed Colab laboratories associated with the project.

These notebooks are not decorative examples.  
They are the implementation layer of the repository.

They exist to show, in executable form, how prompt engineering can be transformed from an informal craft into a controlled workflow with:

- deterministic setup where applicable
- bounded input packets
- explicit prompt versions
- structured outputs
- validation gates
- risk logging
- exported artifacts
- repeatable review procedures

Each notebook should be read as a lab for prompt behavior under constraint.

---

## What this project teaches

This repository is built around a governance-first interpretation of prompt engineering.

That means prompt engineering is not framed here as “clever wording” or “secret tricks.”  
It is framed as a serious operating discipline involving:

- scope control
- boundary control
- evidence discipline
- schema discipline
- version control
- failure detection
- escalation rules
- reproducibility expectations
- human accountability

The central idea is simple:

A prompt is not just a request.  
A prompt is a **control surface**.

It governs how a model is allowed to behave inside a defined task boundary.

A well-governed prompt should make it easier to detect when the model is wrong, unsupported, incomplete, overconfident, out of scope, or structurally non-compliant. A poorly governed prompt does the opposite: it produces prose that looks polished while concealing ambiguity, unsupported inference, and missing diligence.

This project exists to reduce that risk.

---

## Core themes of the repository

Across the book and notebooks, the repository emphasizes several recurring themes.

### 1. Prompts as contracts
A prompt should define:

- objective
- scope
- allowed evidence
- prohibited behaviors
- required output structure
- uncertainty posture
- escalation conditions
- termination criteria

If these are not explicit, the model will often fill the gaps with stylistic confidence rather than controlled reasoning.

### 2. Structure before style
A polished paragraph is less important than a reviewable output.  
This repository prioritizes outputs that preserve:

- facts provided
- assumptions
- open items
- unresolved questions
- validation status
- decision recommendation

Narrative elegance is secondary to auditability.

### 3. Bounded context
The model should only operate on what it is allowed to use.  
That means context packing matters. Inclusion and exclusion decisions matter. Missing evidence must remain visible instead of being smoothed over through plausible language.

### 4. Failure visibility
A safe system is not one that never fails.  
A safe system is one that fails visibly, traceably, and early enough for a human reviewer to intervene.

### 5. Human accountability
Responsibility does not migrate from the analyst, researcher, practitioner, or reviewer to the model. The human remains accountable for validation, interpretation, and final use.

---

## What every governed notebook should enforce

Every notebook in this repository should be reviewable by artifact inspection.

At minimum, a governed run should make it possible to inspect:

- the prompt version used
- the input packet or evidence packet
- the schema requested
- the model response
- any validation results
- any refusal or boundary event
- any unresolved items
- the final promotion decision

Where implemented, runs should also export artifacts such as:

- `run_manifest.json`
- `prompts_log.jsonl`
- `risk_log.json`
- `final_output.json`
- `validation_report.json`
- generated deliverables in an `artifacts/` directory
- zipped run bundles for audit or review

The exact filenames may differ across notebooks, but the principle does not:  
**a prompt-engineering workflow must leave evidence of its own behavior.**

---

## Recommended way to use this repository

A disciplined way to work through this project is:

1. Read the relevant material in **/book/** first.  
   Understand the mechanism before touching the implementation.

2. Run the corresponding notebook in **/notebooks/** without modification.  
   Observe baseline behavior before “improving” anything.

3. Inspect the artifacts.  
   Focus on boundaries, validation results, open items, and failure signals.

4. Change one variable at a time.  
   For example:
   - tighten the schema
   - narrow the evidence packet
   - strengthen refusal rules
   - increase disclosure requirements
   - change the prompt role or objective framing

5. Re-run and compare artifacts.  
   Do not rely on intuition alone. Compare what actually changed.

6. Record failures explicitly.  
   A failure discovered through artifacts is a contribution, not an embarrassment.

7. Promote only under evidence.  
   If a prompt works only when reviewers ignore open items, schema violations, or missing-evidence warnings, then it is not ready.

---

## Shared governance spine across the project

The following principles apply throughout the repository.

### Generation is not verification
A model can generate fluent text without proving the truth of the content.  
All outputs should be treated as **Not verified** unless separately validated.

### Facts, assumptions, and open items must remain separate
Prompted outputs should distinguish between:

- **facts_provided**
- **assumptions**
- **open_items / open_questions**

This separation is not cosmetic. It is essential to trustworthy review.

### Scope must be explicit
The model should know what it is being asked to do, what it is not allowed to do, and when it must stop.

### Refusal is a feature
In professional settings, a system that refuses unsupported inference can be more valuable than one that produces persuasive but unsafe prose.

### Auditability matters
A run that cannot be reconstructed cannot be reliably reviewed.

### Humans remain accountable
The model can support drafting, structuring, summarizing, and organizing.  
It does not absorb professional responsibility.

---

## Who this repository is for

This repository is designed for readers who need more than prompt tricks.

It is for:

- MBA students
- Master of Finance students
- finance practitioners
- corporate finance teams
- board-facing analysts
- strategy and research teams
- educators teaching AI under institutional constraints
- professionals who need prompt behavior to be explainable, bounded, and reviewable

It is especially relevant for environments where the cost of polished nonsense is high.

---

## What this repository is not

To avoid confusion, this repository is **not**:

- a collection of magical prompt hacks
- a claim that models can replace expert review
- a substitute for legal, accounting, audit, tax, compliance, or investment judgment
- a promise that structured output equals reliable output
- a production system by default
- a guarantee of correctness, safety, or business value

The repository is a governed educational and research environment.

Its purpose is to help users design prompt workflows that are more transparent, disciplined, and inspectable than ordinary ad hoc prompting.

---

## IMPORTANT DISCLAIMERS

### Educational / Non-Reliance
All materials in this repository are provided **for educational and research purposes only**.  
Nothing in this repository constitutes investment, trading, legal, tax, accounting, audit, compliance, or other professional advice.

### Not verified
Unless explicitly stated otherwise in a specific artifact, all outputs, claims, calculations, summaries, classifications, and conclusions should be treated as **Not verified**.

### Confidentiality and data hygiene
Do not paste confidential, proprietary, regulated, personal, or sensitive information into external systems. Use anonymization, redaction, and minimum-necessary disclosure by default.

### No fabricated claims
Invented citations, invented facts, invented metrics, invented authority, and invented certainty are unacceptable. When evidence is missing, the correct response is an explicit verification list, not persuasive prose.

---

## License

This project is released under the **MIT License**.

**Copyright (c) 2026 Alejandro Reynoso**

---

## Contact

**Alejandro Reynoso**  
Email: areynoso@yahoo.com  
GitHub: https://github.com/alexdibol
