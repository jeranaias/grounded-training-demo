# Gameday kit

Everything a team member (or their Claude Code instance) needs to arrive ready. Clone the repo,
read these three, then jump to your lane's deep docs in [`../`](../README.md).

| File | What it is |
|---|---|
| [RANGE-CARD.md](RANGE-CARD.md) | The operator's brief — pitch, numbers, architecture, the four integration sequences, runbook, the 5-minute demo, contingencies, submission. |
| [COLD-BORE.md](COLD-BORE.md) | The battle plan — scheme, the five use cases, the arsenal (12 repos), assembly, the **Build Kit** (design/data/grounding/env/consume), Orin access, the honest scorecard. |
| [TEAM-PLAN.md](TEAM-PLAN.md) | Who owns what — the five lanes, the QA→triage→build→review loop, per-member tasks, and McDonald's ramp. |

## Set up your Claude Code instance (5 minutes)

1. Install Node 18+, Git, and Claude Code. `git clone` this repo.
2. `npm install` — then `npm run dev` and open `http://localhost:3111/learn` (once the app exists on the fresh repo).
3. Tell your instance to read the docs for **your lane** (from [TEAM-PLAN.md](TEAM-PLAN.md)):
   - **Jesse / White (backend, grounding):** `../02-architecture` · `../03-data-model` · `../04-grounding-and-anchor` · `../05-arsenal-contracts` · `../08-build-guide`
   - **McDonald (frontend):** `../01-design-system` (primary) · `../06-learner-loop` · `../07-instructor-loop`
   - **Thompson (QA):** the deployed site + the QA widget; `../06-learner-loop` + `../07-instructor-loop` for intended behavior
   - **Morgan (content/SME):** `../07-instructor-loop` · `../04-grounding-and-anchor` · `../05-arsenal-contracts` · `../03-data-model`
4. You're armed. The whole spec travels with the repo — no external docs, no artifact access needed.

## The one rule that never bends
Grounded, verified, offline, human-led. Every claim cites the manual or the system refuses;
nothing `PENDING` reaches a learner. That guarantee is the product — protect it in every lane.
