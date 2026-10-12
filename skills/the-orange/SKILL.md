---
name: the-orange
description: "Positions-vs-interests negotiation: two teams, one orange, hidden complementary briefs (flesh vs peel). Half-half is legal; integration is the lesson."
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*), Bash(npm:*), Bash(formlm-cli:*), Bash(python3:*)
metadata:
  category: conflict
  group_size: 4
  duration_minutes: 20
  setting: offline
  props: [poker prop cards, 1 orange or stand-in object]
  depth: assessment-type
  language: en
  updated: 2026-10-11
---

# The Orange

Both teams want the orange. Nobody asks what for — and that one missing question is the whole lesson.

## When to use this activity

- Two teams fight over one shared resource — headcount, budget, roadmap, one engineer.
- A negotiation or stakeholder-alignment module needs a physical, fast exercise.
- The room defaults to compromise — and you want to price what compromise costs.

## What is in the folder

| File | Purpose |
|---|---|
| `the-orange-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): juicer brief, baker brief, facilitator card |
| `the-orange-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 PDF |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `the-orange-guide.md` | Run sheet: rules, minute-by-minute script, the reveal, agreement scoring |
| `the-orange-debrief.md` | 8 debrief questions + 3 debrief failure modes with rescues |
| `the-orange-assessment.json` | Pre/post measure preset: 6 items, team-level deltas |
| `the-orange-paper-form.pdf` | A4 answer sheet — print-and-fill form (workshop version) |
| `the-orange-slide-deck.pdf` | Slide deck — 12 slides for running the session, one idea per slide |
| `the-orange-slide-deck.html` | Slide deck (HTML) — present from any browser, one keypress per point, speaker notes built in |
| `the-orange-workbook.pdf` | Participant workbook — plain-language intro, guided items, notes and action pages |
| `the-orange-license.md` | License in plain language — what you may do, what you must keep |
| `the-orange-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `the-orange-start-here.md` | Start here — pick your lane, file map, print lists |

## Running it

1. Print the brief cards. Place two tables out of earshot; put one orange between them.
2. Run the pre-measure (2 min) **before** briefs go out.
3. Hand each team its confidential card. State the deadline: 8 minutes, no deal = nothing.
4. Negotiation: float, answer process questions only, never hint at the hidden facts.
5. The reveal: both cards up, read aloud. Score the agreement slips.
6. Run the debrief from `the-orange-debrief.md` — the slips are the data.
7. Run the post-measure (2 min). Report team deltas, never rankings.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/the-orange/files/the-orange.zip
unzip the-orange.zip   # -> the-orange/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `the-orange` holding this SKILL.md, every file it references, and a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable props (poker confidential briefs + facilitator card, CC BY 4.0)
curl -O https://workshopskill.com/en/activities/the-orange/files/the-orange-prop-cards.pdf

# 2. Get the A4 answer sheet (print one per participant for offline workshops)
curl -O https://workshopskill.com/en/activities/the-orange/files/the-orange-paper-form.pdf

# 3. Get the debrief questions (8 questions + 3 failure-mode rescues)
curl -O https://workshopskill.com/en/activities/the-orange/files/the-orange-debrief.md

# 4. Get the run sheet (rules + minute-by-minute script)
curl -O https://workshopskill.com/en/activities/the-orange/files/the-orange-guide.md
```

The measured result does not depend on FormLM — you can score the pre/post offline with no account (see "Score it offline" below). The live form is purely optional.

The live pre/post measure is built with the FormLM CLI. It needs a free FormLM account; the form and its data stay in your own workspace:

```bash
npm install -g @formlm/cli
formlm-cli auth login
formlm-cli smart generate --input "Pre/post measure for The Orange negotiation exercise: 6 Likert items on interest exploration, information sharing and integrative thinking — the same 6 items before and after the activity, so each participant's delta is computed automatically"
```

If the agent cannot complete the interactive `formlm-cli auth login` (headless run, CI, no browser): still run the curl steps, keep `the-orange-assessment.json` as the measure spec, and hand the login and the generate command to a human — or have a human log in once, then re-run only the generate step.

Useful preparation facts for the agent:
- Runs on two teams of 2–4; scale by adding orange pairs, each with its own tables.
- Agenda math: pre-measure 2 + activity 20 + post-measure 2 = 24 minutes total.
- A real orange makes the reveal physical; any object works as a stand-in.
- If nobody opens by minute 5, announce 3 minutes of mandatory-honest Q&A.

**Where to put the skill.** Drop the unzipped `the-orange/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/the-orange/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/the-orange/`, Qoder `~/.qoder/skills/the-orange/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- Never hint at the hidden facts — the premature half-split is the debrief's centerpiece.
- Lying about the brief is legal in this game; note it and hand it to the debrief.
- Someone should eat the orange — it closes the exercise better than any summary.

## Score it offline (no account)

The full scoring spec already ships in this folder's `the-orange-assessment.json` (the `scoring` field), so you can produce a result without FormLM — an agent can compute it locally:

1. Collect each respondent's Likert answers for every `items` question (a pre round and a post round).
2. Reverse-score the items flagged in `scoring.reverse_scored_items` (or `items[].reverse` true): `new = scale_max + scale_min - raw`.
3. Tally by `scoring.method` (`sum` adds the items) into a pre total and a post total.
4. Emit exactly `scoring.reported`: `pair_delta` (post - pre, per the top-level `unit`) and `construct_deltas` (repeat per `items[].construct` group).
5. Honour `scoring.report_note`: report pair-level change only, never an individual ranking.

Copy-paste implementation using only the standard library:

```python
import json
m = json.load(open("the-orange-assessment.json"))
sc, items = m["scoring"], m["items"]
hi, lo = len(m["scale"]["labels"]), 1            # likert bounds (this scale is 1..5)
rev = {it["id"] for it in items if it.get("reverse")}
def total(ans):                                   # ans: {item_id: score}
    return sum((hi + lo - v) if k in rev else v for k, v in ans.items())
# pair_delta = total(post) - total(pre)
# construct_deltas: per construct, take that dimension's items and apply the same two totals
print(sc["reported"], "| unit:", m["unit"], "|", sc["report_note"])
```

// Note: the `version` inside `the-orange-assessment.json` describes the scale itself and is independent of this skill's frontmatter `version`.

## Remix: make it yours

Want to rebrand this folder or package it for your own shelf? The license file (`the-orange-license.md`) spells out the tiers, and `the-orange-prop-cards.pdf` carries the print specs (poker trim, bleed, corner radius, gsm). Keep the CC BY attribution line and you're free to use it, sell it, or redistribute it.

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
