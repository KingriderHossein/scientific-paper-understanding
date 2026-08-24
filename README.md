# Scientific Paper Understanding

A ChatGPT Skill for understanding, teaching, mapping, and critically evaluating one scientific paper without reducing it to a generic summary.

## What it does

The Skill first identifies the document role and study design, then builds an evidence-grounded mental model of the paper. It separates author claims, reported results, supported interpretation, analyst inference, and external context.

It includes dedicated guardrails for protocols, secondary analyses, clinical trials, observational studies, prediction and machine-learning studies, qualitative and mixed-methods research, omics and bioinformatics studies, software/resource papers, reviews, corrections, and retractions.

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
│   └── pedagogy.md
└── benchmark/
    └── benchmark-100.md
```

## Skill package

For ChatGPT Skill upload, package the Skill files with `SKILL.md` as the entry point. The benchmark report is development evidence and is not required at runtime.

## Version

Current release: **v1.0.0**

See `CHANGELOG.md` for release notes.

## Benchmark

The current release was stress-tested on 100 real scientific documents across multiple study and document types, with deeper checks on selected high-risk cases. See `benchmark/benchmark-100.md` for scope and limitations of that evaluation.
