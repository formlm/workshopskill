# Training Evaluation Form — Facilitator Guide

> Folder: `training-evaluation-form` · Category: feedback forms · any group size · 7 min on the day + 3 min at day 30 · paper or online
> License: CC BY 4.0

A Kirkpatrick-ready evaluation pack for corporate training: eight reaction items, three confidence self-reports, two keep/change questions — plus the day-30 follow-up that turns feedback into behavior evidence. It produces a one-page report a manager can forward without translation.

---

## What this form covers

Kirkpatrick's four levels, mapped honestly:

| Level | What it asks | Where it lives in this folder |
|---|---|---|
| 1 — Reaction | Did the room find it relevant, deep, well-run? | The 8 items on the form |
| 2 — Learning | Can people now do the core things? | 3 confidence self-reports (a proxy — see below) |
| 3 — Behavior | Is it showing up in the work? | The day-30 follow-up (3 questions by email) |
| 4 — Results | Did business numbers move? | **Not covered.** Not with a form. Be suspicious of any form that claims it. |

The honest boundary at Level 4 is the feature: evaluation forms that pretend to measure business results produce numbers nobody believes, and then nobody believes the rest of the form either.

---

## Why eight reaction items

Grouped, not piled: four content items (relevance, depth, instructor, materials), three delivery items (exercises, logistics, workload), one overall. In corporate training the delivery items matter as much as the content — a well-taught course with a broken sign-up flow gets scored like a bad course, and the item means will tell you which half to fix.

---

## Level 2: the self-report proxy

The three confidence items are a proxy for learning — cheaper than a test, rougher than a test, and honest about being a proxy. Self-report inflates when the training felt inspiring; it inflates less when the items ask for narrow, checkable abilities ("explain it in two minutes", "apply it without help"). That is why these three are phrased narrow.

If you can collect a baseline — the same three items at sign-up — the delta becomes the credible number. If you cannot, report the absolute values and write "self-report, no baseline" in the report. That one line of honesty is worth more than a chart.

---

## The keep/change questions

The two open questions are not comments; they are the agenda of the next design meeting:

- "What worked so well it should stay exactly as it is?" — protects the good parts from a redesign that "improves" them away.
- "What should change in the next run?" — the fix list, in the participants' own words.

For repeat programs this pair is worth more than every rating combined: ratings tell you where you stand, keep/change tells you what to do.

---

## The day-30 follow-up

Thirty days after the training, send three questions by email (template in the debrief sheet): used-it frequency, what helped or blocked, what support would make it stick. This is the Level 3 behavior check — the level most evaluation never reaches, and the level that answers the question the sponsor actually asked: "did anything change?".

Expect a third of the response rate of the in-room form. That is normal and still enough: behavior counts from a 30% sample are evidence; satisfaction means from a 90% sample are not evidence of behavior at all.

---

## Known failure modes & rescues

1. **The form becomes a satisfaction contest between vendors.** The moment item means are used to rank instructors, answers turn diplomatic and the instrument dies. Rescue: report room-level means to the program owner, never per-instructor league tables.
2. **The day-30 email never gets sent.** The pack halves itself: Level 3 evidence requires the follow-up, and it is always the first thing a busy calendar drops. Rescue: schedule the follow-up email the same day you run the training — write it before you forget who was in the room.
3. **Self-reports reported as learning gains.** Without a baseline, a 4.3 confidence mean is a feeling, not a gain. Rescue: say "self-report, no baseline" in the report — one honest line beats a decorated chart.

---

## Variations

- **Multi-session programs:** run the form after each session; run the day-30 follow-up once, 30 days after the last session.
- **Compliance documentation (Taiwan / Hong Kong):** the item means plus the follow-up behavior counts are exactly what quality systems want as training-effectiveness evidence (TTQS course documentation, QF-style records). File the room-level summary; individual sheets stay private.
- **Vendor-delivered training:** add one item — "My manager knew what I was learning" — the cheapest measure of the transfer climate you will ever install.

---

## Props in this folder

- `training-evaluation-form-prop-cards.pdf` — poker print-ready deck: instruction card, reaction-item cards, confidence card, keep/change card
- `training-evaluation-form-guide.md` — this guide
- `training-evaluation-form-debrief.md` — reading the results, the day-30 email template, the management one-pager
- `training-evaluation-form-assessment.json` — the full question set as plain JSON
- `training-evaluation-form-paper-form.pdf` — the A4 answer sheet: the measure as a print-and-fill form
- `training-evaluation-form-workbook.pdf` — participant workbook: the idea in plain words, guided items, notes and action pages
- `training-evaluation-form-slide-deck.pdf` — the slide deck for teaching or projecting
- `training-evaluation-form-slide-deck.html` — the same deck for any browser, speaker notes on N
- `training-evaluation-form-license.md` — what you may do with all of this, in plain language
- `training-evaluation-form-activity-poster.pdf` — The whole activity on one wall (A3): meta, run of show, debrief questions, watch-outs.
- `training-evaluation-form-start-here.md` — one page, thirty seconds, then print and go
- `SKILL.md` — machine-readable manifest for AI agents
- `training-evaluation-form-run-sheet.pdf` — the print edition: this run sheet + the debrief sheet, bound as one A4 PDF

## Agent version

Every file in this folder has a stable public URL — an AI agent can fetch the cards, the reading guide and this run sheet with three curl commands (see `SKILL.md`), or build the online evaluation in one `formlm-cli smart generate` step — including the day-30 follow-up as a scheduled second collection. The paper version needs no screen: cards, pens, and an email client you already own.
