---
name: scientific-paper-understanding
description: Understand, teach, map, and critically evaluate one scientific paper without reducing it to a generic summary. Use when a user provides or names a paper, PDF, DOI, URL, preprint, protocol, trial report, secondary analysis, observational study, qualitative or mixed-methods study, computational or machine-learning study, method/software paper, database/resource paper, case report, review/meta-analysis, perspective, or related scientific document and wants to know what it does, why it exists, how its evidence supports its claims, what prerequisites are needed, how to read its figures/tables/equations, or how strong its conclusions are. Adapt depth for orientation, learning, or audit while keeping document identity, source coverage, author claims, observed results, external evidence, and analyst inference separate.
---

# Scientific Paper Understanding

## Purpose

Turn one scientific paper into the smallest accurate mental model that lets the user understand its question, logic, methods, evidence, claims, limitations, and practical meaning. Teach the paper instead of dumping a long summary.

Treat the target as a **paper package** when associated material is available: main text, supplement, appendices, correction/erratum, expression of concern or retraction notice, current preprint/version, registration/protocol, and relevant code/data links. Never silently treat an abstract or search snippet as a full paper.

## Non-Negotiable Rules

1. Ground important statements in the available paper package. Never invent missing methods, results, sample details, author intent, or study status.
2. Determine **document role before study design**. A protocol, secondary analysis, letter, editorial, review protocol, correction notice, or retracted article can mention an RCT without being the primary RCT results paper.
3. Keep these distinct:
   - **Author statement**: what the authors explicitly say.
   - **Reported result**: what the study reports, measures, estimates, or derives.
   - **Supported interpretation**: what the evidence reasonably supports within design limits.
   - **Analyst inference**: an inference made while analyzing the paper.
   - **External context**: information from outside the target paper.
4. Treat `not reported`, `not found in available sources`, and `not done` as different states.
5. Preserve evidence scope. Never silently convert:
   - association -> causation;
   - no significant difference -> equivalence;
   - prediction -> intervention benefit;
   - internal validation -> external validation;
   - benchmark success -> universal performance;
   - in-vitro/ex-vivo/animal/in-silico evidence -> human clinical validation;
   - qualitative themes -> prevalence;
   - single case -> population evidence;
   - planned protocol -> observed outcome;
   - preprint -> peer-reviewed evidence.
6. Retraction status overrides normal evidence use. Surface it before interpretation and do not present the retracted findings as reliable current evidence. A correction/erratum is different: determine what changed and whether it materially changes interpretation.
7. Do not invent numerical confidence scores. Describe support using evidence, uncertainty, and explicit caveats.
8. Reporting quality is not the same as methodological quality, risk of bias, evidence certainty, or reproducibility.
9. Prefer the user's language. Preserve important technical names and give English terms on first use when useful. For Persian, Arabic, and other right-to-left outputs, apply bidirectional-text-safe formatting: start mixed prose with the RTL language, keep English technical spans isolated with inline code or parentheses, and never combine RTL prose with LTR labels inside ASCII/code-block diagrams.
10. Minimize friction. Do not maximize information; maximize useful understanding per interaction.
11. If the user asks a narrow question, answer it directly. Do not force the complete workflow.
12. If the user explicitly asks for a full analysis, traverse the full relevant workflow.

## Modes

Infer the mode. Do not ask the user to choose unless necessary.

- **Orient**: identify what the document is, why it exists, what it did or plans to do, what it found or contributes, and why it matters.
- **Learn**: default for understanding. Build prerequisite dependencies and guide the next useful reading step.
- **Audit**: evaluate claims, methods, statistics/computation, bias, evidence strength, reproducibility, and interpretation boundaries.

Modes can combine.

## Workflow

### 0. Establish Identity, Status, and Source Coverage

Before interpreting results, identify the scientific object actually in hand.

Determine when possible:
- exact title and stable identifier;
- **document role**: primary-results report, secondary/reanalysis report, protocol/plan, method/tool/resource report, evidence synthesis, case report/series, qualitative/mixed-methods report, guideline/consensus, editorial/letter/commentary/position paper, correction/notice, or other;
- relationship to a parent study or related document when relevant;
- publication status: peer reviewed, preprint/versioned, corrected, expression of concern, or retracted;
- source coverage: full package, main text without all supplements, abstract plus excerpts, abstract only, or metadata only.

When metadata/web access exists and the user has not prohibited it:
- verify corrections, errata, expressions of concern, and retractions;
- for preprints/versioned publications, identify the version/date analyzed and newer versions when material;
- identify linked supplements or protocols when they contain evidence needed for the question.

Do not trust database `paper_type`, article title, journal label, or section names as final classification. Inspect the actual document content available.

If only partial text is available, give the strongest valid answer and state the coverage limit. Do not call it a full-paper audit.

For software/database/resource papers, separate historical claims in the paper from current operational facts. Check current status only when the user asks about current use or current status materially changes the answer.

### 1. Fingerprint the Scientific Work

Create a compact multi-label fingerprint only as needed:
- document role;
- publication type;
- study design;
- scientific domain;
- population/sample/model system or data type;
- experimental level when relevant: in vitro, ex vivo, in vivo animal, human observational/interventional, in silico;
- analytical approach;
- validation type;
- publication/status modifier.

For secondary analyses, identify the parent study and state what is new in this paper. For protocols, state that the work is plan-bearing. For non-empirical argument papers, identify thesis/evidence rather than inventing experiments.

Read `references/article-types.md` when routing is not obvious or type-specific analysis is required.

### 2. Build the Orientation

Answer compactly:
1. What scientific problem is addressed?
2. What gap or uncertainty motivated the work?
3. What is this document specifically trying to do?
4. What did the authors do, analyze, synthesize, propose, or plan?
5. What is the main result or contribution? For plan-bearing documents, state the planned contribution and explicitly say outcomes are not yet reported.
6. Why does it matter within the actual evidence scope?

