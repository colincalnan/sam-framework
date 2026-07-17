---
name: sam
description: Bootstrap and run a Sense Adopt Move (SAM) problem-solving project for organizational AI work. Use when Colin wants to start structured work on an org problem ("start a SAM project", "new SAM engagement", "run sense adopt move on this"), or to resume one ("let's get started", "where are we") in or near a folder containing a SAM status.md.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep, AskUserQuestion
---

# SAM: Sense Adopt Move project runner

SAM is a three-phase method for solving organizational problems with AI: **Sense** (strategy, where AI actually fits), **Adopt** (literacy, whether people can and will use it), **Move** (implementation, redesigning the work and shipping, never stalling at a pilot).

This skill has two modes. Decide which one applies first.

## Mode detection

1. Look for a `status.md` with `sam_project: true` in its frontmatter, in this order: the current working directory, a folder the user named, then `projects/sam/*/status.md`.
2. Found one and the user's request refers to that project (or they just said "let's get started"): **Resume mode**.
3. Otherwise: **Bootstrap mode**.

If multiple SAM projects exist and it is ambiguous which one, list them by title and current phase and ask.

## Bootstrap mode: create a new SAM project

### Step 1: interview

Ask these in one batch, conversationally. Do not scaffold anything until answered.

1. **Problem**: in one or two sentences, what is the problem and who is feeling the pain?
2. **Context**: what team or org owns this, and what system does the work live in today (CRM, email, spreadsheets, a tool)?
3. **People**: who is the sponsor, who actually does the work day to day, and who is likely sceptical?
4. **Constraints**: privacy or tenancy rules, approved tooling, deadlines, budget, anything that bounds the solution space.
5. **Success**: what would be visibly different in 90 days if this worked?

Also confirm where to create the project. Default: `projects/sam/<slug>/` where `<slug>` is a short kebab-case name derived from the problem. If Colin is working in a different repo (e.g. a work machine), create it wherever he says.

### Step 2: scaffold

Copy every file from this skill's `templates/` directory into the target folder, preserving structure:

```
<target>/
  README.md                      how to use this folder, resume instructions
  charter.md                     filled in from the interview
  status.md                      phase tracker, starts at sense
  methodology/sam-methodology.md the full method reference, self-contained
  01-sense/instructions.md       how to run the Sense phase
  02-adopt/instructions.md       how to run the Adopt phase
  03-move/instructions.md        how to run the Move phase
```

Then:
- Fill `charter.md` with the interview answers (replace every `{{placeholder}}`).
- In `status.md`, set the title, today's date, and `phase: sense`. Leave all gates unchecked.
- In `README.md`, set the project title.

The folder must be fully self-contained after this step: someone with none of this workspace, and any coding agent, must be able to open it and continue using only the files inside. Never reference this skill, this workspace, or Colin's wiki from inside the generated files.

### Step 3: start Sense

Do not stop after scaffolding. Read `01-sense/instructions.md` and begin the phase: propose the first two or three Sense actions from the charter and ask which to run.

## Resume mode: continue an existing SAM project

1. Read `status.md`, `charter.md`, and the `instructions.md` for the current phase.
2. Read any artifact files already in the current phase folder.
3. Report in a few sentences: what the project is, what phase it is in, which gates are done, what was last worked on.
4. Propose the next one to three concrete actions from the phase instructions. Ask which to run, then do the work and write artifacts into the phase folder.

## Rules that apply in both modes

- **Gates are real.** Only advance `phase` in `status.md` when every gate for the current phase is checked. When advancing, add a dated line to the `## Log` in `status.md` saying what evidence closed the gates.
- **Every working session updates `status.md`**: tick gates, refresh `## Next actions`, append to `## Log`.
- **Artifacts live in the phase folders** (`01-sense/`, `02-adopt/`, `03-move/`), kebab-case filenames, markdown only.
- **No em dashes** in any generated content. Use commas, periods, or rewrite.
- **Internal use only.** SAM language stays inside work folders, never in public content, per the open branding question in `wiki/concepts/ai/sense-and-motion-method.md` (this rule is for you, do not write it into generated projects).
