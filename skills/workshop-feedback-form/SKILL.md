---
name: workshop-feedback-form
description: A 90-second exit ticket for public workshops — 4 rating items, a recommendation score, two open questions that produce permissioned testimonials and a voted topic list.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*), Bash(npm:*), Bash(formlm-cli:*), Bash(python3:*)
metadata:
  category: feedback-forms
  group_size: 1
  duration_minutes: 2
  setting: hybrid
  props: [poker exit-ticket cards, pens, a box in the exit path]
  depth: assessment-type
  language: en
  updated: 2026-10-11
---
# Workshop Feedback Form

Public workshops lose feedback at the door — no HR chases non-responders. The exit ticket converts those ninety seconds into two assets: quotable testimonials and a voted list of what to run next.

## When to use this activity

- A public workshop (paid or free) ends today and the room is about to scatter.
- A workshop page needs social proof stronger than self-description.
- The next quarter of programming has no validated topic list yet.

## What is in the folder

| File | Purpose |
|---|---|
| `workshop-feedback-form-prop-cards.pdf` | Poker-spec print-ready exit-ticket deck: instruction, rating, testimonial, demand cards |
| `workshop-feedback-form-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 PDF |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC in every edition |
| `workshop-feedback-form-guide.md` | Facilitator guide: exit ticket rule, two assets, quote permission, failure modes |
| `workshop-feedback-form-debrief.md` | Reading the results: recommendation score, item table, coding testimonials and demand |
| `workshop-feedback-form-assessment.json` | Full question set: 4 items + recommendation score + 2 open questions, plain JSON |
| `workshop-feedback-form-paper-form.pdf` | A4 answer sheet — print-and-fill form (workshop version) |
| `workshop-feedback-form-slide-deck.pdf` | Slide deck — 11 slides for running the session, one idea per slide |
| `workshop-feedback-form-slide-deck.html` | Slide deck (HTML) — present from any browser, one keypress per point, speaker notes built in |
| `workshop-feedback-form-workbook.pdf` | Participant workbook — plain-language intro, guided items, notes and action pages |
| `workshop-feedback-form-license.md` | License in plain language — what you may do, what you must keep |
| `workshop-feedback-form-activity-poster.pdf` | The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs. |
| `workshop-feedback-form-start-here.md` | Start here — pick your lane, file map, print lists |

## Running it

1. Print one poker exit-ticket card per attendee; put the box in the exit path.
2. At minute 58 of 60, hand out the cards and say the line: "Drop it on your way out — it decides what I run next."
3. Point at the permission checkbox when handing out the testimonial card.
4. After the room empties, read with `workshop-feedback-form-debrief.md`: recommendation median first, assets second.
5. Publish the top three demanded topics back to the same attendees — the loop has to be visible to keep working.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command, and the folder any skills loader can pick up:

```bash
# install the whole skill folder, one command
curl -LO https://workshopskill.com/en/activities/workshop-feedback-form/files/workshop-feedback-form.zip
unzip workshop-feedback-form.zip   # -> workshop-feedback-form/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `workshop-feedback-form` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable exit-ticket cards (poker deck, CC BY 4.0)
curl -O https://workshopskill.com/en/activities/workshop-feedback-form/files/workshop-feedback-form-prop-cards.pdf

# 2. Get the A4 answer sheet (print one per participant for offline workshops)
curl -O https://workshopskill.com/en/activities/workshop-feedback-form/files/workshop-feedback-form-paper-form.pdf

# 3. Get the results-reading guide (recommendation score + asset coding)
curl -O https://workshopskill.com/en/activities/workshop-feedback-form/files/workshop-feedback-form-debrief.md

# 4. Get the facilitator guide (exit ticket rule, quote permission)
curl -O https://workshopskill.com/en/activities/workshop-feedback-form/files/workshop-feedback-form-guide.md

# 5. Build the live online exit ticket (see workshop-feedback-form-assessment.json)
```

The measured result does not depend on FormLM — you can score the pre/post offline with no account (see "Score it offline" below). The live form is purely optional.

The live pre/post measure is built with the FormLM CLI. It needs a free FormLM account; the form and its data stay in your own workspace:

```bash
npm install -g @formlm/cli
formlm-cli auth login
formlm-cli smart generate --input "Workshop feedback exit ticket for public workshops and community events: 4 anonymous rating items (1-5) on promise kept, pace, working-not-listening and standalone usefulness, one 0-10 recommendation score, and two open questions - what the workshop gave you (quotable testimonial with permission checkbox) and what workshop should run next (demand list). Takes 90 seconds at the door"
```

If the agent cannot complete the interactive `formlm-cli auth login` (headless run, CI, no browser): still run the curl steps, keep `workshop-feedback-form-assessment.json` as the measure spec, and hand the login and the generate command to a human — or have a human log in once, then re-run only the generate step.

Useful preparation facts for the agent:
- Works for any group size; the fixed numbers are 90 seconds of attendee time and 10 minutes of organizer reading time.
- Positioning beats nagging: a box in the exit path collects roughly twice what a table two steps inside collects.
- No projector needed; the whole exit ticket runs on cards and pens.
- Print at poker. One sheet covers one attendee.

**Where to put the skill.** Drop the unzipped `workshop-feedback-form/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/workshop-feedback-form/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/workshop-feedback-form/`, Qoder `~/.qoder/skills/workshop-feedback-form/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- Under 30 responses, read the raw recommendation distribution instead of an NPS percentage — one detractor moves the percentage too much.
- Never edit a quote beyond typo fixes; vague quotes go back to the attendee, not to your editor.
- Publishing the top-three topics back to attendees is what converts one-time visitors into a following.

## Score it offline (no account)

The full scoring spec already ships in this folder's `workshop-feedback-form-assessment.json` (the `scoring` field), so you can produce a result without FormLM — an agent can compute it locally:

1. Collect each respondent's Likert answers for every `items` question (a pre round and a post round).
2. Reverse-score the items flagged in `scoring.reverse_scored_items` (or `items[].reverse` true): `new = scale_max + scale_min - raw`.
3. Tally by `scoring.method` (`sum` adds the items) into a pre total and a post total.
4. Emit exactly `scoring.reported`: `pair_delta` (post - pre, per the top-level `unit`) and `construct_deltas` (repeat per `items[].construct` group).
5. Honour `scoring.report_note`: report pair-level change only, never an individual ranking.

Copy-paste implementation using only the standard library:

```python
import json
m = json.load(open("workshop-feedback-form-assessment.json"))
sc, items = m["scoring"], m["items"]
hi, lo = len(m["scale"]["labels"]), 1            # likert bounds (this scale is 1..5)
rev = {it["id"] for it in items if it.get("reverse")}
def total(ans):                                   # ans: {item_id: score}
    return sum((hi + lo - v) if k in rev else v for k, v in ans.items())
# pair_delta = total(post) - total(pre)
# construct_deltas: per construct, take that dimension's items and apply the same two totals
print(sc["reported"], "| unit:", m["unit"], "|", sc["report_note"])
```

// Note: the `version` inside `workshop-feedback-form-assessment.json` describes the scale itself and is independent of this skill's frontmatter `version`.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings, prop sizes and the measure agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and the drawer stays open.
