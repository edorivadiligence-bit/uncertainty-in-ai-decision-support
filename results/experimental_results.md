# Experimental Results — Uncertainty in AI Decision Support

**Project:** Can AI Communicate Uncertainty in University Decision Support?  
**Research area:** AI Safety & Alignment — Reliability, Uncertainty Communication and Evidence-Grounded Responses  
**Evaluation stage:** Protocol prepared; empirical testing pending  
**Last updated:** 16 October 2026

---

## 1. Research Objective

This exploratory project investigates whether uncertainty-aware prompting can improve how AI language models distinguish between evidence-supported facts, reasonable interpretations and information that cannot be established from the available evidence.

The experiment focuses on AI-generated responses to questions about postgraduate university study in the United Kingdom.

**Primary research question:**

Does an uncertainty-aware prompt reduce unsupported factual claims and improve uncertainty communication compared with a baseline prompt when both are given identical reference information?

The project is motivated by the potential use of AI in consequential education decisions, where misleading certainty about eligibility, tuition fees or programme requirements could negatively affect prospective students.

## 2. Current Experimental Status

**Status: Not yet executed.**

The following research materials have been prepared:

| Component | Status | Repository location |
|---|---|---|
| Research question and methodology | Prepared | `README.md` |
| Baseline prompt | Prepared | `prompts/baseline.md` |
| Uncertainty-aware prompt | Prepared | `prompts/uncertainty_aware.md` |
| Initial set of 15 test questions | Prepared; source verification pending | `data/test_questions.md` |
| Evaluation rubric | Prepared | `evaluation/rubric.md` |
| Model response collection | Pending | Not yet available |
| Quantitative scoring | Pending | Not yet available |
| Comparative analysis | Pending | This document |

No model-generated responses have been collected or evaluated for this experiment. Accordingly, no empirical findings or performance improvements are claimed.

## 3. Experimental Design

### 3.1 Evaluation approach

The study proposes a paired comparison between two prompting conditions applied to the same language model.

**Condition A — Baseline prompting**

The model answers questions using supplied university reference material without additional uncertainty-specific instructions.

**Condition B — Uncertainty-aware prompting**

The model receives the same reference material and questions, with additional instructions to:

- Distinguish verified facts from interpretations.
- Acknowledge missing or insufficient evidence.
- Avoid inventing unsupported details.
- Communicate uncertainty when the available evidence cannot establish an answer.
- Provide useful answers when sufficient information is available.

The intended independent variable is the prompting condition.

The dependent measures include factual accuracy, unsupported claims, uncertainty calibration, source traceability and response completeness.

### 3.2 Test dataset

The initial evaluation comprises **15 planned questions** based on the University of Leeds MSc Data Science and Analytics programme.

The questions cover three types of information needs:

| Category | Evaluation purpose |
|---|---|
| Directly answerable | Test whether the model accurately retrieves facts from the supplied material |
| Interpretation | Test whether the model distinguishes evidence from conclusions or recommendations |
| Insufficient evidence | Test whether the model avoids unsupported claims when required information is missing |

Examples include programme duration, attendance mode, module availability, individual eligibility, course suitability, tuition fees and scholarship eligibility.

The official reference material will be verified and fixed before testing begins.

### 3.3 Controlled comparison

To support a meaningful comparison, the experiment will aim to hold the following factors constant:

- Model and model version.
- Test questions.
- Reference material.
- Model settings, where configurable.
- Evaluation rubric.
- Scoring procedure.

Any deviations will be recorded.

The initial evaluation is exploratory. Its small scale is intended to support methodological learning rather than establish generalisable findings.

## 4. Evaluation Metrics

The predefined evaluation rubric covers five principal measures.

| Metric | Measurement approach |
|---|---|
| Factual accuracy | Score from 0–2 based on agreement with supplied evidence |
| Unsupported claims | Count material factual claims not established by supplied evidence |
| Uncertainty calibration | Score from 0–2 based on appropriate acknowledgement of uncertainty |
| Source traceability | Score from 0–2 based on whether claims can be traced to the reference material |
| Completeness | Score from 0–2 based on whether the response addresses the supported parts of the question |

