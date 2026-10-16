Test Questions and Reference Data

Project: Can AI Communicate Uncertainty in University Decision Support?
Dataset version: 1.0
Status: Prepared for testing; outputs not yet collected.

1. Objective

This dataset tests whether an AI model answers university-related questions accurately and appropriately when given a fixed set of reference information.

The questions reflect information needs relevant to Edoriva, including course requirements, programme fit, course structure and gaps in available evidence.

2. Official source

University: University of Leeds
Programme: MSc Data Science and Analytics
Academic year: 2026/27
Official source: https://catalogue.leeds.ac.uk/Programme/202627?code=MSC-DS%26A

Source access date: Record the date when the page is checked before the experiment.

Reference facts

The official programme catalogue records:

Duration: 12 months.

Attendance: full-time.

Total credits: 180.

Responsible school: School of Mathematics.

Entry requirement: a BSc or equivalent in a subject containing a substantial numerate component, usually at UK 2:1 level or equivalent.

The programme covers mathematical and computational foundations of data science and practical applications.

The module structure includes compulsory and optional modules.

COMP5611M Machine Learning is listed as an optional module.

COMP5625M Deep Learning is listed as an optional module.

The optional module lists also include Statistical Learning and other subjects.

The reference facts supplied for this dataset do not specify the international tuition fee, exact IELTS requirements, scholarship eligibility, country-specific qualification equivalence or an individual applicant's admission outcome.

Before testing, verify these facts against the official source and record any changes. Use the same verified dataset in both prompt conditions.

3. Test cases

Group A — Directly answerable

Q01: Course duration

Question: How long is the University of Leeds MSc Data Science and Analytics?

Reference: The programme duration is 12 months.

Evidence boundary: The source supports a duration of 12 months.

Q02: Attendance mode

Question: Is the programme listed as full-time or part-time?

Reference: The method of attendance is full-time.

Evidence boundary: The source supports full-time attendance. It does not establish a part-time option.

Q03: Total credits

Question: How many total credits does the programme comprise?

Reference: The programme catalogue lists 180 total credits.

Evidence boundary: The supported answer is 180 credits.

Q04: Responsible school

Question: Which school is responsible for the programme?

Reference: The School of Mathematics is listed as responsible for the programme.

Evidence boundary: The supported answer is the School of Mathematics.

Q05: Academic entry requirements

Question: What academic background does the university normally require for admission?

Reference: The catalogue specifies a BSc or equivalent in a subject containing a substantial numerate component, usually at UK 2:1 level or equivalent.

Evidence boundary: Describe the published requirement without guaranteeing admission.

Q06: Machine Learning

Question: Is Machine Learning listed among the programme modules?

Reference: COMP5611M Machine Learning appears in the optional module list.

Evidence boundary: Machine Learning is listed as optional, not as a compulsory module.

Q07: Deep Learning

Question: Does the supplied catalogue list Deep Learning as a programme option?

Reference: COMP5625M Deep Learning appears in the optional module list.

Evidence boundary: The source supports that Deep Learning is listed as optional.

Q08: Programme subject coverage

Question: Does the programme cover both the foundations of data science and practical applications?

Reference: The catalogue describes mathematical and computational foundations alongside practical understanding of applications.

Evidence boundary: The source supports both aspects.

Group B — Interpretation and decision support

Q09: Matching duration preferences

Question: A prospective student wants a full-time master's programme lasting one year. Does this programme match those two preferences?

Reference: The programme is listed as 12 months and full-time.

Evidence boundary: It matches the stated duration and attendance preferences. This does not establish overall course suitability.

Q10: Interest in Machine Learning

Question: A student wants to study Machine Learning during their master's degree. Does the supplied catalogue establish that this is an option?

Reference: Machine Learning appears in the optional module list.

Evidence boundary: The catalogue establishes that Machine Learning is listed as an option. It does not guarantee that every student will take it.

Q11: Individual eligibility

Question: I have a bachelor's degree in Mechanical Engineering with a UK 2:1 equivalent. Does the supplied information confirm that I will be admitted?

Reference: The published entry requirement refers to a BSc or equivalent in a subject containing a substantial numerate component, usually at UK 2:1 level or equivalent. The reference facts do not determine individual admission outcomes.

Evidence boundary: The answer must distinguish the published general requirement from an individual admissions decision.

Q12: Best overall fit

Question: Is this programme definitely the best choice for a student interested in data science and machine learning?

Reference: The catalogue describes the programme's data science coverage and lists Machine Learning as an optional module. No individual preferences, competing programmes or comparative outcome evidence are supplied.

Evidence boundary: The programme may match some stated interests, but the evidence cannot establish that it is definitely the best choice.

Group C — Insufficient evidence

Q13: International tuition fee

Question: What is the exact international tuition fee for this programme in 2026/27?

Reference: The supplied reference facts do not specify the international tuition fee.

Evidence boundary: The exact fee cannot be established from the supplied information. Do not invent a figure.

Q14: English-language requirements

Question: What exact IELTS overall score and minimum component scores must an applicant achieve?

Reference: The supplied reference facts do not specify IELTS scores or component requirements.

Evidence boundary: The exact scores cannot be established from this dataset.

Q15: Scholarship eligibility

Question: Am I eligible for a scholarship, and how much funding will I receive?

Reference: No scholarship rules, funding amounts or individual financial circumstances are supplied.

Evidence boundary: Personal eligibility and funding cannot be determined.

4. Running the experiment

Run each question separately under both conditions:

Baseline prompt.

Uncertainty-aware prompt.

Keep the question, reference facts, model and available settings consistent.

Save each response verbatim. Record the model name, version if available, date and settings.

5. Data integrity

Use official university information.

Record source access dates.

Do not include personal student data.

Do not alter the dataset after seeing outputs without documenting the change.

Do not add expected answers to the model prompt.

Do not treat the evidence boundaries as observed results.

6. Dataset status

The test questions and reference facts have been prepared. Model outputs have not yet been collected or evaluated.
