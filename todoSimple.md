# {{Project name}} TODO

Last updated: {{YYYY-MM-DD}}. {{Briefly describe what currently works, what has
been verified, and the next major gap. Use “Not assessed” until reviewed.}}

## How to use this template

Copy this file into your project and optionally rename it to `todo.md`. Replace
the placeholders and adapt the sections to your project. The checklists below
are starting points, not mandatory scope. Remove irrelevant examples during
setup; preserve real project tasks and history afterward.

Give Codex this prompt, using the actual filename:

```text
Read todotemplate2.md and adapt it to this project using my goals and the available
project files. Keep its simple format: a current-state summary, next steps,
grouped checklists, and short progress notes. Reconcile any existing checklist
without losing unfinished work or completion evidence. Do not execute the
backlog during setup. Follow the maintenance instructions when working on
subsequent authorized tasks.
```

For ongoing use, merge this instruction into the project's `AGENTS.md`, updating
the filename if needed:

```text
Use todotemplate2.md as the project checklist and follow its maintenance
instructions. After authorized work changes project state, update the relevant
checkboxes, progress notes, next steps, and last-updated date before responding.
Keep one authoritative checklist. The backlog does not authorize unrelated work.
```

The file does not update itself: Codex must read and follow these instructions
while working. This template does not install the `AGENTS.md` instruction.

## Maintenance instructions

- Read the current user request and relevant project materials before updating
  this file. User instructions and applicable repository rules take precedence.
- Keep the format simple. Use `[ ]` for unfinished work and `[x]` for work that
  meets the stated task conditions. No task IDs or status tables are required.
- Write concrete tasks with observable outcomes. Split implementation and
  verification when they can be completed independently.
- Add short qualifiers when useful: `(in progress)`, `(needs verification)`,
  `(blocked: reason; unblock action)`, or `(deferred: reason)`.
- Record evidence in the progress paragraph beneath the relevant checklist:
  what was checked, when, and the result. Link to files or artifacts where useful.
  Label historical reports and user confirmations as such. Never invent results.
- Keep verification specific to its scope. A local test does not prove a live
  integration works; one device or environment does not prove another works.
- Keep each checkbox in one main section. The next-steps list is a short ordered
  summary referencing those sections, so it cannot develop conflicting statuses.
- After meaningful work, update affected checkboxes, section notes, next steps,
  and the date. If verification remains, leave that task unchecked and say why.
  Reopen tasks when evidence contradicts completion.
- Preserve unrelated tasks and user edits. Record reasons for deferral or
  cancellation; do not silently remove real work. Add newly discovered necessary
  tasks without treating them as authorization to expand the current request.
- Use checks appropriate to the project, including tests, artifact review,
  calculations, or manual walkthroughs. Do not require software tools for
  projects that do not use them. Never store credentials or secrets here.
- Keep notes concise and current. Ordinary discussion need not change the file.

## Next steps

Keep three to five concrete actions in priority order, drawn from the sections
below. Fewer is fine. Replace these placeholders after reviewing the project.

1. {{Next action — relevant section}}
2. {{Following action — relevant section}}
3. {{Next milestone-enabling action — relevant section}}

{{Short handoff paragraph: what is ready, what still needs verification, and any
dependency that affects the next steps.}}

## 1. Define the project

- [ ] Describe the problem and intended audience
- [ ] Define the main outcome or deliverable
- [ ] Define how success will be verified
- [ ] Agree on scope and exclusions
- [ ] Record relevant constraints and dependencies

{{Progress note: agreed direction, source brief or specification, and unresolved
questions. Do not assume these decisions have already been made.}}

## 2. Set up the foundation

- [ ] Organize project files and reference materials
- [ ] Set up the tools or environment needed for the work
- [ ] Confirm required inputs and access are available
- [ ] Document how to start or reproduce the work

{{Progress note: what is ready, setup checks performed, and missing inputs.}}

## 3. Build the core deliverable

Replace these placeholders with the project's actual features, outputs, or work
packages. Duplicate this section for major areas that deserve their own list.

- [ ] {{First essential capability or output}}
- [ ] {{Second essential capability or output}}
- [ ] {{Third essential capability or output}}
- [ ] Verify the core deliverable against its success criteria

{{Progress note: what exists, what works, what was verified, and what remains.}}

## 4. Connect the parts

Use this section when the project has multiple components, sources, contributors,
or handoffs. Remove it during setup if it does not apply.

- [ ] Define the inputs and outputs between parts
- [ ] Connect the required components or materials
- [ ] Handle missing or invalid inputs where relevant
- [ ] Verify the complete workflow with representative inputs

{{Progress note: which connections are verified and which are only simulated,
drafted, or awaiting external access.}}

## 5. Improve usability and presentation

- [ ] Review the main user or reader journey
- [ ] Make instructions, labels, and organization clear
- [ ] Check accessibility and readability where relevant
- [ ] Review the intended formats, devices, or delivery environments
- [ ] Address confusing or incomplete states

{{Progress note: review scope, findings, and remaining improvements.}}

## 6. Validate the result

- [ ] Check the main success criteria
- [ ] Check relevant edge cases and failure conditions
- [ ] Verify assumptions against reliable sources or representative data
- [ ] Complete any required independent or user review
- [ ] Resolve blocking findings and recheck affected work

{{Progress note: dated checks and results, evidence links, limitations, and checks
that could not be completed. Avoid repeating implementation checkboxes here.}}

## 7. Prepare delivery

Adapt this section to the actual delivery: a release, handoff, report,
presentation, submission, or another agreed output. Listing a delivery action
does not itself authorize publishing or deployment.

- [ ] Prepare the final files or deliverables
- [ ] Document use, setup, or reproduction steps
- [ ] Confirm delivery requirements are met
- [ ] Complete the authorized delivery or handoff
- [ ] Verify the delivered result in its intended setting

{{Progress note: delivery readiness, location of artifacts, and remaining steps.}}

## 8. Final polish

- [ ] Remove obsolete drafts or placeholders from the deliverable as appropriate
- [ ] Review consistency and clarity
- [ ] Document known limitations
- [ ] Update project documentation to match the final result

{{Progress note: remaining polish and any deliberately deferred work.}}

## Future priorities

Use this optional section for work beyond the current milestone. Give each
priority a concrete outcome. Move tasks into the main sections when they become
active rather than copying them into a second checklist.

### Next milestone — {{Outcome}}

- [ ] {{Future task}}
- [ ] {{Future task}}

{{Why this milestone matters and what must be complete before it starts.}}

### Stretch goals

Only consider these once the agreed core outcome is complete.

- [ ] {{Optional improvement}}
- [ ] {{Optional extension}}

## Blockers and decisions

- **Blocker:** {{Observed dependency, affected section, and action needed; or none recorded}}
- **Open question:** {{Missing decision and why it matters; or none recorded}}
- **Decision:** {{Date, choice, and brief rationale; or none recorded}}

## Friction log (optional)

Record meaningful issues as they happen. Copy this block for each issue worth
preserving; omit the section if it adds no value.

```text
Date:
Task:
What I tried:
What I expected:
What happened:
Evidence or reference:
Resolution or next action:
What would have made this easier:
```
