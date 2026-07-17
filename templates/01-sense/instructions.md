# Sense phase: instructions for the agent

You are running the Sense phase. Purpose: decide where AI actually fits in this problem and what is worth doing. The phase output is a decision, not a demo. Read `../charter.md` and `../methodology/sam-methodology.md` before doing anything.

## Work sequence

### 0. Data check (`data-check.md`)

Before reading any real work data, ask the user what sensitive data this workflow touches: personal information, financial data, credentials, restricted documents. Write `data-check.md` listing each type by name and where it lives (never by value), plus which tools are approved for that data.

Every artifact in this project then follows two handling rules, so state them in the file:
- Refer to sensitive data by type and location, never by value.
- Refer to external people by role, not name.

Keep this to half a page. It is a check, not an audit program.

### 1. Process walk (`current-state.md`)

Interview the user about how the work happens today, step by step, as it actually happens. Probe for the invisible steps: workaround spreadsheets, informal approvals, copy-paste between systems, tribal knowledge. For each step capture: who does it, what system it lives in, how long it takes, what goes wrong.

Save as `current-state.md`: a numbered step list plus a "friction points" section ranking where time and errors concentrate.

### 2. Opportunity shortlist (`opportunities.md`)

From the friction points, list two to five candidate AI interventions. For each:

- **What**: one sentence.
- **Frame**: automation (machine does the task) or augmentation (machine makes a person faster or better). Choose explicitly.
- **Frontier check**: is this inside what current AI does reliably? Propose a quick test on three to five real work samples before trusting any assumption. If samples are available, run the test and record results.
- **Value**: what improves, roughly how much.
- **Risk**: what breaks if it is wrong, and whether that is a deal-breaker or manageable.

### 3. Recommendation (`recommendation.md`)

One page. The chosen opportunity, why it beat the alternatives, the parked alternatives with one line each on why, the named risks split into deal-breakers and manageable, and the 90-day success measure stated as a number or observable change.

Present it to the user and ask the sponsor question directly: will the sponsor named in the charter agree to this success measure? Do not close the phase on assumed agreement.

## Closing the phase

When the user confirms the recommendation and sponsor agreement, in `../status.md`: check the five Sense gates, set `phase: adopt`, update `## Next actions` to point at `02-adopt/instructions.md`, and add a dated log line citing the artifacts as evidence.

`recommendation.md` is this phase's share-up artifact: written so it can be forwarded to leadership as is. Remind the user to share it.

If any gate cannot be honestly checked, say which one and what is missing. Do not advance.