Include any caveat that changes the headline meaning now, not later: retraction/correction status, preprint status, secondary-analysis status, low-certainty synthesis, observational design, model-system limitation, major attrition, simulated validation, or restricted dataset.

### 3. Build the Paper Understanding Graph

Map semantics, not headings. Start with:

`Problem -> Gap -> Objective -> Approach -> Evidence/Result -> Claim -> Meaning`

Then apply only the relevant overlay. Do not force result-bearing nodes into protocols, perspectives, guidelines, or other non-result documents.

Read `references/paper-graph.md` for graph nodes, relations, source anchors, evidence layers, and Evidence Cards.

### 4. Build the Learning Dependency Graph When Needed

In Learn mode, identify only concepts that block the next important paper node. Do not create a glossary dump.

Prefer a short prerequisite chain and 3-7 blockers. Distinguish domain blockers from method/statistics/computation blockers when useful.

Select the **next best learning action**: the smallest concept, figure, method, or result that unlocks the most important next layer.

Read `references/pedagogy.md` for prerequisite selection and teaching rules.

### 5. Traverse the Needed Paper Objects

For each section, method, figure, table, or equation the user needs, explain:
- what it is;
- why it is there;
- how it connects to the objective;
- what was actually done or observed;
- what must be understood to interpret it;
- what it establishes and what it does not.

For figures, inspect the question, axes/encodings, groups/comparisons, uncertainty, main pattern, and supported claim.

For tables, inspect population/data, denominators, groups, effect/uncertainty, missingness where relevant, and supported conclusion.

For equations, unpack variables, units when reported, assumptions, role, scientific meaning, inputs, and how outputs are used.

Follow important supplement material before declaring a method absent.

### 6. Trace Major Claims to Evidence

Use Evidence Cards for claims that matter to the user's goal:

- **Claim**
- **Evidence**
- **Source anchor**
- **Evidence layer/type**
- **Relationship**: directly supports / partially supports / indirectly supports / does not establish / contradicts / unclear from available source
- **Scope**
- **Caveat**
- **Certainty** only when the paper or an appropriate evidence-assessment framework explicitly provides one

For secondary analyses, anchor claims to the current paper and distinguish parent-study evidence. For reviews, distinguish completed synthesis from protocol/planned synthesis. For model/benchmark papers, distinguish technical validation from biological or clinical validation.

### 7. Audit When Requested or Material

In Audit mode, read `references/critical-review.md` and apply only design-relevant checks.

Always test:
- can this document/design answer the stated question?
- does sample/data/model-system provenance fit the claim?
- are outcomes/targets/comparators and analysis populations appropriate?
- are uncertainty and validation interpreted correctly?
- are conclusions broader than the evidence layer?
- do missing data, attrition, confounding, leakage, benchmark design, or qualitative sampling materially change interpretation?
- do supplement, protocol, registration, correction/status, code, or data change the conclusion?

Use reporting guidelines as reporting aids, never as automatic quality scores.

### 8. End With the Next Useful Action

Unless the user requested a complete report, stop after a meaningful unit and state one next best action: learn one blocker, inspect one key figure, unpack one method, trace one claim, or audit one risk.

Do not manufacture quizzes when they interrupt the task.

## External Information Policy

Keep the target paper primary. Use external sources only when they materially help with:
- terminology/prerequisites not explained in the paper;
- version/correction/retraction status;
- current software/database/resource status;
- necessary methodological/reporting standards;
- novelty or literature context when requested.

Label external information. Never make it look as if it came from the paper.

## Output Discipline

Read `references/output-contract.md` before broad Orient, Learn, Audit, or full-analysis outputs.

For Persian, Arabic, or other RTL output, enforce the bidirectional-text rules in `references/output-contract.md`. In particular, do not create mixed-language ASCII trees like `English label -> Persian explanation` inside code fences. Use an English-only diagram plus RTL explanation outside it, or use a fully RTL Markdown list instead.

Do not expose internal workflow bookkeeping. Do not print every possible category/checklist. Surface only what helps the user understand or evaluate the paper.

## Release Quality Gates

Before finalizing a substantial analysis, verify:
- the actual document role was identified rather than trusted from metadata alone;
- source coverage is not overstated;
- retraction/expression/correction/version status is handled correctly when checked;
- a primary-results paper is not confused with its protocol, secondary analysis, editorial, reply, or review;
- no paper content was fabricated;
- major claims are traceable to the available source;
- author claims and analyst inferences remain distinct;
- `not reported` is not rewritten as `not done`;
- causal language matches design;
- no-significance is not called equivalence without an equivalence/non-inferiority design;
- RCT analysis population, attrition, treatment contrast, and harms are not ignored when material;
- a failed/unsupported primary outcome is not silently rescued by exploratory secondary, subgroup, or post-hoc findings;
- prediction performance is not reduced to AUC/accuracy when calibration, thresholds, or external validation matter;
- qualitative themes are not converted into prevalence/frequency claims;
- in-vitro, ex-vivo, animal, in-silico, and human evidence remain distinct;
- benchmark/method performance is not treated as biological/clinical validation;
- review/meta-analysis results retain risk-of-bias, heterogeneity, and certainty context when available;
- protocols/review protocols remain planned evidence;
- case reports remain case-level evidence;
- retracted findings are not presented as reliable evidence;
- correction materiality is assessed rather than treating every correction as a retraction;
- for RTL output, no decorative/code-block diagram mixes RTL prose with LTR labels, and mixed prose does not begin with an LTR label followed by an RTL sentence;
- the response is no longer than required by the user's goal.
