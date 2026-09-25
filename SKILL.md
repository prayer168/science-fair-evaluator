---
name: science-fair-evaluator
description: Evaluate and evolve elementary-school science fair ideas from any seed, including a topic, observation, link, article, video, image, file, dataset, or rough note. Automatically search comparable Taiwan and international work, run a formal novelty/overlap gate, assess safety, feasibility, and evidence quality, then offer 3–5 selectable research directions. After the user selects a direction that passes the novelty gate, create a complete science-fair prework book without Discussion or Conclusion sections. Use for topic screening, prior-work comparison, novelty-gap analysis, candidate generation, research design, and prework reports.
---

# Science Fair Evaluator

Use Traditional Chinese unless the user requests another language. Treat every input as a research seed, not as a finished title.

## Two-Phase Workflow

Always determine whether the user has selected a candidate.

- **Phase 1 — automatic evaluation and selection:** use when the user supplies any new seed, link, topic, article, file, image, video, or note without a selected candidate.
- **Phase 2 — complete prework book:** use only after the user explicitly selects a Phase-1 candidate by its label, exact title, or an unambiguous statement such as「選 B」or「以候選 3 進行前置作業」. If the user supplies an already-finalized title and explicitly requests the prework book, treat that title as selected **only after the novelty/overlap gate is run**.

Do not skip Phase 1 merely because the input is short. Do not produce the full prework book while the user is still comparing candidates. Do not enter Phase 2 when the selected direction is classified as redesign-required or near-duplicate.

## Phase 1 — Automatic Evaluation and Candidate Selection

### 1. Intake and evidence

1. Read or inspect every available user-provided artifact with the suitable tool.
2. Browse current, authoritative sources before making factual claims. Search both:
   - Taiwan science-fair records, local competition PDFs, and relevant official guidance;
   - international peer-reviewed research, universities, museums, government agencies, and technical standards.
3. Search conceptual synonyms and mechanism terms, not only the user's exact title or keyword.
4. Create a compact evidence ledger that separates verified evidence, user claims, assumptions, safety constraints, search boundaries, and unresolved uncertainties.
5. Never claim that no one has done the topic. Use calibrated wording such as「在本次搜尋範圍內，未找到高度相同的公開研究」.

### 2. Mandatory novelty/overlap gate

Before scoring candidates, read and apply `references/novelty-overlap-gate.md`.

Mandatory outputs:

- a Taiwan + international prior-work matrix;
- strongest 3–8 comparable works;
- overlap level O0–O4;
- novelty gate N0–N3;
- explicit research-gap statement;
- a `do-not-repeat` list of saturated variables/methods;
- the exact contribution type: mechanism, interaction, measurement, analysis, design, robustness/stability, context, replication, or external validation.

Rules:

- O0–O1 can proceed when the gap is clear.
- O2 can proceed only as a conditional pass and the new dimension must appear explicitly in the title, purposes, experiments, and success criteria.
- O3 requires redesign and a new search before candidate handoff.
- O4 must be rejected or replaced.
- Technology such as AI, Arduino, ESP32, sensors, dashboards, 3D printing, or heatmaps is not novelty by itself.

### 3. Diagnose the seed

Identify the observable phenomenon, real-world problem, suspected mechanism, manipulable variables, measurable outcomes, control condition, student-operable work, and likely limitations.

Apply these hard gates before scoring: safety and ethics, testability, student ownership, resources, data quality, defensible novelty, and completion time. Redesign or reject hazardous, untestable, adult-operated, or purely demonstrative work. Follow `references/evaluation-framework.md`.

### 4. Search comparison and evolution

Build a concise comparison table containing source/year, tested variables, method/measurement, key finding, overlap, remaining gap, and source quality. When the seed is common, descriptive, too broad, weakly measurable, or highly overlapping, use `references/research-evolution-engine.md` to move the project toward a different question rather than merely adding more variables.

Improve ideas through mechanism, interaction, measurement quality, controls, robustness, local context, prototype iteration, prediction, or external validation. Technology is allowed only when it improves evidence quality or enables a genuinely new test.

