---
name: the-listening-ladder
description: A 15-minute, 2-person (or trio) listening exercise that climbs three rungs — the words, the feeling, what was left unsaid — with poker-spec role cards, a validator mechanic and a pair-level pre/post measure.
version: 2.1.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*), Bash(npm:*), Bash(formlm-cli:*), Bash(python3:*)
metadata:
  category: communication
  group_size: 2
  duration_minutes: 15
  setting: offline
  props: [poker role cards, 3 round cards, 1 validator card per trio]
  depth: assessment-type
  language: en
  updated: 2026-10-11
---

# The Listening Ladder

Words, then the feeling under them, then what was left unsaid. A third role — the validator — says only *landed* or *not yet*, so hearing becomes something you can check instead of something you claim.

## When to use this activity

- A team hears the words but keeps missing the point, and is surprised by what comes back.
- You have 15 minutes and pairs or trios, not a whole-room energy to burn.
- You want a measurable before/after for a communication session — this folder carries a pair-level pre/post measure.

## What is in the folder

| File | Purpose |
|---|---|
| `the-listening-ladder-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): Speaker, Listener, Validator + three round cards |
| `the-listening-ladder-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `the-listening-ladder-guide.md` | Run sheet: objectives, setup with a materials table, minute-by-minute script, failure modes and rescues, variations |
| `the-listening-ladder-debrief.md` | 6 debrief questions with what each targets + validator-card reading + four failure modes of the debrief |
| `the-listening-ladder-assessment.json` | Pre/post measure preset: 5 items, one reverse-scored, pair-level deltas |
| `the-listening-ladder-paper-form.pdf` | A4 answer sheet — print-and-fill form (workshop version) |
| `the-listening-ladder-slide-deck.pdf` | Slide deck — 12 slides for running the session, one idea per slide |
| `the-listening-ladder-slide-deck.html` | Slide deck (HTML) — present from any browser, one keypress per point, speaker notes built in |
| `the-listening-ladder-workbook.pdf` | Participant workbook — plain-language intro, guided rung notes, action page |
| `the-listening-ladder-license.md` | License in plain language — what you may do, what you must keep |
| `the-listening-ladder-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `the-listening-ladder-start-here.md` | Start here — pick your lane, file map, print lists |

## Running it

1. Print one prop-card set per trio (or per pair, if the pair self-validates).
2. Run the pre-measure (2 min) **before** pairing up.
3. Round A: literal paraphrase, words only. Validator raises *landed / not yet*.
4. Round B: same speaker, add the feeling, then check "have I got that right?".
5. Round C: new topic, one question about what was left unsaid — then hold the silence.
6. Run the debrief from `the-listening-ladder-debrief.md`; the cards stay on the table.
7. Run the post-measure (2 min). Report pair deltas, never individual rankings.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/the-listening-ladder/files/the-listening-ladder.zip
unzip the-listening-ladder.zip   # -> the-listening-ladder/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `the-listening-ladder` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable role cards (poker prop-card deck, CC BY 4.0)
curl -O https://workshopskill.com/en/activities/the-listening-ladder/files/the-listening-ladder-prop-cards.pdf

# 2. Get the A4 pre/post answer sheet (print one per participant)
curl -O https://workshopskill.com/en/activities/the-listening-ladder/files/the-listening-ladder-paper-form.pdf

# 3. Get the debrief (questions + rescues) and the run sheet
curl -O https://workshopskill.com/en/activities/the-listening-ladder/files/the-listening-ladder-debrief.md
curl -O https://workshopskill.com/en/activities/the-listening-ladder/files/the-listening-ladder-guide.md
```

The measured result does not depend on FormLM — you can score the pre/post offline with no account (see "Score it offline"). The live form is purely optional.

The live pre/post measure is built with the FormLM CLI. It needs a free FormLM account; the form and its data stay in your own workspace:

```bash
npm install -g @formlm/cli
formlm-cli auth login
formlm-cli smart generate --input "Pre/post measure for The Listening Ladder: 5 Likert items on paraphrase-before-reply, feeling-recognition, unsaid-checking, self-reference (reverse-scored) and repair — the same 5 items before and after the three-round exercise, so each pair's delta is computed automatically"
```

If the agent cannot complete the interactive `formlm-cli auth login` (headless run, CI, no browser): still run the curl steps, keep `the-listening-ladder-assessment.json` as the measure spec, and hand the login and the generate command to a human — or have a human log in once, then re-run only the generate step.

Useful preparation facts for the agent:
- Works in pairs or trios: 12 people = 6 pairs (self-validating) or 4 trios (dedicated validator).
- Agenda math: pre-measure 2 + three rounds 9 + debrief 3 + post-measure 2 ≈ 16 minutes.
- No projector needed; the deck is optional and nothing in the folder requires a screen.
- Print at poker. One card set per trio fits one A4 sheet.

**Where to put the skill.** Drop the unzipped `the-listening-ladder/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/the-listening-ladder/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/the-listening-ladder/`, Qoder `~/.qoder/skills/the-listening-ladder/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- The silence after a round-C question is the design, not a failure to facilitate. Do not fill it.
- If the validator softens to "close enough", restate the rule: two faces only, and "not yet" is the useful one.
- The strongest transfer question: "Which rung do you already skip at work, and what does skipping it cost you?"

## Score it offline (no account)

The full scoring spec already ships in this folder's `the-listening-ladder-assessment.json` (the `scoring` field), so you can produce a result without FormLM — an agent can compute it locally:

1. Collect each respondent's Likert answers for every `items` question (a pre round and a post round).
2. Reverse-score the items flagged in `scoring.reverse_scored_items` (or `items[].reverse` true): `new = scale_max + scale_min - raw`.
3. Tally by `scoring.method` (`sum` adds the items) into a pre total and a post total.
4. Emit exactly `scoring.reported`: `pair_delta` (post - pre, per the top-level `unit`) and `construct_deltas` (repeat per `items[].construct` group).
5. Honour `scoring.report_note`: report pair-level change only, never an individual ranking.

Copy-paste implementation using only the standard library:

```python
import json
m = json.load(open("the-listening-ladder-assessment.json"))
sc, items = m["scoring"], m["items"]
hi, lo = len(m["scale"]["labels"]), 1            # likert bounds (this scale is 1..5)
rev = {it["id"] for it in items if it.get("reverse")}
def total(ans):                                   # ans: {item_id: score}
    return sum((hi + lo - v) if k in rev else v for k, v in ans.items())
# pair_delta = total(post) - total(pre)
# construct_deltas: per construct, take that dimension's items and apply the same two totals
print(sc["reported"], "| unit:", m["unit"], "|", sc["report_note"])
```

// Note: the `version` inside `the-listening-ladder-assessment.json` describes the scale itself and is independent of this skill's frontmatter `version`.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the ladder stays open.
