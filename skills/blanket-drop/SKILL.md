---
name: blanket-drop
description: "Two-team name game behind a dropping blanket: first correct shout scores, wrong names give a free point. Planted-feet safety rule; names learned at recall speed."
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*), Bash(npm:*), Bash(formlm-cli:*), Bash(python3:*)
metadata:
  category: icebreakers
  group_size: 8
  duration_minutes: 10
  setting: offline
  props: [one opaque blanket or bedsheet]
  depth: assessment-type
  language: en
  updated: 2026-10-11
---

# Blanket Drop

The blanket drops and names fly across the room — the classic name game, rebuilt with a safety rule and rescues for every way it goes wrong.

## When to use this activity

- A room of strangers must learn every name before the first coffee break.
- You have ten minutes and three meters of clear floor.
- The group needs one shared laugh before any serious work starts.

## What is in the folder

| File | Purpose |
|---|---|
| `blanket-drop-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 PDF |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `blanket-drop-guide.md` | Run sheet: spoken rules, minute-by-minute flow, variations, failure rescues |
| `blanket-drop-debrief.md` | 6 light debrief questions + 3 failure modes with rescues |
| `blanket-drop-assessment.json` | 4-row pre/post name-recall measure, plain JSON — room-level reporting |
| `blanket-drop-paper-form.pdf` | A4 answer sheet — print-and-fill form (workshop version) |
| `blanket-drop-slide-deck.pdf` | Slide deck — 11 slides for running the session, one idea per slide |
| `blanket-drop-slide-deck.html` | Slide deck (HTML) — present from any browser, one keypress per point, speaker notes built in |
| `blanket-drop-workbook.pdf` | Participant workbook — plain-language intro, guided items, notes and action pages |
| `blanket-drop-license.md` | License in plain language — what you may do, what you must keep |
| `blanket-drop-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `blanket-drop-start-here.md` | Start here — pick your lane, file map, print lists |

## Running it

1. Clear a three-meter strip of floor. Hold the blanket between two equal teams.
2. State the spoken rules: first correct name scores; a wrong name gives the other team a free point; feet stay planted.
3. Rounds (~30 s each): both teams send one person forward; drop the blanket on "three".
4. Rotate by counting off — no volunteers, no exceptions.
5. Surprise tally, then the light debrief from `blanket-drop-debrief.md`.
The game needs one blanket; the measure ships on one answer sheet — filled twice, before the teams split and after the debrief.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/blanket-drop/files/blanket-drop.zip
unzip blanket-drop.zip   # -> blanket-drop/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `blanket-drop` holding this SKILL.md, every file it references, and a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the A4 answer sheet (print one per participant for offline workshops)
curl -O https://workshopskill.com/en/activities/blanket-drop/files/blanket-drop-paper-form.pdf

# 2. Get the debrief questions (6 light questions + 3 failure-mode rescues)
curl -O https://workshopskill.com/en/activities/blanket-drop/files/blanket-drop-debrief.md

# 3. Get the run sheet (spoken rules + minute-by-minute script)
curl -O https://workshopskill.com/en/activities/blanket-drop/files/blanket-drop-guide.md
```

The measured result does not depend on FormLM — you can score the pre/post offline with no account (see "Score it offline" below). The live form is purely optional.

The live pre/post measure is built with the FormLM CLI. It needs a free FormLM account; the form and its data stay in your own workspace:

```bash
npm install -g @formlm/cli
formlm-cli auth login
formlm-cli smart generate --input "Pre/post measure for the Blanket Drop name game: 4 Likert items (1-5) on name recall, name avoidance (reverse-scored), recall under mild pressure and using names out loud — the same 4 items before the teams split and after the light debrief, so each participant's delta is computed automatically. Anonymous, room-level reporting, 1 minute"
```

If the agent cannot complete the interactive `formlm-cli auth login` (headless run, CI, no browser): still run the curl steps, keep `blanket-drop-assessment.json` as the measure spec, and hand the login and the generate command to a human — or have a human log in once, then re-run only the generate step.

Useful preparation facts for the agent:
- Needs one opaque blanket or bedsheet and two holders (you plus a volunteer, or two chairs).
- Rounds run ~30 seconds; 8–12 rounds fills the core of the ten minutes.
- Over 12 people, split into two pairs of teams and alternate.
- Remote version: camera off then on — first to name the face wins.

**Where to put the skill.** Drop the unzipped `blanket-drop/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/blanket-drop/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/blanket-drop/`, Qoder `~/.qoder/skills/blanket-drop/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- The planted-feet rule is a safety rule — say it out loud, enforce it with humor.
- Never mock a miss; the free point is the joke, not the person.
- Rotate by counting off — volunteers create an escape hatch that dodgy people will use.

## Score it offline (no account)

The full scoring spec already ships in this folder's `blanket-drop-assessment.json` (the `scoring` field), so you can produce a result without FormLM — an agent can compute it locally:

1. Collect each respondent's Likert answers for every `items` question (a pre round and a post round).
2. Reverse-score the items flagged in `scoring.reverse_scored_items` (or `items[].reverse` true): `new = scale_max + scale_min - raw`.
3. Tally by `scoring.method` (`sum` adds the items) into a pre total and a post total.
4. Emit exactly `scoring.reported`: `pair_delta` (post - pre, per the top-level `unit`) and `construct_deltas` (repeat per `items[].construct` group).
5. Honour `scoring.report_note`: report pair-level change only, never an individual ranking.

Copy-paste implementation using only the standard library:

```python
import json
m = json.load(open("blanket-drop-assessment.json"))
sc, items = m["scoring"], m["items"]
hi, lo = len(m["scale"]["labels"]), 1            # likert bounds (this scale is 1..5)
rev = {it["id"] for it in items if it.get("reverse")}
def total(ans):                                   # ans: {item_id: score}
    return sum((hi + lo - v) if k in rev else v for k, v in ans.items())
# pair_delta = total(post) - total(pre)
# construct_deltas: per construct, take that dimension's items and apply the same two totals
print(sc["reported"], "| unit:", m["unit"], "|", sc["report_note"])
```

// Note: the `version` inside `blanket-drop-assessment.json` describes the scale itself and is independent of this skill's frontmatter `version`.

## Remix: make it yours

Want to rebrand this folder or package it for your own shelf? Under CC BY you can swap the deck placeholders, the card and poster art, and the packaging yourself. Keep the attribution line and you're free to use it, sell it, or redistribute it.

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
