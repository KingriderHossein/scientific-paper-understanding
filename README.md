# Scientific Paper Understanding

A ChatGPT Skill for understanding, teaching, mapping, and critically evaluating one scientific paper without reducing it to a generic summary.

## What it does

The Skill first establishes the actual document identity, status, source coverage, and study role. It then builds an evidence-grounded mental model of the paper while keeping author claims, reported results, supported interpretation, analyst inference, and external context separate.

Version 1.1.0 adds explicit source-access routing for user-provided PDFs, DOI/URLs, title-only inputs, abstract/excerpt-only coverage, search snippets, versioned/preprint records, and correction/retraction checks. It also moves the detailed release checklist out of `SKILL.md` into a focused runtime reference so the entrypoint remains a control plane.

The Skill includes dedicated guardrails for protocols, secondary analyses, clinical trials, observational studies, prediction and machine-learning studies, qualitative and mixed-methods research, omics and bioinformatics studies, software/resource papers, reviews, corrections, and retractions.

## Repository structure

```text
.
├── SKILL.md
├── CHANGELOG.md
├── README.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── article-types.md
│   ├── critical-review.md
│   ├── output-contract.md
│   ├── paper-graph.md
│   ├── pedagogy.md
│   └── release-gates.md
└── benchmark/
    └── benchmark-100.md
```

## Skill package

For ChatGPT Skill upload, package the runtime Skill files with `SKILL.md` as the entry point and `agents/openai.yaml` as UI metadata. The benchmark report, README, and changelog are repository/development material rather than required runtime context.

## Version

Current release: **v1.1.0**

See `CHANGELOG.md` for release notes.

## Benchmark

The core routing and evidence policies were previously stress-tested on 100 real scientific documents across multiple study and document types, with deeper checks on selected high-risk cases. See `benchmark/benchmark-100.md` for scope and limitations. Version 1.1.0 is primarily an architecture and source-routing refactor; it does not claim a new 100-paper behavioral benchmark.
