---
name: post-training-survey
description: A one-page post-training feedback survey — 6 Likert items plus 2 open questions, printable poker cards or a live online form, built one step past the smile sheet.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*), Bash(npm:*), Bash(formlm-cli:*), Bash(python3:*)
metadata:
  category: feedback-forms
  group_size: 1
  duration_minutes: 5
  setting: hybrid
  props: [poker survey cards, pens, a collection box by the door]
  depth: assessment-type
  language: en
  updated: 2026-10-11
---
# Post-Training Survey

Satisfaction is easy to collect and says nothing. This survey asks whether anything from the session will show up in the work — and produces a Monday commitment list plus an obstacle list as evidence.

## When to use this activity

- A training session or workshop ends today and the sponsor expects evidence, not applause.
- A smile sheet already exists and everyone can predict its 4.6.
- A quality system (TTQS, QF-style records) needs course-questionnaire evidence at room level.

## What is in the folder

| File | Purpose |
|---|---|
| `post-training-survey-prop-cards.pdf` | Poker-spec print-ready survey deck: instruction card, item cards, open-questions card |
| `post-training-survey-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 PDF |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `post-training-survey-guide.md` | Facilitator guide: timing, paper vs online, anonymity promise, failure modes |
| `post-training-survey-debrief.md` | Reading the answers: item-by-item table, open-question coding, sponsor reporting |
| `post-training-survey-assessment.json` | Full question set: 6 Likert items + 2 open questions, plain JSON |
| `post-training-survey-paper-form.pdf` | A4 answer sheet — print-and-fill form (workshop version) |
| `post-training-survey-slide-deck.pdf` | Slide deck — 11 slides for running the session, one idea per slide |
| `post-training-survey-slide-deck.html` | Slide deck (HTML) — present from any browser, one keypress per point, speaker notes built in |
| `post-training-survey-workbook.pdf` | Participant workbook — plain-language intro, guided items, notes and action pages |
| `post-training-survey-license.md` | License in plain language — what you may do, what you must keep |
| `post-training-survey-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `post-training-survey-start-here.md` | Start here — pick your lane, file map, print lists |

## Running it

1. Print one survey-card set per participant; put a collection box by the door.
2. Protect the last five minutes of the agenda — hand the survey out **in the room**.
3. State the anonymity promise out loud, in your own words, before handing out cards.
4. Collect, then read with `post-training-survey-debrief.md`: item 2 and the open questions first, averages last.
5. Report four numbers and one sentence — response rate, item-2 mean, lowest item by name, commitment count, one quoted obstacle.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/post-training-survey/files/post-training-survey.zip
unzip post-training-survey.zip   # -> post-training-survey/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `post-training-survey` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable survey cards (poker deck, CC BY 4.0)
curl -O https://workshopskill.com/en/activities/post-training-survey/files/post-training-survey-prop-cards.pdf

# 2. Get the A4 answer sheet (print one per participant for offline workshops)
curl -O https://workshopskill.com/en/activities/post-training-survey/files/post-training-survey-paper-form.pdf

# 3. Get the answer-reading guide (item table + reporting rules)
curl -O https://workshopskill.com/en/activities/post-training-survey/files/post-training-survey-debrief.md

# 4. Get the facilitator guide (timing, anonymity, failure modes)
curl -O https://workshopskill.com/en/activities/post-training-survey/files/post-training-survey-guide.md

# 5. Build the live online survey (6 items + 2 open questions, see post-training-survey-assessment.json)
```

The measured result does not depend on FormLM — you can score the pre/post offline with no account (see "Score it offline" below). The live form is purely optional.

The live pre/post measure is built with the FormLM CLI. It needs a free FormLM account; the form and its data stay in your own workspace:

```bash
npm install -g @formlm/cli
formlm-cli auth login
formlm-cli smart generate --input "Post-training survey for a workshop or training session: 6 anonymous Likert items (1-5) on relevance, transfer intent, pace, facilitation quality and clarity, with one reverse-scored blocker item, plus two open questions - the one thing participants will do differently on Monday, and what got in the way of learning. Takes 5 minutes, room-level reporting only"
```

If the agent cannot complete the interactive `formlm-cli auth login` (headless run, CI, no browser): still run the curl steps, keep `post-training-survey-assessment.json` as the measure spec, and hand the login and the generate command to a human — or have a human log in once, then re-run only the generate step.

Useful preparation facts for the agent:
- Works for any group size; the only fixed numbers are 5 minutes of participant time and 15 minutes of facilitator reading time for 20 responses.
- Timing decays fast: in-room 90%+, same-evening link 40-60%, next-day under 25%. Schedule accordingly.
- No projector needed; the whole survey runs on paper and pens.
- Print at poker. One sheet covers one participant.

**Where to put the skill.** Drop the unzipped `post-training-survey/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/post-training-survey/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/post-training-survey/`, Qoder `~/.qoder/skills/post-training-survey/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- The reverse item (item 6) is the lie detector — polite rooms score it high while scoring everything else high too. Trust it over the average.
- Never report individual sheets or rankings; room-level reporting is what keeps answers honest.
- Quote one obstacle for every compliment you quote — the contrast is what sponsors trust.

## Score it offline (no account)

The full scoring spec already ships in this folder's `post-training-survey-assessment.json` (the `scoring` field), so you can produce a result without FormLM — an agent can compute it locally:

1. Collect each respondent's Likert answers for every `items` question (a pre round and a post round).
2. Reverse-score the items flagged in `scoring.reverse_scored_items` (or `items[].reverse` true): `new = scale_max + scale_min - raw`.
3. Tally by `scoring.method` (`sum` adds the items) into a pre total and a post total.
4. Emit exactly `scoring.reported`: `pair_delta` (post - pre, per the top-level `unit`) and `construct_deltas` (repeat per `items[].construct` group).
5. Honour `scoring.report_note`: report pair-level change only, never an individual ranking.

Copy-paste implementation using only the standard library:

```python
import json
m = json.load(open("post-training-survey-assessment.json"))
sc, items = m["scoring"], m["items"]
hi, lo = len(m["scale"]["labels"]), 1            # likert bounds (this scale is 1..5)
rev = {it["id"] for it in items if it.get("reverse")}
def total(ans):                                   # ans: {item_id: score}
    return sum((hi + lo - v) if k in rev else v for k, v in ans.items())
# pair_delta = total(post) - total(pre)
# construct_deltas: per construct, take that dimension's items and apply the same two totals
print(sc["reported"], "| unit:", m["unit"], "|", sc["report_note"])
```

// Note: the `version` inside `post-training-survey-assessment.json` describes the scale itself and is independent of this skill's frontmatter `version`.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
