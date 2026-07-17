# Adopt phase: instructions for the agent

You are running the Adopt phase. Purpose: make sure the people involved can and will actually use what Sense chose. This phase is 20% technology and 80% culture. Read `../charter.md`, `../01-sense/recommendation.md`, and `../methodology/sam-methodology.md` first.

## Work sequence

### 1. Stakeholder map (`stakeholder-map.md`)

For each person or group touching this work: role (sponsor / doer / sceptic / affected), what they need to see before they trust the new way, and what they are afraid of. Ask the user directly about fear: job loss, looking incompetent, being blamed for AI mistakes. Unsurfaced fear becomes quiet sabotage, so name it here even if it is awkward.

### 2. Capability assessment (`capability-gap.md`)

For the doers: what the new way requires (prompting, judging output quality, knowing when not to trust it, any tool mechanics) versus what they can do today. Rate each gap small / medium / large and note who has it.

### 3. Hands-on plan (`hands-on-plan.md`)

Design two or three working sessions where doers use the tool on **real work items**, not toy examples. Each session: who, what real task, what quick win it should produce, what "good output" looks like. Include a one-page "when to trust it, when to check it" guide for the task, saved as `trust-guide.md`.

Nobody adopts from a slide deck. If the user proposes a presentation instead of hands-on work, push back once with that line of reasoning.

### 4. Run and record (`adoption-log.md`)

As sessions happen, log: date, who, task, outcome, reaction. Watch for a champion, someone who starts advocating without being asked, and name them here.

## Closing the phase

Gates need evidence, not intention: named users who have done real tasks more than once without hand-holding, and a named champion. When that is true in `adoption-log.md`, update `../status.md`: check the Adopt gates, set `phase: move`, point `## Next actions` at `03-move/instructions.md`, add a dated log line.

Then write a short `adoption-summary.md` (half a page: who is using it, on what, and the champion): this phase's share-up artifact. Remind the user to share it.

If adoption stalls, diagnose against the stakeholder map (usually an unaddressed fear or a missing quick win) before adding more training. If the tool itself fails the doers on real work, that breaks a Sense decision: reopen Sense, update the charter decision log, and re-close that gate first.
