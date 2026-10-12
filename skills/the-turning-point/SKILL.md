---
name: the-turning-point
description: A 25-minute, 4–12 person review that rebuilds a project's timeline from start to now, marks the dated moments it turned up or down, names the decision or habit behind each turn, and commits to keep one good-turn habit and kill one bad-turn habit. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: reviews
  group_size: 4
  duration_minutes: 25
  setting: hybrid
  props: [turning-point card, cause card, keep-this card, kill-this card, blank cards]
  depth: tool-type
  language: en
  updated: 2026-10-09
---

# The Turning Point

Most retrospectives collect opinions about a project; this one rebuilds its timeline — start to now — and marks the moments the story turned: up or down. Then it names the decision or habit behind each turn, so the team stops arguing about how it feels and starts seeing what caused what.

## When to use this activity

- A finished project or milestone where "how did that go?" has become a debate about feelings.
- A mid-project check-in to see whether you're accelerating or drifting.
- You have 4–12 people who were on it and 25 minutes; it runs on a shared board online.

## What's in the folder

| File | Use |
|---|---|
| `the-turning-point-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed, cut guides, back, blank): a "the turning point" card, a "what caused it" card, a "keep this" card, a "kill this" card |
| `the-turning-point-run-sheet.pdf` | Print edition: facilitator guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper for this folder's print files — same content, every version bookmarked with a linked contents page |
| `the-turning-point-guide.md` | Facilitator guide: objectives, when to use, setup, how to run it, the card, failure modes, variations, facilitation notes |
| `the-turning-point-debrief.md` | Debrief: how to run it, reading the shape of the line, four debrief questions, failure-mode table |
| `the-turning-point-start-here.md` | Start here — pick a route, set the room, print checklist |
| `the-turning-point-license.md` | Plain-language license — what you can do, what you must keep |
| `the-turning-point-activity-poster.pdf` | The whole review on one wall (A3): the timeline, the two lanes, the minute flow, the two rules. |

## How to run it

1. Sketch the timeline from kickoff to now; everyone adds real, dated moments.
2. Circle the turning points and place each in the up or down lane.
3. For each turn, name the decision or habit that caused it — not the market.
4. Commit to keep one good-turn habit and kill one bad-turn habit, each with an owner and a date.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/the-turning-point/files/the-turning-point.zip
unzip the-turning-point.zip   # -> the-turning-point/SKILL.md + every file + manifest
```

You get a directory named `the-turning-point` with this SKILL.md, every file it references, and a manifest.

Want just some files — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/the-turning-point/files/the-turning-point-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/the-turning-point/files/the-turning-point-activity-poster.pdf

# 3. Get the debrief and the guide
curl -O https://workshopskill.com/en/activities/the-turning-point/files/the-turning-point-debrief.md
curl -O https://workshopskill.com/en/activities/the-turning-point/files/the-turning-point-guide.md
```

This review needs no online form and no account — a long timeline on a wall and sticky notes. There is no pre/post measure; the artifact is the causal map and the two habits you committed to keep and kill.

Prep facts for the agent:
- 4–12 people who were on the same project from start to now.
- Flow sums to: draw the timeline 5 + mark the turns 7 + name the causes 6 + the lesson 7 = 25 minutes.
- No projector; the poster is optional and nothing needs a screen.
- Print at poker spec. One set of prompt cards per group.

**Where the skill goes.** Drop the unzipped `the-turning-point/` into your agent's skills directory to auto-load it: Claude Code `~/.claude/skills/the-turning-point/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/the-turning-point/`, Qoder `~/.qoder/skills/the-turning-point/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Step-by-step for each agent: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- Push every "it just got hard" back to a dated event with a named decision behind it.
- Watch for external-only causes; the team can only keep or kill what was in its hands.
- Reframe down-turns from blame to mechanism so the real causes get said out loud.

## Adapt it: make it yours

Want to rebrand this folder or package it as your own shelf product? The license file spells out what you may do: rename the card faces, reprint the cards and poster at spec, and keep the CC BY attribution line — then use, sell, and redistribute freely.

## Credit

Hand-filed file by file, and cross-checked inside the folder — script, timings, and prop sizes agree with each other. CC BY 4.0, free — run it, copy it, rebrand it for your own workshop; keep the attribution line and this review stays open.
