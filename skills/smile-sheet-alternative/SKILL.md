---
name: smile-sheet-alternative
description: A 10-minute feedback question bank that goes past the smile sheet — six printable poker items capturing what landed, confidence to apply and the barrier, plus a reading guide.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: feedback-forms
  group_size: 1
  duration_minutes: 10
  setting: hybrid
  props: [poker question cards, pen per participant]
  depth: tool-type
  language: en
  updated: 2026-10-11
---

# Beyond the Smile Sheet

A reaction form that stops at satisfaction prices the next session wrong. These items keep the warmth and add the three signals you can act on.

## When to use this activity

- Your reaction form returns high satisfaction and nobody changes anything on Monday.
- You want learning and intent signals without running a certified assessment.
- You need something that fits on five index-card lines and reads in two minutes.

## What is in the folder

| File | Purpose |
|---|---|
| `smile-sheet-alternative-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): six question cards, one is a control |
| `smile-sheet-alternative-run-sheet.pdf` | Print edition: facilitator guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `smile-sheet-alternative-guide.md` | Facilitator guide: objectives, when to use, setup, minute script, the card, failure modes, variations |
| `smile-sheet-alternative-debrief.md` | Debrief: run, read the six cards, four questions, failure modes and rescues |
| `smile-sheet-alternative-license.md` | License in plain language — what you may do, what you must keep |
| `smile-sheet-alternative-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `smile-sheet-alternative-start-here.md` | Start here — pick your lane, file map, print list |

## Running it

Pick five of the six cards for your session — always keep the control card. Hand one set per table, or paste the items into a live form. Collect before people leave the room. Read the three signals (landed, confidence, barrier) separately; never average them into one score. Publish one change you made because of the form.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/smile-sheet-alternative/files/smile-sheet-alternative.zip
unzip smile-sheet-alternative.zip   # -> smile-sheet-alternative/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `smile-sheet-alternative` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable poker question deck (CC BY 4.0)
curl -O https://workshopskill.com/en/activities/smile-sheet-alternative/files/smile-sheet-alternative-prop-cards.pdf

# 2. Get the reading guide (item-by-item signals + reporting rules)
curl -O https://workshopskill.com/en/activities/smile-sheet-alternative/files/smile-sheet-alternative-debrief.md

# 3. Get the facilitator guide (what it replaces, timing, anonymity, failure modes)
curl -O https://workshopskill.com/en/activities/smile-sheet-alternative/files/smile-sheet-alternative-guide.md
```

Everything above runs with no account and no login.

Useful preparation facts for the agent:
- Group size is irrelevant — it is a form, not an exercise.
- Agenda math: frame 2 + answer 5 + read 3 = 10 minutes.
- Works on paper with a marker or pasted into any online form.
- Keep the form to five items — longer forms get abandoned half-way.

**Where to put the skill.** Drop the unzipped `smile-sheet-alternative/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/smile-sheet-alternative/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/smile-sheet-alternative/`, Qoder `~/.qoder/skills/smile-sheet-alternative/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- The free-text "one thing you will use" line is the most honest signal in the pack — trust it over the numbers.
- Pair intent with barrier every time. Confidence without a named obstacle is a wish, not a plan.
- Say the anonymity promise out loud before you collect. It is what makes honest answers arrive.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
