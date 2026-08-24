# Changelog

This file records product-level changes to the Skill. Version numbers follow semantic-versioning intent.

## [1.0.0] - 2026-08-25

### Added
- Identity-first routing that separates document role from study design.
- Explicit primary-results versus secondary/subgroup/post-hoc/reanalysis handling, including parent-study relationships.
- Source-coverage states: full package, main text without all associated material, abstract plus excerpts, abstract only, and metadata only.
- Retraction-first handling: retracted findings are not presented as reliable current evidence.
- Correction-materiality handling that distinguishes corrections/errata from retractions.
- Qualitative and mixed-methods overlays, including theme-versus-prevalence boundaries and integration/triangulation checks.
- Experimental-level routing for in-vitro, ex-vivo, animal in-vivo, human, and in-silico evidence.
- Diagnostic/prediction audit for ground truth, split unit, leakage, discrimination, calibration, thresholds, prevalence effects, external validation, and decision utility.
- RCT checks for analysis population, baseline imbalance, attrition, treatment contrast/adherence, run-in periods, harms, and primary-versus-exploratory outcomes.
- Review-protocol versus completed-review routing.
- Perspective/position/editorial/letter routing that maps thesis and evidence instead of inventing empirical results.
- Bioinformatics/omics checks for preprocessing, batch effects, annotation/reference choice, multiple testing, sample independence, benchmark fairness, and biological validation.
- Non-paper-object guardrail for books/manuals/notices returned by noisy scholarly retrieval.
- Evidence-literacy blockers in the learning graph when the learner's main problem is interpreting evidence rather than terminology.

### Changed
- Fingerprinting now begins with document role, then study design and evidence layer.
- Paper graph now supports `secondary_analysis_of`, `protocol_for`, `correction_of`, `retraction_of`, and `version_of` relationships.
- Source anchors and output contracts now expose partial-source coverage when it limits interpretation.
- Method/software benchmarking now checks parameter and hyperparameter fairness rather than assuming default-versus-tuned comparisons are fair.
- Systematic-review routing now treats review protocols as plan-bearing documents and scoping reviews as descriptive/synthesis objects rather than forced meta-analyses.
- Final release gates now block rescue of an unsupported primary outcome by exploratory secondary/subgroup/post-hoc findings.

### Fixed
- Prevents a database `paper_type`, title, or journal label from overriding the actual document role.
- Prevents a protocol found in a clinical-trial search from being described as completed trial evidence.
- Prevents an RCT secondary analysis from being described as the trial's primary results report.
- Prevents qualitative themes from being interpreted as population prevalence.
- Prevents AUC/accuracy from being treated as sufficient evidence of calibration, clinical utility, or transportability.
- Prevents corrected papers from being treated as automatically invalid and retracted papers from being treated as valid evidence.
- Prevents animal, in-vitro, ex-vivo, and in-silico findings from silently crossing the human-clinical evidence boundary.
- Prevents a method's tuned result from being compared uncritically against baseline tools run only at defaults.

### Evaluation
- Expanded the empirical stress corpus from 10 to 100 real scientific papers/documents across 10 strata: randomized trials, observational studies, prediction/diagnostic studies, evidence syntheses, qualitative/protocol/case studies, animal/in-vitro studies, omics/bioinformatics, computational/ML, software/resource/benchmark papers, and correction/retraction status cases.
- Replaced one non-paper retrieval false-positive with a genuine animal-model paper so the final corpus contains 100 papers.
- Performed a routing/status/evidence-boundary stress review on all 100 cases.
- Performed deeper excerpt-level checks on 10 high-risk exemplars covering RCT analysis populations/attrition, failed-primary-outcome rescue risk, protocol identity, secondary analysis, external prediction validation, qualitative secondary analysis, review protocol, corrected multi-omics benchmarking, bioinformatics method limitations, and retracted ML evidence.
- All 100 final cases have an explicit applicable route and evidence/status guardrail in v1.0.0 after the benchmark-driven revisions.
- The Skill passes the official Skill Creator validator.

### Evaluation Limits
- The 100-paper benchmark is a manual, source-grounded stress test of routing, evidence boundaries, and analysis policy. It is not 100 independent blinded full-text peer reviews.
- Full text/supplements were not uniformly available for every corpus item; the benchmark therefore preserves source-coverage labels rather than claiming full-paper audit where only abstracts/indexed excerpts were accessible.
- Cross-model behavioral equivalence on Claude, Qwen, and DeepSeek remains unverified; the core remains structurally vendor-neutral.

## [1.0.0-rc.2] - 2026-08-25

### Added
- Study-protocol, case-report, guideline/consensus, and unusual-genre routing.
- Function-first fallback for nonstandard scientific objects.

### Changed
- Orientation became plan-aware instead of requiring a result for every paper.
- Architecture was reduced to a compact portable Skill with five focused reference files.

### Evaluation
- Manual benchmark expanded to 10 heterogeneous papers before the 100-paper final benchmark.

## [1.0.0-rc.1] - 2026-08-25

### Added
- Paper-package intake, version/correction checks, evidence cards, article-type overlays, preprint/version rules, resource freshness, and supplement-aware analysis.

### Changed
- Replaced earlier overengineered multi-graph/agent architecture with Paper Understanding Graph + Learning Dependency Graph and three modes: Orient, Learn, Audit.

## [0.1.0-alpha.1] - 2026-08-25

### Added
- Initial dual-graph design.
- Orient, Learn, Audit modes.
- Paper Understanding Graph.
- Learning Dependency Graph.
