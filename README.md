# WorkshopSkill — facilitation activity skills for AI agents

46 ready-to-run facilitation activities, each packaged as an agent skill folder. Every
folder holds a `SKILL.md` (frontmatter for matching, minute-by-minute run sheet, debrief
script, prep facts), the supporting markdown the skill references, a machine-readable
pre/post measure spec where the activity has one, and a browser-presentable slide deck.
Free under [CC BY 4.0](LICENSE.md).

The canonical archive is **[workshopskill.com](https://workshopskill.com)** — printable
PDFs (run sheets, poker-spec prop cards, A3 posters, workbooks, US Letter editions) and
the full zip bundles are served from there, not from this repo, to keep the clone light.
Each `SKILL.md` carries the one-command curl to pull the full bundle when you need it.

## Install

**npx skills (Claude Code, Codex, Cursor, Gemini CLI, Qoder and other loaders):**

```bash
npx skills add formlm/workshopskill            # all 46
npx skills add formlm/workshopskill --list     # see what is there
npx skills add formlm/workshopskill --skill blind-portrait
```

**Claude Code plugin marketplace:**

```bash
claude plugin marketplace add formlm/workshopskill
claude plugin install workshopskill@workshopskill
```

**By hand:** copy any `skills/<name>/` folder into your agent's skills directory
(`~/.claude/skills/`, `~/.codex/skills/`, `~/.qoder/skills/`, or `.claude/skills/` per
project) and it loads automatically.

## The catalog

| Skill | Category | What it is |
|---|---|---|
| [`advantage-compass`](skills/advantage-compass/SKILL.md) — The Advantage Compass | self-assessment | A personal strategy self-assessment — two axes (strength x weakness, vision x pain), four quadrants, a two-week time audit and one committed move. Poker-spec print cards, an A3 model poster, a presenter-grade HTML deck, or a live online form. |
| [`assumption-audit`](skills/assumption-audit/SKILL.md) — Assumption Audit | creativity | A 20-minute, 3-8 person pass that surfaces the unwritten things a plan needs to be true, tags each as Evidence / To-verify / Fragile-if-false, and ranks the fragile ones down to the two or three that would actually break the plan — each with an owner and a date to check. Printable poker cards and an A3 poster; no account, no projector. |
| [`blanket-drop`](skills/blanket-drop/SKILL.md) — Blanket Drop | icebreakers | Two-team name game behind a dropping blanket: first correct shout scores, wrong names give a free point. Planted-feet safety rule; names learned at recall speed. |
| [`blind-portrait`](skills/blind-portrait/SKILL.md) — Blind Portrait | communication | A 15-minute, 2-person back-to-back drawing exercise that makes one-way communication visible — with printable prop cards, an 8-question debrief, and a pre/post pair-level assessment. |
| [`common-ground`](skills/common-ground/SKILL.md) — Common Ground | icebreakers | Group icebreaker with a scoring engine: facts true of everyone score 1, surprising grounds score 3, opinions score 0, every member verifies every line. |
| [`draw-what-i-mean`](skills/draw-what-i-mean/SKILL.md) — Draw What I Mean | communication | A 12-minute, pairs (2 people) describe-and-draw tool that runs three rounds — free words, a shared shape-word card, then open clarifying questions — to show that instruction precision and a shared shorthand beat a confident description. Printable poker-spec cards and an A3 poster; no account, no projector. |
| [`escalation-map`](skills/escalation-map/SKILL.md) — Escalation Map | conflict | A 25-minute, 4-12 person conflict post-mortem that plots the arc of a getting-hot disagreement as a heat ladder — Warm, Heated, Boiling, Point of no return — writes what could have kept each rung one degree cooler, and circles the earliest cheap move. Names stay off the wall; the map is about the shape of getting hot. Printable poker rung cards and an A3 poster; no account, no projector. |
| [`exit-ticket`](skills/exit-ticket/SKILL.md) — Exit Ticket | feedback-forms | A 3-minute printable exit-ticket pack — each person writes three lines (learned, open question, next move) on a printed blank slip, plus a guide for reading the collected slips fast. |
| [`four-lens-sweep`](skills/four-lens-sweep/SKILL.md) — Four-Lens Sweep | creativity | A 20-minute, 4-10 person way to review one idea four times — Facts, then Feelings, then Risks, then Upside — with everyone in the same lens at the same time, so a room looks at one object four ways instead of arguing positions. Printable poker lens cards and an A3 poster; no account, no projector. |
| [`mad-sad-glad`](skills/mad-sad-glad/SKILL.md) — Mad · Sad · Glad | reviews | A 20-minute, 6–20 person retrospective. Everyone writes what about the last cycle made them mad, sad, and glad — the team clusters the notes, dot-votes what resonates, and lands one concrete, owned action per colour. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`minefield`](skills/minefield/SKILL.md) — Minefield | trust | Trust exercise in pairs: a blindfolded walker crosses a soft-obstacle course guided by voice only. Stop-word is absolute; both trust directions get debriefed. |
| [`one-minute-meetup`](skills/one-minute-meetup/SKILL.md) — One-Minute Meetup | icebreakers | A 15-minute, 6-20 person rotating-pairs energizer where each pair gets exactly one minute to find a surprising shared thing — three escalating timed rounds plus a one-line gallery — so a room of semi-strangers builds real common ground faster than an open mingle. Printable poker-spec cards and an A3 poster; no account, no projector. |
| [`paper-plane-intros`](skills/paper-plane-intros/SKILL.md) — Paper Plane Intros | icebreakers | A 15-minute, 8-20 person icebreaker where everyone writes one non-obvious line about themselves, folds it into a paper plane and throws it across the room, then finds the author and asks a real follow-up question — a physical remix plus a genuine exchange that mixes a room past its usual clusters. Printable instruction cards and an A3 poster; no account, no projector. |
| [`paper-tower`](skills/paper-tower/SKILL.md) — Paper Tower | communication | Team build challenge: 20 sheets, 1 m tape, 12 minutes; the tallest tower that holds a book for ten seconds wins. The book test exposes the height-vs-stability trade. |
| [`post-training-survey`](skills/post-training-survey/SKILL.md) — Post-Training Survey | feedback-forms | A one-page post-training feedback survey — 6 Likert items plus 2 open questions, printable poker cards or a live online form, built one step past the smile sheet. |
| [`relay-brief`](skills/relay-brief/SKILL.md) — Relay Brief | communication | A 20-minute, 8-20 person telephone-game exercise where a five-constraint task brief is relayed down a line and rebuilt, exposing how verbal handover leaks — with printable cards, an observer tally and an individual pre/post measure on handover discipline. |
| [`roleswap-argument`](skills/roleswap-argument/SKILL.md) — Roleswap Argument | conflict | A 20-minute, 6–16 person conflict tool. Take a real disagreement in the room, then make each side argue the *other* side's position honestly — steel-man it, land one true thing in it, and name the shared need underneath both. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`rotate-the-lead`](skills/rotate-the-lead/SKILL.md) — Rotate the Lead | leadership | A 25-minute, 8–16 person leadership tool. Give the team a real small task, then rotate who's leading every ~4 minutes — each handover restates the goal, what's done, and the next move before directing, and each lead makes one visible, owned call. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`same-boat`](skills/same-boat/SKILL.md) — Same Boat | conflict | A 20-minute, 6-16 person conflict reframe where two sides at odds each list only what they will both lose if the dispute keeps running, and the overlap becomes one shared "same boat" card — moving from "against them" to "beside them, facing the same problem", with a separate "still different" card for genuine disagreement. Printable poker cards and an A3 poster; no account, no projector. |
| [`silent-lineup`](skills/silent-lineup/SKILL.md) — Silent Lineup | leadership | Whole-group lineups in silence: birthday round then seniority round. Non-verbal coordination reveals who leads, who follows early, and who unsticks jams. |
| [`skill-radar`](skills/skill-radar/SKILL.md) — Skill Radar | self-assessment | A 20-minute, 6–16 person self-assessment tool. Each person rates themselves 1–5 across five or six role-specific axes, connects the points into a radar (spider) chart, overlays the shape the role needs, and targets the one short spoke. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`smile-sheet-alternative`](skills/smile-sheet-alternative/SKILL.md) — Beyond the Smile Sheet | feedback-forms | A 10-minute feedback question bank that goes past the smile sheet — six printable poker items capturing what landed, confidence to apply and the barrier, plus a reading guide. |
| [`start-stop-continue`](skills/start-stop-continue/SKILL.md) — Start · Stop · Continue | reviews | Wall retrospective with three verbs: start, stop, continue. One behavior per card, never a person; no card survives without an owner and a date. |
| [`step-in-if`](skills/step-in-if/SKILL.md) — Step In If… | trust | A 15-minute, 8–20 person trust and belonging exercise. The group stands in a circle; read-aloud "Step in if…" statements, and anyone they're true for steps into the centre, sees who's standing with them, and steps back — no explanation, no names attached. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`storyboard-the-journey`](skills/storyboard-the-journey/SKILL.md) — Storyboard the Journey | creativity | A 25-minute, 4-12 person mapping tool that lays one person's end-to-end experience out as a strip of storyboard panels, marks each with a high / low / hope, and draws the experience line through them — so a team argues about the same valley instead of its own box. Printable poker panel cards and an A3 poster; no account, no projector. |
| [`the-decision-rights-map`](skills/the-decision-rights-map/SKILL.md) — The Decision Rights Map | leadership | A 25-minute, 4–10 person leadership tool. Lay out the decisions a team actually makes and, for each, name exactly one decider, who must be consulted before, and who is informed after — then find the decisions where the pen is in the wrong hand and reassign one. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`the-delegation-map`](skills/the-delegation-map/SKILL.md) — The Delegation Map | leadership | A 25-minute, 4–10 person leadership tool that lays out everything a leader still personally owns, sorts it into Only me · Coach someone · Anyone can run, and circles the one highest-leverage hand-off for this week with a named owner, the support they get, and a review date. Poker-spec zone cards and an A3 poster included; no account, no projector. |
| [`the-energy-audit`](skills/the-energy-audit/SKILL.md) — The Energy Audit | self-assessment | A 15-minute, solo-or-pair self-assessment tool. List the recurring things you actually do in a normal week, mark each + (gives energy) / − (drains) / = (neutral), name the biggest drain you keep choosing and the biggest + you keep skipping, and commit one dated swap. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`the-feedback-digest`](skills/the-feedback-digest/SKILL.md) — The Feedback Digest | self-assessment | A 20-minute, 1–2 person self-assessment tool. Collect the feedback you've actually received, sort it into Already knew / Surprised me / I'll dismiss, read the surprised pile as your blindspot, then write one honest sentence the evidence supports and one action that follows from the surprise. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`the-leader-checkup`](skills/the-leader-checkup/SKILL.md) — The Leader Checkup | leadership | A 25-minute, 3–10 person leadership tool. The team gives their leader structured upward feedback — what's working, what quietly blocks them, one ask — and the leader's only job is to listen without defending, then commit to one change with a follow-up date. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`the-listening-ladder`](skills/the-listening-ladder/SKILL.md) — The Listening Ladder | communication | A 15-minute, 2-person (or trio) listening exercise that climbs three rungs — the words, the feeling, what was left unsaid — with poker-spec role cards, a validator mechanic and a pair-level pre/post measure. |
| [`the-not-anymore-list`](skills/the-not-anymore-list/SKILL.md) — The Not-Anymore List | reviews | A 25-minute, 4–12 person review pointed at subtraction. The team lists its recurring work, runs the "if we weren't doing this, would we start it today?" test, and actually stops one thing — with a bring-back trigger, an owner, and a review date. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`the-orange`](skills/the-orange/SKILL.md) — The Orange | conflict | Positions-vs-interests negotiation: two teams, one orange, hidden complementary briefs (flesh vs peel). Half-half is legal; integration is the lesson. |
| [`the-premortem`](skills/the-premortem/SKILL.md) — The Premortem | reviews | A 25-minute, 4–12 person review that runs backwards from a future failure. The team assumes the project already failed, writes the story of how, and turns polite-unsaid risks into causes with early-warning signals and one preventive action with an owner and a by-when. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`the-reliability-ledger`](skills/the-reliability-ledger/SKILL.md) — The Reliability Ledger | trust | A 25-minute, 4–10 person trust tool that treats trust as a record of kept promises. Each person writes two commitments ("I'll reliably…") and one need ("I quietly need…"), the group surfaces one broken-but-unspoken expectation, and they commit one repair with an owner and a check-in date. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`the-safety-check`](skills/the-safety-check/SKILL.md) — The Safety Check | trust | A 20-minute, 4–12 person trust tool. Everyone privately rates four statements — I can ask a dumb question / admit a mistake / disagree with the decision-maker / take a risk without it being used against me — the team reveals the four bars, circles the lowest one, and commits to one concrete behavior that raises it, with a re-check date. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`the-third-story`](skills/the-third-story/SKILL.md) — The Third Story | conflict | A 25-minute, 4–10 person conflict tool. Two sides at odds each tell, in the third person, the story a neutral observer would tell about what's happening between them — what a camera would see, not who's right. Then both name the need under each position and commit one move that serves a shared need. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`the-trust-timeline`](skills/the-trust-timeline/SKILL.md) — The Trust Timeline | trust | A 25-minute, 4–10 person trust tool. A team lays its shared history on a line — moments trust grew, broke, and got repaired — reads the pattern of what breaks and rebuilds trust here, and picks one live break to repair with an owner and a check-in date. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`the-turning-point`](skills/the-turning-point/SKILL.md) — The Turning Point | reviews | A 25-minute, 4–12 person review that rebuilds a project's timeline from start to now, marks the dated moments it turned up or down, names the decision or habit behind each turn, and commits to keep one good-turn habit and kill one bad-turn habit. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`the-values-sort`](skills/the-values-sort/SKILL.md) — The Values Sort | self-assessment | A 20-minute, 1–8 person self-assessment tool that makes choosing values expensive. You sort a value-card deck into Core / Important / Not mine with a hard cap of five on Core, cut to five, then check one real recent decision against them and close one gap. Poker-spec cards and an A3 poster included; no account, no projector. |
| [`training-evaluation-form`](skills/training-evaluation-form/SKILL.md) — Training Evaluation Form | feedback-forms | A Kirkpatrick-ready training evaluation pack — 8 reaction items, confidence self-reports, keep/change questions, and a day-30 follow-up for Level 3 behavior evidence. |
| [`training-needs-survey`](skills/training-needs-survey/SKILL.md) — Training Needs Survey | feedback-forms | A 15-minute pre-course training-needs questionnaire — six printable poker items capturing current ability, target ability, priority and the cost of the gap, plus a guide for turning answers into a curriculum. |
| [`two-truths`](skills/two-truths/SKILL.md) — Two Truths and a Lie | icebreakers | Icebreaker with guardrails: three statements per person, all public work facts, one false; the group votes eyes-closed. Nobody is publicly wrong about a colleague. |
| [`workshop-feedback-form`](skills/workshop-feedback-form/SKILL.md) — Workshop Feedback Form | feedback-forms | A 90-second exit ticket for public workshops — 4 rating items, a recommendation score, two open questions that produce permissioned testimonials and a voted topic list. |
| [`worst-idea-first`](skills/worst-idea-first/SKILL.md) — Worst Idea First | creativity | Reverse brainstorm: five minutes engineering how a real target fails, then flip every item into prevention. The game rewards saying the awkward thing. |
| [`yes-and-ramp`](skills/yes-and-ramp/SKILL.md) — Yes-And Ramp | creativity | A 15-minute, 4-12 person creativity drill where a group builds one idea by each person saying "yes, and…" and adding a turn — accepts only, never "but" — so a plain seed climbs a ramp until it's unrecognisable, training building-on-others over editing-them. Printable poker prompt cards and an A3 poster; no account, no projector. |

## Languages

This repo mirrors the English skill files. Simplified and Traditional Chinese editions of
every skill ship on the site, indexed per language:
[skills.json](https://workshopskill.com/skills.json) →
[/zh/skills.json](https://workshopskill.com/zh/skills.json) ·
[/zh-hant/skills.json](https://workshopskill.com/zh-hant/skills.json)

## Licensing

Tier 0 is CC BY 4.0: run it for money, print unlimited copies, adapt, translate,
rebrand — keep the attribution line in each folder's `*-license.md`. Paid tiers (single
event, organization) waive the attribution line:
[workshopskill.com/en/licensing.html](https://workshopskill.com/en/licensing.html).

Questions: hello@workshopskill.com
