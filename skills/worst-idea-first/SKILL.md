---
name: worst-idea-first
description: Reverse brainstorm: five minutes engineering how a real target fails, then flip every item into prevention. The game rewards saying the awkward thing.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*), Bash(npm:*), Bash(formlm-cli:*), Bash(python3:*)
metadata:
  category: creativity
  group_size: 8
  duration_minutes: 20
  setting: hybrid
  props: [real target + wall or shared board; optional poker round cards]
  depth: assessment-type
  language: en
  updated: 2026-10-11
---

# Worst Idea First

Don't ask how it succeeds — ask how it fails, badly. Then flip every answer. The worst ideas are the easiest to say and the sharpest to act on.

## When to use this activity

- A launch, reorg or bet deserves a pre-mortem, and the room is too polite to give it one.
- Brainstorming has gone safe and useless — ideas circulate, nothing lands.
- Psychological safety is the real theme; you need an exercise that measures it.

## What is in the folder

| File | Purpose |
|---|---|
| `worst-idea-first-prop-cards.pdf` | Optional poker deck: target, sabotage, the worst, flip, timing cards |
| `worst-idea-first-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 PDF |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `worst-idea-first-guide.md` | Run sheet: target selection, minute-by-minute script, the flip, variations |
| `worst-idea-first-debrief.md` | 8 debrief questions + 3 debrief failure modes with rescues |
| `worst-idea-first-assessment.json` | Pre/post measure preset: 6 items, group-level deltas |
| `worst-idea-first-paper-form.pdf` | A4 answer sheet — print-and-fill form (workshop version) |
| `worst-idea-first-slide-deck.pdf` | Slide deck — 12 slides for running the session, one idea per slide |
| `worst-idea-first-slide-deck.html` | Slide deck (HTML) — present from any browser, one keypress per point, speaker notes built in |
| `worst-idea-first-workbook.pdf` | Participant workbook — plain-language intro, guided items, notes and action pages |
| `worst-idea-first-license.md` | License in plain language — what you may do, what you must keep |
| `worst-idea-first-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `worst-idea-first-start-here.md` | Start here — pick your lane, file map, print lists |

## Running it

1. Pick one real target — a project, product or event the group cares about.
2. Run the pre-measure (2 min) **before** groups form.
3. Worst round (5 min): "how do we make it fail — badly?" Quantity over quality.
4. Each group presents its single most catastrophic idea.
5. The flip (6 min): "how do we prevent exactly this?" One line per action.
6. Each group reads its two sharpest actions — they go on the owner list.
7. Run the debrief from `worst-idea-first-debrief.md`.
8. Run the post-measure (2 min). Report group deltas, never rankings.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/worst-idea-first/files/worst-idea-first.zip
unzip worst-idea-first.zip   # -> worst-idea-first/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `worst-idea-first` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the optional poker deck (target, sabotage, the worst, flip, timing)
curl -O https://workshopskill.com/en/activities/worst-idea-first/files/worst-idea-first-prop-cards.pdf

# 2. Get the A4 answer sheet (print one per participant for offline workshops)
curl -O https://workshopskill.com/en/activities/worst-idea-first/files/worst-idea-first-paper-form.pdf

# 3. Get the debrief questions (8 questions + 3 failure-mode rescues)
curl -O https://workshopskill.com/en/activities/worst-idea-first/files/worst-idea-first-debrief.md

# 4. Get the run sheet (target + minute-by-minute script)
curl -O https://workshopskill.com/en/activities/worst-idea-first/files/worst-idea-first-guide.md
```

The measured result does not depend on FormLM — you can score the pre/post offline with no account (see "Score it offline" below). The live form is purely optional.

The live pre/post measure is built with the FormLM CLI. It needs a free FormLM account; the form and its data stay in your own workspace:

```bash
npm install -g @formlm/cli
formlm-cli auth login
formlm-cli smart generate --input "Pre/post measure for the Worst Idea First reverse-brainstorm: 6 Likert items on voice, risk-naming, specificity and safety to say awkward things — the same 6 items before and after the activity, so each participant's delta is computed automatically"
```

If the agent cannot complete the interactive `formlm-cli auth login` (headless run, CI, no browser): still run the curl steps, keep `worst-idea-first-assessment.json` as the measure spec, and hand the login and the generate command to a human — or have a human log in once, then re-run only the generate step.

Useful preparation facts for the agent:
- The game needs zero props — one real target and groups of three or four; the poker deck is optional paper.
- Agenda math: pre-measure 2 + activity 20 + post-measure 2 = 24 minutes total.
- Online: breakout rooms for the worst round, shared doc for the flip.
- If a worst idea is a real grievance in disguise, honor it — flip it first.

**Where to put the skill.** Drop the unzipped `worst-idea-first/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/worst-idea-first/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/worst-idea-first/`, Qoder `~/.qoder/skills/worst-idea-first/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- Push for quantity in the worst round — dumber, cheaper to say, faster.
- Hold the flip until the disaster round is done; premature prevention kills the fun and the safety.
- The room getting louder and funnier is safety rising — name it in the debrief.

## Score it offline (no account)

The full scoring spec already ships in this folder's `worst-idea-first-assessment.json` (the `scoring` field), so you can produce a result without FormLM — an agent can compute it locally:

1. Collect each respondent's Likert answers for every `items` question (a pre round and a post round).
2. Reverse-score the items flagged in `scoring.reverse_scored_items` (or `items[].reverse` true): `new = scale_max + scale_min - raw`.
3. Tally by `scoring.method` (`sum` adds the items) into a pre total and a post total.
4. Emit exactly `scoring.reported`: `pair_delta` (post - pre, per the top-level `unit`) and `construct_deltas` (repeat per `items[].construct` group).
5. Honour `scoring.report_note`: report pair-level change only, never an individual ranking.

Copy-paste implementation using only the standard library:

```python
import json
m = json.load(open("worst-idea-first-assessment.json"))
sc, items = m["scoring"], m["items"]
hi, lo = len(m["scale"]["labels"]), 1            # likert bounds (this scale is 1..5)
rev = {it["id"] for it in items if it.get("reverse")}
def total(ans):                                   # ans: {item_id: score}
    return sum((hi + lo - v) if k in rev else v for k, v in ans.items())
# pair_delta = total(post) - total(pre)
# construct_deltas: per construct, take that dimension's items and apply the same two totals
print(sc["reported"], "| unit:", m["unit"], "|", sc["report_note"])
```

// Note: the `version` inside `worst-idea-first-assessment.json` describes the scale itself and is independent of this skill's frontmatter `version`.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
