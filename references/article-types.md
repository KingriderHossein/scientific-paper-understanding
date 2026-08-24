# Article-Type Routing

## Contents

- Identity before design
- Core map
- Primary, secondary, protocol, and non-empirical roles
- Experimental and observational overlays
- Qualitative and mixed-methods overlays
- Prediction/ML and computational overlays
- Method/software/resource overlays
- Evidence-synthesis overlays
- Case, guideline, and status modifiers
- Unusual documents

## Identity Before Design

First classify **what document this is**, then classify the underlying study design.

Common document roles:
- primary-results report;
- secondary/subgroup/post-hoc/reanalysis report;
- study protocol or review protocol;
- method/software/benchmark paper;
- database/resource/web-server paper;
- systematic/scoping/narrative review or meta-analysis;
- case report/case series;
- qualitative or mixed-methods report;
- guideline/consensus/reporting statement;
- perspective/position/commentary/editorial/letter/reply;
- correction/erratum/expression/retraction notice.

A document can mention an RCT or cohort without being the primary report. Do not trust database labels or titles alone.

## Core Map

Use only nodes that exist:

`Problem -> Gap -> Objective -> Approach -> Evidence/Contribution -> Claim -> Meaning`

## Primary Results vs Secondary Analysis

For a primary-results report, map the prespecified main question and primary outcomes.

For a secondary/subgroup/reanalysis paper, add:

`Parent study -> Original data/intervention -> Current secondary question -> Current analysis -> Current result -> Scope`

State whether the secondary question was prespecified when known. Do not attribute the parent study's primary result to the secondary paper or treat exploratory/post-hoc findings as confirmatory without support.

## Study Protocol / Review Protocol

Add:

`Rationale -> Objective -> Planned population/data -> Planned intervention/exposure/search -> Planned outcomes -> Sample/eligibility -> Planned analysis -> Registration/version/amendments`

Do not create observed effects, recruitment success, harms, or synthesis results. For review protocols, distinguish the planned evidence synthesis from a completed review.

## Randomized Controlled Trial

Add:

`Population -> Intervention -> Comparator -> Randomization -> Primary outcome -> Analysis population -> Effect + uncertainty -> Harms -> Follow-up`

Inspect when available:
- baseline balance and any important chance imbalance;
- allocation/blinding;
- ITT/mITT/per-protocol definitions;
- attrition/missing outcomes;
- adherence and whether intervention groups actually separated on the intended exposure;
- run-in periods or enrichment;
- multiplicity and early stopping;
- adverse events;
- protocol/registration deviations;
- whether an unsupported primary outcome is being overshadowed by secondary/subgroup/post-hoc findings.

No significant difference is not equivalence unless the design and margin support that inference.

## Observational Study

Add:

`Population -> Time zero -> Exposure -> Outcome -> Confounders -> Analysis -> Association -> Sensitivity/robustness -> Bias/generalizability`

Guard against:
- reverse causation;
- residual/unmeasured confounding;
- immortal-time or survivor bias where relevant;
- selection and loss-to-follow-up bias;
- exposure/outcome measurement error;
- missing/self-reported data;
- causal language not supported by design.

## Qualitative Study

Add:

`Question -> Sampling/context -> Data collection -> Researcher role/reflexivity -> Analysis/coding -> Themes/findings -> Supporting quotations/examples -> Interpretation -> Transferability limits`

Inspect:
- sampling logic and context;
- interview/focus-group/observation procedures;
- coding/analysis method;
- reflexivity and researcher influence when relevant;
- saturation/information power only if claimed/used;
- negative/divergent cases and triangulation when relevant.

Themes describe patterns/meaning in the sampled data. Do not turn them into population prevalence.

## Mixed-Methods Study

Map each component separately, then add:

`Qualitative strand <-> Integration/triangulation <-> Quantitative strand`

Ask whether integration occurs at design, analysis, or interpretation. Two parallel analyses are not automatically a meaningful mixed-methods integration.

## In-Vitro / Ex-Vivo / Animal Experimental Study

Add:

`Model system/species -> Manipulation -> Controls -> Measurement -> Result -> Replication -> Translational boundary`

Tag the experimental level explicitly when it matters. A disease model, cell line, organ perfusion system, or animal phenotype can support mechanism/model validity without establishing human clinical benefit.

For animal studies, inspect randomization/blinding/sample-size rationale and exclusions when relevant.

## Computational / Mechanistic Modeling

Add:

