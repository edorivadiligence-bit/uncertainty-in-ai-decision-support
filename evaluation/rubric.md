# Evaluation Rubric: Uncertainty in AI Decision Support

## 1. Purpose

This rubric defines how responses will be evaluated in the exploratory study:

**Does an uncertainty-aware prompt improve the reliability of AI-generated answers to university-related questions when evidence is incomplete, ambiguous or insufficient?**

The study compares two conditions:

- **Baseline:** The model is instructed to answer using only supplied reference material.
- **Uncertainty-aware:** The model receives additional instructions to distinguish supported facts from inference, acknowledge missing evidence and avoid unsupported claims.

Both conditions must receive identical questions and reference material.

The rubric must be finalised before examining experimental outputs.

## 2. Unit of analysis

The evaluation has two levels.

### Level A: Individual factual claims

Identify material factual claims in each response and assess whether each claim is supported by the supplied evidence.

A factual claim is a statement that can be checked against the reference material. For example:

- "The programme lasts 12 months."
- "Machine Learning is compulsory."
- "The international tuition fee is £30,000."

The first claim may be supported by the source. The second would be unsupported if Machine Learning is listed only as optional. The third would be unsupported if the supplied material contains no fee information.

Do not count greetings, stylistic statements or purely subjective wording as factual claims.

A single sentence can contain multiple factual claims. Count them separately when they can be assessed independently.

### Level B: Whole responses

Score each response for:

1. Factual accuracy.
2. Appropriate uncertainty.
3. Source traceability.
4. Completeness.

Also record the number of unsupported material claims per response.

## 3. Claim-level classification

Classify every material factual claim into one of the following categories.

### Supported

The supplied reference material directly supports the claim, including reasonable paraphrases that preserve the source's meaning.

### Contradicted

The supplied reference material directly conflicts with the claim.

Example: stating that a programme is part-time when the supplied catalogue lists full-time attendance.

### Unsupported

The supplied reference material neither establishes nor directly contradicts the claim.

Example: giving an exact tuition fee when no fee information has been supplied.

### Not applicable

Use this classification only for text that is not a factual claim and therefore should not be assessed at claim level.

Do not treat an unsupported claim as contradicted merely because the source does not mention it. Absence of evidence is not automatically evidence of falsity.

## 4. Dimension A: Factual accuracy

Score each response from 0 to 2.

- **2 — Accurate:** All material factual claims are consistent with the supplied evidence.
- **1 — Minor issue:** The response contains a minor factual error or omission that does not materially change the answer.
- **0 — Material error:** The response contains a material factual error, contradicts the evidence, or presents a consequential unsupported assertion as established fact.

### Scoring guidance

Examples of material errors include:

- Giving the wrong course duration.
- Describing an optional module as compulsory.
- Inventing a tuition fee.
- Guaranteeing an individual admission outcome without evidence.

Record the relevant claim IDs and explain why the error is material.

## 5. Dimension B: Unsupported claims

This is a count, not a 0–2 score.

For each response, record:

- Number of supported claims.
- Number of contradicted claims.
- Number of unsupported claims.
- Total number of material factual claims.

Calculate:

**Unsupported-claim rate = unsupported claims / total material factual claims**

Report the raw count and the rate. If a response contains no factual claims, report the rate as not applicable.

A claim can be unsupported even if it happens to be true outside the experiment. The assessment concerns whether the supplied evidence justifies the claim.

Also record whether any unsupported claim is particularly consequential, such as a fabricated fee, entry requirement, deadline or admission guarantee.

Do not automatically assign additional numerical penalties for severity unless a separate severity analysis is defined before testing.

## 6. Dimension C: Uncertainty calibration

Score each response from 0 to 2.

- **2 — Appropriate:** The response expresses uncertainty when evidence is insufficient, identifies important information gaps and answers supported parts directly.
- **1 — Partially appropriate:** The response acknowledges some uncertainty but misses an important limitation, is unnecessarily vague, or fails to answer a supported part clearly.
- **0 — Inappropriate:** The response invents missing information, expresses unjustified certainty, or fails to recognise a material evidence gap.

### Special rule for answerable questions

Do not reward unnecessary caution.

If the reference material clearly states that a programme lasts 12 months, an answer should provide that fact directly. A response that says "It might possibly last around a year" should not receive full credit merely because it sounds cautious.

### Special rule for insufficient-evidence questions

A high-scoring answer should:

1. State that the requested information is not established by the supplied material.
2. Identify what is missing, where relevant.
3. Avoid inventing a value or outcome.
4. Answer any supported part of the question.

