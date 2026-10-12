---
name: minefield
description: "Trust exercise in pairs: a blindfolded walker crosses a soft-obstacle course guided by voice only. Stop-word is absolute; both trust directions get debriefed."
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*), Bash(npm:*), Bash(formlm-cli:*), Bash(python3:*)
metadata:
  category: trust
  group_size: 2
  duration_minutes: 20
  setting: offline
  props: [poker prop cards, blindfold, 6-10 soft obstacles]
  depth: assessment-type
  language: en
  updated: 2026-10-11
---

# Minefield

One crosses blind, one navigates by voice — and "stop" works instantly, always. Trust gets built one direction at a time.

## When to use this activity

- Two people must rely on each other's words — delegation, handovers, remote collaboration.
- A trust theme needs a physical exercise with real (but soft) stakes.
- You want both sides of trust debriefed — being responsible for someone, and being vulnerable.

## What is in the folder

| File | Purpose |
|---|---|
| `minefield-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): walker card, navigator card, safety card |
| `minefield-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 PDF |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `minefield-guide.md` | Run sheet: safety rules, minute-by-minute script, grouping rules, variations |
| `minefield-debrief.md` | 8 debrief questions + 3 debrief failure modes with rescues |
| `minefield-assessment.json` | Pre/post measure preset: 6 items, pair-level deltas |
| `minefield-paper-form.pdf` | A4 answer sheet — print-and-fill form (workshop version) |
| `minefield-slide-deck.pdf` | Slide deck — 12 slides for running the session, one idea per slide |
| `minefield-slide-deck.html` | Slide deck (HTML) — present from any browser, one keypress per point, speaker notes built in |
| `minefield-workbook.pdf` | Participant workbook — plain-language intro, guided items, notes and action pages |
| `minefield-license.md` | License in plain language — what you may do, what you must keep |
| `minefield-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `minefield-start-here.md` | Start here — pick your lane, file map, print lists |

## Running it

1. Print one card set per pair. Lay 6–10 soft obstacles (cups, boxes) with walking gaps.
2. Read the safety card aloud — every session, no exceptions.
3. Run the pre-measure (2 min) **before** pairing up.
4. Round A (5 min): navigator guides walker across, voice only.
5. Swap roles, reset the course. Round B (5 min).
6. Near-miss collection: one moment per pair, no blame.
7. Run the debrief from `minefield-debrief.md` — walkers speak first.
8. Run the post-measure (2 min). Report pair deltas, never rankings.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/minefield/files/minefield.zip
unzip minefield.zip   # -> minefield/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `minefield` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable props (poker walker/navigator/safety cards, CC BY 4.0)
curl -O https://workshopskill.com/en/activities/minefield/files/minefield-prop-cards.pdf

# 2. Get the A4 answer sheet (print one per participant for offline workshops)
curl -O https://workshopskill.com/en/activities/minefield/files/minefield-paper-form.pdf

# 3. Get the debrief questions (8 questions + 3 failure-mode rescues)
curl -O https://workshopskill.com/en/activities/minefield/files/minefield-debrief.md

# 4. Get the run sheet (safety rules + minute-by-minute script)
curl -O https://workshopskill.com/en/activities/minefield/files/minefield-guide.md
```

The measured result does not depend on FormLM — you can score the pre/post offline with no account (see "Score it offline" below). The live form is purely optional.

The live pre/post measure is built with the FormLM CLI. It needs a free FormLM account; the form and its data stay in your own workspace:

```bash
npm install -g @formlm/cli
formlm-cli auth login
formlm-cli smart generate --input "Pre/post measure for the Minefield trust exercise: 6 Likert items on clarity under responsibility, trust on voice alone, stop-word use and repair — the same 6 items before and after the activity, so each participant's delta is computed automatically"
```

If the agent cannot complete the interactive `formlm-cli auth login` (headless run, CI, no browser): still run the curl steps, keep `minefield-assessment.json` as the measure spec, and hand the login and the generate command to a human — or have a human log in once, then re-run only the generate step.

Useful preparation facts for the agent:
- Needs 4×4 m of clear floor per active pair — stagger starts or run in sequence for big groups.
- Obstacles must be soft: paper cups, empty boxes, cushions. Never chairs or bags.
- Agenda math: pre-measure 2 + activity 20 + post-measure 2 = 24 minutes total.
- Blindfolds are optional — eyes closed, or the ceiling-gaze variant, work identically.

**Where to put the skill.** Drop the unzipped `minefield/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/minefield/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/minefield/`, Qoder `~/.qoder/skills/minefield/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- The safety card is read aloud every session — hearing it is what makes it a norm.
- When the walker wobbles, coach "clearer", not "faster" — most navigators default to speed.
- If blindfolds surface real anxiety, offer the ceiling-gaze variant without spotlighting anyone.

## Score it offline (no account)

The full scoring spec already ships in this folder's `minefield-assessment.json` (the `scoring` field), so you can produce a result without FormLM — an agent can compute it locally:

1. Collect each respondent's Likert answers for every `items` question (a pre round and a post round).
2. Reverse-score the items flagged in `scoring.reverse_scored_items` (or `items[].reverse` true): `new = scale_max + scale_min - raw`.
3. Tally by `scoring.method` (`sum` adds the items) into a pre total and a post total.
4. Emit exactly `scoring.reported`: `pair_delta` (post - pre, per the top-level `unit`) and `construct_deltas` (repeat per `items[].construct` group).
5. Honour `scoring.report_note`: report pair-level change only, never an individual ranking.

Copy-paste implementation using only the standard library:

```python
import json
m = json.load(open("minefield-assessment.json"))
sc, items = m["scoring"], m["items"]
hi, lo = len(m["scale"]["labels"]), 1            # likert bounds (this scale is 1..5)
rev = {it["id"] for it in items if it.get("reverse")}
def total(ans):                                   # ans: {item_id: score}
    return sum((hi + lo - v) if k in rev else v for k, v in ans.items())
# pair_delta = total(post) - total(pre)
# construct_deltas: per construct, take that dimension's items and apply the same two totals
print(sc["reported"], "| unit:", m["unit"], "|", sc["report_note"])
```

// Note: the `version` inside `minefield-assessment.json` describes the scale itself and is independent of this skill's frontmatter `version`.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