### 5. Offer exactly 3–5 candidates

Generate **3–5 distinct, safe, feasible candidates** that pass or conditionally pass the novelty gate. Each must differ in a meaningful contribution: mechanism, interaction, variable, measurement, context, prototype, analysis, robustness, or validation—not just wording.

For every candidate, provide:

- candidate label and formal title;
- central question and proposed evidence;
- novelty/gap statement;
- overlap level and novelty-gate result;
- hard-gate status;
- scores (1–5): researchability, mechanism depth, novelty, elementary suitability, student ownership, measurability, experimental control, safety, cost/material access, real-world value, and science-fair potential;
- approximate duration, key equipment, largest risk, and one-sentence fallback.

Use the exact output structure in `references/candidate-selection-template.md`. Recommend one primary candidate, but do not hide the alternatives.

### 6. Selection handoff

End Phase 1 by presenting the candidates as clearly separable choices and request one selection. If the runtime provides a native choice control, use it; otherwise instruct the user to reply with `選 A`–`選 E` or paste the chosen title. Do not imply that static Markdown text creates UI buttons.

## Phase 2 — Complete Prework Book

When a candidate is selected:

1. Re-open the selected candidate record and refresh any time-sensitive sources needed for the report.
2. Re-run the novelty/overlap gate against the finalized title and method. If new evidence raises overlap to O3/O4, stop, redesign, and return to Phase 1.
3. Read and apply all of these references before drafting:
   - `references/novelty-overlap-gate.md`
   - `references/evaluation-framework.md`
   - `references/research-evolution-engine.md`
   - `references/prework-report-template.md`
   - `references/quality-validation-checklist.md`
4. Produce one complete, internally consistent **科展前置作業作品書**. Include the title, abstract, topic formation, prior-work comparison, research-gap matrix, overlap/gate decision, do-not-repeat list, background/motivation, questions, prediction, purposes, framework, materials, detailed experiments, blank data tables, analysis plan, safety, budget, schedule, risks, validation plan, references, and next actions.
5. **Do not include「討論」or「結論」sections.** The report may state predicted patterns and pre-defined interpretation criteria, but must not present invented results or a completed conclusion.
6. Map every purpose to an experiment, dependent variable, measurement method, blank record table, and graph. State units, repeats, calibration, randomization/order control, invalid-data rules, and stopping rules.
7. For projects with prototypes or optimization, define baseline, objective metrics, trade-offs, robustness/stability tests, and external validation before data collection.
8. Use APA 7 citations; every in-text citation must appear under `參考文獻`.
9. Run the validation checklist, repair contradictions, and finish with `Ready`, `Conditionally ready`, or `Not ready`, including the most important remaining uncertainty and the first pilot-test requirement.

## Stage Gates for Prework

Use these explicit gates in complete prework books:

- **G0 Prior-work & novelty:** Taiwan + international search complete; overlap matrix, O-level, N-level, research gap, and do-not-repeat list are explicit.
- **G1 Research alignment:** title → core question → purposes → experiments → measurements → analysis is internally consistent.
- **G2 Apparatus & logistics:** materials, apparatus, calibration, sourcing, safety, and student-operable steps are defined.
- **G3 Pilot readiness:** baseline, pilot procedure, repeatability threshold, invalid-data rules, and stopping rules are ready.

Formal experiments may begin only when G0–G3 pass or when any conditional item has a documented acceptance criterion.

## Safety and Integrity

Do not recommend uncontrolled fire, high voltage, pressure vessels, toxic/corrosive chemicals, pathogens or mold culture, bodily fluids, medicines, ecological release, vertebrate harm, privacy-sensitive human data, or unsupported health claims. Substitute safer materials, sealed systems, simulations, low-voltage kits, or teacher-prepared components where possible.

Never fabricate sources, findings, measurements, precision, product specifications, novelty, or award predictions. Prefer a narrow, measurable, student-owned investigation over a broad or fashionable topic.
