# Scientific Paper Understanding — 100-Paper Benchmark

**Skill candidate:** `scientific-paper-understanding` v1.0.0  
**Benchmark date:** 2026-08-25  
**Purpose:** stress-test routing, scientific evidence boundaries, status/version handling, adaptive reading logic, and design-specific audit rules before final release.

## What This Benchmark Is

This is a manual source-grounded stress benchmark, not a claim that 100 full peer reviews were completed. The corpus was evaluated using scholarly metadata, abstracts, indexed full-text excerpts when available, publication/status notices, and targeted web verification. Ten high-risk cases received deeper excerpt-level inspection.

The benchmark tests whether the Skill can correctly determine what scientific object is in hand, select the right reading/audit route, preserve the evidence layer, expose status/version problems, and avoid predictable overclaiming.

## Test Gates

Each corpus case was checked for the applicable subset of these gates:

1. document-role identity;
2. study-design routing;
3. source-coverage honesty;
4. version/correction/retraction handling;
5. semantic paper-map fit;
6. claim-to-evidence boundary;
7. evidence-layer/translational boundary;
8. design-specific audit coverage;
9. parent-study/protocol/secondary-analysis relationship when relevant;
10. overclaim prevention;
11. learning/prerequisite route viability;
12. output-friction control.

A case passes the final conformance review when v1.0.0 contains a direct rule for every material stressor identified in that case. This is a specification-level stress test, not an independent behavioral benchmark of another model instance.

## Corpus

### A. Randomized trial and clinical-trial routing — 10

1. `10.1002/ajh.27692` — randomized sickle-cell pain trial; failed primary outcome, secondary/subgroup interpretation, imbalance/confounding risk.
2. `10.1093/ofid/ofae615` — randomized placebo-controlled probiotic trial.
3. `10.1002/cpz1.70423` — randomized-trial **study protocol** returned in a trial search; plan-bearing override required.
4. `10.1371/journal.pmed.1004440` — randomized knee-osteoarthritis trial; null primary result boundary.
5. `10.2196/50855` — digital asthma RCT; per-protocol primary analysis, modified-ITT sensitivity, attrition risk.
6. `10.1681/asn.0000000000000292` — VALOR-CKD randomized trial; treatment contrast/run-in interpretation.
7. `10.2337/dc25-2379` — phase-2 randomized trial in type 1 diabetes.
8. `10.1111/ctr.70370` — prespecified **secondary outcome analysis** of the IronIC RCT; parent-study relationship required.
9. `10.1200/jco.24.00975` — phase-III randomized CLL trial.
10. `10.1200/jco.23.01836` — randomized oncology supportive-treatment trial.

### B. Observational / genre-confusion stress — 10

11. `10.1097/ebp.0000000000002239` — evidence-practice summary returned by observational-topic search; identity before design.
12. `10.1001/jamapediatrics.2024.6848` — prospective childhood cohort; association/causation boundary.
13. `10.1001/jamanetworkopen.2025.44324` — long-follow-up birth cohort; attrition/generalizability.
14. `10.1136/jnis-2026-025026` — observational follow-up study.
15. `10.1093/qjmed/hcae098` — commentary/letter-like object discussing cohort evidence; metadata/title mismatch stress.
16. `10.21203/rs.3.rs-7663149/v1` — Research Square preprint; observational outcome/status handling.
17. `10.1111/apt.17999` — authors' reply/editorial object; do not route as primary study.
18. `10.5603/ep.100762` — prospective longitudinal observational study.
19. `10.1001/jamasurg.2024.1158` — editorial/commentary on intervention evidence; identity stress.
20. `10.3390/jcm14030810` — review article returned by observational-topic search.

### C. Diagnostic / prediction / ML validation — 10

21. `10.1002/alr.70024` — external validation of a diagnostic prediction system.
22. `10.1002/hsr2.72469` — systematic review/meta-analysis of prediction models; review versus model-study routing.
23. `10.1007/s00068-026-03175-8` — TraumaTriage model development plus external validation; calibration and decision-utility stress.
24. `10.1097/md.0000000000038238` — external validation using administrative data.
25. `10.1038/s41598-025-28694-z` — explainable hybrid diagnostic ML system.
26. `10.1136/bmj-2023-074819` — methodology article about prediction-model evaluation; not a primary model-development study.
27. `10.1093/noajnl/vdae157` — externally validated radiomics/ML model.
28. `10.3390/life14060744` — external AI validation with small sample; transportability limits.
29. `10.21203/rs.3.rs-5810875/v1` — preprint systematic review of ML prediction.
30. `10.3390/diagnostics15060686` — external model validation with decision-curve analysis.

