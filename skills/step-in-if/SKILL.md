---
name: step-in-if
description: A 15-minute, 8–20 person trust and belonging exercise. The group stands in a circle; read-aloud "Step in if…" statements, and anyone they're true for steps into the centre, sees who's standing with them, and steps back — no explanation, no names attached. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.1.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: trust
  group_size: 8
  duration_minutes: 15
  setting: hybrid
  props: [statement card, step-in card, look-around card, step-back card, someone-alone card, debrief card]
  depth: tool-type
  language: en
  updated: 2026-10-10
---

# Step In If…

Trust grows less from talking about the team than from physically seeing how much you already share. The group stands in a circle; someone reads a "Step in if…" statement aloud, everyone it's true for steps into the centre, pauses to see who's standing with them, and steps back. Nobody explains a step and nobody is watched for not taking one — which is exactly what makes it safe enough to be true.

## When to use this activity

- A team (or two that must work together) that's civil but hasn't yet seen how much they share.
- A new group where people are performing confidence and hiding that they feel like outsiders.
- You have 8–20 people who can stand in a circle (or raise a hand online) and 15 minutes.

## What's in the folder

| File | Use |
|---|---|
| `step-in-if-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed, cut guides, back, blank): statement, step-in, look-around, step-back, someone-alone, debrief cards |
| `step-in-if-run-sheet.pdf` | Print edition: facilitator guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper for this folder's print files — same content, every version bookmarked with a linked contents page |
| `step-in-if-guide.md` | Facilitator guide: objectives, when to use, setup, minute-by-minute script, the card, failure modes, variations |
| `step-in-if-debrief.md` | Debrief: how to run it, six numbered questions with what each targets, and the failure modes of the debrief |
| `step-in-if-start-here.md` | Start here — pick a route, set the room, print checklist |
| `step-in-if-license.md` | Plain-language license — what you can do, what you must keep |
| `step-in-if-activity-poster.pdf` | The whole thing on one wall (A3): the circle, the minute flow, the two rules. |

## How to run it

1. Everyone stands in a circle with a clear centre; state the two rules and the commitment.
2. Read 8–10 "Step in if…" statements, easiest first; anyone it's true for steps into the centre.
3. They pause a beat to see who's there — then step back. No one says why they stepped in.
4. Debrief what it felt like to step in, to stand alone, and to see others already there.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/step-in-if/files/step-in-if.zip
unzip step-in-if.zip   # -> step-in-if/SKILL.md + every file + manifest
```

You get a directory named `step-in-if` with this SKILL.md, every file it references, a manifest.

Want just some files — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/step-in-if/files/step-in-if-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/step-in-if/files/step-in-if-activity-poster.pdf

# 3. Get the debrief and the guide
curl -O https://workshopskill.com/en/activities/step-in-if/files/step-in-if-debrief.md
curl -O https://workshopskill.com/en/activities/step-in-if/files/step-in-if-guide.md
```

This exercise needs no online form and no account — a circle, a read-aloud, and a step. There is no pre/post measure; the artifact is a room that has physically seen how much it shares, and a few quiet assumptions broken in silence.

Prep facts for the agent:
- 8–20 people who can stand in a loose circle; above 20, run two circles; remote, a hand-raise replaces the step.
- Flow sums to: set circle & rules 3 + run 8–10 statements 9 + land / debrief 3 = 15 minutes.
- No projector; the poster is optional and nothing needs a screen.
- Print at poker spec. One set of statement + role cards per circle.

**Where the skill goes.** Drop the unzipped `step-in-if/` into your agent's skills directory to auto-load it: Claude Code `~/.claude/skills/step-in-if/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/step-in-if/`, Qoder `~/.qoder/skills/step-in-if/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Step-by-step for each agent: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- Hold the rule hard: people may only see who stepped in, never audit who stayed out. The watching is what kills it.
- Ease in with cheap statements so stepping feels safe, then build to the ones that matter.
- When someone stands alone, don't rush or coo — let them be seen; that's where the trust is made.

## Adapt it: make it yours

Want to rebrand this folder or package it as your own shelf product? Keep the CC BY attribution line and you're free to use, sell, and redistribute.

## Credit

Hand-filed file by file, and cross-checked inside the folder — script, timings, and prop sizes agree with each other. CC BY 4.0, free — run it, copy it, rebrand it for your own workshop; keep the attribution line and this circle stays open.
