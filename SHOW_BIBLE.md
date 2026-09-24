# Project Show Bible

> A living reference for building more of this project without losing its identity. Copy this file into a repository, replace the bracketed prompts, and delete sections that truly do not apply. Record what exists today separately from what you intend to build.

## 0. At a glance

| Field | Answer |
| --- | --- |
| Project | [Name and repository link] |
| One sentence premise | [What it is, for whom, and why it matters] |
| Current stage | [Idea / prototype / usable / maintained / archived] |
| Canonical branch and release | [Branch, tag, or deployment] |
| Owner / decision maker | [Name or team] |
| Last verified | [YYYY-MM-DD; checked against commit or release] |
| Start here | [Links to README, demo, setup, and issue tracker] |

## 1. The premise

**The user and their problem:** [Describe a real user and the situation they encounter.]

**What this project lets them do:** [A concrete outcome, preferably in one sentence.]

**The experience in three beats:**

1. [What the user sees or does first.]
2. [The core interaction or transformation.]
3. [The useful result and what happens next.]

**The promise:** [What someone should be able to depend on.]

**Outside the premise:** [Adjacent ideas this project will not pursue now; include the reason or a link to the decision.]

## 2. Canon: what is true today

Write verifiable facts here. Link to the implementation, a screenshot, a test, a demo, or a release. Mark unverified statements `UNVERIFIED`; mark proposed behavior `PLANNED` and keep it in the roadmap.

| Area | Current behavior | Evidence | Confidence / caveat |
| --- | --- | --- | --- |
| Main user flow | [Actual behavior] | [Path, URL, or test] | [Verified at commit / caveat] |
| Data and persistence | [What is stored and where] | [Path or schema] | [Caveat] |
| Integrations | [What actually connects] | [Path or docs] | [Caveat] |
| Deployment | [Where and how it runs] | [Config or URL] | [Caveat] |

**Known failures and rough edges:** [Links to issues; include how to reproduce when useful.]

## 3. The world and its rules

**Domain vocabulary:** Define terms that have a specific meaning in this project.

| Term | Meaning here | Where used |
| --- | --- | --- |
| [Term] | [Plain definition] | [Code, UI, docs] |

**Invariants:** Rules that must remain true after any change. Prefer statements that can be checked.