### D. Systematic/scoping review and review-protocol routing — 10

31. `10.37766/inplasy2025.12.0066` — scoping-review registration/protocol object.
32. `10.37766/inplasy2025.6.0094` — systematic-review protocol.
33. `10.37766/inplasy2025.6.0059` — planned network-meta-analysis protocol.
34. `10.1097/md.0000000000036897` — systematic review/meta-analysis.
35. `10.1097/md.0000000000036907` — pooled evidence synthesis.
36. `10.37766/inplasy2024.8.0028` — review protocol.
37. `10.12688/f1000research.156907.1` — scoping-review protocol/versioned publication.
38. `10.12688/wellcomeopenres.24335.2` — systematic-review protocol v2; planned narrative synthesis, not completed evidence.
39. `10.1136/bmj.r892` — commentary about evidence synthesis; not a systematic review.
40. `10.1097/opx.0000000000002282` — letter concerning a living systematic review; not the review itself.

### E. Qualitative / mixed methods / protocol / case-logic stress — 10

41. `10.1177/01939459241263011` — scoping review of triangulation in case studies.
42. `10.3233/tad-230024` — narrative review of qualitative/mixed analysis approaches.
43. `10.1101/2025.04.10.25325587` — mixed-methods preprint; explicit triangulation, trial results not yet available.
44. `10.1017/s1463423625100790` — qualitative/proposed-study wording stress.
45. `10.52783/jes.1360` — mixed-methods case-study object.
46. `10.1017/cjn.2024.348` — qualitative interview/survey analysis of clinical management.
47. `10.3389/fmed.2023.1291189` — qualitative thematic-content study.
48. `10.31963/rial.v2i2.4811` — qualitative multiple-case study; cross-domain portability stress.
49. `10.1002/acm2.14313` — qualitative thematic **secondary analysis** of prior survey/task-group work.
50. `10.2196/57596` — international qualitative-study **protocol**.

### F. Animal / in-vitro / ex-vivo model evidence — 10

51. `10.1152/ajpheart.00358.2023` — in-vivo/ex-vivo electrophysiology protocol in a rat disease model.
52. `10.21873/invivo.13538` — rat/mouse bilateral renal ischemia-reperfusion models; animal-to-human boundary.
53. `10.1002/mp.18062` — small-animal irradiation setup for **future** in-vivo experiments; design versus efficacy.
54. `10.1538/expanim.23-0089` — Aspa-knockout rat disease model.
55. `10.1155/term/2583925` — review of ex-vivo organ-perfusion systems.
56. `10.1002/epi4.12941` — review of in-vitro human-cell models.
57. `10.1111/cts.70161` — translational-method review of human plasma/serum cell culture.
58. `10.1101/2024.03.27.586980` — bioRxiv 3D in-vitro assay preprint.
59. `10.18805/ijar.b-5325` — review of in-vitro cell culture.
60. `10.15671/hjbc.1374824` — LUHMES in-vitro oxidative-stress model.

### G. Omics / bioinformatics — 10

61. `10.3390/ijms252312940` — single-cell/multi-omics review.
62. `10.1002/ctd2.70049` — translational perspective on single-cell technology.
63. `10.1038/s41467-024-50194-3` — OmicVerse framework; method/resource claims and simulation limitations.
64. `10.1186/s13059-025-03805-1` — MOADE multi-omics method; correction notice and benchmark-fairness stress.
65. `10.1093/nar/gkae911` — MAPbrain multi-omics atlas/resource.
66. `10.1016/j.csbj.2025.05.008` — DiabetesOmic database/resource.
67. `10.1016/j.xgen.2025.100950` — OmicsTweezer deconvolution method/benchmark.
68. `10.1093/bib/bbaf669` — assessment/review of joint single-cell profiling.
69. `10.3324/haematol.2022.282557` — single-cell multi-omics review.
70. `10.3390/biom14060692` — integrated multi-omics review.

### H. Computational / ML / argumentative-paper routing — 10

71. `10.21203/rs.3.rs-10685167/v1` — 2026 AI-prediction preprint.
72. `10.3390/bioengineering13060683` — biomedical-ML review.
73. `10.3390/bioengineering13060633` — systems-biology/GEM/ML review.
74. `10.3390/biology14101453` — AI/ML biology review.
75. `10.4108/eetel.5256` — general complex-systems/AI article; cross-domain scientific routing.
76. `10.48550/arxiv.2510.25368` — **position paper** on biology-informed ML; thesis/argument route required.
77. `10.1049/syb2.70066` — review of ML for protein-sequence analysis.
78. `10.48550/arxiv.2604.21473` — computational drug-synergy prediction preprint.
79. `10.21203/rs.3.rs-9672899/v1` — explainable-AI/survival-analysis preprint.
80. `10.1088/2632-2153/ae365f` — benchmark study; fair-baseline and benchmark-generalization stress.

