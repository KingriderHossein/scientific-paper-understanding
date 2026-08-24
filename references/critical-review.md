# Critical Review

## Contents

- Universal audit
- Status and document-role audit
- Randomized and observational studies
- Qualitative and mixed methods
- Experimental model systems
- Prediction/diagnostic/ML
- Computational and bioinformatics studies
- Evidence synthesis
- Method/software/resource papers
- Protocols, cases, and non-empirical documents
- Epistemic guardrails

Audit only dimensions that can change interpretation.

## Universal Audit

1. Is the actual document role identified correctly?
2. Can this design/document answer the stated objective?
3. Are population/sample/data/model-system provenance and inclusion/exclusion appropriate?
4. Are outcomes, targets, comparisons, ground truth, and analysis populations appropriate?
5. Are uncertainty, missingness, and validation interpreted correctly?
6. Do author conclusions exceed evidence scope?
7. Do protocol, supplement, registration, correction/status, code, or data materially change interpretation?
8. Are important limitations distinguished from mere reporting omissions?
9. Is the paper's contribution separated from parent-study or external evidence?
10. Does the response reflect the actual source coverage available?

## Status and Document Role

Before methodological scoring:
- verify whether the object is primary results, secondary analysis, protocol, review protocol, letter/editorial/reply, correction notice, or other;
- identify parent study/data source for secondary analyses;
- check correction/erratum/expression/retraction status when possible;
- for retractions, do not continue as though evidence is valid;
- for corrections, assess materiality instead of treating every correction as fatal.

## Randomized Trials

Inspect:
- sequence generation/allocation concealment when available;
- blinding and feasibility;
- prespecified primary outcome and time point;
- analysis population: ITT, modified ITT, per-protocol, as-treated;
- attrition and missing outcomes;
- baseline imbalances that can matter even after randomization;
- adherence, crossover, treatment fidelity, and whether groups separated on the intended exposure;
- run-in/enrichment periods;
- early stopping/interim analysis;
- multiplicity;
- absolute and relative effects with uncertainty when useful;
- harms/adverse events;
- registration/protocol deviations;
- whether exploratory secondary/subgroup/post-hoc findings are being used to rescue an unsupported primary outcome.

A null superiority result is not equivalence. A secondary analysis of an RCT is not the same evidentiary object as the primary trial report.

CONSORT 2025 is current general reporting guidance for randomized-trial results; SPIRIT 2025 applies to randomized-trial protocols. Reporting completeness is not risk of bias.

## Observational Studies

Inspect:
- cohort/case-control/cross-sectional design fit;
- time zero and temporal ordering;
- participant selection/representativeness;
- exposure and outcome measurement;
- confounder selection/residual confounding;
- reverse causation;
- immortal-time, survivor, or referral bias when plausible;
- loss to follow-up and missing data;
- model assumptions and sensitivity analyses;
- generalizability and causal wording.

STROBE is reporting guidance, not a quality score.

## Qualitative Studies

Inspect:
- research question and qualitative approach fit;
- sampling strategy and context;
- data collection procedures;
- researcher position/reflexivity when material;
- transcription/coding/analysis process;
- triangulation, multiple coders, negative cases, or audit trail when relevant;
- saturation/information power only when authors invoke them;
- adequacy of quotations/examples supporting themes;
- transferability limits.

Do not turn themes into frequencies, prevalence, effect sizes, or population estimates. COREQ/SRQR can aid reporting review but do not replace methodological judgment.

## Mixed Methods

Inspect each strand with the appropriate rules, then assess:
- why mixed methods were needed;
- where integration occurs;
- whether findings converge, complement, or conflict;
- whether one strand is being overused to support a claim it cannot establish.

## In-Vitro, Ex-Vivo, and Animal Studies

Inspect:
- model/system/species appropriateness;
- controls, randomization/blinding when relevant;
- biological/technical replicates and exclusions;
- dose/exposure/context realism;
- outcome measurement;
- whether model phenotype maps to the human/biological phenomenon claimed;
- translational boundary.

For in-vivo animal research, ARRIVE 2.0 is reporting guidance. Never convert animal/model-system efficacy directly into human clinical efficacy.

## Prediction / Machine Learning

