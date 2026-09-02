---
name: scientific-paper-understanding
description: Understand, teach, map, and critically evaluate one scientific paper without reducing it to a generic summary. Use when a user provides or names a paper, PDF, DOI, URL, preprint, protocol, trial report, secondary analysis, observational study, qualitative or mixed-methods study, computational or machine-learning study, method/software paper, database/resource paper, case report, review/meta-analysis, perspective, or related scientific document and wants to know what it does, why it exists, how its evidence supports its claims, what prerequisites are needed, how to read its figures/tables/equations, or how strong its conclusions are. Adapt depth for orientation, learning, or audit while keeping document identity, source coverage, author claims, observed results, external evidence, and analyst inference separate.
---

# Scientific Paper Understanding

Protocol version: 1.1.0

## Purpose

Turn one scientific paper into the smallest accurate mental model that lets the user understand its question, logic, methods, evidence, claims, limitations, and practical meaning. Teach the paper instead of dumping a generic summary.

Treat the target as a **paper package** when associated material is available: main text, supplement, appendices, correction/erratum, expression of concern or retraction notice, current preprint/version, registration/protocol, and relevant code/data links.

## Core invariants

1. Ground important statements in the available paper package. Never invent missing methods, results, sample details, author intent, study status, code/data availability, or validation.
2. Determine **document role before study design**. A protocol, secondary analysis, letter, editorial, review protocol, correction notice, or retracted article can mention an RCT without being the primary RCT results paper.
3. Keep these evidence layers distinct:
   - **Author statement:** what the authors explicitly say.
   - **Reported result:** what the study reports, measures, estimates, or derives.
   - **Supported interpretation:** what the available evidence reasonably supports within design limits.
   - **Analyst inference:** an inference made while analyzing the paper.
   - **External context:** information from outside the target paper.
4. Treat `not reported`, `not found in available sources`, and `not done` as different states.
5. Preserve evidence scope. Never silently convert association to causation, no significant difference to equivalence, prediction to intervention benefit, internal to external validation, benchmark success to universal performance, non-human/in-silico evidence to human clinical validation, qualitative themes to prevalence, a case to population evidence, a protocol to observed results, or a preprint to peer-reviewed evidence.
6. Retraction status overrides normal evidence use. For corrections/errata, determine what changed and whether interpretation is materially affected.
7. Do not invent numerical confidence scores. Use evidence, uncertainty, and explicit caveats.
8. Reporting quality is not the same as methodological quality, risk of bias, evidence certainty, or reproducibility.
9. Prefer the user's language. For Persian and other RTL outputs, follow the bidirectional-text rules in `references/output-contract.md`.
10. Match effort to the user's goal. Answer narrow questions directly; traverse the full relevant workflow only for broad or full-analysis requests.

## Source-access routing

Establish the evidence object before interpretation.

- **User-provided PDF or file:** treat the supplied document as the primary paper evidence. Use external sources only for status/version/correction checks, associated material that is needed, or external context requested by the user.
- **DOI, journal URL, repository URL, or stable identifier:** resolve the actual document and prefer the publisher, journal, official repository, or other primary publication source before interpreting substantive claims.
- **Title or citation only:** use search for identity resolution, then obtain the best available primary paper source before substantive analysis.
- **Abstract or indexed excerpts only:** label the coverage as partial. Do not infer absent methods/results and do not call the output a full-paper audit.
- **Search snippets:** use for discovery only. Do not treat them as evidence for detailed claims when the paper or a primary source can be obtained.
- **Versioned/preprint records:** identify the exact version analyzed and newer or peer-reviewed versions when material.
- **Correction/retraction/status checks:** verify them when web or metadata access exists and the status can change interpretation.

If only partial text is available, give the strongest valid answer and state the coverage limit. Do not block a useful narrow answer merely because the complete package is unavailable.

## Modes

Infer the mode unless the user explicitly specifies one.

- **Orient:** identify what the document is, why it exists, what it did or plans to do, what it found or contributes, and why it matters.
- **Learn:** build prerequisite dependencies, explain the paper as a connected model, and select the next useful reading or learning step.
- **Audit:** evaluate claims, methods, statistics/computation, bias, evidence strength, reproducibility, and interpretation boundaries.

Modes can combine.

## Reference routing

Load detailed references only when their stage is reached.

- `references/article-types.md` — use when document-role or study-type routing is uncertain or type-specific analysis is needed.
- `references/paper-graph.md` — use when building the semantic Paper Understanding Graph or Evidence Cards.
- `references/pedagogy.md` — use in Learn mode for prerequisite selection and teaching depth.
- `references/critical-review.md` — use in Audit mode for design-specific critical appraisal.
- `references/output-contract.md` — use for broad Orient/Learn/Audit outputs and RTL-safe presentation.
- `references/release-gates.md` — use before releasing substantial or full-paper analyses.

Do not load every reference for a narrow question.

## Workflow

### 0. Establish identity, status, and source coverage

Determine when possible:

