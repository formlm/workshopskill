---
name: advantage-compass
description: A personal strategy self-assessment — two axes (strength x weakness, vision x pain), four quadrants, a two-week time audit and one committed move. Poker-spec print cards, an A3 model poster, a presenter-grade HTML deck, or a live online form.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*), Bash(npm:*), Bash(formlm-cli:*), Bash(python3:*)
metadata:
  category: self-assessment
  group_size: 1
  duration_minutes: 25
  setting: hybrid
  props: [poker compass cards, pen, two weeks of calendar]
  depth: assessment-type
  language: en
  updated: 2026-10-11
---
# The Advantage Compass

Personality tests label you; the Compass locates you. Six items and a two-week audit map your hours onto four quadrants — and name the one move that shifts them.

## When to use this activity

- A coachee says "I am busy all day but going nowhere" and needs evidence, not sympathy.
- A career or strategy workshop needs a solo exercise that produces a dated commitment, not just discussion.
- A manager wants to see who on the team is working on the future, not only on today.

## What is in the folder

| File | Purpose |
|---|---|
| `advantage-compass-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides): compass card, four quadrant cards, audit card, backs and blanks |
| `advantage-compass-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 PDF |
| `*-Letter.pdf` | US Letter paper size for all four print documents (run sheet, workbook, answer sheet, facilitator notes) — same content, bookmarks and linked TOC in every edition |
| `advantage-compass-guide.md` | Guide: the two axes, four steps, four known distortions |
| `advantage-compass-debrief.md` | Reading the map: quadrant by quadrant, audit table, exit moves |
| `advantage-compass-assessment.json` | 6 placement items + two-week audit, plain JSON |
| `advantage-compass-paper-form.pdf` | A4 answer sheet — the 6 items + audit as a print-and-fill form (workshop version) |
| `advantage-compass-facilitator-notes.pdf` | Facilitator notes — the 25-minute run of show for teaching the model |
| `advantage-compass-slide-deck.pdf` | Slide deck — 16 slides for teaching, one idea per slide (print fallback of the HTML deck) |
| `advantage-compass-slide-deck.html` | The deck as a stage tool: presenter drawer (S) with notes + run-of-show timer, live audit device, silence timer (T), house mode (B), offline single file, white-label = 3 replacements |
| `advantage-compass-activity-poster.pdf` | A3 model poster: the dial, healthy calendar, exit moves and the cited theory trail |
| `advantage-compass-workbook.pdf` | Participant workbook — the model in plain words, guided items, the work-block log, three questions, a re-run tracker |
| `advantage-compass-license.md` | License in plain language — CC BY 4.0 baseline plus Tier 1 (single event) and Tier 2 (organization) commercial licenses |
| `advantage-compass-start-here.md` | Start here — pick your lane, file map, print lists |

## Running it

1. Print the poker deck (one sheet of faces + one of backs per table set): one compass card, four quadrant cards, one audit card per person.
2. Step 1 (10 min): list the last two weeks from the calendar — every block, strong/weak and vision/pain.
3. Step 2 (5 min): sort every block into a quadrant; count the hours.
4. Step 3 (5 min): read with `advantage-compass-debrief.md` — three questions, in order.
5. Step 4 (5 min): one move, one date, one check-back. Re-run monthly; the delta is the score.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/advantage-compass/files/advantage-compass.zip
unzip advantage-compass.zip   # -> advantage-compass/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `advantage-compass` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the poker-spec compass card print sheet (bleed + cut guides, CC BY 4.0)
curl -O https://workshopskill.com/en/activities/advantage-compass/files/advantage-compass-prop-cards.pdf

# 2. Get the A4 answer sheet (print one per participant for offline workshops)
curl -O https://workshopskill.com/en/activities/advantage-compass/files/advantage-compass-paper-form.pdf

# 3. Get the map-reading guide (quadrant table + exit moves)
curl -O https://workshopskill.com/en/activities/advantage-compass/files/advantage-compass-debrief.md