`Scientific problem -> Model assumptions -> Input/parameter provenance -> Constraints/boundary conditions -> Computation/simulation -> Output -> Sensitivity/validation -> Interpretation`

Keep simulated output distinct from measured biology.

## Machine Learning / Prediction

Add:

`Intended prediction task -> Target/ground truth -> Data provenance -> Split unit/strategy -> Preprocessing/features -> Training/tuning -> Comparator -> Evaluation -> Calibration/thresholds -> External validation -> Intended-use limits`

Inspect:
- leakage and related/duplicate samples;
- preprocessing/feature selection fitted inside training data only;
- site/time/patient-level independence;
- class imbalance;
- discrimination and calibration as appropriate;
- threshold-dependent sensitivity/specificity/PPV/NPV;
- decision utility when clinical use is claimed;
- external validation and population shift;
- fair baselines and ablations.

AUC/accuracy alone is not clinical utility.

## Diagnostic Accuracy Study

Add:

`Target condition -> Index test/model -> Reference standard -> Spectrum/population -> Threshold -> Sensitivity/specificity + uncertainty -> Clinical setting`

Check verification/reference-standard bias and whether thresholds were prespecified or optimized on the same data.

## Method / Software / Benchmark Paper

Add:

`Pain point -> Proposed method -> Assumptions -> Implementation -> Benchmark data -> Baselines -> Metrics -> Robustness/failure cases -> Availability`

For independent benchmarks, inspect ground truth, dataset diversity, parameter fairness, runtime/resource constraints, and whether authors benchmark their own method versus independent tools.

Method performance supports method claims, not automatically new biological claims.

## Omics / Bioinformatics Method or Analysis

Additionally inspect:
- raw-data provenance and sample independence;
- preprocessing/QC;
- normalization and batch effects;
- annotation/reference choice;
- multiple testing where relevant;
- feature-selection leakage;
- simulated versus real-data benchmark;
- biological/experimental validation of computational candidates;
- code/data/version availability.

## Database / Resource / Web-Server Paper

Add:

`Resource purpose -> Source data -> Coverage -> Processing/QC -> Annotation/confidence -> Access/API -> Update/version policy -> Use cases -> Limitations`

Operational facts age. Separate publication-time facts from current status.

## Systematic Review / Meta-Analysis

First determine whether the document is a **completed review** or a **review protocol**.

For completed reviews add:

`Review question -> Search date/sources -> Eligibility -> Included studies -> Risk of bias -> Synthesis -> Effect/summary -> Heterogeneity -> Certainty -> Claim`

For network meta-analysis also inspect network connectivity, direct/indirect evidence, transitivity, inconsistency, rankings, and certainty per comparison.

For scoping reviews, do not force pooled-effect logic. Map scope, search, inclusion, charting, and descriptive/thematic synthesis.

## Narrative Review / Perspective / Position Paper

Add:

`Scope/problem -> Thesis -> Evidence/arguments -> Counterarguments/uncertainty -> Author interpretation -> Implications`

Do not invent experiments or treat narrative selection as systematic synthesis.

## Case Report / Case Series

Add:

`Presentation -> History -> Work-up -> Key finding -> Management/intervention -> Course -> Outcome -> Interpretation -> Alternative explanations -> Case-level limits`

Do not infer prevalence, comparative efficacy, population risk, or general causality.

## Guideline / Consensus / Reporting Statement

Add:

`Problem/scope -> Development process -> Evidence/consensus inputs -> Recommendations/items -> Intended users -> Update policy -> Limits`

Recommendation strength and evidence basis can differ. Consensus is not experimental confirmation.

## Status Modifiers

### Preprint / Versioned Publication

Surface version/date when material and peer-review state. Do not assume an older version is current when a newer version is known.

### Correction / Erratum

Use the corrected content when possible. State what changed and whether the change is material to the user's question. A correction does not automatically invalidate the paper.

### Expression of Concern

Surface prominently. Explain that reliability is under question and avoid stronger certainty than the notice permits.

### Retraction

Surface before scientific interpretation. Do not use the retracted findings as reliable current evidence. If the user wants historical/content analysis, proceed with a clear retraction boundary and inspect the notice reason when available.

## Unusual or Non-Paper Scientific Documents

If the source is a book/chapter/manual, conference item, editorial notice, or other non-paper object, label it correctly. Do not pretend it is a research paper. If the user's goal still makes sense, adapt the semantic map to the object's function.
