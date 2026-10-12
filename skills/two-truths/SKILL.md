---
name: two-truths
description: "Icebreaker with guardrails: three statements per person, all public work facts, one false; the group votes eyes-closed. Nobody is publicly wrong about a colleague."
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*), Bash(npm:*), Bash(formlm-cli:*), Bash(python3:*)
metadata:
  category: icebreakers
  group_size: 8
  duration_minutes: 15
  setting: hybrid
  props: []
  depth: assessment-type
  language: en
  updated: 2026-10-11
---

# Two Truths and a Lie

Three statements, one is false, all eyes closed before the vote — the classic icebreaker, rebuilt so nobody gets embarrassed in a professional room.

## When to use this activity

- A group of strangers or semi-strangers needs to learn names and facts in the first fifteen minutes.
- The room includes senior people and new hires at once — the boundary rule keeps both safe.
- You are online and need an icebreaker that survives a video call.

## What is in the folder

| File | Purpose |
|---|---|
| `two-truths-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 PDF |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `two-truths-guide.md` | Run sheet: boundary rule, eyes-closed script, minute-by-minute flow, variations |
| `two-truths-debrief.md` | 6 light debrief questions + 3 failure modes with rescues |
| `two-truths-assessment.json` | 4-row pre/post recall measure, plain JSON — room-level reporting |
| `two-truths-paper-form.pdf` | A4 answer sheet — print-and-fill form (workshop version) |
| `two-truths-slide-deck.pdf` | Slide deck — 11 slides for running the session, one idea per slide |
| `two-truths-slide-deck.html` | Slide deck (HTML) — present from any browser, one keypress per point, speaker notes built in |
| `two-truths-workbook.pdf` | Participant workbook — plain-language intro, guided items, notes and action pages |
| `two-truths-license.md` | License in plain language — what you may do, what you must keep |
| `two-truths-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `two-truths-start-here.md` | Start here — pick your lane, file map, print lists |

## Running it

1. State the boundary rule out loud: "public work facts only — projects, skills, first jobs, countries worked in."
2. You go first: model two truths and one lie, all work facts.
3. Rounds: each speaker says three statements, then the group votes eyes-closed (A / B / C).
4. Reveal, one line of story per truth.
5. Light debrief from `two-truths-debrief.md` — recall, not scores.
The game needs no props; the measure ships on one answer sheet — filled twice, before the circle and after the debrief.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/two-truths/files/two-truths.zip
unzip two-truths.zip   # -> two-truths/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `two-truths` holding this SKILL.md, every file it references, and a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the A4 answer sheet (print one per participant for offline workshops)
curl -O https://workshopskill.com/en/activities/two-truths/files/two-truths-paper-form.pdf

# 2. Get the debrief questions (6 light questions + 3 failure-mode rescues)
curl -O https://workshopskill.com/en/activities/two-truths/files/two-truths-debrief.md

# 3. Get the run sheet (boundary rule + minute-by-minute script)
curl -O https://workshopskill.com/en/activities/two-truths/files/two-truths-guide.md
```

The measured result does not depend on FormLM — you can score the pre/post offline with no account (see "Score it offline" below). The live form is purely optional.

The live pre/post measure is built with the FormLM CLI. It needs a free FormLM account; the form and its data stay in your own workspace:

```bash
npm install -g @formlm/cli
formlm-cli auth login
formlm-cli smart generate --input "Pre/post measure for the Two Truths and a Lie icebreaker: 4 Likert items (1-5) on colleague knowledge, first impressions (reverse-scored), follow-up curiosity and self-disclosure ease — the same 4 items before the circle and after the light debrief, so each participant's delta is computed automatically. Anonymous, room-level reporting, 1 minute"
```

If the agent cannot complete the interactive `formlm-cli auth login` (headless run, CI, no browser): still run the curl steps, keep `two-truths-assessment.json` as the measure spec, and hand the login and the generate command to a human — or have a human log in once, then re-run only the generate step.

Useful preparation facts for the agent:
- Zero props — works with chairs in a circle or a single video call.
- Over 12 people, split into two circles; below 12, one circle runs faster.
- Agenda math: 15 minutes total, including a 5-minute light debrief.
- Online voting: statements in chat, emoji reactions (A/B/C), reveal on mic.

**Where to put the skill.** Drop the unzipped `two-truths/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/two-truths/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/two-truths/`, Qoder `~/.qoder/skills/two-truths/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- The boundary rule must be spoken, not printed — hearing it sets the norm.
- You demonstrate first; your lie calibrates the room's difficulty.
- If a statement crosses the privacy line, offer an easy swap before the vote — no lecture.

## Score it offline (no account)

The full scoring spec already ships in this folder's `two-truths-assessment.json` (the `scoring` field), so you can produce a result without FormLM — an agent can compute it locally:

1. Collect each respondent's Likert answers for every `items` question (a pre round and a post round).
2. Reverse-score the items flagged in `scoring.reverse_scored_items` (or `items[].reverse` true): `new = scale_max + scale_min - raw`.
3. Tally by `scoring.method` (`sum` adds the items) into a pre total and a post total.
4. Emit exactly `scoring.reported`: `pair_delta` (post - pre, per the top-level `unit`) and `construct_deltas` (repeat per `items[].construct` group).
5. Honour `scoring.report_note`: report pair-level change only, never an individual ranking.

Copy-paste implementation using only the standard library:

```python
import json
m = json.load(open("two-truths-assessment.json"))
sc, items = m["scoring"], m["items"]
hi, lo = len(m["scale"]["labels"]), 1            # likert bounds (this scale is 1..5)
rev = {it["id"] for it in items if it.get("reverse")}
def total(ans):                                   # ans: {item_id: score}
    return sum((hi + lo - v) if k in rev else v for k, v in ans.items())
# pair_delta = total(post) - total(pre)
# construct_deltas: per construct, take that dimension's items and apply the same two totals
print(sc["reported"], "| unit:", m["unit"], "|", sc["report_note"])
```

// Note: the `version` inside `two-truths-assessment.json` describes the scale itself and is independent of this skill's frontmatter `version`.

## Remix: make it yours

Want to rebrand this folder or package it for your own shelf? Under CC BY you can swap the deck placeholders, the card and poster art, and the packaging yourself. Keep the attribution line and you're free to use it, sell it, or redistribute it.

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