1. [Example: An event's displayed time always reflects its original timezone.]
2. [Example: A user can reach the primary action without creating an account.]

**Boundaries and constraints:** [Privacy, accessibility, platform limitations, performance budgets, API limits, licensing, and supported environments. Include why each matters.]

**Design principles:** [Three to five priorities with a concrete implication each.]

| Principle | In practice | Example of a bad fit |
| --- | --- | --- |
| [Principle] | [Decision it guides] | [Specific pattern to avoid] |

## 4. Cast: people, components, and dependencies

**Users and roles:** [Who uses it; permissions and distinct needs, if any.]

**System map:** [A short paragraph or link to an up-to-date diagram showing entry point, major components, external services, and data flow.]

| Component | Responsibility | Source of truth | Inputs / outputs | Owner or dependency |
| --- | --- | --- | --- | --- |
| [Component] | [One responsibility] | [Path] | [Interfaces] | [Person, service, or package] |

**Key files:**

| Path | Why a newcomer should open it |
| --- | --- |
| `[path]` | [Purpose] |

**External assumptions:** [What must be available for the project to work, and what happens when it is unavailable. Never include secrets.]

## 5. Visual and interaction language

Fill this out for a visual product; otherwise link to the relevant API or CLI conventions.

**Personality and tone:** [How the product should feel; include two representative strings or screenshots.]

**Visual rules:** [Tokens, typography, spacing, colors, motion, imagery, and responsive behavior, with links to their actual definitions.]

**Interaction rules:** [Navigation, focus, empty/loading/error states, input methods, accessibility, and feedback.]

**Signature moments:** [The two or three details that make this project recognizable and where they are implemented.]

**Reference examples:** [Current screenshots or recordings, dated and linked. Distinguish shipped UI from concepts.]

## 6. Episodes: core flows and edge cases

For each important flow, duplicate this small card:

### Flow: [Name]

- **Trigger:** [What starts it.]
- **Steps:** [Observable sequence, including important state changes.]
- **Result:** [What success looks like.]
- **Failure and recovery:** [What the user sees and can do.]
- **Implementation:** [Paths and tests.]
- **Status:** [Shipped / partial / planned; commit or issue link.]

## 7. Continuity ledger: decisions and open questions

Record decisions that would otherwise be reopened by every new contributor. Keep full discussion in linked issues or ADRs.

| Date | Decision | Reason | Tradeoff | Evidence / discussion | Revisit when |
| --- | --- | --- | --- | --- | --- |
| [YYYY-MM-DD] | [Chosen approach] | [Reason] | [Cost accepted] | [Link] | [Trigger, if any] |

**Open questions:**

| Question | What would resolve it | Owner / issue |
| --- | --- | --- |
| [Question] | [Experiment, user evidence, or decision] | [Link] |

## 8. The season arc: roadmap

Keep aspirations out of the canon above. Point to issues for actionable detail.

| Horizon | Outcome | Why now | Dependency | Evidence of done | Issue |
| --- | --- | --- | --- | --- | --- |
| Now | [Smallest useful outcome] | [Reason] | [Dependency] | [Observable criterion] | [Link] |
| Next | [Likely next outcome] | [Reason] | [Dependency] | [Criterion] | [Link] |
| Later | [Possibility, not commitment] | [Reason] | [Dependency] | [Criterion] | [Link] |

**Parking lot:** [Ideas worth retaining but not yet prioritized, with links.]

## 9. How to make a new episode

Use this sequence when adding a feature, redesigning a flow, or asking an agent to work on the repo.

1. Read this bible, the README, relevant code, and linked decisions. Check whether the bible still matches the current branch.
2. State the user outcome, the entry point, the expected behavior, and the affected invariants.
3. Find an existing analogous flow or component and follow its conventions. Record a deliberate exception in the continuity ledger.
4. Make the smallest coherent change. Cover the meaningful failure path and accessibility or platform behavior that the feature touches.
5. Run the relevant checks listed below. Inspect the actual UI or output where applicable.
6. Update canon, flow cards, key paths, screenshots, roadmap, and decisions only where the change makes them stale. Link the PR or commit.

**Definition of done:** [Project-specific checklist: behavior, tests, docs, design review, release, etc.]

**Useful commands:**

```sh
# install: [command]
# run: [command]
# test: [command]
# lint/typecheck: [command]
# build: [command]
```

**Agent handoff format:**

```md
Goal: [User outcome]
Current behavior and evidence: [Paths / screenshots / commit]
Relevant rules: [Invariants, design principles, constraints]
Scope: [What to change]
Acceptance: [Observable result and checks]
Open choice: [Decision the implementer may make]
Afterward: [Bible sections and docs to update]
```

## 10. Bible maintenance

- **Update trigger:** A merged change alters a documented behavior, rule, component, decision, or flow; update this file in the same PR.
- **Fact discipline:** Link claims to current code or a working demo. Give screenshots a date. Never turn a plan into a shipped feature merely by rewriting prose.
- **Size discipline:** Keep this file navigable. Move long setup steps to the README, detailed proposals to issues, and lengthy technical decisions to ADRs; link back here.
- **Conflict rule:** Running code and current tests establish observed behavior; product decisions describe intended behavior. If they disagree, flag the gap and resolve it explicitly.
- **Review cadence:** [Monthly / before each release / at each project restart]. Owner: [Name or team].

### Change log for the bible

| Date | What changed | Related PR / commit |
| --- | --- | --- |
| [YYYY-MM-DD] | [Short description] | [Link] |
