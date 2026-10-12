---
name: training-evaluation-form
description: A Kirkpatrick-ready training evaluation pack — 8 reaction items, confidence self-reports, keep/change questions, and a day-30 follow-up for Level 3 behavior evidence.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*), Bash(npm:*), Bash(formlm-cli:*), Bash(python3:*)
metadata:
  category: feedback-forms
  group_size: 1
  duration_minutes: 7
  setting: hybrid
  props: [poker evaluation cards, pens, an email client for the day-30 follow-up]
  depth: assessment-type
  language: en
  updated: 2026-10-11
---
# Training Evaluation Form

Most evaluation stops at satisfaction. This pack walks Level 1 to Level 3 with honest boundaries, and ends as a one-page report a manager can forward without translation.

## When to use this activity

- A corporate training program ends and management expects evidence, not applause.
- A repeat program needs a keep/change list, not just trend lines.
- A quality system (TTQS, QF-style records) asks for training-effectiveness documentation at room level.

## What is in the folder

| File | Purpose |
|---|---|
| `training-evaluation-form-prop-cards.pdf` | Poker-spec print-ready evaluation deck: instruction, reaction-item, confidence, keep/change cards |
| `training-evaluation-form-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 PDF |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `training-evaluation-form-guide.md` | Facilitator guide: level coverage, Level 2 proxy, day-30 follow-up, failure modes |
| `training-evaluation-form-debrief.md` | Reading the results: item table, day-30 email template, management one-pager |
| `training-evaluation-form-assessment.json` | Full question set: 8 items + 3 self-reports + 2 open + 3 day-30 follow-up, plain JSON |
| `training-evaluation-form-paper-form.pdf` | A4 answer sheet — print-and-fill form (workshop version) |
| `training-evaluation-form-slide-deck.pdf` | Slide deck — 11 slides for running the session, one idea per slide |
| `training-evaluation-form-slide-deck.html` | Slide deck (HTML) — present from any browser, one keypress per point, speaker notes built in |
| `training-evaluation-form-workbook.pdf` | Participant workbook — plain-language intro, guided items, notes and action pages |
| `training-evaluation-form-license.md` | License in plain language — what you may do, what you must keep |
| `training-evaluation-form-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `training-evaluation-form-start-here.md` | Start here — pick your lane, file map, print lists |

## Running it

1. Print one evaluation-card set per participant; hand out in the last minutes of the final session.
2. Read with `training-evaluation-form-debrief.md`: item means first, confidence second, keep/change lists last.
3. On the training day itself, schedule the day-30 email (template in the debrief sheet) — before you forget who was in the room.
4. At day 30, send it; a third of the response rate is normal and still enough.
5. Fill the management one-pager from the template — one page is the ceiling, not the starting point.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/training-evaluation-form/files/training-evaluation-form.zip
unzip training-evaluation-form.zip   # -> training-evaluation-form/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `training-evaluation-form` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable evaluation cards (poker deck, CC BY 4.0)
curl -O https://workshopskill.com/en/activities/training-evaluation-form/files/training-evaluation-form-prop-cards.pdf

# 2. Get the A4 answer sheet (print one per participant for offline workshops)
curl -O https://workshopskill.com/en/activities/training-evaluation-form/files/training-evaluation-form-paper-form.pdf

# 3. Get the results-reading guide (item table + one-pager template)
curl -O https://workshopskill.com/en/activities/training-evaluation-form/files/training-evaluation-form-debrief.md

# 4. Get the facilitator guide (levels, day-30 follow-up)
curl -O https://workshopskill.com/en/activities/training-evaluation-form/files/training-evaluation-form-guide.md

# 5. Build the live online evaluation (8 items + follow-up, see training-evaluation-form-assessment.json)
```

The measured result does not depend on FormLM — you can score the pre/post offline with no account (see "Score it offline" below). The live form is purely optional.

The live pre/post measure is built with the FormLM CLI. It needs a free FormLM account; the form and its data stay in your own workspace:

```bash
npm install -g @formlm/cli
formlm-cli auth login
formlm-cli smart generate --input "Training evaluation form for corporate training programs: 8 anonymous Likert reaction items (1-5) across relevance, depth, instructor, materials, exercises, logistics, workload and overall value, 3 confidence self-report items (level-2 proxy), 2 open keep/change questions for the next run, plus a 3-item 30-day follow-up email (level-3 behavior check). Produces a management one-pager with item means, confidence deltas and day-30 behavior counts"
```

If the agent cannot complete the interactive `formlm-cli auth login` (headless run, CI, no browser): still run the curl steps, keep `training-evaluation-form-assessment.json` as the measure spec, and hand the login and the generate command to a human — or have a human log in once, then re-run only the generate step.

Useful preparation facts for the agent:
- Works for any group size; the fixed numbers are 7 minutes of participant time on the day, 30 seconds at day 30, and 20 minutes of reading for a cohort of 20.
- Expect about a third of the in-room response rate on the day-30 email; that is normal and still enough for behavior evidence.
- No projector needed; the in-room part runs on cards and pens, the follow-up on an email client you already own.
- Print at poker. One sheet covers one participant.

**Where to put the skill.** Drop the unzipped `training-evaluation-form/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/training-evaluation-form/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/training-evaluation-form/`, Qoder `~/.qoder/skills/training-evaluation-form/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- Report levels in separate lines, never averaged together — the gap between reaction and behavior is the finding.
- Self-reports without a baseline are labeled "self-report, no baseline" — one honest line beats a decorated chart.
- Level 4 is out of scope for any form; saying so out loud is what keeps the other three levels believable.

## Score it offline (no account)

The full scoring spec already ships in this folder's `training-evaluation-form-assessment.json` (the `scoring` field), so you can produce a result without FormLM — an agent can compute it locally:

1. Collect each respondent's Likert answers for every `items` question (a pre round and a post round).
2. Reverse-score the items flagged in `scoring.reverse_scored_items` (or `items[].reverse` true): `new = scale_max + scale_min - raw`.
3. Tally by `scoring.method` (`sum` adds the items) into a pre total and a post total.
4. Emit exactly `scoring.reported`: `pair_delta` (post - pre, per the top-level `unit`) and `construct_deltas` (repeat per `items[].construct` group).
5. Honour `scoring.report_note`: report pair-level change only, never an individual ranking.

Copy-paste implementation using only the standard library:

```python
import json
m = json.load(open("training-evaluation-form-assessment.json"))
sc, items = m["scoring"], m["items"]
hi, lo = len(m["scale"]["labels"]), 1            # likert bounds (this scale is 1..5)
rev = {it["id"] for it in items if it.get("reverse")}
def total(ans):                                   # ans: {item_id: score}
    return sum((hi + lo - v) if k in rev else v for k, v in ans.items())
# pair_delta = total(post) - total(pre)
# construct_deltas: per construct, take that dimension's items and apply the same two totals
print(sc["reported"], "| unit:", m["unit"], "|", sc["report_note"])
```

// Note: the `version` inside `training-evaluation-form-assessment.json` describes the scale itself and is independent of this skill's frontmatter `version`.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