### I. Software / resource / benchmark / platform — 10

81. `10.64898/2026.04.28.721523` — BixBench skill-augmented-agent benchmark preprint.
82. `10.1128/mra.01261-25` — QIIME 2/decontam software integration; current-name/version drift.
83. `10.48550/arxiv.2601.12927` — LLM system-building benchmark; tool-use benchmark route.
84. `10.3762/bjnano.15.119` — scientific-computing platform perspective; non-empirical route.
85. `10.1016/j.csbj.2024.04.003` — PS-GO protein search engine.
86. `10.1093/bib/bbaf659` — community biocuration/resource case study.
87. `10.1080/07853890.2024.2382949` — bioinformatics candidate-target analysis; computational versus experimental validation boundary.
88. `10.1101/2025.07.21.665920` — independent benchmark of long-read single-cell/spatial tools; self-benchmark optimism stress.
89. `10.3389/fhpcp.2024.1390709` — Galaxy-based scientific-computing platform paper.
90. `10.3389/fgene.2024.1469011` — m7GRegpred bioinformatics prediction framework.

### J. Publication-integrity/status stress — 10

Corrections:
91. `10.1111/ajsp.70013`
92. `10.1007/s44322-024-00011-y`
93. `10.3389/fopht.2023.1322178`
94. `10.3390/arts13040127`
95. `10.3389/fsoc.2024.1393607`

Retractions:
96. `10.1017/s0080440125000015`
97. `10.1016/j.heliyon.2024.e26218`
98. `10.1111/iwj.14615`
99. `10.1177/14727978251364477`
100. `10.1016/j.heliyon.2024.e24979`

## Ten Deep-Check Exemplars

The following cases received additional excerpt-level inspection beyond basic routing:

1. `10.1002/ajh.27692` — primary outcome not met; secondary/subgroup interpretation and imbalance risk.
2. `10.2196/50855` — per-protocol primary analysis plus modified-ITT sensitivity and attrition caveat.
3. `10.1002/cpz1.70423` — trial protocol despite clinical-trial framing.
4. `10.1111/ctr.70370` — prespecified secondary outcome of parent IronIC trial; primary outcome published elsewhere.
5. `10.1007/s00068-026-03175-8` — external validation with c-statistic, calibration, and decision-curve analysis.
6. `10.1002/acm2.14313` — qualitative thematic secondary analysis; themes require qualitative scope.
7. `10.12688/wellcomeopenres.24335.2` — versioned systematic-review protocol with planned narrative synthesis.
8. `10.1186/s13059-025-03805-1` — correction plus benchmark asymmetry: baseline methods at defaults versus selected/tuned MOADE result.
9. `10.1038/s41467-024-50194-3` — bioinformatics framework with simulation/model limitations and method/resource contributions.
10. `10.1016/j.heliyon.2024.e26218` — retracted ML paper; retraction must override normal evidence presentation.

## Failures Found Before v1.0.0

The 100-paper expansion exposed recurring failures that the 10-paper benchmark did not fully cover:

- scholarly search categories can return protocols, editorials, replies, reviews, books, or secondary analyses;
- document role and study design must be separate fields;
- RCT evidence can be distorted by analysis population, attrition, baseline imbalance, weak treatment contrast, or post-hoc rescue of a failed primary outcome;
- prediction papers require calibration, threshold, validation-independence, leakage, and intended-use checks, not only AUC/accuracy;
- qualitative results require sampling/context/reflexivity/analysis logic and cannot be translated into prevalence;
- review protocols must not be described as completed syntheses;
- mixed-methods studies require actual integration/triangulation, not merely two parallel datasets;
- model-system evidence needs explicit in-vitro/ex-vivo/animal/human/in-silico boundaries;
- computational benchmarks can be unfair when one method is tuned/selected while baselines use defaults;
- omics papers require preprocessing, batch/reference/annotation, multiple-testing, data-reuse, and biological-validation checks;
- corrections need materiality assessment; retractions require evidence invalidation for current use;
- partial text must not be presented as a full-paper review.

Every item above is now represented explicitly in `SKILL.md` or one of the five focused reference files.

## Final Conformance Result

- Corpus size: **100 real scientific papers**.
- Stress strata: **10**.
- Deep-check exemplars: **10**.
- Final cases without an applicable route/guardrail: **0**.
- Official Skill Creator validation: **PASS**.

This result means the final specification has direct handling for all material stressors found in the corpus. It does **not** prove universal correctness on every future paper or behavioral equivalence across every model/runtime.