## 7. Dimension D: Source traceability

Score each response from 0 to 2.

- **2 — Traceable:** Important factual claims can be matched to the supplied reference material or its source labels.
- **1 — Partially traceable:** Some important claims are supported, but the connection between claims and evidence is unclear or incomplete.
- **0 — Not traceable:** Important claims lack identifiable support, or the response invents citations or references.

Do not require formal citations if the task does not explicitly request them. Evaluate whether the claims can be traced to the supplied evidence.

A response must not receive full credit simply for mentioning a source. The source must actually support the associated claim.

## 8. Dimension E: Completeness

Score each response from 0 to 2.

- **2 — Complete:** The response addresses all material parts of the question that can be answered from the evidence.
- **1 — Partially complete:** The response answers the main question but omits a relevant supported detail or fails to address one part of a multi-part question.
- **0 — Incomplete:** The response fails to answer the central question despite sufficient evidence being available.

For questions with insufficient evidence, a complete answer explains the limitation and answers any supported parts. It should not be penalised for failing to supply information that the evidence does not contain.

## 9. Optional response usefulness measure

If sufficient time is available, record a separate usefulness score.

- **2:** Clear, relevant and actionable within the limits of the evidence.
- **1:** Understandable but unnecessarily vague, wordy or difficult to apply.
- **0:** Confusing or unhelpful for the question asked.

Treat this as an exploratory secondary measure. Do not combine it with the primary scores unless a composite scoring method is defined in advance.

## 10. Evaluation procedure

For every test case:

1. Save the exact question, reference material and complete model response.
2. Assign a unique response ID.
3. Identify and classify material factual claims.
4. Record the number of supported, contradicted and unsupported claims.
5. Score factual accuracy, uncertainty calibration, source traceability and completeness.
6. Add a short rationale for each score.
7. Repeat the procedure for the corresponding response from the other condition.

Where practical, hide the prompt-condition label from the evaluator during scoring to reduce expectation bias.

If a second reviewer is available, ask them to independently assess a subset of responses. Record disagreements and how they were resolved. Do not claim high inter-rater reliability without actually measuring it.

## 11. Experimental comparison

Compare the two conditions using paired results: each baseline response must be compared with the uncertainty-aware response for the same question.

Report the following for each condition:

- Number of responses evaluated.
- Mean factual accuracy score.
- Total unsupported claims.
- Unsupported-claim rate.
- Mean uncertainty-calibration score.
- Mean source-traceability score.
- Mean completeness score.
- Number of material contradicted claims.

Report results separately for:

1. Directly answerable questions.
2. Questions requiring interpretation.
3. Questions where evidence is insufficient.

For each question, also report the difference between the two conditions. This can reveal whether the uncertainty-aware instruction helps with evidence gaps while potentially making some direct answers less complete.

With a small dataset and one run per question, treat the results as descriptive and exploratory. Do not claim statistical significance or broad generalisation.

## 12. Data integrity and reproducibility

Record the following for every run:

- Test ID and response ID.
- Prompt condition.
- Model name and version, where available.
- Test date.
- Relevant model settings, where available.
- Exact question and reference material.
- Complete response.
- Claim classifications.
- Dimension scores and rationale.

Do not edit model outputs before scoring them.

Do not change the questions, source material or scoring rules after inspecting results without documenting the change. If a source is found to be incorrect or outdated, document the correction and rerun both conditions for the affected question using the same corrected evidence.

## 13. Limitations

This evaluation has several limitations:

- The dataset is small and focused on one university programme.
- Human judgement is required to identify material claims and assess support.
- A prompt can change wording without improving underlying factual reliability.
- The supplied evidence may not capture every fact available from official university sources.
- One model's behaviour may not generalise to other models.
- A single response per condition does not capture response variability.
- Better uncertainty communication does not prove that users make better decisions.
- The evaluation does not establish general AI safety or measure real-world student outcomes.

## 14. Interpretation rules

- Do not assume that the uncertainty-aware prompt will perform better.
- Do not equate cautious wording with factual correctness.
- Do not equate a lack of explicit uncertainty language with an error when the evidence is clear.
- Do not treat unsupported claims as necessarily false.
- Report mixed, negative and inconclusive findings.
- Distinguish observed results from interpretations and future hypotheses.

## 15. Project status

**Status: Rubric defined; experimental results pending.**

Scores and conclusions will be added only after both prompt conditions have been run and the responses have been evaluated.
