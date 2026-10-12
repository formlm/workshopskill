---
name: the-decision-rights-map
description: A 25-minute, 4–10 person leadership tool. Lay out the decisions a team actually makes and, for each, name exactly one decider, who must be consulted before, and who is informed after — then find the decisions where the pen is in the wrong hand and reassign one. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.2.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: leadership
  group_size: 4
  duration_minutes: 25
  setting: hybrid
  props: [Decides, slide deck v2 (12 slides), participant workbook, one-page session sheet, tool preset]
  depth: tool-type
  language: en
  updated: 2026-10-10
---

# The Decision Rights Map

Most team friction isn't disagreement about the answer — it's two people who each thought the decision was theirs, or one person waiting for permission nobody knew they needed. This lays out the decisions a team actually makes and names, for each, exactly one decider, who must be consulted first, and who just needs to be told after. Then it finds the decisions where the pen is in the wrong hand and reassigns one.

## When to use this activity

- A team that keeps relitigating the same decisions because nobody's sure who owns them.
- A new manager inheriting a set of invisible decision rights.
- You have 4–10 people and 25 minutes; it runs on a shared board online.

## What's in the folder

| File | Use |
|---|---|
| `the-decision-rights-map-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed, cut guides, branded back, blank): the The Decision Rights Map cards. |
| `the-decision-rights-map-worksheet.pdf` | The one-page session sheet, print-and-fill: the decision grid — one decider, consulted before, informed after — plus one reassigned row. One per group. |
| `the-decision-rights-map-workbook.pdf` | The participant’s copy: the sheet in plain words, the artifact as fill-in pages, session notes, a before-you-leave page (A4). |
| `the-decision-rights-map-slide-deck.html` | The deck as a stage tool: 12 slides, presenter drawer (S) with run-of-show clock, round timer (T), house mode (B), built-in QR, print fallback. Single offline HTML file. |
| `the-decision-rights-map-slide-deck.pdf` | The 12-slide deck as print — one idea per slide, A4 landscape. |
| `the-decision-rights-map-activity-poster.pdf` | The whole session on one wall (A3 landscape): the decision grid — one decider, consulted before, informed after — plus one reassigned row, the run of show, the rule. |
| `the-decision-rights-map-guide.md` | Facilitator guide: objectives, when to use, the mechanism table, setup, the run, the card, failure modes, variations, facilitation notes, a wall line and an agent version. |
| `the-decision-rights-map-debrief.md` | 12 numbered debrief questions with what each targets, plus failure modes of the debrief. |
| `the-decision-rights-map-start-here.md` | This page: pick a lane, see what every file is, the print list per scenario. |
| `the-decision-rights-map-license.md` | What you may do with this folder, in plain language; keep the attribution line. |
| `the-decision-rights-map-tool.json` | machine-facing file (not listed in the download table): the artifact as a machine-readable template — columns, flow, fields, prompts, watch-outs. Plain JSON, no lock-in. |
| `the-decision-rights-map-run-sheet.pdf` | The print edition: guide + debrief bound as one document, linked contents and PDF bookmarks. |
| `*-Letter.pdf` | US Letter paper size of every print document in this folder — same content, bookmarks and a linked contents page in each edition |

## How to run it

1. Name the recurring decisions this team actually makes.
2. For each, write exactly one name under Decides, list who's Consulted before, and who's Informed after.
3. Circle the decisions where the decider was contested, blank, absent, or a group.
4. Reassign one out loud: name its single owner and say what changes now.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/the-decision-rights-map/files/the-decision-rights-map.zip
unzip the-decision-rights-map.zip   # -> the-decision-rights-map/SKILL.md + every file + manifest
```

You get a directory named `the-decision-rights-map` with this SKILL.md, every file it references, a manifest, and the changelog.

Want just some files — anonymous, CC BY 4.0:

```bash

# 1. Get the printable cards

curl -O https://workshopskill.com/en/activities/the-decision-rights-map/files/the-decision-rights-map-prop-cards.pdf

# 2. Get the wall poster

curl -O https://workshopskill.com/en/activities/the-decision-rights-map/files/the-decision-rights-map-activity-poster.pdf

# 3. Get the debrief and the guide

curl -O https://workshopskill.com/en/activities/the-decision-rights-map/files/the-decision-rights-map-debrief.md
curl -O https://workshopskill.com/en/activities/the-decision-rights-map/files/the-decision-rights-map-guide.md
```

This map needs no online form and no account — a board, three columns, and cards. There is no pre/post measure; the artifact is the wall of owned decisions and the one you reassigned out loud.

Prep facts for the agent:
- 4–10 people who share a set of recurring decisions.
- Flow sums to: list 5 + assign 8 + spot the unclear ones 6 + reassign one 6 = 25 minutes.
- No projector; the poster is optional and nothing needs a screen.
- Print at poker spec. One set of prompt cards per group.

**Where the skill goes.** Drop the unzipped `the-decision-rights-map/` into your agent's skills directory to auto-load it: Claude Code `~/.claude/skills/the-decision-rights-map/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/the-decision-rights-map/`, Qoder `~/.qoder/skills/the-decision-rights-map/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Step-by-step for each agent: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- "The team decides" is never an answer here — it's the finding; force a single name to own the consequence.
- Keep consulted-before clearly separate from informed-after; conflating them is how decisions stall.
- If one person ends up on every row, that's not clarity — it's a bottleneck; spread the pen.

## Adapt it: make it yours

Want to rebrand this folder or package it as your own shelf product? The license file spells out what you may do: rename the card faces, reprint the cards and poster at spec, and keep the CC BY attribution line — then use, sell, and redistribute freely.

## Credit

Hand-filed file by file, and cross-checked inside the folder — script, timings, and prop sizes agree with each other. CC BY 4.0, free — run it, copy it, rebrand it for your own workshop; keep the attribution line and this map stays open.
