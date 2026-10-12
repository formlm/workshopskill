---
name: the-not-anymore-list
description: A 25-minute, 4–12 person review pointed at subtraction. The team lists its recurring work, runs the "if we weren't doing this, would we start it today?" test, and actually stops one thing — with a bring-back trigger, an owner, and a review date. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: reviews
  group_size: 4
  duration_minutes: 25
  setting: hybrid
  props: [it-costs card, nobody-needs card, kill-or-trial-stop card, bring-it-back-if card, owner-and-date card, blank cards]
  depth: tool-type
  language: en
  updated: 2026-10-09
---

# The Not-Anymore List

A review pointed at subtraction. Teams accumulate work that stopped earning its keep. List the recurring things, ask "if we weren't already doing this, would we start it today?", and actually stop one thing — with a "bring it back if…" trigger, an owner, and a review date so stopping is safe.

## When to use this activity

- A team whose calendar has filled with meetings, reports, and rituals nobody chose this year.
- After a launch, when the process that got you across the line shouldn't survive it.
- You have 4–12 people and 25 minutes; online works if the two columns live on a shared board.

## What's in the folder

| File | Use |
|---|---|
| `the-not-anymore-list-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed, cut guides, card back, blank): an it-costs card, a nobody-needs-it card, a kill-or-trial-stop card, a bring-it-back-if card, an owner-and-date card, a blank card |
| `the-not-anymore-list-run-sheet.pdf` | Print edition: guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size of the print files in this folder — same content, bookmarks and linked contents in every edition |
| `the-not-anymore-list-guide.md` | Facilitator guide: objectives, when to use, setup, how to run it, the card, failure modes, variations, facilitation notes |
| `the-not-anymore-list-debrief.md` | Debrief: how to run it, reading the list, four debrief questions, failure-mode table |
| `the-not-anymore-list-start-here.md` | Quick start — pick a route, set the room, print list |
| `the-not-anymore-list-license.md` | Plain-language licence — what you can do, what you must keep |
| `the-not-anymore-list-activity-poster.pdf` | The whole session on one wall (A3): the two columns, the flow, the two rules |

## How to run it

1. List every recurring thing the team does — meetings, reports, rituals, approvals.
2. For each, ask "if we weren't already doing this, would we start it today?" Mark the failures.
3. Pick ONE thing to stop this week (or trial-stop if the room is nervous).
4. Set the "bring it back if…" trigger, an owner, and a review date.
5. Name what you'll do with the freed capacity — or it silently comes back.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/the-not-anymore-list/files/the-not-anymore-list.zip
unzip the-not-anymore-list.zip   # -> the-not-anymore-list/SKILL.md + every file + manifest
```

Unzipped you get a directory named `the-not-anymore-list` containing this SKILL.md, every file it references, and a manifest.

Only want some files — anonymous, CC BY 4.0:

```bash
# 1. get the printable cards
curl -O https://workshopskill.com/en/activities/the-not-anymore-list/files/the-not-anymore-list-prop-cards.pdf

# 2. get the wall poster
curl -O https://workshopskill.com/en/activities/the-not-anymore-list/files/the-not-anymore-list-activity-poster.pdf

# 3. get the debrief and the guide
curl -O https://workshopskill.com/en/activities/the-not-anymore-list/files/the-not-anymore-list-debrief.md
curl -O https://workshopskill.com/en/activities/the-not-anymore-list/files/the-not-anymore-list-guide.md
```

This session needs no online form and no account — two columns, cards, sticky notes. There is no pre/post measure; the artifact is one thing actually stopped, with a bring-back trigger, an owner, and a review date.

Prep facts for the agent:
- 4–12 people who run recurring work together.
- Flow sums: list it 5 + the test 6 + pick one 6 + make it safe 8 = 25 minutes.
- No projector needed; the poster is optional and nothing requires a screen.
- Print at poker spec. One card sheet per group.

**Where the skill goes.** Drop the unzipped `the-not-anymore-list/` into your agent's skills directory and it loads automatically: Claude Code `~/.claude/skills/the-not-anymore-list/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/the-not-anymore-list/`, Qoder `~/.qoder/skills/the-not-anymore-list/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- If nobody will let go, make it a trial-stop with a date — pausing is easier than killing.
- If the list is all other teams' processes, narrow to what this team can drop unilaterally.
- Push every bring-back trigger until it's observable; a fuzzy trigger means the thing returns by default.

## Remix: make it yours

Want this folder under your own brand, or packaged as your own marketplace product? The license file spells out what you may do: rename the card prompts, reprint the cards and poster at spec, and keep the CC BY attribution line — then use, sell, and redistribute it freely.

## Attribution

Filed by hand and checked folder-to-folder — the script, timings, and prop dimensions agree with each other. CC BY 4.0 free — run it, copy it, rebrand it for your own workshop; keep the attribution line and the list stays open.