# 4. Get the facilitator guide (axes, four steps, distortions)
curl -O https://workshopskill.com/en/activities/advantage-compass/files/advantage-compass-guide.md

# 5. Build the live self-assessment (6 items + audit, see advantage-compass-assessment.json)
```

The measured result does not depend on FormLM — you can score the pre/post offline with no account (see "Score it offline" below). The live form is purely optional.

The live pre/post measure is built with the FormLM CLI. It needs a free FormLM account; the form and its data stay in your own workspace:

```bash
npm install -g @formlm/cli
formlm-cli auth login
formlm-cli smart generate --input "Personal strategy self-assessment for the Advantage Compass: 6 Likert items (1-5) on strength-awareness, vision-clarity, pain-share, firefighting-trap, burnout-exposure and golden-track-protection (items 3-5 reverse-scored), plus two open questions - a two-week time audit estimating hours per quadrant, and one committed move with a check-back date. Self-paced, 25 minutes, monthly re-run"
```

If the agent cannot complete the interactive `formlm-cli auth login` (headless run, CI, no browser): still run the curl steps, keep `advantage-compass-assessment.json` as the measure spec, and hand the login and the generate command to a human — or have a human log in once, then re-run only the generate step.

Useful preparation facts for the agent:
- Solo tool, 25 minutes; a one-to-one coaching version and a team-aggregation version are described in the guide.
- Three of the six items are reverse-scored; the scoring note says when to trust the audit over the means.
- Designed for monthly re-runs; the point is the delta between runs, not the absolute score.
- Print cards at poker spec (63.5 × 88.9 mm, 3 mm bleed); the PDF carries the full print-order sheet for your vendor.
- Workshop version: print one A4 answer sheet per participant — the 6 items and the audit with room to write; facilitator notes cover the teaching version.

**Where to put the skill.** Drop the unzipped `advantage-compass/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/advantage-compass/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/advantage-compass/`, Qoder `~/.qoder/skills/advantage-compass/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- Never let the coachee fill the audit from memory — calendars do not flatter, memories do. That is the whole point of Step 1.
- The facilitator asks the three Step-3 questions and stays silent after each. People answer honestly when nobody rescues them from the pause.
- A first-run result of "15% golden track" is the norm, not a crisis. The commitment is one move, not a life overhaul.

## Score it offline (no account)

The full scoring spec already ships in this folder's `advantage-compass-assessment.json` (the `scoring` field), so you can produce a result without FormLM — an agent can compute it locally:

1. Collect each respondent's Likert answers for every `items` question (a pre round and a post round).
2. Reverse-score the items flagged in `scoring.reverse_scored_items` (or `items[].reverse` true): `new = scale_max + scale_min - raw`.
3. Tally by `scoring.method` (`sum` adds the items) into a pre total and a post total.
4. Emit exactly `scoring.reported`: `pair_delta` (post - pre, per the top-level `unit`) and `construct_deltas` (repeat per `items[].construct` group).
5. Honour `scoring.report_note`: report pair-level change only, never an individual ranking.

Copy-paste implementation using only the standard library:

```python
import json
m = json.load(open("advantage-compass-assessment.json"))
sc, items = m["scoring"], m["items"]
hi, lo = len(m["scale"]["labels"]), 1            # likert bounds (this scale is 1..5)
rev = {it["id"] for it in items if it.get("reverse")}
def total(ans):                                   # ans: {item_id: score}
    return sum((hi + lo - v) if k in rev else v for k, v in ans.items())
# pair_delta = total(post) - total(pre)
# construct_deltas: per construct, take that dimension's items and apply the same two totals
print(sc["reported"], "| unit:", m["unit"], "|", sc["report_note"])
```

// Note: the `version` inside `advantage-compass-assessment.json` describes the scale itself and is independent of this skill's frontmatter `version`.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
