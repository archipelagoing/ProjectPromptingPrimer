# Project Tracker

> Drop this file into any project and use the setup prompt below. It works for
> software, research, design, documentation, and other deliverables. No particular
> framework, platform, service, or build tool is required.
>
> This file provides instructions, not background automation. Updates happen when
> an assistant follows it while working on an authorized task.

## Quick start

1. Copy this file into your project. Keep the filename or rename it.
2. Give your assistant the setup prompt below, adjusting the filename if needed.
3. For ongoing Codex use, add the optional instruction to your project's
   `AGENTS.md`. Merge it with existing instructions rather than replacing them.

**Setup prompt:**

```text
Use todotemplate.md as this project's living tracker. Read its maintenance
instructions and initialize it from my stated goals and available project
materials. Replace placeholders with supported facts; label unknowns explicitly.
If an existing tracker exists, reconcile it without losing tasks or history and
establish one authoritative tracker. Do not execute the backlog just to populate
it. Summarize the current state and the next actionable work.
```

**Optional AGENTS.md instruction:**

```text
Use todotemplate.md as the project's authoritative task tracker. Follow its
maintenance instructions during authorized project work. Before your final
response, update affected tasks, evidence, blockers, and next actions whenever
project state changes. A backlog entry does not authorize unrelated work.
If this file is renamed, update this reference. Follow an explicit user choice
of a different tracker and avoid maintaining duplicate task lists.
```

## Maintenance instructions

### Initialize once

- Read the user's goals, applicable project instructions, and relevant available
  materials. These may include source code, briefs, existing checklists, notes,
  specifications, or deliverables. Do not assume every project has code or tests.
- Fill the snapshot and define concrete tasks based on that evidence. Remove
  unused placeholder rows, but retain reusable examples inside code fences.
- Use `Unknown` for missing facts and `Not verified` for unvalidated claims.
  Ask for missing information only when it materially affects the work; continue
  independent work while it remains unresolved.
- Preserve existing task history and user edits. When trackers overlap, choose
  one canonical location using the user's instructions and link to other sources.
  Do not silently discard conflicting requirements or completion claims.
- Record the actual initialization date. Do not treat template examples or
  placeholder tasks as real requirements or completed work.

### Maintain during work

1. Read the current request and relevant task entries. Work within authorized
   scope; a task list is context, not permission to execute the whole backlog.
2. Give each task a stable ID such as `TASK-001`. Maintain one canonical entry
   per task. Reference IDs from summaries, milestones, and next actions.
3. Define observable acceptance criteria before marking work complete. Split
   tasks when deliverables, environments, or validation can succeed independently.
4. Set status to `in-progress` when work begins. Use `needs-verification` when
   the deliverable exists but required validation remains. Use `blocked` for a
   concrete dependency, missing input, or access issue, with an unblock action.
5. Check `[x]` only when all acceptance criteria are met and evidence is recorded.
   Every other status stays unchecked. Reopen completed work if new evidence
   contradicts it and record why. Do not infer completion from elapsed time.
6. Validate appropriately for the work: tests, builds, source checks, calculations,
   artifact inspection, manual walkthroughs, or explicit user review. Record what
   was checked, the result, and the date. Distinguish current verification from
   historical reports. Never invent results or imply unavailable checks passed.
7. Keep validation scoped to its evidence. A simulated result does not establish
   live behavior; one environment does not establish success in every environment.
   Record required checks that were not run and why.
8. Before the final response, update affected tasks, the snapshot, and next
   actions when project state changes. Leave an accurate partial status if work
   stops before completion. Routine discussion need not create tracker churn.
9. Preserve unrelated work. Add newly discovered necessary work as scoped tasks;
   record deferred or canceled work with reasons instead of silently deleting it.
   Do not broaden the user's request to finish newly discovered tasks.
10. Keep entries concise. Record meaningful status changes, decisions, and evidence,
    not every tool call. Update dates only when content changes. Never store
    secrets, credentials, or unnecessary sensitive information in the tracker.

## Project snapshot

