# Kickoff prompts — paste one into your Claude Code instance

Each teammate: clone the repo, open a terminal in it, run `claude`, and paste **your** block below
as your first message. It tells your instance who you are, what to read, and your first job.
Everyone reads `RANGE-CARD.md` + `COLD-BORE.md` first — these prompts point your instance at the
rest of your lane.

> Repo until the fresh one exists: `git clone https://github.com/jeranaias/grounded-training-demo`
> then `cd grounded-training-demo`. Once `SchoolCircleLMS` is stood up, use that instead — the same
> `docs/` travels with it.

---

## Morgan (Jesse) — Lead · grounding, integration & corpus

```
I'm Morgan, lead on this hackathon build (SchoolCircleLMS — a grounded, offline, human-led
training platform for the Marine Corps). You are my pair for the backend, grounding, and
integration lane, and you'll also help me run the content/SME guardrail.

Read these in order, then give me a one-paragraph confirmation of the plan and the single most
important thing to get right first:
- docs/gameday/RANGE-CARD.md and docs/gameday/COLD-BORE.md (mission + wiring)
- docs/README.md, then docs/02-architecture.md, docs/04-grounding-and-anchor.md,
  docs/05-arsenal-contracts.md, docs/08-build-guide.md
- docs/03-data-model.md and docs/07-instructor-loop.md (for the SME/ratify side)

The non-negotiable: every claim cites the manual or the system refuses; nothing PENDING reaches a
learner. Anchor (the grounding engine on the Orin) is the source of truth — do not let anything
fall back to an ungrounded answer. My first job is standing Anchor up and wiring the four
integration sequences from the Range Card. Walk me through it step by step and stop for my go
before any push.
```

## White — Backend & function (LMS host)

```
I'm White, backend and app-host lead on this hackathon build (SchoolCircleLMS — a grounded,
offline, human-led Marine Corps training platform). You are my pair for the Next.js/Prisma app,
the API routes, and the data lifecycle.

Read these, then confirm the plan and flag anything in the data model you'd change:
- docs/gameday/RANGE-CARD.md and docs/gameday/COLD-BORE.md (mission + wiring)
- docs/03-data-model.md (the Prisma schema — this is authoritative), docs/02-architecture.md,
  docs/05-arsenal-contracts.md, docs/04-grounding-and-anchor.md

My first job: stand up the data layer — migrate the schema and seed one TC 3-22.9 course, one
instructor, one learner. Then own the API contracts each screen calls. The human-in-the-loop
review must be real: nothing with status PENDING is ever served to a learner. Give me the exact
commands and the seed script, and stop for my go before any push.
```

## McDonald — Frontend (mentored, new to development)

```
I'm McDonald. I'm new to software development — I've never used GitHub or written code before, so
please teach as you go: explain what each command does before I run it, keep steps small, and
never assume I know a term. You are my pair-programmer and my patient guide on the frontend lane
of a hackathon build (SchoolCircleLMS, a training platform for the Marine Corps).

First, help me get set up and oriented:
- Confirm I have Node (run `node --version`) and Git (`git --version`); if either is missing, walk
  me through installing it on Windows.
- Read docs/01-design-system.md — this is how everything should look (the colors, the shell, the
  components). It's my source of truth. Summarize it for me in plain English.
- Read docs/06-learner-loop.md and docs/07-instructor-loop.md so we both know what the screens do.
- Open the live example so I can see the target: docs points to the showcase at
  app.html — open it in a browser and describe what I'm looking at.

Then give me ONE small, safe first task: pick a single screen or component from the design system
and let's build it together, one piece at a time. Explain every step. I'll tell you when I'm ready
to move on. Don't push anything to GitHub without walking me through it first.
```

## Thompson — QA & product voice

```
I'm Thompson, the QA and product voice on this hackathon build (SchoolCircleLMS — a grounded,
offline, human-led Marine Corps training platform). I'm testing it as a Marine would actually use
it. I don't need to write code.

Read these so you know what "correct" looks like, then help me build a test plan:
- docs/gameday/RANGE-CARD.md (esp. the 5-minute demo / run-of-show)
- docs/06-learner-loop.md and docs/07-instructor-loop.md (what each screen is supposed to do)

Then help me:
1. Walk the live showcase (jeranaias.github.io/grounded-training-demo — the landing page and
   /app.html) as a student AND as an instructor, and list what I should try to break.
2. For every bug OR idea, I'll use the QA widget (the button at the bottom-left of the app) — it
   auto-captures where I am and opens a GitHub issue. Help me write each one clearly: what I did,
   what I expected, what happened, and how bad it is (block-the-demo / annoying / nice-to-have).
3. Help me rank the issue board and shape the 5-minute run-of-show from a judge's eyes — what
   would make someone say "wow."
```

---

**Guardrails baked in:** every prompt tells the instance to stop before pushing, and reinforces the
one rule — grounded, verified, offline, human-led. Nothing ungrounded, nothing PENDING, ever
reaches a learner.
