---
name: training-needs-survey
description: A 15-minute pre-course training-needs questionnaire — six printable poker items capturing current ability, target ability, priority and the cost of the gap, plus a guide for turning answers into a curriculum.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: feedback-forms
  group_size: 1
  duration_minutes: 15
  setting: hybrid
  props: [poker prompt cards, pen per participant]
  depth: tool-type
  language: en
  updated: 2026-10-11
---

# Training Needs Survey

Most courses are built on what the trainer assumes. This survey moves the evidence up front, before you design a slide.

## When to use this activity

- You are about to design a course and are guessing what the room needs.
- A cohort arrives with wildly different starting points and you need to split the track.
- You need the cost of the gap in participants’ own words to open the session.

## What is in the folder

| File | Purpose |
|---|---|
| `training-needs-survey-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): six prompt cards, one is a control |
| `training-needs-survey-run-sheet.pdf` | Print edition: facilitator guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `training-needs-survey-guide.md` | Facilitator guide: objectives, when to use, setup, minute script, the card, failure modes, variations |
| `training-needs-survey-debrief.md` | Debrief: run, read the six items, four questions, failure modes and rescues |
| `training-needs-survey-license.md` | License in plain language — what you may do, what you must keep |
| `training-needs-survey-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `training-needs-survey-start-here.md` | Start here — pick your lane, file map, print list |

## Running it

Send the survey before the agenda is locked. Six items: current ability, target, cost, priority, format, and one control. Cluster the free-text by theme and count — the biggest theme becomes your session spine, the outliers your optional track. Pair every need with its cost line. Report one line back before the course.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/training-needs-survey/files/training-needs-survey.zip
unzip training-needs-survey.zip   # -> training-needs-survey/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `training-needs-survey` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable poker prompt deck (CC BY 4.0)
curl -O https://workshopskill.com/en/activities/training-needs-survey/files/training-needs-survey-prop-cards.pdf

# 2. Get the sorting guide (per-item signals + curriculum rules)
curl -O https://workshopskill.com/en/activities/training-needs-survey/files/training-needs-survey-debrief.md

# 3. Get the facilitator guide (when to send, how to run, failure modes)
curl -O https://workshopskill.com/en/activities/training-needs-survey/files/training-needs-survey-guide.md
```

Everything above runs with no account and no login.

Useful preparation facts for the agent:
- Send before enrolment closes — after the agenda is fixed it is decoration.
- Agenda math: frame 2 + answer 10 + sort 3 = 15 minutes.
- Six items; a needs survey longer than ten minutes gets abandoned.
- Works on paper or pasted into any pre-course online form.

**Where to put the skill.** Drop the unzipped `training-needs-survey/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/training-needs-survey/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/training-needs-survey/`, Qoder `~/.qoder/skills/training-needs-survey/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- If the design is already locked, do not send it — a needs survey that cannot change anything burns trust.
- Sort by cluster size, not by the loudest single answer.
- The cost line is the gold: it becomes the opening slide in the room’s own words.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
