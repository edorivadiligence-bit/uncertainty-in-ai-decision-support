AI Uncertainty in University Decision Support

1. Project purpose

This file defines the uncertainty-aware condition for an exploratory evaluation of AI-generated answers to questions about UK university study.

The project is motivated by Edoriva, a platform designed to help prospective international students and their families make more informed study-abroad decisions.

The research question is:

Does an instruction to communicate uncertainty improve the reliability of AI-generated answers when information is incomplete, ambiguous or unsupported by the supplied evidence?

This condition will be compared with the baseline prompt using the same questions, reference material, model and settings wherever possible.

This file defines the experimental instructions. It does not contain experimental results.

2. Uncertainty-aware instructions

You are an assistant helping prospective international students understand UK university information.

Answer the user's question using only the reference material provided for the relevant test case.

Provide a clear, direct and useful answer. Follow the instructions below.

A. Ground claims in evidence

Use only the supplied reference material to establish factual claims.

Distinguish information explicitly supported by the reference material from interpretation or inference.

Do not present an inference as a verified fact.

Do not invent university requirements, tuition fees, deadlines, scholarship details, course modules or admissions outcomes.

Do not use outside knowledge to fill gaps in the supplied evidence.

B. Communicate uncertainty appropriately

If the reference material does not contain enough information to answer a question, state what is missing.

If the evidence is ambiguous or does not support a definite conclusion, explain the limitation.

If only part of a question can be answered, answer the supported part and identify the unsupported part.

Do not claim certainty about an individual applicant's admission, scholarship eligibility or qualification equivalence unless the supplied evidence explicitly establishes it.

Do not express unnecessary uncertainty when the supplied evidence clearly answers the question.

C. Make evidence traceable

Identify which supplied source supports important factual claims, using source labels or section names where available.

Do not invent citations, source URLs or quotations.

If the supplied material does not identify a source for a claim, do not imply that the claim has been independently verified.

D. Preserve usefulness

Answer the question directly before explaining limitations.

Keep the response concise but include the information needed to understand the answer.

Where evidence is insufficient, identify the specific additional information or official source that would be needed.

Do not refuse to answer supported parts of the question simply because other details are unknown.

E. Avoid unsupported recommendations

Do not claim that a programme is the best choice for a particular student based only on a few course facts.

Distinguish between:

Facts established by the supplied material.

Preferences expressed in the question.

Inferences about possible fit.

Information that remains unknown.

Do not present a tentative match as a guaranteed admission outcome or an objectively best choice.

3. Test procedure

Run each test case separately.

For each test case:

Copy the exact test question.

Copy only the reference material assigned to that question.

Submit the question and reference material with the uncertainty-aware instructions in Section 2.

Save the complete model response without editing it.

Record the model name, model version if available, test date and settings.

Evaluate the response using the same predefined rubric used for the baseline condition.

Run the same test case using the baseline prompt. Keep the question and reference material identical across the two conditions.

Do not change the uncertainty-aware instructions between test cases.

4. User question

[INSERT ONE TEST QUESTION FROM THE BASELINE TEST SET]

5. Reference material

[INSERT THE IDENTICAL REFERENCE MATERIAL USED FOR THE SAME TEST CASE IN THE BASELINE CONDITION]

Include only the information assigned to that test case. Preserve relevant dates, academic years, qualifications, fees and limitations.

Record the official source URL and access date with the test record.

6. Test cases

Use the same 15 test cases defined in prompts/baseline.md.

Group A — Directly answerable questions

Q01 — Course duration and attendance.

Q02 — Academic entry requirements.

Q03 — Machine Learning module.

Q04 — Programme credits.

Q05 — Responsible school.

Q06 — Programme subject coverage.

Group B — Questions requiring careful interpretation

Q07 — Matching study preferences.

Q08 — Individual admission eligibility.

Q09 — Optional module choice.

Q10 — Overall course suitability.

Group C — Questions with insufficient evidence

Q11 — International tuition fee.

Q12 — English-language requirements.

Q13 — Scholarship entitlement.

Q14 — Qualification equivalence.

Q15 — Future tuition fees.

For each test, use the exact question and reference material in the baseline test set. Do not create a different version of a question for this condition.

7. Experimental record

Complete a separate record for every test case and prompt condition.

Test ID:

Condition: Uncertainty-aware

Model name:

Model version, if available:

Test date:

Model settings, where available:

Exact question:

Exact reference material supplied:

Official source URL:

Source access date:

Complete model response:

Response saved: Yes / No

8. Evaluation criteria

Use the same predefined rubric for both conditions.

Factual accuracy

Are the material factual claims correct according to the supplied evidence?

Score the answer based on its factual content, not on how cautious or confident its tone sounds.

Unsupported claims

Count material factual claims that cannot be supported by the supplied reference material.

Do not treat an unsupported claim as supported merely because it might be true outside the experiment.

Uncertainty calibration

Assess whether the answer recognises missing, ambiguous or insufficient evidence when appropriate.

For directly answerable questions, an answer should still provide the supported facts clearly rather than becoming unnecessarily vague.

Source traceability

Assess whether important factual claims can be traced to the supplied reference material.

Do not award credit for invented citations or references that do not support the claim.

Completeness

Assess whether the answer addresses all parts of the question that can be answered from the supplied evidence.

Record each dimension separately. Apply the same scoring rules to the baseline and uncertainty-aware responses.

9. Hypotheses

The evaluation investigates the following hypotheses:

H1: The uncertainty-aware instruction may reduce unsupported factual claims.

H2: The uncertainty-aware instruction may improve recognition of insufficient evidence.

H3: The uncertainty-aware instruction may change completeness or usefulness, creating a potential trade-off.

These are hypotheses, not findings. The experiment may support, contradict or fail to resolve them.

10. Interpretation and limitations

This is a small exploratory evaluation of prompt-level instructions in a university decision-support context.

The experiment does not establish that a model is generally safe, that its advice is suitable for an individual student's circumstances, or that the findings generalise to other domains.

A response can sound cautious and still contain errors. A response can also be appropriately confident when the evidence is sufficient. The evaluation must therefore consider factual accuracy, unsupported claims, uncertainty calibration, source traceability and completeness separately.

The results may depend on the selected model, model version, prompt wording, reference material and settings.

11. Reproducibility

Save the exact prompts, questions, reference material and model outputs.

Record the model name and version, testing date and available settings. If a setting is unavailable, record it as unavailable rather than guessing.

If repeated runs are conducted, record the number of runs and how variation between responses is handled.

Do not change the test questions, evidence or scoring rules after examining the results without documenting the change and explaining its effect on comparability.

12. Project status

Status: Experimental design prepared; results pending.

No empirical results or conclusions are claimed in this file.

Update the project status only after the test cases have been run, the outputs saved and the responses assessed using the predefined rubric.
