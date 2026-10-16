# Can AI Communicate Uncertainty in University Decision Support?

**An exploratory evaluation of uncertainty communication in AI-generated answers about UK university study.**

## 1. Overview

Students considering international education often need to make consequential decisions using information about university entry requirements, tuition fees, application deadlines and course options. AI systems may help users navigate this information, but an answer that sounds confident can still be incomplete, outdated or unsupported by the available evidence.

This project proposes a small, controlled evaluation of whether explicit instructions to communicate uncertainty change the factual reliability and evidence-grounding of AI-generated answers.

The project is motivated by my experience building **Edoriva**, a platform designed to help prospective international students and their families make more informed study-abroad decisions by connecting them with current students, graduates and professionals.

Edoriva is the context motivating this research question. This evaluation is a separate research exercise and should not be interpreted as evidence that Edoriva currently implements the interventions tested here.

## 2. Research question

**Does instructing an AI model to distinguish verified facts from inference and explicitly acknowledge insufficient evidence reduce unsupported claims in answers about UK university study?**

The evaluation will compare two prompt conditions using the same questions, reference material and model configuration.

### Hypotheses

- **H1:** The uncertainty-aware instruction will reduce the number of unsupported factual claims.
- **H2:** The uncertainty-aware instruction will improve the identification of questions that cannot be answered confidently from the supplied evidence.
- **H3:** Explicit uncertainty communication may sometimes reduce answer completeness or usefulness, creating a trade-off that should be measured rather than assumed away.

These are hypotheses to test, not established findings.

## 3. Why this matters

Users need to distinguish between an answer that is plausible and one that is supported by reliable evidence.

In university decision support, an unsupported statement about a fee, admission requirement or deadline could influence a student's planning. A useful AI system should therefore do more than generate fluent answers: it should communicate what the evidence supports, identify gaps and avoid presenting uncertain information as established fact.

This project focuses on one narrow aspect of trustworthy AI: **whether prompt-level instructions can improve the communication of uncertainty and the grounding of answers in supplied evidence.**

It does not attempt to evaluate AI safety as a whole.

## 4. Experimental design

### Conditions

**Condition A — Baseline**

The model receives a question and the relevant reference material. It is asked to answer the question clearly using the available information.

**Condition B — Uncertainty-aware**

The model receives the same question and reference material, with an additional instruction to:

- Distinguish facts directly supported by the sources from inference.
- Identify information that is missing or cannot be verified.
- State when the available evidence is insufficient to answer.
- Avoid inventing details or implying that a claim has been verified when it has not.
- Identify the source supporting important factual statements.

The same model, questions, reference documents and other settings should be used in both conditions wherever possible.

### Test questions

The test set will cover a small number of publicly documented university-information topics, such as:

- Tuition fees and the relevant academic year.
- Course entry requirements.
- English-language requirements.
- Application deadlines.
- Questions for which the supplied sources do not contain enough information to provide a reliable answer.

The test set should include both answerable and deliberately under-specified questions. The latter are important for testing whether the model recognises the limits of its evidence.

### Reference sources

Use official university webpages and documents wherever possible. Record the source URL, the date accessed and the academic year or course to which the information applies.

The reference material should be captured or recorded before testing so that the evidence used to assess each answer is clear.

## 5. Evaluation rubric

Each response will be assessed against a predefined rubric.

| Dimension | Evaluation question |
|---|---|
| Factual accuracy | Are the factual statements consistent with the reference evidence? |
| Unsupported claims | Does the answer include factual claims that the supplied evidence does not support? |
| Uncertainty calibration | Does the response acknowledge missing, ambiguous or insufficient evidence when appropriate? |
| Source traceability | Can important factual statements be traced to the supplied sources? |
| Completeness | Does the answer address the question without omitting important information available in the evidence? |

Before evaluating the outputs, define the scoring rules and what counts as a factual claim, an unsupported claim and an appropriate expression of uncertainty.

Where feasible, assess responses in a consistent manner and record the rationale for each score. If possible, have a second reviewer independently assess a subset of responses and document disagreements.

## 6. Methodology and reproducibility

The experiment will document:

- Model and version, where available.
- Date of testing.
- Exact prompts used in each condition.
- Test questions and source material.
- Relevant model settings.
- Raw responses.
- Scoring rubric and assessment records.
- Any code used to organise or analyse the results.

The aim is to make the evaluation understandable and repeatable by another person.

If repeated runs are feasible, record the number of runs and how variability between answers is handled. Do not treat multiple outputs from the same small test set as independent evidence without considering that limitation.

## 7. Results

**Status: Pending evaluation.**

Results will be added after the experiment has been run and the responses assessed.

The results section will report the number of questions tested, scores for each condition, observed differences and relevant examples. It will include results that contradict the hypotheses as well as those that support them.

No conclusions about the effectiveness of uncertainty-aware prompting should be drawn before the evaluation is completed.

## 8. Limitations

This evaluation has several important limitations:

- A small set of university-related questions cannot represent the full range of AI use cases.
- Results may depend on the selected model, model version, prompts and settings.
- Assessing whether a claim is unsupported can require judgement, particularly when sources are ambiguous or incomplete.
- A prompt that improves uncertainty communication in one setting may not generalise to other domains.
- Better uncertainty communication does not necessarily mean that the underlying answer is more accurate.
- The experiment does not measure real-world user behaviour, decision quality or long-term reliance on AI.
- A successful result would not establish that the model is safe in general.

These limitations will be refined after the methodology and results are finalised.

## 9. Relevance to trustworthy AI

This project explores a practical question about how AI systems communicate the boundaries of their knowledge.

Potential follow-up work could investigate whether users can better identify unsupported claims when uncertainty is communicated explicitly, whether source references improve users' ability to verify answers, and whether these approaches work across different models and domains.

These are future research directions, not claims of completed experiments.

## 10. Project status and contributions

**Current status:** Proposed evaluation. Experimental results have not yet been established.

The project will document which parts of the research design, implementation, data preparation and analysis were completed by the author, along with any tools or assistance used.

The repository will be updated as the methodology, evaluation and results are completed.

## 11. Ethical and data considerations

The project will use public university information and synthetic test questions. It will not require personal student records or confidential user conversations.

The evaluation is intended to examine model outputs, not to provide admissions, immigration or financial advice to individual students.

## 12. Connection to Edoriva

Edoriva provides the practical context for my interest in trustworthy decision-support technology. Building a platform around consequential education choices has prompted me to consider how people assess information, how limitations should be communicated and how technology can support rather than replace human judgement.

This research exercise is a separate attempt to investigate one of those questions through a small, documented evaluation.

---

**Repository status:** Work in progress. Conclusions will be reported only after the evaluation has been conducted and the evidence reviewed.
