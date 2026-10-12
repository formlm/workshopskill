---
name: mad-sad-glad
description: A 20-minute, 6–20 person retrospective. Everyone writes what about the last cycle made them mad, sad, and glad — the team clusters the notes, dot-votes what resonates, and lands one concrete, owned action per colour. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: reviews
  group_size: 6
  duration_minutes: 20
  setting: hybrid
  props: [mad card, sad card, glad card, cluster-vote card, one-action card, owner-revisit card]
  depth: tool-type
  language: en
  updated: 2026-10-10
---

# Mad · Sad · Glad

People rarely say "I'm quietly demotivated" in a standup — but given a Sad column, they'll write it down. Mad/Sad/Glad gets the emotional truth of a sprint or project onto the wall fast, then forces the discipline most retros skip: one concrete action per colour, with a named owner and a revisit date.

## When to use this activity

- A team finishing a sprint, project, or quarter that needs to name how it actually felt — not just what shipped.
- A retro that keeps producing action items nobody owns.
- You have 6–20 people and 20 minutes; it runs on a shared board online.

## What's in the folder

| File | Use |
|---|---|
| `mad-sad-glad-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed, cut guides, back, blank): mad, sad, glad, cluster & vote, one action each, owner & revisit cards |
| `mad-sad-glad-run-sheet.pdf` | Print edition: facilitator guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper for this folder's print files — same content, every version bookmarked with a linked contents page |
| `mad-sad-glad-guide.md` | Facilitator guide: objectives, when to use, setup, how to run it, the card, failure modes, variations, facilitation notes |
| `mad-sad-glad-debrief.md` | Debrief: how to run it, reading the emotional shape, four debrief questions, failure-mode table |
| `mad-sad-glad-start-here.md` | Start here — pick a route, set the room, print checklist |
| `mad-sad-glad-license.md` | Plain-language license — what you can do, what you must keep |
| `mad-sad-glad-activity-poster.pdf` | The whole retro on one wall (A3): the three columns, the minute flow, the two rules. |

## How to run it

1. Silent notes, one item per note, across three columns: Mad, Sad, Glad. No names.
2. Post to the columns, read aloud, then cluster duplicates.
3. Dot-vote what resonates; pick one concrete action for the top item in each colour.
4. Give each action an owner and a revisit date, and write all three where everyone can see them.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/mad-sad-glad/files/mad-sad-glad.zip
unzip mad-sad-glad.zip   # -> mad-sad-glad/SKILL.md + every file + manifest
```

You get a directory named `mad-sad-glad` with this SKILL.md, every file it references, and a manifest.

Want just some files — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/mad-sad-glad/files/mad-sad-glad-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/mad-sad-glad/files/mad-sad-glad-activity-poster.pdf

# 3. Get the debrief and the guide
curl -O https://workshopskill.com/en/activities/mad-sad-glad/files/mad-sad-glad-debrief.md
curl -O https://workshopskill.com/en/activities/mad-sad-glad/files/mad-sad-glad-guide.md
```

This retro needs no online form and no account — three columns on a wall and nameless notes. There is no pre/post measure; the artifact is three clusters that show how the cycle felt plus one owned action per colour.

Prep facts for the agent:
- 6–20 people who just finished a shared cycle; above 20, run two groups on one board theme.
- Flow sums to: silent write 5 + post & cluster 6 + vote & choose 6 + own & revisit 3 = 20 minutes.
- No projector; the poster is optional and nothing needs a screen.
- Print at poker spec. One set of column cards per team.

**Where the skill goes.** Drop the unzipped `mad-sad-glad/` into your agent's skills directory to auto-load it: Claude Code `~/.claude/skills/mad-sad-glad/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/mad-sad-glad/`, Qoder `~/.qoder/skills/mad-sad-glad/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Step-by-step for each agent: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- Keep it to systems, not people — a Mad column that turns to blame poisons the room and gets the notes held back next time.
- Don't leave with actions but no owners; three that happen beat ten that get posted.
- A thin Glad column is itself the finding — say so out loud.

## Adapt it: make it yours

Want to rebrand this folder or package it as your own shelf product? The license file spells out what you may do: rename the column prompts, reprint the cards and poster at spec, and keep the CC BY attribution line — then use, sell, and redistribute freely.

## Credit

Hand-filed file by file, and cross-checked inside the folder — script, timings, and prop sizes agree with each other. CC BY 4.0, free — run it, copy it, rebrand it for your own workshop; keep the attribution line and this retro stays open.
