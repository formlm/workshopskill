---
name: common-ground
description: Group icebreaker with a scoring engine: facts true of everyone score 1, surprising grounds score 3, opinions score 0, every member verifies every line.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*), Bash(npm:*), Bash(formlm-cli:*), Bash(python3:*)
metadata:
  category: icebreakers
  group_size: 3
  duration_minutes: 15
  setting: hybrid
  props: [poker record & scoring cards, pens]
  depth: assessment-type
  language: en
  updated: 2026-10-11
---

# Common Ground

Find what everyone at the table shares — but the money is in the surprises. The hunt forces the questions nobody asks in week one.

## When to use this activity

- A merged or cross-department group needs real connection, not just names.
- You want an icebreaker with measurable outcomes — this one has a pre/post measure.
- The room is online; breakout rooms of four work fine.

## What is in the folder

| File | Purpose |
|---|---|
| `common-ground-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): recorder card and scoring card |
| `common-ground-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 PDF |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `common-ground-guide.md` | Run sheet: scoring rule, minute-by-minute script, grouping rules, variations |
| `common-ground-debrief.md` | 8 debrief questions + 3 debrief failure modes with rescues |
| `common-ground-assessment.json` | Pre/post measure preset: 6 items, group-level deltas |
| `common-ground-paper-form.pdf` | A4 answer sheet — print-and-fill form (workshop version) |
| `common-ground-slide-deck.pdf` | Slide deck — 12 slides for running the session, one idea per slide |
| `common-ground-slide-deck.html` | Slide deck (HTML) — present from any browser, one keypress per point, speaker notes built in |
| `common-ground-workbook.pdf` | Participant workbook — plain-language intro, guided items, notes and action pages |
| `common-ground-license.md` | License in plain language — what you may do, what you must keep |
| `common-ground-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `common-ground-start-here.md` | Start here — pick your lane, file map, print lists |

## Running it

1. Print one card set per group (recorder + scoring cards).
2. Run the pre-measure (2 min) **before** groups form.
3. State the scoring rule aloud: ordinary ground 1 pt, surprising ground 3 pts, opinions 0, everyone verifies.
4. The hunt: 10 minutes. At minute 5 announce "3-point grounds now score 5" if groups camp on easy facts.
5. Read-out: each group reads only its two highest-scoring grounds.
6. Run the debrief from `common-ground-debrief.md`.
7. Run the post-measure (2 min). Report group deltas, never rankings.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/common-ground/files/common-ground.zip
unzip common-ground.zip   # -> common-ground/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `common-ground` holding this SKILL.md, every file it references, and a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable props (poker recorder + scoring cards, CC BY 4.0)
curl -O https://workshopskill.com/en/activities/common-ground/files/common-ground-prop-cards.pdf

# 2. Get the A4 answer sheet (print one per participant for offline workshops)
curl -O https://workshopskill.com/en/activities/common-ground/files/common-ground-paper-form.pdf

# 3. Get the debrief questions (8 questions + 3 failure-mode rescues)
curl -O https://workshopskill.com/en/activities/common-ground/files/common-ground-debrief.md

# 4. Get the run sheet (minute-by-minute script)
curl -O https://workshopskill.com/en/activities/common-ground/files/common-ground-guide.md
```

The measured result does not depend on FormLM — you can score the pre/post offline with no account (see "Score it offline" below). The live form is purely optional.

The live pre/post measure is built with the FormLM CLI. It needs a free FormLM account; the form and its data stay in your own workspace:

```bash
npm install -g @formlm/cli
formlm-cli auth login
formlm-cli smart generate --input "Pre/post measure for the Common Ground group exercise: 6 Likert items on curiosity, second questions, listening and safety to disagree — the same 6 items before and after the activity, so each participant's delta is computed automatically"
```

If the agent cannot complete the interactive `formlm-cli auth login` (headless run, CI, no browser): still run the curl steps, keep `common-ground-assessment.json` as the measure spec, and hand the login and the generate command to a human — or have a human log in once, then re-run only the generate step.

Useful preparation facts for the agent:
- Scales by tables: 4 groups of 4 = 16 people run in parallel, one card set per group.
- Agenda math: pre-measure 2 + activity 15 + post-measure 2 = 19 minutes total.
- Online: breakout rooms of four, recorder card shared on screen, one person types.
- Best score on record: 23 points. Announce it — it makes groups hunt harder.

**Where to put the skill.** Drop the unzipped `common-ground/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/common-ground/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/common-ground/`, Qoder `~/.qoder/skills/common-ground/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- The inflation announcement at minute five is the activity — do not skip it when groups camp.
- Verification by the quietest member first; the loudest voice always claims "true for me" fastest.
- Praise a false-verification confession louder than a 3-point ground — that is the safety culture forming.

## Score it offline (no account)

The full scoring spec already ships in this folder's `common-ground-assessment.json` (the `scoring` field), so you can produce a result without FormLM — an agent can compute it locally:

1. Collect each respondent's Likert answers for every `items` question (a pre round and a post round).
2. Reverse-score the items flagged in `scoring.reverse_scored_items` (or `items[].reverse` true): `new = scale_max + scale_min - raw`.
3. Tally by `scoring.method` (`sum` adds the items) into a pre total and a post total.
4. Emit exactly `scoring.reported`: `pair_delta` (post - pre, per the top-level `unit`) and `construct_deltas` (repeat per `items[].construct` group).
5. Honour `scoring.report_note`: report pair-level change only, never an individual ranking.

Copy-paste implementation using only the standard library:

```python
import json
m = json.load(open("common-ground-assessment.json"))
sc, items = m["scoring"], m["items"]
hi, lo = len(m["scale"]["labels"]), 1            # likert bounds (this scale is 1..5)
rev = {it["id"] for it in items if it.get("reverse")}
def total(ans):                                   # ans: {item_id: score}
    return sum((hi + lo - v) if k in rev else v for k, v in ans.items())
# pair_delta = total(post) - total(pre)
# construct_deltas: per construct, take that dimension's items and apply the same two totals
print(sc["reported"], "| unit:", m["unit"], "|", sc["report_note"])
```

// Note: the `version` inside `common-ground-assessment.json` describes the scale itself and is independent of this skill's frontmatter `version`.

## Remix: make it yours

Want to rebrand this folder or package it for your own shelf? Under CC BY you can swap the deck placeholders, the card and poster art, and the packaging yourself. Keep the attribution line and you're free to use it, sell it, or redistribute it.

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
