# Relay Brief — Debrief Sheet

> Six questions, three failure modes of the debrief itself, one rule: both versions stay visible until the room is done with them.
> Use with `relay-brief-guide.md`. The debrief runs minutes 14–18.

---

## How to run this debrief

- Write the original brief on one side of a flip chart and the rebuild on the other, **in the words the last person used**. Erasing nothing is the whole discipline.
- Go hop by hop, not person by person. The unit of analysis is the hop; the moment the room starts analysing people, the lesson is gone.
- End on a sentence someone will actually say out loud tomorrow. Insight without a script evaporates by Wednesday.

---

## Read the two versions side by side

1. **What survived.** Count the constraints the rebuild kept. Most lines land two or three out of five. That number is the data, not a score to defend.
2. **What was dropped.** Which constraint vanished first? Usually the least vivid one — a bare date, a finish spec — which is exactly what quietly falls out of real handovers.
3. **What was invented.** Point at a detail in the rebuild that was never in the original. Nobody lied; every hole gets filled with something plausible. That is assumption-injection, live.

---

## The six questions

**1. The line at work.**
"Where in a normal week does your work go down a four-hop line like this one — stand-up, ticket, forward, 'as discussed'?"
→ Targets: transfer. Expect ticket comments, shift handovers, "I'll just tell them at stand-up". Ask which specific chain they mean.

**2. Confident and wrong.**
"Which hop felt most certain it passed it on clearly?"
→ Targets: the gap between certainty and fidelity — the finding itself. Do not let the room turn hop three into a character; the hop was certain *because* it had nothing else to work with.

**3. The written form.**
"What one written form — a spec, a checklist, a recap message — would have stopped the biggest loss you just saw?"
→ Targets: a concrete repair with an owner. A recap message costs ten seconds; the rebuild cost the line three constraints.

**4. The invented detail.**
"Point at something in the rebuild that was never in the original. Where did it come from?"
→ Targets: assumption-injection made visible. Naming one invented detail is worth more than a rule about "don't guess".

**5. What fell first, and why that one.**
"Which constraint vanished first in your line — the date, the quantity, the finish, the place? Why that one?"
→ Targets: salience. Vivid, concrete items survive a hop; bare numbers and qualifiers die. That ordering is what a written spec is for.

**6. The restated brief.**
"Who will restate the next real brief back to its author today? Say the sentence you will use."
→ Targets: rehearsal in words. "Can I read that back to you?" is a habit; "let's communicate better" is a poster.

---

## Failure modes of the debrief itself

| Failure mode | Why it happens | The rescue |
|---|---|---|
| It plays as a party game | The dropped bits are genuinely funny | Laugh once, then point at the chart: "that exact loss is in your inbox this week." |
| The line blames the middle | One hop clearly dropped a lot | Read the hops in order — each had only what the last gave it. The channel leaks, not the person. |
| Nobody owns a fix | The debrief stalls at "wow" | End on one written-handover habit with a name and a when, out loud, in the room. |

---

## Scoring cues (assessment-type sessions)

If you ran the pre/post measure (`relay-brief-assessment.json`), these observables during the relay are what justify the shift in the report:

| Observable | Points to |
|---|---|
| A hop asks a question and is correctly refused | The rule is understood, not resented |
| The rebuild keeps a qualifier nobody emphasised | Salience, not effort, decided what survived |
| Someone volunteers "I added that" about an invention | Assumption-injection recognised in themselves |
| At the reveal, a hop revises its own confidence | The measure's target construct, moving in real time |

---

## Reading the pre/post

Score the individual before/after delta and the team's average shift (see `relay-brief-assessment.json`). Report `total_delta` and `construct_deltas`, honour `report_note` — and never rank a person by how much they dropped. A relay loses information at every hop by design; the finding is about the channel.
