---
name: silent-lineup
description: Whole-group lineups in silence: birthday round then seniority round. Non-verbal coordination reveals who leads, who follows early, and who unsticks jams.
version: 2.1.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*), Bash(npm:*), Bash(formlm-cli:*), Bash(python3:*)
metadata:
  category: leadership
  group_size: 8
  duration_minutes: 10
  setting: offline
  props: [open floor along a wall; optional poker observer cards]
  depth: assessment-type
  language: en
  updated: 2026-10-11
---

# Silent Lineup

No talking, no writing, no phones — just gestures and choices. Two lineups, ten minutes, and a debrief about who leads when words are gone.

## When to use this activity

- A leadership theme needs behavioral evidence, not role-play.
- The group needs a physical ten-minute exercise between sedentary blocks.
- You want a silent temperature check on a sensitive topic (opinion-lineup variation).

## What is in the folder

| File | Purpose |
|---|---|
| `silent-lineup-prop-cards.pdf` | Optional poker deck: rules, gesture code, observer, timing cards |
| `silent-lineup-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 PDF |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `silent-lineup-guide.md` | Facilitator guide: objectives, when to use, the mechanism table, setup, the run, the card, failure modes, variations, facilitation notes, a wall line and an agent version. |
| `silent-lineup-debrief.md` | 8 numbered debrief questions with what each targets, plus failure modes of the debrief. |
| `silent-lineup-assessment.json` | machine-facing file (not listed in the download table): pre/post measure preset: 6 items, group-level deltas |
| `silent-lineup-paper-form.pdf` | A4 answer sheet — print-and-fill form (workshop version) |
| `silent-lineup-slide-deck.pdf` | Slide deck — 12 slides for running the session, one idea per slide |
| `silent-lineup-slide-deck.html` | Slide deck (HTML) — present from any browser, one keypress per point, speaker notes built in |
| `silent-lineup-workbook.pdf` | Participant workbook — plain-language intro, guided items, notes and action pages |
| `silent-lineup-license.md` | License in plain language — what you may do, what you must keep |
| `silent-lineup-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `silent-lineup-start-here.md` | Start here — pick your lane, file map, print lists |

## Running it

1. Clear floor space along a wall. No props needed.
2. Run the pre-measure (2 min) **before** the first lineup.
3. Round one: line up by birthday, 3 minutes, total silence — then the verification walk.
4. Round two: line up by years in the company, same rules.
5. Run the debrief from `silent-lineup-debrief.md` — moves, not personalities.
6. Run the post-measure (2 min). Report group deltas, never rankings.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/silent-lineup/files/silent-lineup.zip
unzip silent-lineup.zip   # -> silent-lineup/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `silent-lineup` holding this SKILL.md, every file it references, a manifest and a changelog.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the optional poker deck (rules, gesture code, observer, timing)
curl -O https://workshopskill.com/en/activities/silent-lineup/files/silent-lineup-prop-cards.pdf

# 2. Get the A4 answer sheet (print one per participant for offline workshops)
curl -O https://workshopskill.com/en/activities/silent-lineup/files/silent-lineup-paper-form.pdf

# 3. Get the debrief questions (8 questions + 3 failure-mode rescues)
curl -O https://workshopskill.com/en/activities/silent-lineup/files/silent-lineup-debrief.md

# 4. Get the run sheet (rules + minute-by-minute script)
curl -O https://workshopskill.com/en/activities/silent-lineup/files/silent-lineup-guide.md
```

The measured result does not depend on FormLM — you can score the pre/post offline with no account (see "Score it offline" below). The live form is purely optional.

The live pre/post measure is built with the FormLM CLI. It needs a free FormLM account; the form and its data stay in your own workspace:

```bash
npm install -g @formlm/cli
formlm-cli auth login
formlm-cli smart generate --input "Pre/post measure for the Silent Lineup leadership exercise: 6 Likert items on initiative, legibility, distributed permission and early following — the same 6 items before and after the activity, so each participant's delta is computed automatically"
```

If the agent cannot complete the interactive `formlm-cli auth login` (headless run, CI, no browser): still run the curl steps, keep `silent-lineup-assessment.json` as the measure spec, and hand the login and the generate command to a human — or have a human log in once, then re-run only the generate step.

Useful preparation facts for the agent:
- The lineups need zero props — floor space along a wall is the entire setup; the poker deck is optional paper.
- Two rounds (birthday + seniority) fill ten minutes with a verification walk between.
- Agenda math: pre-measure 2 + activity 10 + post-measure 2 = 14 minutes total.
- Over 16 people, run two lines and compare how each organized itself.

**Where to put the skill.** Drop the unzipped `silent-lineup/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/silent-lineup/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/silent-lineup/`, Qoder `~/.qoder/skills/silent-lineup/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- The silence is the design — one word collapses the exercise. Restart with a smile.
- The verification walk makes the system honest; applaud fixes, not perfection.
- Debrief moves, not personalities — "what did they do that worked", not "who is a leader".

## Score it offline (no account)

The full scoring spec already ships in this folder's `silent-lineup-assessment.json` (the `scoring` field), so you can produce a result without FormLM — an agent can compute it locally:

1. Collect each respondent's Likert answers for every `items` question (a pre round and a post round).
2. Reverse-score the items flagged in `scoring.reverse_scored_items` (or `items[].reverse` true): `new = scale_max + scale_min - raw`.
3. Tally by `scoring.method` (`sum` adds the items) into a pre total and a post total.
4. Emit exactly `scoring.reported`: `pair_delta` (post - pre, per the top-level `unit`) and `construct_deltas` (repeat per `items[].construct` group).
5. Honour `scoring.report_note`: report pair-level change only, never an individual ranking.

Copy-paste implementation using only the standard library:

```python
import json
m = json.load(open("silent-lineup-assessment.json"))
sc, items = m["scoring"], m["items"]
hi, lo = len(m["scale"]["labels"]), 1            # likert bounds (this scale is 1..5)
rev = {it["id"] for it in items if it.get("reverse")}
def total(ans):                                   # ans: {item_id: score}
    return sum((hi + lo - v) if k in rev else v for k, v in ans.items())
# pair_delta = total(post) - total(pre)
# construct_deltas: per construct, take that dimension's items and apply the same two totals
print(sc["reported"], "| unit:", m["unit"], "|", sc["report_note"])
```

// Note: the `version` inside `silent-lineup-assessment.json` describes the scale itself and is independent of this skill's frontmatter `version`.

## Remix: make it yours

Want to rebrand this folder or package it for your own shelf? The license file spells out what you may do: edit the deck placeholders, reprint the cards and poster at spec, and keep the CC BY attribution line — then use, sell, or redistribute freely.

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
