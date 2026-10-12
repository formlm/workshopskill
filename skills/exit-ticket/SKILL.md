---
name: exit-ticket
description: A 3-minute printable exit-ticket pack — each person writes three lines (learned, open question, next move) on a printed blank slip, plus a guide for reading the collected slips fast.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: feedback-forms
  group_size: 1
  duration_minutes: 3
  setting: hybrid
  props: [poker exit slips, pen per participant]
  depth: tool-type
  language: en
  updated: 2026-10-11
---

# Exit Ticket

Ninety seconds at the door that tell you what actually landed — the smallest honest check for understanding there is.

## When to use this activity

- You want a real comprehension check without spending ten minutes of class.
- You need the next session to open on the questions people actually still have.
- You want transfer signal — who intends to do something — right while the room is warm.

## What is in the folder

| File | Purpose |
|---|---|
| `exit-ticket-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): master card, three prompt cards, watch-out card — the blanks become the slips |
| `exit-ticket-run-sheet.pdf` | Print edition: facilitator guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `exit-ticket-guide.md` | Facilitator guide: objectives, when to use, setup, minute script, the card, failure modes, variations |
| `exit-ticket-debrief.md` | Debrief: run, read the three lines, three questions, failure modes and rescues |
| `exit-ticket-license.md` | License in plain language — what you may do, what you must keep |
| `exit-ticket-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `exit-ticket-start-here.md` | Start here — pick your lane, file map, print list |

## Running it

Print a batch of slips. Hand one out as the session wraps: three lines — one learned, one open question, one next move. Collect at the door, anonymous. Read the questions first; they become your opener. Count repeats, do not average. Open next session by answering one out loud.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/exit-ticket/files/exit-ticket.zip
unzip exit-ticket.zip   # -> exit-ticket/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `exit-ticket` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable exit slips (poker deck, CC BY 4.0)
curl -O https://workshopskill.com/en/activities/exit-ticket/files/exit-ticket-prop-cards.pdf

# 2. Get the reading guide (what each line tells you + sorting rules)
curl -O https://workshopskill.com/en/activities/exit-ticket/files/exit-ticket-debrief.md

# 3. Get the facilitator guide (door timing, anonymity, failure modes)
curl -O https://workshopskill.com/en/activities/exit-ticket/files/exit-ticket-guide.md
```

Everything above runs with no account and no login.

Useful preparation facts for the agent:
- Group size is irrelevant — one slip per person either way.
- Agenda math: hand out 1 + fill 1 + read at the door 1 = about 3 minutes.
- Print a batch; one card holds the three prompts.
- Works on paper or lifted into a closing online form.

**Where to put the skill.** Drop the unzipped `exit-ticket/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/exit-ticket/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/exit-ticket/`, Qoder `~/.qoder/skills/exit-ticket/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- Three lines is the ceiling at the door — a fourth prompt starts the completion rate falling.
- Read the questions first; they are the most actionable paper you will collect all week.
- Never grade it. The moment an exit ticket counts for a mark, it becomes performance.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
