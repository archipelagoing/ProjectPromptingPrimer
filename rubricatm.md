# rubricatm.md

> A reusable rubric for judging this repository **at the moment** against the best credible version of the project. The top of this file defines the target; the assessment at the bottom records what exists now. Keep one current assessment here. Git history preserves older ones.

## How to use this file

1. Replace the bracketed fields in **Project target** and **Scoring rubric**. Define the best version that still belongs to this project's purpose, users, platform, and reasonable scope. A bigger feature list is not automatically a better project.
2. After a meaningful iteration, ask a contributor or coding agent to run the **Assessment prompt** below.
3. The agent reads the current repo and the existing rubric, gathers evidence, and **replaces only the Latest assessment section at the bottom**. It does not append another full assessment to this file.
4. Commit the update. The previous assessment remains available in Git history. A returning agent reads only this file's target, criteria, and latest assessment; it need not reconstruct every previous score.
5. If you want explicit snapshots outside Git history, copy the prior assessment to `rubrics/YYYY-MM-DD-<short-sha>.md` **before** replacing it. Never treat an archived snapshot as the current score.

Reassess after a release, substantial feature, major refactor, or shift in project scope. Small commits do not require a new grade.

## Project target

**Project:** [Name and repository URL]

**Intended user:** [Who uses it and in what situation?]

**Core job:** [What should they be able to accomplish?]

**Best credible version:** [Describe the experience in 3–5 sentences. Include the result, reliability, and polish that would make it excellent. Do not assume every possible integration or feature belongs.]

**Explicit boundaries:** [What is outside scope and why?]

**Target environment:** [Platforms, browsers/devices, runtime, deployment.]

**Success signals:** [Observable user outcomes or meaningful measures; avoid vanity metrics.]

**Reference documents:** [README, repository guide, requirements, issues, designs, demo. When sources disagree, flag the conflict.]

## Scoring rules

- Score **the checked-out commit**, not a roadmap, claim in a README, mockup, or unmerged branch.
- Each criterion has a fixed weight and a score from 0 to 4. Contribution = `weight × score ÷ 4`. Total weights must add to 100; the total grade is the sum of contributions.
- Use the anchors below consistently. A feature is **included** only when there is working evidence. Mark **missing** when the implementation is absent. Mark **unknown** when access or verification is insufficient; do not silently score unknown as zero. Give a provisional score and disclose which criteria are unverified.
- Evidence can be a source path, test result, build output, screenshot, deployed behavior, or reproduction steps. Cite specific paths and commands rather than saying “the code looks good.”
- Assess the user experience as well as the code. A green test suite cannot by itself prove the product is usable.
- Keep weights stable across iterations. If the project's goal changes, update the target and weights explicitly and mark the new grade as a **new baseline**, not an improvement over the old score.
- Call out blockers separately: a critical security, data-loss, or core-flow defect should remain visible even if the weighted total is high.

| Score | Meaning |
| --- | --- |
| 0 | Absent or does not run. |
| 1 | Started, but the primary use case is blocked or mostly manual. |
| 2 | Works for a narrow happy path; significant gaps remain. |
| 3 | Works for the intended use case, with limited gaps or polish needed. |
| 4 | Meets the defined target, including important edge cases and evidence. |

## Scoring rubric

Edit the criteria and weights to fit this project **before** grading. These defaults are a starting point, not universal standards. For each criterion, say what a 4/4 actually means.

| Criterion | Weight | A 4/4 means... |
| --- | ---: | --- |
| Core user outcome | 25 | [A user can complete the main task end to end without hidden manual steps.] |
| Correctness and edge cases | 15 | [Expected inputs, boundary cases, errors, and recovery behave as specified.] |
| Usability and accessibility | 15 | [The flow is clear on supported devices and usable with relevant input/access needs.] |
| Reliability and performance | 10 | [It stays responsive and recovers predictably under realistic conditions.] |
| Architecture and maintainability | 10 | [Responsibilities are clear and a contributor can extend the project without duplicating logic.] |
| Tests and verification | 10 | [Meaningful checks cover key behavior; commands run and results are reproducible.] |
| Setup and documentation | 10 | [A newcomer can install, run, understand, and contribute using accurate docs.] |
| Deployment and operations | 5 | [The intended release can be built, deployed, observed, and rolled back.] |
| **Total** | **100** | |

## Assessment prompt

Copy this prompt when asking an agent to update the rubric:

```text
Assess this repository at the current checked-out commit using rubricatm.md.

1. Read the Project target, Scoring rules, and Scoring rubric first. Then inspect the relevant implementation, tests, docs, configuration, and working UI or output where feasible. Do not rely on the README as proof that a feature works.
2. For each criterion, record its score (0–4), weighted contribution, concrete evidence, what is included, and what is missing. Separate unknown/unverified claims from confirmed missing work. Run the most relevant existing checks; report commands, results, and anything you could not test.
3. Identify the three improvements with the greatest impact on the intended user. For each, give a clear acceptance condition and link an existing issue when possible. Do not inflate the score for planned features.
4. Replace ONLY the Latest assessment section at the bottom of rubricatm.md with the new assessment. Preserve the target, scoring rules, weights, and prompt unless I explicitly ask you to revise them. Do not append a second current assessment.
5. State the commit SHA and date. If the target or weights changed since the previous assessment, label this a new baseline and do not claim a direct score increase. Summarize score changes only when the same criteria and weights were used.
```

## Latest assessment

> Replace everything in this section after each meaningful iteration. Leave the rest of the file intact.

**Date:** [YYYY-MM-DD]  
**Commit:** [Full or short SHA]  
**Assessment status:** [Verified / provisional, with reason]  
**Target version:** [Short description; note if this is a new baseline]  
**Total:** [X/100, or provisional X/100 with unverified criteria listed]

| Criterion | Weight | Score / 4 | Contribution | Evidence | Included | Missing / unknown |
| --- | ---: | ---: | ---: | --- | --- | --- |
| Core user outcome | 25 | [0–4] | [0–25] | [Paths, demo, checks] | [Observed] | [Gaps; label unknown] |
| Correctness and edge cases | 15 | [0–4] | [0–15] | [Evidence] | [Observed] | [Gaps] |
| Usability and accessibility | 15 | [0–4] | [0–15] | [Evidence] | [Observed] | [Gaps] |
| Reliability and performance | 10 | [0–4] | [0–10] | [Evidence] | [Observed] | [Gaps] |
| Architecture and maintainability | 10 | [0–4] | [0–10] | [Evidence] | [Observed] | [Gaps] |
| Tests and verification | 10 | [0–4] | [0–10] | [Evidence] | [Observed] | [Gaps] |
| Setup and documentation | 10 | [0–4] | [0–10] | [Evidence] | [Observed] | [Gaps] |
| Deployment and operations | 5 | [0–4] | [0–5] | [Evidence] | [Observed] | [Gaps] |
| **Total** | **100** | | **[X/100]** | | | |

**Checks run:** [Command → result; manual checks; unrun checks and why.]

**Critical blockers:** [None observed / specific blocker and reproduction.]

**Top three next improvements:**

1. [Improvement → why it matters → observable acceptance condition → issue.]
2. [Improvement → why it matters → observable acceptance condition → issue.]
3. [Improvement → why it matters → observable acceptance condition → issue.]

**Change since previous assessment:** [Comparable score change and reason, or “new baseline” / “first assessment.”]
