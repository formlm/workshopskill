---
name: the-delegation-map
description: A 25-minute, 4–10 person leadership tool that lays out everything a leader still personally owns, sorts it into Only me · Coach someone · Anyone can run, and circles the one highest-leverage hand-off for this week with a named owner, the support they get, and a review date. Poker-spec zone cards and an A3 poster included; no account, no projector.
version: 2.2.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: leadership
  group_size: 4
  duration_minutes: 25
  setting: hybrid
  props: [Only me, slide deck v2 (12 slides), participant workbook, one-page session sheet, tool preset]
  depth: tool-type
  language: en
  updated: 2026-10-10
---

# The Delegation Map

A leader lays out every task they still personally own, sorts it into three zones — Only me, Coach someone, Anyone can run — and commits to exactly one hand-off this week, with a named owner, the support that owner gets, and a review date. The map makes invisible load visible; the circled hand-off is the decision.

## When to use this activity

- A leader whose plate is full mostly with things that were never anyone's but habit.
- A peer circle of leads who each need to see what they should stop owning.
- You have 4–10 people and 25 minutes; online works if the three columns live on a shared board.

## What's in the folder

| File | Use |
|---|---|
| `the-delegation-map-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed, cut guides, branded back, blank): the The Delegation Map cards. |
| `the-delegation-map-worksheet.pdf` | The one-page session sheet, print-and-fill: three zones plus one circled hand-off, with owner, support and review date. One per group. |
| `the-delegation-map-workbook.pdf` | The participant’s copy: the sheet in plain words, the artifact as fill-in pages, session notes, a before-you-leave page (A4). |
| `the-delegation-map-slide-deck.html` | The deck as a stage tool: 12 slides, presenter drawer (S) with run-of-show clock, round timer (T), house mode (B), built-in QR, print fallback. Single offline HTML file. |
| `the-delegation-map-slide-deck.pdf` | The 12-slide deck as print — one idea per slide, A4 landscape. |
| `the-delegation-map-activity-poster.pdf` | The whole session on one wall (A3 landscape): three zones plus one circled hand-off, with owner, support and review date, the run of show, the rule. |
| `the-delegation-map-guide.md` | Facilitator guide: objectives, when to use, the mechanism table, setup, the run, the card, failure modes, variations, facilitation notes, a wall line and an agent version. |
| `the-delegation-map-debrief.md` | 12 numbered debrief questions with what each targets, plus failure modes of the debrief. |
| `the-delegation-map-start-here.md` | This page: pick a lane, see what every file is, the print list per scenario. |
| `the-delegation-map-license.md` | What you may do with this folder, in plain language; keep the attribution line. |
| `the-delegation-map-tool.json` | machine-facing file (not listed in the download table): the artifact as a machine-readable template — columns, flow, fields, prompts, watch-outs. Plain JSON, no lock-in. |
| `the-delegation-map-run-sheet.pdf` | The print edition: guide + debrief bound as one document, linked contents and PDF bookmarks. |
| `*-Letter.pdf` | US Letter paper size of every print document in this folder — same content, bookmarks and a linked contents page in each edition |

## How to run it

1. Put three columns on a wall: Only me · Coach someone · Anyone can run.
2. Dump every task the leader owns, one per note; the team may add what they see.
3. Sort each note into a zone; the leader speaks last and does not defend.
4. In Anyone can run, circle the single highest-leverage hand-off for this week.
5. Name the owner, the support they get, and a review date; each person says one sentence aloud.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/the-delegation-map/files/the-delegation-map.zip
unzip the-delegation-map.zip   # -> the-delegation-map/SKILL.md + every file + manifest
```

Unzipped you get a directory named `the-delegation-map` containing this SKILL.md, every file it references, a manifest, and the changelog.

Only want some files — anonymous, CC BY 4.0:

```bash

# 1. get the printable zone cards

curl -O https://workshopskill.com/en/activities/the-delegation-map/files/the-delegation-map-prop-cards.pdf

# 2. get the wall poster

curl -O https://workshopskill.com/en/activities/the-delegation-map/files/the-delegation-map-activity-poster.pdf

# 3. get the debrief and the guide

curl -O https://workshopskill.com/en/activities/the-delegation-map/files/the-delegation-map-debrief.md
curl -O https://workshopskill.com/en/activities/the-delegation-map/files/the-delegation-map-guide.md
```

This session needs no online form and no account — three columns, zone cards, sticky notes. There is no pre/post measure; the artifact is the map plus one circled hand-off with a named owner, support, and review date.

Prep facts for the agent:
- 4–10 people around one leader's real, current plate; the leader speaks last in Sort.
- Flow sums: dump 5 + sort 7 + circle one 4 + name it 6 + say it 3 = 25 minutes.
- No projector needed; the poster is optional and nothing requires a screen.
- Print at poker spec. One zone-card sheet per group plus the Hand-off and Review-date cards.

**Where the skill goes.** Drop the unzipped `the-delegation-map/` into your agent's skills directory and it loads automatically: Claude Code `~/.claude/skills/the-delegation-map/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/the-delegation-map/`, Qoder `~/.qoder/skills/the-delegation-map/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- If everything lands in Only me, the leader is protecting identity, not work — ask what would have to be true for someone else to do it well.
- If everything lands in Anyone can run, pull back the two notes carrying real accountability and say aloud why they stay.
- A circled hand-off with no named support is a dump; force one hour of coaching or one document before anyone leaves.

## Remix: make it yours

Want this folder under your own brand, or packaged as your own marketplace product? The license file spells out what you may do: rename the zones on the card faces, reprint the cards and poster at spec, and keep the CC BY attribution line — then use, sell, and redistribute freely.

## Attribution

Filed by hand and checked folder-to-folder — the script, timings, and prop dimensions agree with each other. CC BY 4.0 free — run it, copy it, rebrand it for your own workshop; keep the attribution line and the map stays open.
