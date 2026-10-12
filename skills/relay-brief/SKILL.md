---
name: relay-brief
description: A 20-minute, 8-20 person telephone-game exercise where a five-constraint task brief is relayed down a line and rebuilt, exposing how verbal handover leaks — with printable cards, an observer tally and an individual pre/post measure on handover discipline.
version: 2.1.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*), Bash(npm:*), Bash(formlm-cli:*), Bash(python3:*)
metadata:
  category: communication
  group_size: 8
  duration_minutes: 20
  setting: hybrid
  props: [poker brief + rebuild cards, observer tally card]
  depth: assessment-type
  language: en
  updated: 2026-10-11
---

# Relay Brief

A five-constraint brief, whispered down a line of four to six people, rebuilt out loud at the end. The distance between the original and the rebuild is the lesson: every hop drops a constraint, compresses a number and injects a guess — and everyone felt certain they passed it on fine.

## When to use this activity

- A team keeps getting work wrong downstream and blames inattentiveness; the real culprit is the handover itself.
- You want a fast, visceral demo of why specs need to be written and checked.
- You have 20 minutes and a line of 4-6 (run two lines for a bigger room).

## What is in the folder

| File | Purpose |
|---|---|
| `relay-brief-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): brief card (facilitator), rebuild-record cards, observer tally card |
| `relay-brief-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `relay-brief-guide.md` | Run sheet: objectives, setup with a materials table, minute-by-minute script, failure modes and rescues, variations |
| `relay-brief-debrief.md` | 6 debrief questions with what each targets + reading the two versions + three failure modes of the debrief |
| `relay-brief-assessment.json` | Pre/post measure preset: 5 items, two reverse-scored, individual delta + team shift |
| `relay-brief-paper-form.pdf` | A4 answer sheet — print-and-fill form (workshop version) |
| `relay-brief-slide-deck.pdf` | Slide deck — 12 slides for running the session, one idea per slide |
| `relay-brief-slide-deck.html` | Slide deck (HTML) — present from any browser, speaker notes built in |
| `relay-brief-workbook.pdf` | Participant workbook — plain intro, the hop log, notes and action pages |
| `relay-brief-license.md` | License in plain language — what you may do, what you must keep |
| `relay-brief-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `relay-brief-start-here.md` | Start here — pick your lane, file map, print lists |

## Running it

1. Write one brief with exactly five constraints on the brief card; hand it only to person one.
2. Run the pre-measure (2 min) before lining up.
3. Line up 4-6, facing away; each whispers the brief on once, no repeats, no notes.
4. Reveal: the last person states the rebuild; read the original aloud; count surviving constraints on the observer card.
5. Run the debrief from `relay-brief-debrief.md` — both versions side by side.
6. Run the post-measure (2 min). Report the shift, never a culprit.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/relay-brief/files/relay-brief.zip
unzip relay-brief.zip   # -> relay-brief/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `relay-brief` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/relay-brief/files/relay-brief-prop-cards.pdf

# 2. Get the A4 answer sheet
curl -O https://workshopskill.com/en/activities/relay-brief/files/relay-brief-paper-form.pdf

# 3. Get the debrief and the run sheet
curl -O https://workshopskill.com/en/activities/relay-brief/files/relay-brief-debrief.md
curl -O https://workshopskill.com/en/activities/relay-brief/files/relay-brief-guide.md
```

The measured result does not depend on FormLM — you can score the pre/post offline with no account (see "Score it offline"). The live form is purely optional.

The live pre/post measure is built with the FormLM CLI. It needs a free FormLM account; the form and its data stay in your own workspace:

```bash
npm install -g @formlm/cli
formlm-cli auth login
formlm-cli smart generate --input "Pre/post measure for Relay Brief: 5 Likert items on info-retention, clarify-before-act, assumption-injection (reverse), rebuild-fidelity and single-source-confidence (reverse) — the same 5 items before and after the relay, so each person's delta is computed automatically"
```

If the agent cannot complete the interactive `formlm-cli auth login` (headless run, CI, no browser): still run the curl steps, keep `relay-brief-assessment.json` as the measure spec, and hand the login and the generate command to a human — or have a human log in once, then re-run only the generate step.

Useful preparation facts for the agent:
- One line is 4-6 people; for a room over ~12 run two lines in parallel.
- Agenda math: pre-measure 2 + relay 8 + reveal 3 + debrief 4 + post-measure 2 = 19 minutes.
- No projector needed; the deck is optional and nothing in the folder requires a screen.
- Print at poker. One brief card per line, one rebuild card per late hop.

**Where to put the skill.** Drop the unzipped `relay-brief/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/relay-brief/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/relay-brief/`, Qoder `~/.qoder/skills/relay-brief/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- The strong moment is person one hearing the final rebuild and recognising it came from their own accurate telling.
- If a hop jokes or writes notes, reset the rule: everyone passes honestly, no notes — the honest distortion is the lesson.
- The strongest transfer question: "Which handover this week went down a line like this one?"

## Score it offline (no account)

The full scoring spec already ships in this folder's `relay-brief-assessment.json` (the `scoring` field), so you can produce a result without FormLM — an agent can compute it locally:

1. Collect each respondent's Likert answers for every `items` question (a pre round and a post round).
2. Reverse-score the items flagged in `scoring.reverse_scored_items` (or `items[].reverse` true): `new = scale_max + scale_min - raw`.
3. Tally by `scoring.method` (`sum` adds the items) into a pre total and a post total.
4. Emit exactly `scoring.reported`: `total_delta` (post - pre, per the top-level `unit`) and `construct_deltas` (repeat per `items[].construct` group).
5. Honour `scoring.report_note`: report each person's own shift and the team average, never a culprit ranking.

Copy-paste implementation using only the standard library:

```python
import json
m = json.load(open("relay-brief-assessment.json"))
sc, items = m["scoring"], m["items"]
hi, lo = len(m["scale"]["labels"]), 1            # likert bounds (this scale is 1..5)
rev = {it["id"] for it in items if it.get("reverse")}
def total(ans):                                   # ans: {item_id: score}
    return sum((hi + lo - v) if k in rev else v for k, v in ans.items())
# total_delta = total(post) - total(pre)
# construct_deltas: per construct, take that dimension's items and apply the same two totals
print(sc["reported"], "| unit:", m["unit"], "|", sc["report_note"])
```

// Note: the `version` inside `relay-brief-assessment.json` describes the scale itself and is independent of this skill's frontmatter `version`.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the relay stays open.
