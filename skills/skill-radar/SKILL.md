---
name: skill-radar
description: A 20-minute, 6–16 person self-assessment tool. Each person rates themselves 1–5 across five or six role-specific axes, connects the points into a radar (spider) chart, overlays the shape the role needs, and targets the one short spoke. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.1.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: self-assessment
  group_size: 6
  duration_minutes: 20
  setting: hybrid
  props: [choose-axes card, self-rate card, plot card, target-shape card, the-gap card, one-invest card]
  depth: tool-type
  language: en
  updated: 2026-10-10
---

# Skill Radar

Self-assessments usually collapse into one confidence number, which hides the thing that matters: you can be strong everywhere except the one axis your role lives by. A radar keeps the detail — rate yourself 1–5 on each spoke, connect the points, and the shape shows exactly where to invest against the target the role actually needs.

## When to use this activity

- Someone preparing for, or already in, a role and wanting a concrete read on where to invest — not a generic score.
- A manager and report who need a non-blaming feedback conversation about capability.
- You have 6–16 people (or work solo) and 20 minutes; it runs on a shared doc online.

## What's in the folder

| File | Use |
|---|---|
| `skill-radar-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed, cut guides, back, blank): choose-axes, self-rate, plot, target-shape, the-gap, one-invest cards |
| `skill-radar-run-sheet.pdf` | Print edition: facilitator guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper for this folder's print files — same content, every version bookmarked with a linked contents page |
| `skill-radar-guide.md` | Facilitator guide: goal, setup, minute script, ground rules, variations |
| `skill-radar-debrief.md` | Debrief questions + three rescues |
| `skill-radar-start-here.md` | Start here — pick a route, set the room, print checklist |
| `skill-radar-license.md` | Plain-language license — what you can do, what you must keep |
| `skill-radar-activity-poster.pdf` | The whole read on one wall (A3): the radar shape, the minute flow, the two rules. |

## How to run it

1. Name 5–6 capability axes specific to this role — not generic ones.
2. Rate yourself 1–5 on each spoke and connect the points into a shape.
3. Overlay, in a second colour, the shape the role actually needs.
4. Mark the one spoke furthest from target, and name a single action to push it out — with a re-plot date.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/skill-radar/files/skill-radar.zip
unzip skill-radar.zip   # -> skill-radar/SKILL.md + every file + manifest
```

You get a directory named `skill-radar` with this SKILL.md, every file it references, a manifest.

Want just some files — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/skill-radar/files/skill-radar-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/skill-radar/files/skill-radar-activity-poster.pdf

# 3. Get the debrief and the guide
curl -O https://workshopskill.com/en/activities/skill-radar/files/skill-radar-debrief.md
curl -O https://workshopskill.com/en/activities/skill-radar/files/skill-radar-guide.md
```

This radar needs no online form and no account — a blank five- or six-spoke grid and two pens. There is no pre/post measure; the artifact is each person's plotted shape against the target, the one short spoke, and a single action with a re-plot date.

Prep facts for the agent:
- 6–16 people assessing a shared role; below 6, run it as a self-only exercise.
- Flow sums to: choose axes 4 + plot 6 + overlay target 5 + find gap & invest 5 = 20 minutes.
- No projector; the poster is optional and nothing needs a screen.
- Print at poker spec. One set of cards per person.

**Where the skill goes.** Drop the unzipped `skill-radar/` into your agent's skills directory to auto-load it: Claude Code `~/.claude/skills/skill-radar/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/skill-radar/`, Qoder `~/.qoder/skills/skill-radar/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Step-by-step for each agent: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- Read the shape, not the average — that's the entire reason a radar beats a score.
- Keep it five or six axes; a dozen axes hides the one gap again behind noise.
- It's self-versus-the-role's-target, never a ranking of people.

## Adapt it: make it yours

Want to rebrand this folder or package it as your own shelf product? The white-label guide in the folder (the "white-label & marketplace guide" row in the file list) spells out renaming the axes and card prompts, the card and poster print specs, and the packaging steps. Keep the CC BY attribution line and you're free to use, sell, and redistribute.

## Credit

Hand-filed file by file, and cross-checked inside the folder — script, timings, and prop sizes agree with each other. CC BY 4.0, free — run it, copy it, rebrand it for your own workshop; keep the attribution line and this radar stays open.
