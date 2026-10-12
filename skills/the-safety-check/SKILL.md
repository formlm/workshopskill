---
name: the-safety-check
description: A 20-minute, 4–12 person trust tool. Everyone privately rates four statements — I can ask a dumb question / admit a mistake / disagree with the decision-maker / take a risk without it being used against me — the team reveals the four bars, circles the lowest one, and commits to one concrete behavior that raises it, with a re-check date. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.1.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: trust
  group_size: 4
  duration_minutes: 20
  setting: hybrid
  props: [statement cards, lowest-one card, behavior card]
  depth: tool-type
  language: en
  updated: 2026-10-10
---

# The Safety Check

Psychological safety isn't a mood — it shows up in four concrete questions, and teams almost always have one that scores far below the rest. Everyone privately rates those four, the team reveals together, and the lowest-scoring one becomes the target: name a single behavior that would raise it, and commit to try it before you check again.

## When to use this activity

- A team that "gets along" but quietly holds back questions, mistakes, or disagreement.
- After something went wrong that nobody reported in time — check the "admit a mistake" bar.
- You have 4–12 people who share decisions and 20 minutes; it runs on a shared board online.

## What's in the folder

| File | Use |
|---|---|
| `the-safety-check-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed, cut guides, back, blank): four statement cards (ask a dumb question · admit a mistake · disagree with the decision-maker · take a risk without it being used against me), "the lowest one," "one behavior to raise it" |
| `the-safety-check-run-sheet.pdf` | Print edition: facilitator guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper for this folder's print files — same content, every version bookmarked with a linked contents page |
| `the-safety-check-guide.md` | Facilitator guide: objectives, when to use, setup, minute-by-minute script, the card, failure modes, variations |
| `the-safety-check-debrief.md` | Debrief: how to run it, six numbered questions with what each targets, and the failure modes of the debrief |
| `the-safety-check-start-here.md` | Start here — pick a route, set the room, print checklist |
| `the-safety-check-license.md` | Plain-language license — what you can do, what you must keep |
| `the-safety-check-activity-poster.pdf` | The whole check on one wall (A3): the four statements, the minute flow, the two rules. |

## How to run it

1. Each person privately puts a nameless 1–5 dot on all four statements.
2. Reveal together and count the dots per statement — see the shape of the four bars.
3. Circle the lowest-scoring statement; don't average it away.
4. Name one concrete behavior that would raise it, commit to it, and set a re-check date.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/the-safety-check/files/the-safety-check.zip
unzip the-safety-check.zip   # -> the-safety-check/SKILL.md + every file + manifest
```

You get a directory named `the-safety-check` with this SKILL.md, every file it references, a manifest.

Want just some files — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/the-safety-check/files/the-safety-check-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/the-safety-check/files/the-safety-check-activity-poster.pdf

# 3. Get the debrief and the guide
curl -O https://workshopskill.com/en/activities/the-safety-check/files/the-safety-check-debrief.md
curl -O https://workshopskill.com/en/activities/the-safety-check/files/the-safety-check-guide.md
```

This check needs no online form and no account — four statements on a wall and nameless dots. There is no pre/post measure; the artifact is the shape of the four bars, the named lowest one, and the behavior the team committed to try.

Prep facts for the agent:
- 4–12 people who work together and share decisions.
- Flow sums to: mark 4 + reveal 4 + find the lowest 4 + name a behavior & commit 8 = 20 minutes.
- No projector; the poster is optional and nothing needs a screen.
- Print at poker spec. One set of statement + prompt cards per group.

**Where the skill goes.** Drop the unzipped `the-safety-check/` into your agent's skills directory to auto-load it: Claude Code `~/.claude/skills/the-safety-check/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/the-safety-check/`, Qoder `~/.qoder/skills/the-safety-check/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Step-by-step for each agent: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- Keep the dots nameless — the moment a score traces to a person, the next ratings turn safe and useless.
- Aim at the single lowest bar, not the average; that's where people actually hold back.
- If everyone scores 5s, the check itself feels unsafe — say so and make it anonymous in writing.

## Adapt it: make it yours

Want to rebrand this folder or package it as your own shelf product? Keep the CC BY attribution line and you're free to use, sell, and redistribute.

## Credit

Hand-filed file by file, and cross-checked inside the folder — script, timings, and prop sizes agree with each other. CC BY 4.0, free — run it, copy it, rebrand it for your own workshop; keep the attribution line and this check stays open.
