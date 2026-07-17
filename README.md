# The SAM Project Framework

*Documentation for teams. This page explains what the framework is, how a SAM project folder works, and how to run one day to day.*

## What it is

SAM (Sense, Adopt, Move) is a three-phase method for solving organizational problems with AI. It is adapted from the Sense and Motion transformation model and extended with practitioner frameworks.

The core claim: most AI initiatives fail not because the technology is wrong but because organizations stop too early. They pick a tool before understanding the work (skipping Sense), roll it out without building capability (skipping Adopt), or run pilots forever without redesigning the work (never reaching Move). BDO Canada's 2026 research found 46% of Canadian leaders experimenting with AI without ROI, and only 18% embedding it into workflows. The gap that matters is between organizations redesigning work around AI and those funding disconnected pilots.

The three phases:

| Phase | Question it answers | Output |
|---|---|---|
| **Sense** (strategy) | Where does AI actually fit, and what is worth doing? | A decision: one chosen opportunity, framed, with risks named and a success measure the sponsor has agreed to |
| **Adopt** (literacy) | Can the people involved actually use it, and will they? | Named users doing real tasks with the tool, repeatedly, without hand-holding, plus a champion |
| **Move** (implementation) | Is the work redesigned around AI and shipped? | The new way live in the system of record, the old way retired or changed, and the success metric measured with an owner |

Phases are sequential in their gates but iterative in practice. Looping back when something breaks an earlier decision is the method working, not failing. Skipping a gate is not allowed.

## How it works: the project folder

Every SAM project is a self-contained folder. The folder carries its own instructions, so an AI coding agent (or a person) can open it cold and know exactly how to proceed. Nothing outside the folder is required.

```
<project>/
  README.md                        how to use the folder, resume instructions
  charter.md                       problem, context, people, constraints, success measure
  status.md                        single source of truth: phase, gate checklist, next actions, log
  methodology/sam-methodology.md   the full method reference
  01-sense/instructions.md         agent instructions for the Sense phase
  02-adopt/instructions.md         agent instructions for the Adopt phase
  03-move/instructions.md          agent instructions for the Move phase
```

Work artifacts are saved into the phase folder they belong to as they are produced.

Two files matter most:

- **`charter.md`** is written once at kickoff and holds the problem statement, the sponsor, the doers, the sceptics, the constraints, and the 90-day success measure. It also has a decision log: any change to scope, approach, or ownership gets a dated entry.
- **`status.md`** is the single source of truth. It records the current phase, a gate checklist for every phase, the next actions, and a dated log line for every working session. If `status.md` is stale, fixing it is the first job of the next session.

## Starting a new project

A new project begins with a short structured interview, five questions:

1. **Problem**: in one or two sentences, what is the problem and who is feeling the pain?
2. **Context**: what team owns this, and what system does the work live in today?
3. **People**: who is the sponsor, who does the work day to day, and who is likely sceptical?
4. **Constraints**: privacy or tenancy rules, approved tooling, deadlines, budget.
5. **Success**: what would be visibly different in 90 days if this worked?

The answers become the charter. The folder is scaffolded from templates, `status.md` starts at `phase: sense` with all gates unchecked, and work begins immediately on the first Sense activity.

## Working in an existing project

Open an AI agent session in the project folder and say **"let's get started"**. The agent:

1. Reads `status.md` for the current phase and open gates.
2. Reads `charter.md` for the problem, people, and constraints.
3. Reads the `instructions.md` for the current phase.
4. Reports where the project stands, proposes the next one to three concrete actions, then does the work and saves artifacts into the phase folder.

Every session ends by updating `status.md`: gates ticked where evidence exists, next actions refreshed, a dated log line appended.

## What each phase produces

**Sense** (`01-sense/`)
- `data-check.md` (first, before any real work data is read): the sensitive data in scope named by type and location, never by value, plus the handling rules every later artifact follows. Half a page, a check, not an audit program.
- `current-state.md`: the workflow as it actually happens, step by step, including the invisible steps (workaround spreadsheets, hallway approvals), with friction points ranked.
- `opportunities.md`: two to five candidate interventions, each framed explicitly as automation (the machine does the task) or augmentation (the machine makes a person faster or better), with a reliability check on real work samples, a value estimate, and risks split into deal-breakers and manageable.
- `recommendation.md`: one page. The chosen opportunity, the parked alternatives, named risks, and a 90-day success measure agreed with the sponsor.

**Adopt** (`02-adopt/`)
- `stakeholder-map.md`: sponsor, doers, sceptics, what each needs to see before they trust the new way, and what they are afraid of. Unsurfaced fear becomes quiet sabotage, so it is named here.
- `capability-gap.md`: what the new way requires versus what the doers can do today.
- `hands-on-plan.md` and `trust-guide.md`: working sessions on real work items (never toy examples), plus a one-page guide on when to trust the tool and when to check it.
- `adoption-log.md`: evidence of real use, and the named champion.
- `adoption-summary.md` at close: half a page on who is using it, on what, and the champion.

**Move** (`03-move/`)
- `workflow-redesign.md`: before/after spec with the AI step embedded, human checkpoints marked, and the old way's fate decided (retired, changed, or kept for listed exceptions; "both, indefinitely" is not an allowed answer).
- `cutover-plan.md`: where it runs (the real system of record, real data, real access rules), the cutover trigger, and the rollback condition.
- `measurement.md`: the charter's success measure, its baseline, and who reads the number. Work outcomes, not tool usage. Logins are not a metric.
- `ownership.md`: a person's name, not a team name, plus escalation path and first post-launch review date.
- `outcome.md` at close: metric movement, what to watch, and candidate follow-on problems (each a new project, not scope creep).

## Ground rules

- **Data check first.** No real work data is read until the sensitive data in scope is named and handling rules are set. Artifacts never reproduce restricted data by value: refer to sensitive data by type and location, and to external people by role, not name. This keeps every artifact safe to share by default.
- **Every phase ends in one share-up artifact.** `recommendation.md` (Sense), `adoption-summary.md` (Adopt), `outcome.md` (Move), each written so it can be forwarded to leadership as is. Visibility is part of the method: the work should be legible to the organization as it happens, not only at the end.
- **Gates are real.** The phase in `status.md` only advances when every gate for the current phase is checked, with a dated log entry citing the evidence. An agent that cannot honestly check a gate says which one and what is missing.
- **Small scope, full depth.** One workflow through all three phases proves more than ten workflows stuck in Sense.
- **Loop back deliberately.** If a later phase breaks an earlier decision (the tool fails doers on real work, the redesign exposes a missed risk), reopen that phase, log the change in the charter's decision log, re-close the gate, and continue.
- **Adopt is 20% technology, 80% culture.** Nobody adopts from a slide deck; adoption is built on real work, quick wins, and surfaced fear.
- **A pilot is not a milestone.** Move is complete when the work is redesigned, embedded, and measured. Parallel-running with no end date is pilot purgatory.

## FAQ

**Why self-contained folders?** So a project survives tool changes and team changes. Any capable AI agent, or a person with no prior context, can open the folder and continue. The method travels with the work.

**Can phases overlap?** Activities can overlap (early Adopt conversations often start during Sense), but gates close in order. You cannot close a Move gate while a Sense gate is open.

**What size problem fits?** One workflow with a nameable owner and a measurable outcome. If the problem needs an org chart to describe, split it into multiple projects.

**What if the AI turns out to be the wrong answer?** That is a successful Sense phase. The recommendation can be "not this, not now", with the reasoning recorded. That outcome costs days instead of quarters.
