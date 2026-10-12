# Post-Training Survey — Facilitator Guide

> Folder: `post-training-survey` · Category: feedback forms · any group size · 5 min to complete · after the session · paper or online
> License: CC BY 4.0

A one-page feedback survey for any training session or workshop — six Likert items and two open questions. It exists because most training feedback stops at the smile sheet: "did you enjoy it?" This survey asks the question sponsors actually care about: "will anything from today show up in the work?"

---

## Why this survey is not a smile sheet

Kirkpatrick's Level 1 measures reaction — satisfaction, fun, energy. It is where most evaluation stops, because satisfaction is easy to collect and pleasant to report. But reaction scores tell a sponsor almost nothing about whether the training worked.

Three of the eight questions here push past it:

| Question | What it actually measures |
|---|---|
| Item 2 — "I can name one thing I will use within two weeks" | Transfer intent (the bridge toward Level 3) |
| Q7 — "the one thing you will do differently on Monday" | A checkable commitment, in the participant's own words |
| Q8 — "what got in the way of your learning" | Design obstacles — free consulting for your next delivery |

A smile sheet can only go up. This survey can tell you what to fix.

---

## When to hand it out

| Timing | Response rate | Notes |
|---|---|---|
| Last 5 minutes, in the room | 90%+ | The default. People are still there; leaving takes effort |
| Same evening, by link | 40–60% | Only if the session runs to the minute. Send before 21:00 |
| The next day | under 25% | Acceptable for multi-day programs, useless for single sessions |

Never announce the survey "later by email" while the room is still together — you are donating your best response window.

---

## Paper or online

The paper cards in this folder are the honest default: no login, no device hunting, no "I'll do it later". Hand them out, collect them in a box by the door, score them on the train home.

The online version earns its keep at volume — 40 participants, automatic scoring, a shareable results link. Every item is identical; use whichever the room allows. The one-click online build is linked from the folder page.

---

## The anonymity promise

Write it on the whiteboard before you hand anything out, and keep it to three claims:

1. No names, no tracking, no code numbers.
2. Results are reported as room-level averages only.
3. The facilitator sees them **after** the report goes to the sponsor, not during.

A promise you cannot keep is worse than no promise — if you must identify respondents (certificate programs, compliance), say so on the form instead and drop the word "anonymous".

---

## Reading the answers

Do not read averages first. Read item 2 and Q7 first — that is your evidence of transfer. The full item-by-item interpretation table, the reverse-item trap, and the sponsor reporting rules live in `post-training-survey-debrief.md`.

---

## Known failure modes & rescues

1. **The survey goes out the next day.** Response rate collapses below 25%. Rescue: keep five blank minutes at the end of every agenda, protected like a fire exit.
2. **The anonymity promise is a formality.** If the promise sounds canned, answers drift polite and useless. Rescue: say it out loud, in your own words, before handing out the cards.
3. **Only the average gets reported.** A 4.1 average with a 2.2 on "pace" is a different session than a flat 4.1. Rescue: report the lowest item, always — see the debrief sheet.

---

## Variations

- **Multi-day programs:** run the survey at the end of each day, not only the last. Day-over-day movement on item 3 (pace) tells you more than the final average.
- **Corporate training with compliance requirements:** the same items double as training-effectiveness evidence for internal quality systems (Taiwan: TTQS-aligned course documentation; Hong Kong: QF-style course records). Attach the room-level summary, not individual sheets.
- **Small senior groups (under 6):** skip the Likert cards and run the two open questions as a closing round, out loud.

---

## Props in this folder

- `post-training-survey-prop-cards.pdf` — poker print-ready card deck: instruction card, item cards, open-questions card
- `post-training-survey-guide.md` — this guide
- `post-training-survey-debrief.md` — how to read and report the answers
- `post-training-survey-assessment.json` — the full question set as plain JSON
- `post-training-survey-paper-form.pdf` — the A4 answer sheet: the measure as a print-and-fill form
- `post-training-survey-workbook.pdf` — participant workbook: the idea in plain words, guided items, notes and action pages
- `post-training-survey-slide-deck.pdf` — the slide deck for teaching or projecting
- `post-training-survey-slide-deck.html` — the same deck for any browser, speaker notes on N
- `post-training-survey-license.md` — what you may do with all of this, in plain language
- `post-training-survey-activity-poster.pdf` — The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs.
- `post-training-survey-start-here.md` — one page, thirty seconds, then print and go
- `SKILL.md` — machine-readable manifest for AI agents
- `post-training-survey-run-sheet.pdf` — the print edition: this run sheet + the debrief sheet, bound as one A4 PDF

## Agent version

Every file in this folder has a stable public URL — an AI agent can fetch the cards, the reading guide and this run sheet with three curl commands (see `SKILL.md`), or build the live online version in one `formlm-cli smart generate` step. The paper version needs no screen at all: cards, pens, and a box by the door.
