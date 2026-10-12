---
name: start-stop-continue
description: Wall retrospective with three verbs: start, stop, continue. One behavior per card, never a person; no card survives without an owner and a date.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*), Bash(npm:*), Bash(formlm-cli:*), Bash(python3:*)
metadata:
  category: reviews
  group_size: 4
  duration_minutes: 30
  setting: hybrid
  props: [poker prop cards, wall or whiteboard, markers]
  depth: assessment-type
  language: en
  updated: 2026-10-11
---

# Start · Stop · Continue

One verb per card, behaviors never people, and no card survives without an owner and a date. The smallest retrospective with real discipline.

## When to use this activity

- A cycle ends — sprint, phase, quarter — and the team needs one honest hour.
- Previous retros produced feelings, not commitments.
- The team is remote; the retro must run on a shared board.

## What is in the folder

| File | Purpose |
|---|---|
| `start-stop-continue-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): START / STOP / CONTINUE cards + timing card |
| `start-stop-continue-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 PDF |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `start-stop-continue-guide.md` | Run sheet: card rule, minute-by-minute script, dot-vote, owner round |
| `start-stop-continue-debrief.md` | 8 debrief questions + 3 debrief failure modes with rescues |
| `start-stop-continue-assessment.json` | Pre/post measure preset: 6 items, team-level deltas |
| `start-stop-continue-paper-form.pdf` | A4 answer sheet — print-and-fill form (workshop version) |
| `start-stop-continue-slide-deck.pdf` | Slide deck — 12 slides for running the session, one idea per slide |
| `start-stop-continue-slide-deck.html` | Slide deck (HTML) — present from any browser, one keypress per point, speaker notes built in |
| `start-stop-continue-workbook.pdf` | Participant workbook — plain-language intro, guided items, notes and action pages |
| `start-stop-continue-license.md` | License in plain language — what you may do, what you must keep |
| `start-stop-continue-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `start-stop-continue-start-here.md` | Start here — pick your lane, file map, print lists |

## Running it

1. Print one verb card per person per pile (START / STOP / CONTINUE), plus the timing card.
2. Run the pre-measure (2 min) **before** cards are dealt.
3. State the card rule aloud: one behavior per card, never a person's name.
4. Silent writing: 8 minutes, all three verbs.
5. The wall: read, cluster duplicates, name the clusters.
6. Dot-vote: three dots each, across all piles.
7. Owner round: top card per pile gets an owner and a date, said aloud.
8. Photograph the wall — it is the contract. Run the post-measure (2 min).

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/start-stop-continue/files/start-stop-continue.zip
unzip start-stop-continue.zip   # -> start-stop-continue/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `start-stop-continue` holding this SKILL.md, every file it references, and a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable props (poker verb cards + timing card, CC BY 4.0)
curl -O https://workshopskill.com/en/activities/start-stop-continue/files/start-stop-continue-prop-cards.pdf

# 2. Get the A4 answer sheet (print one per participant for offline workshops)
curl -O https://workshopskill.com/en/activities/start-stop-continue/files/start-stop-continue-paper-form.pdf

# 3. Get the debrief questions (8 questions + 3 failure-mode rescues)
curl -O https://workshopskill.com/en/activities/start-stop-continue/files/start-stop-continue-debrief.md

# 4. Get the run sheet (card rule + minute-by-minute script)
curl -O https://workshopskill.com/en/activities/start-stop-continue/files/start-stop-continue-guide.md
```

The measured result does not depend on FormLM — you can score the pre/post offline with no account (see "Score it offline" below). The live form is purely optional.

The live pre/post measure is built with the FormLM CLI. It needs a free FormLM account; the form and its data stay in your own workspace:

```bash
npm install -g @formlm/cli
formlm-cli auth login
formlm-cli smart generate --input "Pre/post measure for the Start-Stop-Continue retrospective: 6 Likert items on honesty, behavior-over-person framing and commitment quality — the same 6 items before and after the activity, so each participant's delta is computed automatically"
```

If the agent cannot complete the interactive `formlm-cli auth login` (headless run, CI, no browser): still run the curl steps, keep `start-stop-continue-assessment.json` as the measure spec, and hand the login and the generate command to a human — or have a human log in once, then re-run only the generate step.

Useful preparation facts for the agent:
- Runs on one team of 4–8; larger teams split into pairs to write, then merge boards.
- Agenda math: pre-measure 2 + retro 30 + post-measure 2 = 34 minutes total.
- Remote: shared board with three columns, cards as stickies, emoji dot-vote.
- Cap CONTINUE at three cards per person — it moves honesty into START and STOP.

**Where to put the skill.** Drop the unzipped `start-stop-continue/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/start-stop-continue/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/start-stop-continue/`, Qoder `~/.qoder/skills/start-stop-continue/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- The card rule is spoken every time — behaviors only, never names, no exceptions.
- Silent writing protects the quiet; the wall belongs to the authors.
- A commitment that fails the one-line test is not a commitment — rewrite it on the spot.

## Score it offline (no account)

The full scoring spec already ships in this folder's `start-stop-continue-assessment.json` (the `scoring` field), so you can produce a result without FormLM — an agent can compute it locally:

1. Collect each respondent's Likert answers for every `items` question (a pre round and a post round).
2. Reverse-score the items flagged in `scoring.reverse_scored_items` (or `items[].reverse` true): `new = scale_max + scale_min - raw`.
3. Tally by `scoring.method` (`sum` adds the items) into a pre total and a post total.
4. Emit exactly `scoring.reported`: `pair_delta` (post - pre, per the top-level `unit`) and `construct_deltas` (repeat per `items[].construct` group).
5. Honour `scoring.report_note`: report pair-level change only, never an individual ranking.

Copy-paste implementation using only the standard library:

```python
import json
m = json.load(open("start-stop-continue-assessment.json"))
sc, items = m["scoring"], m["items"]
hi, lo = len(m["scale"]["labels"]), 1            # likert bounds (this scale is 1..5)
rev = {it["id"] for it in items if it.get("reverse")}
def total(ans):                                   # ans: {item_id: score}
    return sum((hi + lo - v) if k in rev else v for k, v in ans.items())
# pair_delta = total(post) - total(pre)
# construct_deltas: per construct, take that dimension's items and apply the same two totals
print(sc["reported"], "| unit:", m["unit"], "|", sc["report_note"])
```

// Note: the `version` inside `start-stop-continue-assessment.json` describes the scale itself and is independent of this skill's frontmatter `version`.

## Remix: make it yours

Want to rebrand this folder or package it for your own shelf? The license file spells out what you may do: swap the deck placeholders, reprint the cards and poster at spec, and keep the CC BY attribution line — then use it, sell it, or redistribute it freely.

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
