---
name: paper-tower
description: "Team build challenge: 20 sheets, 1 m tape, 12 minutes; the tallest tower that holds a book for ten seconds wins. The book test exposes the height-vs-stability trade."
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*), Bash(npm:*), Bash(formlm-cli:*), Bash(python3:*)
metadata:
  category: communication
  group_size: 8
  duration_minutes: 30
  setting: offline
  props: [poker prop cards, 20 A4 sheets, 1 m masking tape, 1 book per team]
  depth: assessment-type
  language: en
  updated: 2026-10-11
---

# Paper Tower

Twenty sheets, one meter of tape, twelve minutes. The tallest tower that survives the book test wins — and the build records how the team plans, shares and recovers.

## When to use this activity

- A team argues about scope and deadlines — the height-versus-stability trade needs a physical exhibit.
- You have 30 minutes and tables, not a stage.
- You want the debrief to point at something — the towers stay standing through it.

## What is in the folder

| File | Purpose |
|---|---|
| `paper-tower-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): builder card, judge card, timing card |
| `paper-tower-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 PDF |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `paper-tower-guide.md` | Run sheet: objectives, setup, minute-by-minute script, grouping rules, variations |
| `paper-tower-debrief.md` | 8 debrief questions + 3 debrief failure modes with rescues |
| `paper-tower-assessment.json` | Pre/post measure preset: 6 items, team-level deltas |
| `paper-tower-paper-form.pdf` | A4 answer sheet — print-and-fill form (workshop version) |
| `paper-tower-slide-deck.pdf` | Slide deck — 12 slides for running the session, one idea per slide |
| `paper-tower-slide-deck.html` | Slide deck (HTML) — present from any browser, one keypress per point, speaker notes built in |
| `paper-tower-workbook.pdf` | Participant workbook — plain-language intro, guided items, notes and action pages |
| `paper-tower-license.md` | License in plain language — what you may do, what you must keep |
| `paper-tower-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `paper-tower-start-here.md` | Start here — pick your lane, file map, print lists |

## Running it

1. Print one prop-card set per team. Put 20 A4 sheets and one pre-cut meter of masking tape on each table.
2. Run the pre-measure (2 min) **before** teams form.
3. Silent planning: 3 minutes, no building.
4. Build: 12 minutes. Announce "two minutes left" at minute 10.
5. The book test: each tower holds a book for ten seconds, scored on the judge card.
6. Run the debrief from `paper-tower-debrief.md` — towers stay standing.
7. Run the post-measure (2 min). Report team deltas, never rankings.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/paper-tower/files/paper-tower.zip
unzip paper-tower.zip   # -> paper-tower/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `paper-tower` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable props (poker prop-card deck, CC BY 4.0)
curl -O https://workshopskill.com/en/activities/paper-tower/files/paper-tower-prop-cards.pdf

# 2. Get the A4 answer sheet (print one per participant for offline workshops)
curl -O https://workshopskill.com/en/activities/paper-tower/files/paper-tower-paper-form.pdf

# 3. Get the debrief questions (8 questions + 3 failure-mode rescues)
curl -O https://workshopskill.com/en/activities/paper-tower/files/paper-tower-debrief.md

# 4. Get the run sheet (minute-by-minute script)
curl -O https://workshopskill.com/en/activities/paper-tower/files/paper-tower-guide.md
```

The measured result does not depend on FormLM — you can score the pre/post offline with no account (see "Score it offline" below). The live form is purely optional.

The live pre/post measure is built with the FormLM CLI. It needs a free FormLM account; the form and its data stay in your own workspace:

```bash
npm install -g @formlm/cli
formlm-cli auth login
formlm-cli smart generate --input "Pre/post measure for the Paper Tower team challenge: 6 Likert items on shared planning, role clarity, information flow and recovery from failure — the same 6 items before and after the activity, so each participant's delta is computed automatically"
```

If the agent cannot complete the interactive `formlm-cli auth login` (headless run, CI, no browser): still run the curl steps, keep `paper-tower-assessment.json` as the measure spec, and hand the login and the generate command to a human — or have a human log in once, then re-run only the generate step.

Useful preparation facts for the agent:
- Scales by tables: 5 teams of 4 = 20 people run in parallel, one prop-card set per team.
- Agenda math: pre-measure 2 + activity 28 + post-measure 2 = 32 minutes total.
- The paper is scrap — used A4 from any recycling bin works; only the tape is consumable.
- Bring one book for the test — any paperback; hardcovers are harder, not easier.

**Where to put the skill.** Drop the unzipped `paper-tower/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/paper-tower/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/paper-tower/`, Qoder `~/.qoder/skills/paper-tower/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- The silent-planning round is the activity — do not let it collapse into building time.
- Do not help any team with structure. A collapsed tower is the debrief's best exhibit.
- The strongest transfer question: "Where does your team build as tall as possible, as fast as possible — and where is your book test?"

## Score it offline (no account)

The full scoring spec already ships in this folder's `paper-tower-assessment.json` (the `scoring` field), so you can produce a result without FormLM — an agent can compute it locally:

1. Collect each respondent's Likert answers for every `items` question (a pre round and a post round).
2. Reverse-score the items flagged in `scoring.reverse_scored_items` (or `items[].reverse` true): `new = scale_max + scale_min - raw`.
3. Tally by `scoring.method` (`sum` adds the items) into a pre total and a post total.
4. Emit exactly `scoring.reported`: `pair_delta` (post - pre, per the top-level `unit`) and `construct_deltas` (repeat per `items[].construct` group).
5. Honour `scoring.report_note`: report pair-level change only, never an individual ranking.

Copy-paste implementation using only the standard library:

```python
import json
m = json.load(open("paper-tower-assessment.json"))
sc, items = m["scoring"], m["items"]
hi, lo = len(m["scale"]["labels"]), 1            # likert bounds (this scale is 1..5)
rev = {it["id"] for it in items if it.get("reverse")}
def total(ans):                                   # ans: {item_id: score}
    return sum((hi + lo - v) if k in rev else v for k, v in ans.items())
# pair_delta = total(post) - total(pre)
# construct_deltas: per construct, take that dimension's items and apply the same two totals
print(sc["reported"], "| unit:", m["unit"], "|", sc["report_note"])
```

// Note: the `version` inside `paper-tower-assessment.json` describes the scale itself and is independent of this skill's frontmatter `version`.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
