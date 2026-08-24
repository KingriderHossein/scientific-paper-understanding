# Paper Understanding Graph

## Contents

- Graph purpose
- Core nodes and relations
- Document relationships/status
- Source anchors and coverage
- Evidence layers
- Claim boundary and scope
- Evidence Cards

The graph is a reasoning model, not a requirement to serialize a formal graph.

## Core Node Types

Use only useful nodes:
- Document / Parent Study / Related Document
- Problem
- Gap
- Question / Objective / Thesis
- Hypothesis
- Concept
- Population / Sample / Study Object / Model System
- Dataset
- Intervention / Exposure / Comparator
- Method / Model
- Experiment / Analysis
- Metric / Outcome / Theme
- Result / Finding
- Evidence
- Claim
- Figure / Table / Equation
- Limitation
- Application / Implication
- External Work
- Protocol / Registration / Supplement
- Version / Correction / Retraction Notice

## Core Relations

Useful relations:
- motivates
- addresses
- tests
- requires
- uses
- applied_to
- measures
- produces
- supports / partially_supports / contradicts
- compared_with
- validated_by
- derived_from
- reported_in / visualized_in
- limited_by
- extends
- secondary_analysis_of
- protocol_for
- correction_of
- retraction_of
- version_of

Do not create edges merely because two concepts are adjacent in text.

## Document Relationships and Status

Represent parent/child relationships when they change interpretation. Examples:

`Secondary paper -> secondary_analysis_of -> Parent RCT`

`Protocol -> protocol_for -> Trial`

`Correction notice -> correction_of -> Paper`

`Retraction notice -> retraction_of -> Paper`

Status is not decoration. A retraction changes whether claims can be used as reliable evidence. A correction requires materiality assessment.

## Source Anchors

Anchor to the smallest useful location:
- `Abstract`
- `Methods - Study population`
- `Results - Figure 2B`
- `Table 1`
- `Supplementary Methods`
- `Protocol - Outcomes`
- `Correction notice`

If only partial sources are available, say so. Useful coverage labels:
- full paper package;
- main text without all associated material;
- abstract plus indexed excerpts;
- abstract only;
- metadata only.

Never create a full-text anchor from an abstract/snippet.

## Evidence Layers

Tag evidence using ordinary scientific meaning, including:
- randomized human comparison;
- human observational association;
- diagnostic/prediction validation;
- qualitative thematic/descriptive evidence;
- in-vitro measurement;
- ex-vivo measurement;
- in-vivo animal experiment;
- simulated/in-silico output;
- benchmark evaluation;
- external validation;
- synthesized/meta-analytic evidence;
- case-level evidence;
- resource coverage/availability evidence;
- planned/protocol statement;
- argumentative/consensus support.

Evidence layers are not interchangeable.

## Claim Boundary

Keep four layers separate:

1. **Author claim** — explicit statement.
2. **Reported result/finding** — measurement, estimate, theme, model output, synthesis, or documented contribution.
3. **Supported interpretation** — what follows reasonably within design limits.
4. **Analyst inference** — additional inference not established by the paper.

## Support Relationships

Use descriptive labels, not invented scores:
- directly supports;
- partially supports;
- indirectly supports;
- does not establish;
- contradicts;
- unclear from available source.

## Scope Tags

State the dimensions that limit generalization:
- document role and analysis status;
- species/model system/experimental level;
- population/eligibility/setting;
- dataset/source/version;
- intervention/exposure;
- outcome/target/time horizon;
- qualitative context;
- simulation/model assumptions;
- validation type;
- publication/version/retraction context.

## Evidence Cards

Use for major claims only.

**Claim:** ...  
**Evidence:** ...  
**Anchor:** ...  
**Layer:** ...  
**Relationship:** ...  
**Scope:** ...  
**Caveat:** ...  
**Certainty:** only if explicitly established.

For secondary analyses, include the relationship to the parent study when it affects interpretation. For protocols, the evidence is the planned design, not an outcome. For retracted papers, the status boundary precedes any historical content analysis.

## Paper Map Construction

Start with the fewest nodes that explain the scientific object. Expand only when useful.

A good map answers:
- What kind of document is this?
- Why does it exist?
- What exactly did it do or plan?
- What evidence/contribution did it produce?
- Which evidence supports which claim?
- What is the strongest boundary on interpretation?
