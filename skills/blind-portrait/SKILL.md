---
name: blind-portrait
description: A 15-minute, 2-person back-to-back drawing exercise that makes one-way communication visible — with printable prop cards, an 8-question debrief, and a pre/post pair-level assessment.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*), Bash(npm:*), Bash(formlm-cli:*), Bash(python3:*)
metadata:
  category: communication
  group_size: 2
  duration_minutes: 15
  setting: offline
  props: [poker prop cards, marker, paper, 2 mystery line drawings per pair]
  depth: assessment-type
  language: en
  updated: 2026-10-11
---

# Blind Portrait

One describes, one draws, nobody watches the pen. The gap between the two pictures is the lesson: instructions sent into silence come back distorted.

## When to use this activity

- A team sends detailed instructions into silence (email specs, handovers, tickets) and is surprised by what comes back.
- You have 15 minutes and pairs, not a full room.
- You want measurable evidence of a communication session, not just a good feeling — this activity has a pre/post pair-level measure.

## What is in the folder

| File | Purpose |
|---|---|
| `blind-portrait-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): describer card, drawer card, judge card, timing card |
| `blind-portrait-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 PDF |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `blind-portrait-guide.md` | Run sheet: objectives, setup, minute-by-minute script, grouping rules, variations |
| `blind-portrait-debrief.md` | 8 debrief questions + 3 debrief failure modes with rescues |
| `blind-portrait-assessment.json` | Pre/post measure preset: 6 items, pair-level deltas |
| `blind-portrait-paper-form.pdf` | A4 answer sheet — print-and-fill form (workshop version) |
| `blind-portrait-slide-deck.pdf` | Slide deck — 12 slides for running the session, one idea per slide |
| `blind-portrait-slide-deck.html` | Slide deck (HTML) — present from any browser, one keypress per point, speaker notes built in |
| `blind-portrait-workbook.pdf` | Participant workbook — plain-language intro, guided items, notes and action pages |
| `blind-portrait-license.md` | License in plain language — what you may do, what you must keep |
| `blind-portrait-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `blind-portrait-start-here.md` | Start here — pick your lane, file map, print lists |

## Running it

1. Print one prop-card set per pair. Prepare two mystery line drawings per pair (round A / round B).
2. Run the pre-measure (2 min) **before** pairing up.
3. Round A: 3 minutes, drawer may not ask questions.
4. Reveal. Round B: roles swap, new image, drawer may ask exactly three questions.
5. Run the debrief from `blind-portrait-debrief.md` — the drawings stay on the table.
6. Run the post-measure (2 min). Report pair deltas, never individual rankings.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/blind-portrait/files/blind-portrait.zip
unzip blind-portrait.zip   # -> blind-portrait/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `blind-portrait` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable props (poker prop-card deck, CC BY 4.0)
curl -O https://workshopskill.com/en/activities/blind-portrait/files/blind-portrait-prop-cards.pdf

# 2. Get the A4 answer sheet (print one per participant for offline workshops)
curl -O https://workshopskill.com/en/activities/blind-portrait/files/blind-portrait-paper-form.pdf

# 3. Get the debrief questions (8 questions + 3 failure-mode rescues)
curl -O https://workshopskill.com/en/activities/blind-portrait/files/blind-portrait-debrief.md

# 4. Get the run sheet (minute-by-minute script)
curl -O https://workshopskill.com/en/activities/blind-portrait/files/blind-portrait-guide.md
```

The measured result does not depend on FormLM — you can score the pre/post offline with no account (see "Score it offline" below). The live form is purely optional.

The live pre/post measure is built with the FormLM CLI. It needs a free FormLM account; the form and its data stay in your own workspace:

```bash
npm install -g @formlm/cli
formlm-cli auth login
formlm-cli smart generate --input "Pre/post measure for the Blind Portrait pairs exercise: 6 Likert items on instruction clarity, assumption-checking, perspective-taking and repair — the same 6 items before and after the activity, so each participant's delta is computed automatically"
```

If the agent cannot complete the interactive `formlm-cli auth login` (headless run, CI, no browser): still run the curl steps, keep `blind-portrait-assessment.json` as the measure spec, and hand the login and the generate command to a human — or have a human log in once, then re-run only the generate step.

Useful preparation facts for the agent:
- Group size scales by pairs: 12 people = 6 pairs, one prop-card set per pair.
- Agenda math: pre-measure 2 + activity 15 + post-measure 2 = 19 minutes total.
- No projector needed; nothing in the folder requires a screen.
- Print at poker. The whole deck fits one sheet per pair.

**Where to put the skill.** Drop the unzipped `blind-portrait/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/blind-portrait/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/blind-portrait/`, Qoder `~/.qoder/skills/blind-portrait/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- The silence in round A is the design, not a failure to facilitate. Do not fill it.
- If the describer narrates meaning instead of shape ("it's like a farm"), restate the rule once and let the round continue.
- The strongest transfer question: "Where does sending instructions into silence show up in your week?"

## Score it offline (no account)

The full scoring spec already ships in this folder's `blind-portrait-assessment.json` (the `scoring` field), so you can produce a result without FormLM — an agent can compute it locally:

1. Collect each respondent's Likert answers for every `items` question (a pre round and a post round).
2. Reverse-score the items flagged in `scoring.reverse_scored_items` (or `items[].reverse` true): `new = scale_max + scale_min - raw`.
3. Tally by `scoring.method` (`sum` adds the items) into a pre total and a post total.
4. Emit exactly `scoring.reported`: `pair_delta` (post - pre, per the top-level `unit`) and `construct_deltas` (repeat per `items[].construct` group).
5. Honour `scoring.report_note`: report pair-level change only, never an individual ranking.

Copy-paste implementation using only the standard library:

```python
import json
m = json.load(open("blind-portrait-assessment.json"))
sc, items = m["scoring"], m["items"]
hi, lo = len(m["scale"]["labels"]), 1            # likert bounds (this scale is 1..5)
rev = {it["id"] for it in items if it.get("reverse")}
def total(ans):                                   # ans: {item_id: score}
    return sum((hi + lo - v) if k in rev else v for k, v in ans.items())
# pair_delta = total(post) - total(pre)
# construct_deltas: per construct, take that dimension's items and apply the same two totals
print(sc["reported"], "| unit:", m["unit"], "|", sc["report_note"])
```

// Note: the `version` inside `blind-portrait-assessment.json` describes the scale itself and is independent of this skill's frontmatter `version`.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