- **Project:** {{Project name}}
- **Objective:** {{Intended outcome and who it serves}}
- **Success criteria:** {{Observable conditions for overall success}}
- **Scope / exclusions:** {{Agreed boundaries}}
- **Source materials:** {{Links or paths to authoritative inputs}}
- **Current state:** {{Evidence-backed summary; distinguish reported from verified}}
- **Current milestone:** {{Milestone ID or none}}
- **Active task IDs:** {{Task IDs or none}}
- **Constraints:** {{Relevant timeline, tools, budget, environment, or unknown}}
- **Known limitations:** {{Verified gaps or none recorded}}
- **Last updated:** {{YYYY-MM-DD}}

## Status and priority

| Checkbox | Status | Meaning |
| --- | --- | --- |
| `[ ]` | todo | Work has not started or needs assessment. |
| `[ ]` | in-progress | Work is actively underway. |
| `[ ]` | needs-verification | Deliverable exists; required checks remain. |
| `[ ]` | blocked | A concrete dependency prevents the next step. |
| `[ ]` | deferred | Intentionally postponed; reason recorded. |
| `[ ]` | canceled | No longer required; reason preserved. |
| `[x]` | done | Acceptance criteria met and evidence recorded. |

Use priorities independently of milestones: **P0** = critical or blocking,
**P1** = next essential work, **P2** = planned improvement, **P3** = optional.
Adapt these definitions if the project already has an established convention.
Milestones use separate IDs such as `M1` and group tasks by outcome.

## Next actions

Keep up to three actionable steps, referencing canonical task IDs. Respect
prerequisites and current user priorities. Fewer than three is fine; do not invent
work to fill the list. Proposed next actions are not execution authorization.

1. {{Task ID — next concrete action}}
2. {{Task ID — next concrete action}}
3. {{Task ID — next concrete action}}

## Tasks

Add real task entries here during initialization. Keep completed entries for
traceability; if the file grows large, archive them with a link and retain IDs.

### Task entry template

Copy this block outside the code fence for each task. Replace placeholders and
omit optional fields that do not apply. Split work too large to validate clearly.

```markdown
### TASK-001 — {{Concrete outcome}}

- [ ] **Status:** todo
- **Priority:** {{P0 | P1 | P2 | P3}}
- **Milestone:** {{Milestone ID or none}}
- **Scope:** {{Deliverable, area, or environment}}
- **Depends on:** {{Task IDs, external prerequisites, or none}}
- **Acceptance criteria:**
  - {{Observable condition}}
  - {{Observable condition}}
- **Evidence:** {{Not verified, or dated check/result and supporting link}}
- **Blocker / unblock action:** {{None, or dependency and exact next step}}
- **Next action:** {{Smallest actionable step; none if complete}}
- **Updated:** {{YYYY-MM-DD}}
```

Optional fields: owner, agreed deadline, relevant files, review requirement,
estimate, or decision reference. Add them only when useful; do not invent owners
or deadlines.

## Milestones (optional)

Use this as a roadmap index, not a duplicate task checklist. Derive progress from
referenced task entries. Delete this section for small projects if unnecessary.

| ID | Outcome | Task IDs | Completion criteria |
| --- | --- | --- | --- |
| {{M1}} | {{Milestone outcome}} | {{Task IDs}} | {{Observable completion conditions}} |

## Decisions and open questions

Record decisions that affect scope, priorities, or acceptance. Keep task blockers
in their canonical entries; reference them here only when a project-wide decision
is required. Unanswered questions are not approval.

| ID | Date | Decision or question | Rationale / needed input | Related tasks |
| --- | --- | --- | --- | --- |
| {{DEC-001}} | {{YYYY-MM-DD}} | {{Decision or open question}} | {{Reason or input needed}} | {{Task IDs}} |

## Recent changes

Record meaningful transitions and outcomes. Keep this section short; consolidate
older entries without losing unresolved issues or the evidence for completion.

| Date | Task IDs | Change | Evidence / validation |
| --- | --- | --- | --- |
| {{YYYY-MM-DD}} | {{Task IDs}} | {{Meaningful change}} | {{Result, link, or not verified}} |

## Issue / learning log (optional)

Use for problems worth remembering. Delete this section if unnecessary.

```markdown
### {{YYYY-MM-DD}} — {{Task ID and issue}}

- **Attempt:** {{Action taken}}
- **Expected / actual:** {{What differed}}
- **Evidence:** {{Sanitized result, observation, or artifact}}
- **Reference:** {{Source consulted, if any}}
- **Resolution / next action:** {{Fix, workaround, or remaining dependency}}
- **Lesson:** {{What would make this easier next time}}
```