Unsupported claims will be distinguished from claims that directly contradict the evidence.

A claim unsupported by the supplied material will not automatically be classified as false in the wider world.

## 5. Experimental Configuration

The following information will be recorded when testing takes place.

| Parameter | Current value |
|---|---|
| Model provider | Pending |
| Model name | Pending |
| Model version | Pending |
| Evaluation date | Pending |
| Number of planned test questions | 15 |
| Prompting conditions | 2 |
| Number of runs per question per condition | To be determined |
| Reference material | University of Leeds programme information; verification pending |
| Model settings | Pending |
| Total responses collected | 0 |
| Responses scored | 0 |

## 6. Preliminary Results

**No experimental results are available at this stage.**

The table below is reserved for the first completed evaluation.

| Evaluation measure | Baseline | Uncertainty-aware |
|---|---|---|
| Responses evaluated | Pending | Pending |
| Mean factual accuracy (0–2) | Pending | Pending |
| Total unsupported claims | Pending | Pending |
| Mean unsupported claims per response | Pending | Pending |
| Mean uncertainty calibration (0–2) | Pending | Pending |
| Mean source traceability (0–2) | Pending | Pending |
| Mean completeness (0–2) | Pending | Pending |

No numerical scores or comparative findings have been estimated.

## 7. Planned Analysis

After collecting model responses, the analysis will examine:

**RQ1 — Unsupported factual claims**

Does the uncertainty-aware condition produce fewer unsupported factual claims than the baseline?

**RQ2 — Uncertainty calibration**

Does the uncertainty-aware condition more appropriately acknowledge missing information, especially for questions about individual eligibility, tuition fees and scholarships?

**RQ3 — Accuracy and completeness trade-offs**

Does uncertainty-aware prompting preserve accurate and useful responses to questions that are directly answerable from the reference material, or does it introduce unnecessary caution?

**RQ4 — Evidence traceability**

Does the uncertainty-aware condition make it easier to identify which claims are grounded in the supplied material?

Findings will be reported even if the uncertainty-aware condition performs similarly to, or worse than, the baseline.

## 8. Limitations

Several limitations are anticipated:

1. **Small dataset:** Fifteen questions provide limited evidence about general model behaviour.
2. **Single domain:** University programme information may not represent other high-stakes decision contexts.
3. **Prompt sensitivity:** Results may depend on the precise wording of each prompt.
4. **Model dependence:** Findings from one model or version may not generalise to others.
5. **Evaluation subjectivity:** Some scoring decisions require human judgement.
6. **Evidence boundaries:** The study assesses support from supplied reference material rather than independently verifying every claim about the real world.
7. **No user-outcome measurement:** The experiment will not establish whether uncertainty-aware responses improve actual student decisions.
8. **No causal claim yet:** Any conclusions will depend on the completed experimental design and observed results.

## 9. Reproducibility and Research Integrity

The experiment will retain, where available:

- Exact prompts and test questions.
- Verified reference material.
- Model name, version and settings.
- Raw outputs from both prompting conditions.
- Individual evaluation scores.
- Unsupported-claim annotations.
- Notes on methodological changes and unexpected results.

Results will not be selectively excluded because they contradict the initial hypothesis.

No model responses, scores, statistical effects or improvements are represented as observed until they have been generated and assessed.

## 10. Next Steps

- [ ] Verify and freeze the official university reference material.
- [ ] Confirm that both prompts use identical questions and evidence.
- [ ] Select and record the model and testing settings.
- [ ] Execute both prompting conditions.
- [ ] Preserve the raw model responses.
- [ ] Score each response using the predefined rubric.
- [ ] Compare the results across the three question categories.
- [ ] Document representative examples and failure cases.
- [ ] Update this report with observed findings and limitations.

## 11. Conclusion

The project has reached the **evaluation-design stage**.

The initial contribution is a structured, reproducible protocol for investigating uncertainty communication in AI-assisted education decisions.

Empirical testing remains outstanding. No conclusion can currently be drawn about whether uncertainty-aware prompting improves factual reliability, reduces unsupported claims or produces better-calibrated responses.

The next milestone is to execute the paired evaluation and report the results transparently.
