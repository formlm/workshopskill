---
name: the-leader-checkup
description: A 25-minute, 3–10 person leadership tool. The team gives their leader structured upward feedback — what's working, what quietly blocks them, one ask — and the leader's only job is to listen without defending, then commit to one change with a follow-up date. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.2.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: leadership
  group_size: 3
  duration_minutes: 25
  setting: hybrid
  props: [Keep doing, slide deck v2 (12 slides), participant workbook, one-page session sheet, tool preset]
  depth: tool-type
  language: en
  updated: 2026-10-10
---

# The Leader Checkup

Feedback flows down easily and rarely up, so a leader who only hears what's filtered learns wrong. This is a structured upward checkup: the team names what's working, what quietly blocks them, and one ask — and the leader's only job is to listen without defending, then commit to one change.

## When to use this activity

- A leader who wants an honest read on how they're landing, not another filtered status report.
- A team where feedback flows down but never up, so small blocks quietly accumulate.
- You have 3–10 people and 25 minutes; online works if the cards live on a shared board.

## What's in the folder

| File | Use |
|---|---|
| `the-leader-checkup-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed, cut guides, branded back, blank): the The Leader Checkup cards. |
| `the-leader-checkup-worksheet.pdf` | The one-page session sheet, print-and-fill: keep / block / ask from every voice, plus the leader’s one commitment and follow-up date. One per group. |
| `the-leader-checkup-workbook.pdf` | The participant’s copy: the sheet in plain words, the artifact as fill-in pages, session notes, a before-you-leave page (A4). |
| `the-leader-checkup-slide-deck.html` | The deck as a stage tool: 12 slides, presenter drawer (S) with run-of-show clock, round timer (T), house mode (B), built-in QR, print fallback. Single offline HTML file. |
| `the-leader-checkup-slide-deck.pdf` | The 12-slide deck as print — one idea per slide, A4 landscape. |
| `the-leader-checkup-activity-poster.pdf` | The whole session on one wall (A3 landscape): keep / block / ask from every voice, plus the leader’s one commitment and follow-up date, the run of show, the rule. |
| `the-leader-checkup-guide.md` | Facilitator guide: objectives, when to use, the mechanism table, setup, the run, the card, failure modes, variations, facilitation notes, a wall line and an agent version. |
| `the-leader-checkup-debrief.md` | 11 numbered debrief questions with what each targets, plus failure modes of the debrief. |
| `the-leader-checkup-start-here.md` | This page: pick a lane, see what every file is, the print list per scenario. |
| `the-leader-checkup-license.md` | What you may do with this folder, in plain language; keep the attribution line. |
| `the-leader-checkup-tool.json` | machine-facing file (not listed in the download table): the artifact as a machine-readable template — columns, flow, fields, prompts, watch-outs. Plain JSON, no lock-in. |
| `the-leader-checkup-run-sheet.pdf` | The print edition: guide + debrief bound as one document, linked contents and PDF bookmarks. |
| `*-Letter.pdf` | US Letter paper size of every print document in this folder — same content, bookmarks and a linked contents page in each edition |

## How to run it

1. Each person writes silently: one thing working, one thing blocking (when you X, we Y), one ask.
2. Round-robin: the team speaks, the leader listens — no defending, no explaining.
3. The leader reflects back what they heard and asks one clarifying question.
4. The leader commits to one concrete change, with a follow-up date.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/the-leader-checkup/files/the-leader-checkup.zip
unzip the-leader-checkup.zip   # -> the-leader-checkup/SKILL.md + every file + manifest
```

Unzipped you get a directory named `the-leader-checkup` containing this SKILL.md, every file it references, a manifest, and the changelog.

Only want some files — anonymous, CC BY 4.0:

```bash

# 1. get the printable cards

curl -O https://workshopskill.com/en/activities/the-leader-checkup/files/the-leader-checkup-prop-cards.pdf

# 2. get the wall poster

curl -O https://workshopskill.com/en/activities/the-leader-checkup/files/the-leader-checkup-activity-poster.pdf

# 3. get the debrief and the guide

curl -O https://workshopskill.com/en/activities/the-leader-checkup/files/the-leader-checkup-debrief.md
curl -O https://workshopskill.com/en/activities/the-leader-checkup/files/the-leader-checkup-guide.md
```

This session needs no online form and no account — a circle, cards, silence to write in. There is no pre/post measure; the artifact is a keep/block/ask set the leader heard and one commitment with a follow-up date.

Prep facts for the agent:
- 3–10 people who report to, or work under, the same leader.
- Flow sums: write 7 + speak & listen 8 + reflect back 5 + commit 5 = 25 minutes.
- No projector needed; the poster is optional and nothing requires a screen.
- Print at poker spec. One card sheet per person.

**Where the skill goes.** Drop the unzipped `the-leader-checkup/` into your agent's skills directory and it loads automatically: Claude Code `~/.claude/skills/the-leader-checkup/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/the-leader-checkup/`, Qoder `~/.qoder/skills/the-leader-checkup/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- Hold the "no defending" line hardest — one defense and the team starts editing the truth.
- If the room says only "everything's great," have the leader open with a real self-critique.
- Keep blocks at behavior + impact; the moment it's about character, the room closes.

## Remix: make it yours

Want this folder under your own brand, or packaged as your own marketplace product? The license file spells out what you may do: rename the card prompts, reprint the cards and poster at spec, and keep the CC BY attribution line — then use, sell, and redistribute freely.

## Attribution

Filed by hand and checked folder-to-folder — the script, timings, and prop dimensions agree with each other. CC BY 4.0 free — run it, copy it, rebrand it for your own workshop; keep the attribution line and the checkup stays open.
