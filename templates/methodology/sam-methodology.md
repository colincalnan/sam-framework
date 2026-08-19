---
title: "Sense Adopt Move (SAM) Methodology"
type: reference
updated: {{date}}
---

# Sense Adopt Move (SAM)

A three-phase method for solving organizational problems with AI. Adapted from the Sense and Motion transformation model (senseandmotion.ai) and extended with practitioner frameworks.

The core claim: most AI initiatives fail not because the technology is wrong but because organizations stop too early. They pick a tool before understanding the work (skipping Sense), roll it out without building capability (skipping Adopt), or run pilots forever without redesigning the work (never reaching Move). BDO Canada's 2026 research found 46% of Canadian leaders experimenting with AI without ROI and only 18% embedding it into workflows. The gap that matters is between organizations redesigning work around AI and those funding disconnected pilots.

SAM is sequential in its gates but iterative in practice. You will loop back. What you may not do is skip a gate.

## Phase 1: Sense (strategy)

**Purpose:** figure out where AI actually fits and what is worth doing. The output is a decision, not a demo.

**Key questions**
- What is the problem, stated in the language of the person feeling it?
- What does the workflow actually look like today? Watch it happen. The invisible steps (the workaround spreadsheet, the hallway approval) are usually where the value is.
- Is the opportunity **automation** (the machine does the task) or **augmentation** (the machine makes a person faster or better)? These have different risk profiles, different adoption paths, and different failure modes. Choose deliberately.
- Is the task inside the frontier of what current AI does reliably? AI capability is jagged: strong at some tasks that look hard, weak at some that look easy. Test on real samples before committing, never assume from a demo.
- What is the risk if it is wrong, and who carries it? Separate deal-breakers (privacy breach, regulatory exposure, trust damage) from manageable risks (rework, slower ramp).
- What would success look like, in a number or an observable change, in 90 days?

**Typical artifacts:** data check (sensitive data in scope named by type, handling rules set, done before any real work data is read), current-state process walk, opportunity shortlist with automation/augmentation framing, risk register, a one-page recommendation.

**Exit gate:** one chosen opportunity, framed, with risks named, alternatives parked, and a success measure the sponsor has agreed to.

**Anti-patterns:** starting from a tool instead of a problem. Boiling the ocean with a transformation program when one workflow would prove the point. Trusting the org chart's version of the process instead of watching the real one.

## Phase 2: Adopt (literacy)

**Purpose:** the people involved can and will actually use it. Rule of thumb: this is 20% technology and 80% culture.

**Key questions**
- Who touches this work? Sponsor, doers, sceptics. What does each need to see before they trust it?
- What is the capability gap between what the doers can do today and what the new way requires? Be concrete: prompting, judging output quality, knowing when not to trust it.
- What builds habit? People adopt tools they use on real work, repeatedly, with quick wins. Nobody adopts from a slide deck.
- Who is afraid, and of what? Job loss, looking incompetent, being blamed for AI mistakes. Fear that is not surfaced becomes quiet sabotage.
- Who could be a champion, someone who advocates without being asked?

**Typical artifacts:** stakeholder map, capability assessment, hands-on session plans using real work items, a short "when to trust it, when to check it" guide for the task.

**Exit gate:** named users doing real tasks with the tool, hands on, more than once, without hand-holding, plus at least one champion.

**Anti-patterns:** training as a one-time event. Mandating use before demonstrating value. Measuring logins instead of work done. Ignoring the sceptics instead of recruiting the persuadable ones.

## Phase 3: Move (implementation)

**Purpose:** redesign the work around AI and ship it. A pilot that runs beside the old process forever is a failure state, not a milestone.

**Key questions**
- What does the workflow look like with the AI step embedded? What steps are removed, what new checks are added, who signs off on output?
- Where does it live? It must run in the real system of record, with real data, under the org's real access and privacy rules. A sidecar demo is still Sense.
- What happens to the old way? Retired, formally changed, or explicitly kept for defined exceptions. "Both, indefinitely" is pilot purgatory.
- Who owns it after launch? A workflow with no owner degrades to shelfware within a quarter.
- Is the success measure from the charter actually moving? Measure the work outcome, not tool usage.

**Typical artifacts:** redesigned workflow spec (before/after), rollout and cutover plan, measurement sheet, ownership and escalation note.

**Exit gate:** new way embedded in the system of record, old way retired or changed, metric measured and owned.

**Anti-patterns:** pilot purgatory. Parallel-running with no end date. Declaring victory at launch instead of at metric movement. No named owner after the project team steps away.

## Running the loop

- Small scope, full depth beats broad scope, shallow depth. One workflow through all three phases proves more than ten workflows stuck in Sense.
- When a phase surfaces something that breaks an earlier decision (the frontier test fails in Adopt, the redesign exposes a risk missed in Sense), go back, update the charter's decision log, and re-close the gate. That is the method working, not failing.
- Every working session ends by updating `status.md`: gates, next actions, log.
