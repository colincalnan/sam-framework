# {{project_title}}

A Sense Adopt Move (SAM) project. This folder is self-contained: everything needed to run the method is inside it.

## How to work in this folder

Open an AI coding agent session in this folder and say **"let's get started"**. The agent should:

1. Read `status.md` to find the current phase and open gates.
2. Read `charter.md` for the problem, people, and constraints.
3. Read the `instructions.md` in the current phase folder.
4. Propose the next one to three actions, then do the work and save artifacts into the phase folder.

If you are the agent reading this: follow those four steps now, then update `status.md` before the session ends.

## Folder map

| Path | What it is |
|---|---|
| `charter.md` | The problem, context, stakeholders, constraints, success measure |
| `status.md` | Single source of truth: current phase, gate checklist, next actions, log |
| `methodology/sam-methodology.md` | The full SAM method reference |
| `01-sense/` | Strategy phase: instructions plus generated artifacts |
| `02-adopt/` | Literacy phase: instructions plus generated artifacts |
| `03-move/` | Implementation phase: instructions plus generated artifacts |

## Ground rules

- **Data check first.** No real work data is read until `01-sense/data-check.md` names the sensitive data in scope and its handling rules.
- **Artifacts never reproduce restricted data by value.** Refer to sensitive data by type and location, and to external people by role, not name.
- **Every phase ends in one share-up artifact** (`recommendation.md`, `adoption-summary.md`, `outcome.md`), written so it can be forwarded to leadership as is.
- `status.md` is updated every working session. If it is stale, fix it first.
- Phases advance only when every gate in `status.md` is checked, with a dated log entry saying what evidence closed them.
- Artifacts are markdown files with kebab-case names, saved in the phase folder they belong to.
