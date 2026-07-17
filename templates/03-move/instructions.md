# Move phase: instructions for the agent

You are running the Move phase. Purpose: redesign the work around AI and ship it into the real system of record. A pilot running beside the old process forever is a failure state, not a milestone. Read `../charter.md`, `../01-sense/recommendation.md`, `../02-adopt/adoption-log.md`, and `../methodology/sam-methodology.md` first.

## Work sequence

### 1. Workflow redesign (`workflow-redesign.md`)

A before/after spec of the workflow with the AI step embedded:

- **Before**: the numbered steps from `../01-sense/current-state.md`.
- **After**: the new numbered steps. Mark explicitly which steps are removed, which are new, and where a human checks or signs off on AI output.
- **The old way**: retired, formally changed, or kept only for defined exceptions (list them). "Both, indefinitely" is not an allowed answer; if the user wants it, name it as pilot purgatory and ask for an end date.

### 2. Cutover plan (`cutover-plan.md`)

Where the new way runs (must be the real system of record with real data under the org's real access and privacy rules), the cutover date or trigger, who communicates the change and to whom, and the rollback condition: what observation would send this back a phase.

### 3. Measurement (`measurement.md`)

The success measure from the charter, its baseline value, how and when it is measured, and who reads the number. Measure the work outcome, not tool usage. Logins are not a metric.

### 4. Ownership (`ownership.md`)

Who owns the workflow after the project steps away, who handles escalations and model or tool changes, and when the first post-launch review happens. A workflow with no owner degrades to shelfware within a quarter, so do not let this file contain a team name where a person's name should be.

## Closing the phase

Check the Move gates in `../status.md` only when: the new way is live in the system of record, the old way's fate is executed as written, and the metric has been measured at least once post-cutover with an owner reading it. Then set `phase: done` in `../status.md`, add a dated log line, and write a short `outcome.md`: metric movement so far, what the org should watch next, and any candidate follow-on problems (which would each be a new SAM project, not scope creep on this one). `outcome.md` is this phase's share-up artifact. Remind the user to share it.

If cutover exposes something broken upstream (a capability gap, a wrong Sense assumption), go back to that phase, update the charter decision log, re-close its gate, and return here. That is the method working, not failing.
