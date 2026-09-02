# Release Gates

Use this checklist for substantial Orient, Learn, Audit, or full-paper outputs. Apply only checks that are relevant to the document role, design, evidence layer, and source coverage. A failed material gate must be fixed or surfaced as a limitation before release.

## Identity and source coverage

- Identify the actual document role from the document, not only from database metadata, title, journal label, or search result type.
- Do not confuse a primary-results paper with a protocol, secondary analysis, subgroup/post-hoc analysis, editorial, reply, review, correction, or retraction notice.
- State source coverage accurately: full package, main text without all associated material, abstract plus excerpts, abstract only, or metadata only.
- Do not call an abstract-only or excerpt-only analysis a full-paper audit.
- Check relevant supplements, appendices, protocols, registrations, corrections, expressions of concern, retractions, and newer versions when they can change interpretation.
- Treat retraction as overriding normal evidence use. Assess correction materiality instead of treating every correction as a retraction.

## Claim and evidence boundaries

- Do not fabricate missing methods, results, sample details, status, code/data availability, or author intent.
- Keep author statements, reported results, supported interpretation, analyst inference, and external context distinct.
- Keep `not reported`, `not found in available sources`, and `not done` distinct.
- Trace major conclusions to the available paper evidence.
- Match causal language to design.
- Do not call `no significant difference` equivalence unless an appropriate equivalence or non-inferiority design supports that interpretation.
- Do not silently rescue an unsupported primary outcome with exploratory secondary, subgroup, or post-hoc findings.

## Study- and evidence-specific gates

- For randomized trials, inspect analysis population, attrition, treatment contrast/adherence, harms, and primary-versus-exploratory outcomes when material.
- For observational studies, keep confounding and association limits visible.
- For prediction/diagnostic studies, do not reduce evaluation to AUC/accuracy when calibration, thresholds, prevalence, split unit, leakage, or external validation matter.
- For qualitative research, do not convert themes into prevalence or population-frequency claims.
- Keep in-vitro, ex-vivo, animal, in-silico, and human evidence levels distinct.
- For method/ML/benchmark papers, do not convert technical benchmark performance into biological or clinical validation. Check benchmark fairness, leakage, parameter tuning, dataset provenance, and external validation when relevant.
- For omics/bioinformatics studies, inspect preprocessing, batch effects, annotation/reference choices, sample independence, multiple testing, benchmark design, and biological validation when material.
- For reviews/meta-analyses, preserve risk-of-bias, heterogeneity, and evidence-certainty context when available.
- Keep protocols and review protocols as planned evidence until observed results are reported.
- Keep case reports and case series at case-level evidence.

## Reproducibility and external context

- Do not infer code, data, repository health, or reproducibility from silence.
- Label external information as external context and do not present it as content from the target paper.
- For software/database/resource papers, separate historical claims in the publication from current operational status.

## Output integrity

- Respect the user's requested scope; do not force a full audit for a narrow question.
- Preserve important uncertainty and limitations near the claim they constrain.
- For Persian and other RTL outputs, apply the bidirectional-text rules in `output-contract.md`; do not mix RTL prose with LTR labels inside decorative ASCII/code-block diagrams.
- Keep the final response no longer than needed for the user's goal.