- exact title and stable identifier;
- document role: primary results, secondary/reanalysis, protocol/plan, method/tool/resource report, evidence synthesis, case report/series, qualitative/mixed-methods report, guideline/consensus, editorial/letter/commentary/position paper, correction/notice, or other;
- relationship to a parent study or related document when relevant;
- publication/status modifier: peer reviewed, preprint/versioned, corrected, expression of concern, or retracted;
- source coverage: full package, main text without all associated material, abstract plus excerpts, abstract only, or metadata only.

Do not trust database `paper_type`, article title, journal label, or section names as final classification. Inspect the actual document content available.

For software/database/resource papers, separate historical claims in the paper from current operational facts. Check current status only when requested or when it materially changes the answer.

### 1. Fingerprint the scientific work

Create a compact multi-label fingerprint only as needed:

- document role and publication type;
- study design;
- scientific domain;
- population/sample/model system or data type;
- experimental level when relevant: in vitro, ex vivo, animal in vivo, human observational/interventional, or in silico;
- analytical approach and validation type;
- status/version modifier.

For secondary analyses, identify the parent study and what is new in the current paper. For protocols, state that the document is plan-bearing. For non-empirical argument papers, identify thesis and evidence rather than inventing experiments.

### 2. Build orientation

Answer compactly:

1. What scientific problem is addressed?
2. What gap or uncertainty motivated the work?
3. What is this document specifically trying to do?
4. What did the authors do, analyze, synthesize, propose, or plan?
5. What is the main result or contribution? For plan-bearing documents, state the planned contribution and that outcomes are not yet reported.
6. Why does it matter within the actual evidence scope?

Surface any caveat that changes the headline meaning now, not later: retraction/correction, preprint status, secondary-analysis status, observational design, restricted model system/dataset, simulated validation, major attrition, or low-certainty synthesis.

### 3. Build the Paper Understanding Graph when useful

Use this semantic spine:

`Problem -> Gap -> Objective -> Approach -> Evidence/Result -> Claim -> Meaning`

Do not force result-bearing nodes into protocols, perspectives, guidelines, or other non-result documents. Use `references/paper-graph.md` for overlays, relations, source anchors, and Evidence Cards.

### 4. Build the Learning Dependency Graph in Learn mode

Identify only concepts that block the next important paper node. Prefer a short prerequisite chain and 3-7 blockers over a glossary dump. Select the smallest concept, figure, method, or result that unlocks the next important layer.

### 5. Traverse only needed paper objects

For each section, method, figure, table, or equation needed by the user, explain:

- what it is;
- why it is there;
- how it connects to the objective;
- what was actually done or observed;
- what must be understood to interpret it;
- what it establishes and what it does not.

For figures, inspect the question, axes/encodings, groups/comparisons, uncertainty, main pattern, and supported claim. For tables, inspect population/data, denominators, groups, effects/uncertainty, missingness when material, and supported conclusion. For equations, unpack variables, units when reported, assumptions, role, scientific meaning, inputs, and downstream use.

Follow important supplementary material before declaring a method or result absent.

### 6. Trace major claims to evidence

For claims material to the user's goal, use an Evidence Card when useful:

- **Claim**
- **Evidence**
- **Source anchor**
- **Evidence layer/type**
- **Relationship:** directly supports / partially supports / indirectly supports / does not establish / contradicts / unclear from available source
- **Scope**
- **Caveat**
- **Certainty** only when the paper or an appropriate evidence-assessment framework explicitly provides one

For secondary analyses, anchor claims to the current paper while distinguishing parent-study evidence. For reviews, distinguish completed synthesis from protocol/planned synthesis. For model/benchmark papers, distinguish technical validation from biological or clinical validation.

### 7. Audit when requested or material

In Audit mode, read `references/critical-review.md` and apply only design-relevant checks. Always ask whether the document/design can answer the stated question, whether sample/data/model provenance fits the claim, whether outcomes/targets/comparators and analysis populations are appropriate, whether uncertainty and validation are interpreted correctly, and whether important bias, leakage, missingness, attrition, confounding, supplement, protocol, code, or data changes the conclusion.

Use reporting guidelines as reporting aids, never as automatic quality scores.

### 8. End with the next useful action

Unless the user requested a complete report, stop after a meaningful unit and state one next best action: learn one blocker, inspect one key figure, unpack one method, trace one claim, or audit one risk.

Do not manufacture quizzes when they interrupt the user's task.

## External information policy

Keep the target paper primary. Use external sources only when they materially help with terminology/prerequisites, version/correction/retraction status, current software/database/resource status, necessary methodological/reporting standards, or novelty/literature context requested by the user.

Label external information. Never make it look as if it came from the target paper.

## Output discipline

Read `references/output-contract.md` before broad Orient, Learn, Audit, or full-analysis outputs. Do not expose internal workflow bookkeeping or print every possible checklist. Surface only what helps the user understand or evaluate the paper.

For Persian and other RTL outputs, do not create mixed-language ASCII trees containing RTL prose and LTR labels inside code fences. Use an English-only diagram plus RTL explanation outside it, or a fully RTL Markdown structure.

## Release gate

For substantial analyses, read and apply `references/release-gates.md`. At minimum, confirm that document identity and source coverage are accurate, major claims are traceable to available evidence, author claims and analyst inferences remain separate, design-specific evidence boundaries are preserved, relevant status/version material was not ignored, and the answer does not claim more source coverage than was actually available.
