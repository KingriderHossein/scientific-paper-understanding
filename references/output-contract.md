# Output Contracts

## Contents

- Status and coverage
- Orient
- Learn
- Audit
- Special document-role outputs
- Full analysis
- Language and RTL/bidirectional formatting

Use these as defaults, not rigid forms.

## Status / Coverage Banner

When material, show a compact status before the main interpretation:
- `Retracted` or `Expression of concern` prominently;
- `Corrected` only with what changed/materiality when known;
- preprint/version status;
- protocol or secondary-analysis identity;
- partial-source coverage such as `abstract + excerpts only`.

Do not clutter ordinary papers with unnecessary metadata.

## Orient

### Identity
Document role / study type / material status.

### In 5-6 Questions
- What problem?
- What gap?
- What is this document specifically doing?
- What did it do/analyze/synthesize/plan?
- What did it find or contribute? For plan-bearing work, what is planned?
- Why does it matter within scope?

Include one material caveat when it changes the headline.

## Learn — First Broad Response

### 1. Paper Identity
Compact fingerprint. Surface protocol/secondary/preprint/correction/retraction/coverage status when material.

### 2. Mental Model
Explain the paper in 5-6 concise answers.

### 3. Paper Map
Use a small semantic flow/tree, not a table-of-contents dump.

### 4. Knowledge Blockers
Normally 3-7 prerequisite-frontier items.

### 5. Next Best Step
One next action and why it unlocks the paper.

Do not automatically continue into a long lesson.

## Learn — Deep Branch

For one concept, section, method, figure, table, or equation:
- what it is;
- why it matters here;
- how it works in this paper;
- what evidence/result it connects to;
- what it does not mean;
- one example/check only if useful.

## Audit

### Executive Assessment
3-6 sentences. No artificial numeric quality score unless the user asks for a scoring rubric.

### Identity and Evidence Boundary
State any document-role/status/coverage issue that changes interpretation.

### Claim-Evidence Core
Use Evidence Cards or a compact table for the important claims.

### Methodological Strengths
Only substantive strengths.

### Interpretation Risks / Limitations
Rank by impact on conclusions.

### Design-Specific Checks
Show only relevant checks.

### Reproducibility / Transparency
Only when relevant.

### Bottom Line
What is well supported, what remains tentative, and what evidence would most change confidence.

## Retracted Paper

Start with the retraction. Do not produce an ordinary positive/negative evidence summary as if current findings are valid. If the user wants to understand the paper historically or inspect why it failed, analyze content under a clear `retracted` boundary.

## Secondary Analysis

State the parent study and the current paper's new question before discussing results. Do not silently import the parent trial's primary conclusions.

## Protocol

Use `planned` language. Never provide a main treatment effect, efficacy/safety result, or completed evidence synthesis that does not exist.

## Full Analysis

When explicitly requested, traverse:
1. identity/status/source coverage;
2. fingerprint;
3. orientation;
4. paper map;
5. prerequisites;
6. section/object walkthrough;
7. claim-evidence matrix;
8. design-specific audit;
9. limitations/alternative explanations;
10. contribution/application;
11. final teach-back mental model.

## Language and Terminology

Use the user's requested language. Preserve model names, genes, packages, metrics, symbols, and other technical identifiers exactly.

### RTL / Bidirectional Text Safety

When the output language is Persian, Arabic, or another right-to-left language, make directionality a formatting requirement, not an afterthought.

1. Start mixed-language prose with the RTL language. Prefer Persian-first wording such as **یادگیری بدون نظارت** (`Unsupervised Learning`). Do not write an English label followed by a colon and then a Persian explanation.
2. Keep short English technical identifiers isolated with inline code when practical: `Random Forest`, `GEM`, `FBA`, gene names, package names, variables, and metrics.
3. Never put Persian/Arabic prose and English node labels together inside the same ASCII-art or fenced-code diagram. Monospace blocks are treated as LTR by many clients and will reorder mixed text.
4. For a diagram in an RTL response, choose one of these two safe forms:
   - **LTR diagram**: keep the diagram entirely English, then explain or translate each node in RTL prose below it.
   - **RTL map**: use Markdown bullets or numbered steps outside a code fence, with the RTL label first and the English term in inline code only when needed.
5. Do not use decorative code fences for Persian prose. Reserve fenced code blocks for actual code, equations/identifiers that require monospace, or English-only ASCII diagrams.
6. In bilingual headings, put the RTL heading first. Example: **یادگیری نظارت‌شده** (`Supervised Learning`).
7. In tables, avoid mixing long RTL and LTR sentences in one cell. When terminology matters, use a separate English-term column or put the RTL explanation first.
8. Keep equations, source code, command lines, file paths, and identifiers LTR. Explain them in a separate RTL sentence instead of appending RTL prose to the same code line.
9. Use Unicode bidi-isolation marks only as a fallback when structural separation and inline code do not render correctly. Prefer visible structural formatting because it is more portable across ChatGPT, Telegram, GitHub, and other clients.
10. Before finalizing, scan every mixed-language line. If it starts with an English label and later contains RTL prose, rewrite it so the RTL phrase comes first or split it into separate lines.

#### Safe Paper Map Pattern for Persian

Use an English-only diagram when a compact flow is useful:

```text
Problem
  ↓
Uncertainty
  ↓
Ensemble of GEMs
  ↓
Gene-knockout simulations
  ↓
Unsupervised learning
  ↓
Supervised learning
  ↓
Important reactions
```

Then explain it in Persian outside the code block:
- مسئله (`Problem`): چرا یک GEM واحد برای این سؤال کافی نیست.
- عدم قطعیت (`Uncertainty`): درباره وجود یا نبود بعضی واکنش‌ها مطمئن نیستیم.
- مجموعه مدل‌ها (`Ensemble of GEMs`): چند مدل سازگار برای نمایش این عدم قطعیت ساخته می‌شود.

If the user wants the map itself fully in Persian, use a normal Markdown list instead of an ASCII tree.
