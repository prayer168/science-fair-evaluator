# Novelty & Overlap Gate（撞題檢核）

Use this gate before candidate scoring and again before writing a complete prework book.

## 1. Mandatory search scope

Search at minimum:

1. Taiwan National Science Fair / NTSEC records, including title variants and conceptually similar projects.
2. Local/regional science-fair or school competition records when discoverable.
3. Peer-reviewed academic literature and university/government technical reports.
4. Relevant patents, engineering demonstrations, standards, or educational projects only when they materially affect novelty.

Search not only the seed keyword. Also search synonyms, mechanism terms, materials, measurement variables, application terms, and likely historical names.

## 2. Prior-work matrix

Build a matrix with at least these fields:

| Source/year | Project/paper title | Population/system | Manipulated variables | Measurements | Analysis/index | Prototype/validation | Main finding | Overlap with proposed work | Remaining gap | Source quality |
|---|---|---|---|---|---|---|---|---|---|---|

When multiple prior works overlap in different dimensions, explicitly state the union of what is already known. Do not treat each paper in isolation and then claim novelty from a combination that is already obvious.

## 3. Overlap levels

Classify the proposed work:

- **O0 Minimal overlap**: same broad domain only; different core question and evidence chain.
- **O1 Low overlap**: some shared materials or measurements, but a clearly different mechanism, context, method, or validation target.
- **O2 Moderate overlap**: one or more central variables or outcome measures are shared; novelty depends on a defensible new dimension.
- **O3 High overlap**: most central variables, apparatus, measures, or analysis already exist; redesign is required before Phase 2.
- **O4 Near-duplicate**: the core question, method, variables, and expected evidence substantially match prior work; reject or replace the direction.

## 4. Research-gap test

A gap is defensible only when it is one or more of:

- unresolved mechanism;
- untested interaction between variables;
- new measurement or analysis that answers a materially different question;
- engineering redesign with pre-defined performance criteria;
- robustness/stability across conditions;
- external or real-world validation not present in prior work;
- local ecological/material/context difference with scientific justification;
- replication that explicitly tests reliability and adds a meaningful comparison.

The following alone are **not** sufficient novelty:

- using Arduino/ESP32/AI/sensors instead of manual measurement;
- making a prettier graph, heatmap, dashboard, or 3D model;
- adding more repeated trials;
- changing only container size, color, brand, or a trivial material variant;
- reproducing a known classroom demonstration;
- combining two already-known factors without a new scientific question.

## 5. Novelty claim calibration

Never write “first,” “no one has studied,” “world first,” or equivalent unless supported by an exhaustive, defensible review. Prefer:

> 在本次檢索到的臺灣歷屆科展與相關學術文獻範圍內，既有研究多聚焦於＿＿；較少同時探討＿＿，因此本研究將＿＿作為主要研究缺口。

State the search boundary and important unresolved uncertainty.

## 6. Gate decision

Before Phase 2, assign:

- **N0 Pass**: O0–O1, clear defensible gap.
- **N1 Conditional pass**: O2, gap is promising but must be explicitly built into title, purposes, experiments, and success criteria.
- **N2 Redesign required**: O3, do not write the full prework book yet. Evolve the question and repeat the search.
- **N3 Reject/replace**: O4 or no defensible student-owned contribution.

The complete prework book may proceed only with N0 or N1.

## 7. Phase-2 traceability

The full report must carry forward:

1. the strongest 3–8 prior works;
2. the overlap matrix;
3. the selected gap statement;
4. the overlap level and gate decision;
5. a “do-not-repeat” list of variables/methods that are already saturated;
6. the exact new contribution type;
7. a validation plan capable of showing whether the proposed contribution actually works.

If new literature discovered during Phase 2 raises overlap to O3/O4, stop, redesign, and re-run the gate before continuing.