Inspect:
- exact task, intended use, prediction horizon, and target/ground truth;
- data provenance and temporal cutoff;
- split unit: patient/sample/site/time/family/sequence relatedness;
- train/tune/test separation;
- leakage from preprocessing, feature selection, normalization, augmentation, or duplicates;
- class imbalance and prevalence;
- comparator/baseline fairness;
- hyperparameter/model selection;
- discrimination and calibration for risk prediction;
- threshold-specific performance where decisions use thresholds;
- PPV/NPV dependence on prevalence when relevant;
- external validation/generalization;
- decision-curve/net-benefit evidence when clinical utility is claimed;
- subgroup/fairness only when relevant to intended use;
- code/model/data availability.

For clinical prediction, TRIPOD+AI is current reporting guidance. AUC/accuracy alone does not establish calibration, clinical utility, or transportability.

## Diagnostic Accuracy

Inspect:
- patient spectrum and setting;
- index test and reference standard;
- independence/blinding between index and reference assessment;
- missing/indeterminate results;
- threshold prespecification versus optimization;
- sensitivity/specificity and uncertainty;
- clinical consequences of threshold choice.

## Computational / Mechanistic Modeling

Inspect:
- model assumptions and scope;
- parameter/constraint provenance;
- boundary/initial conditions;
- sensitivity/uncertainty analysis;
- identifiability when relevant;
- held-out/external/experimental validation;
- whether model outputs are overinterpreted biologically;
- code/model/data reproducibility.

## Bioinformatics / Omics Analysis

Additionally inspect:
- raw-data and metadata provenance;
- biological versus technical replication;
- QC/exclusions;
- normalization and batch correction;
- reference genome/database/version and annotation choices;
- multiple testing and effect size;
- sample independence and leakage;
- data reuse between discovery and validation;
- simulated/pseudo-bulk versus real biological data;
- experimental validation of computational candidates;
- workflow/software versions and availability.

## Method / Software / Benchmark Papers

Inspect:
- intended data regime and assumptions;
- benchmark ground truth;
- dataset diversity and representativeness;
- baseline choice and parameter/hardware fairness;
- self-benchmark versus independent benchmark;
- simulation versus real-data evidence;
- robustness/failure cases and ablation;
- runtime/resource tradeoffs when relevant;
- code/version/dependencies and reproducibility;
- whether performance evidence is being mistaken for biological/clinical validation.

## Database / Resource Papers

Inspect:
- source-data provenance/coverage;
- processing/QC and confidence metadata;
- update/version policy;
- API/download/access mechanisms;
- coverage gaps;
- sustainability/maintenance where relevant;
- whether current operational facts differ from publication-time claims.

## Systematic Reviews / Meta-Analyses

First determine completed review versus protocol.

For completed reviews inspect:
- question and eligibility;
- search sources/date and unpublished evidence where relevant;
- screening/data extraction;
- protocol/registration and deviations;
- risk-of-bias assessment;
- synthesis model/effect measure;
- heterogeneity/inconsistency;
- publication bias/small-study effects when applicable;
- certainty of evidence;
- whether conclusions preserve uncertainty.

For network meta-analysis inspect transitivity, network connectivity, direct/indirect evidence, inconsistency, ranking interpretation, and certainty per comparison.

PRISMA 2020 is reporting guidance, not a methodological quality instrument.

## Protocols

Inspect prespecification, feasibility, outcomes, sample-size rationale, randomization/blinding where applicable, analysis/missing-data plans, registration/version/amendments, ethics, and data-sharing plans. Do not audit unobserved efficacy/safety as if results exist.

## Case Reports / Series

Inspect chronology, diagnostic work-up, alternative explanations, confirmation of genomic/lab findings where relevant, intervention-outcome sequence, and scope. Case-level evidence can generate hypotheses or demonstrate feasibility; it does not estimate population effects.

## Perspective / Position / Editorial / Letter

Audit the thesis and argument rather than inventing a study design:
- what proposition is advanced;
- what evidence is selected;
- whether counterevidence is represented;
- where opinion/interpretation begins;
- whether recommendations exceed the evidence base.

## Epistemic Guardrails

Never silently convert:
- association -> causation;
- statistical significance -> scientific/practical importance;
- no significant difference -> equivalence;
- qualitative theme -> prevalence;
- model prediction -> observed biology;
- benchmark performance -> universal real-world performance;
- internal validation -> external validation;
- preprint -> peer-reviewed evidence;
- planned protocol -> observed result;
- secondary analysis -> primary trial result;
- single case -> population effect;
- animal/in-vitro/ex-vivo result -> human efficacy;
- missing report -> missing procedure;
- reporting-checklist adherence -> low risk of bias;
- corrected article -> retracted article;
- retracted article -> reliable current evidence.
