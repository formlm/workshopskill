---
name: rotate-the-lead
description: A 25-minute, 8–16 person leadership tool. Give the team a real small task, then rotate who's leading every ~4 minutes — each handover restates the goal, what's done, and the next move before directing, and each lead makes one visible, owned call. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.2.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: leadership
  group_size: 8
  duration_minutes: 25
  setting: hybrid
  props: [Round 1 restatement, slide deck v2 (12 slides), participant workbook, one-page session sheet, tool preset]
  depth: tool-type
  language: en
  updated: 2026-10-10
---

# Rotate the Lead

Most teams quietly assume only "the leader" can hold the thread — set the goal, track progress, make the call. This tool rotates the pen every few minutes on a real task, forcing that invisible skill into the open: you see who can carry a round cleanly, what a handover actually requires, and how leading becomes a set of visible moves anyone can make and pass on.

## When to use this activity

- A team where leadership is stuck on one person and nobody else has practiced holding the thread.
- Before handing someone a real stretch assignment — rotate the least-senior person first.
- You have 8–16 people, one small finishable task, and 25 minutes; it runs on a shared doc online.

## What's in the folder

| File | Use |
|---|---|
| `rotate-the-lead-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed, cut guides, branded back, blank): the Rotate the Lead cards. |
| `rotate-the-lead-worksheet.pdf` | The one-page session sheet, print-and-fill: four rounds logged — restatement, the call, its owner — and the handover pattern the team kept. One per group. |
| `rotate-the-lead-workbook.pdf` | The participant’s copy: the sheet in plain words, the artifact as fill-in pages, session notes, a before-you-leave page (A4). |
| `rotate-the-lead-slide-deck.html` | The deck as a stage tool: 12 slides, presenter drawer (S) with run-of-show clock, round timer (T), house mode (B), built-in QR, print fallback. Single offline HTML file. |
| `rotate-the-lead-slide-deck.pdf` | The 12-slide deck as print — one idea per slide, A4 landscape. |
| `rotate-the-lead-activity-poster.pdf` | The whole session on one wall (A3 landscape): four rounds logged — restatement, the call, its owner — and the handover pattern the team kept, the run of show, the rule. |
| `rotate-the-lead-guide.md` | Facilitator guide: objectives, when to use, the mechanism table, setup, the run, the card, failure modes, variations, facilitation notes, a wall line and an agent version. |
| `rotate-the-lead-debrief.md` | 9 numbered debrief questions with what each targets, plus failure modes of the debrief. |
| `rotate-the-lead-start-here.md` | This page: pick a lane, see what every file is, the print list per scenario. |
| `rotate-the-lead-license.md` | What you may do with this folder, in plain language; keep the attribution line. |
| `rotate-the-lead-tool.json` | machine-facing file (not listed in the download table): the artifact as a machine-readable template — columns, flow, fields, prompts, watch-outs. Plain JSON, no lock-in. |
| `rotate-the-lead-run-sheet.pdf` | The print edition: guide + debrief bound as one document, linked contents and PDF bookmarks. |
| `*-Letter.pdf` | US Letter paper size of every print document in this folder — same content, bookmarks and a linked contents page in each edition |

## How to run it

1. Agree one real, small, finishable task and what "done" looks like; name the first lead.
2. Run four ~4-minute rounds. Each incoming lead restates goal / done-so-far / next *before* directing.
3. Each lead makes one visible call and names who owns it, then passes on a clean summary.
4. Close by having each person name one leadership move they saw work — or didn't.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/rotate-the-lead/files/rotate-the-lead.zip
unzip rotate-the-lead.zip   # -> rotate-the-lead/SKILL.md + every file + manifest
```

You get a directory named `rotate-the-lead` with this SKILL.md, every file it references, a manifest, and the changelog.

Want just some files — anonymous, CC BY 4.0:

```bash

# 1. Get the printable cards

curl -O https://workshopskill.com/en/activities/rotate-the-lead/files/rotate-the-lead-prop-cards.pdf

# 2. Get the wall poster

curl -O https://workshopskill.com/en/activities/rotate-the-lead/files/rotate-the-lead-activity-poster.pdf

# 3. Get the debrief and the guide

curl -O https://workshopskill.com/en/activities/rotate-the-lead/files/rotate-the-lead-debrief.md
curl -O https://workshopskill.com/en/activities/rotate-the-lead/files/rotate-the-lead-guide.md
```

This relay needs no online form and no account — one real task, a visible timer, and a rotating lead. There is no pre/post measure; the artifact is the finished task plus a written handover pattern (goal / done / next) the team can keep.

Prep facts for the agent:
- 8–16 people in one working group; above 12, run two parallel rounds of the same task.
- Flow sums to: set the task 4 + four rotating rounds 16 + name one move 5 = 25 minutes.
- No projector; the poster is optional and nothing needs a screen.
- Print at poker spec. One set of role cards per working group.

**Where the skill goes.** Drop the unzipped `rotate-the-lead/` into your agent's skills directory to auto-load it: Claude Code `~/.claude/skills/rotate-the-lead/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/rotate-the-lead/`, Qoder `~/.qoder/skills/rotate-the-lead/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Step-by-step for each agent: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- Restating before directing is the whole lesson — if a new lead can't, that gap is the finding, not a failure.
- Keep the timer hard. A round that drifts past four minutes lets the confident people run long and hides the pattern.
- Watch for the real manager re-taking the pen; note who it displaces.

## Adapt it: make it yours

Want to rebrand this folder or package it as your own shelf product? The license file spells out what you may do: rename the card prompts, reprint the cards and poster at spec, and keep the CC BY attribution line — then use, sell, and redistribute freely.

## Credit

Hand-filed file by file, and cross-checked inside the folder — script, timings, and prop sizes agree with each other. CC BY 4.0, free — run it, copy it, rebrand it for your own workshop; keep the attribution line and this relay stays open.
