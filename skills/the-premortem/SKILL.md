---
name: the-premortem
description: A 25-minute, 4–12 person review that runs backwards from a future failure. The team assumes the project already failed, writes the story of how, and turns polite-unsaid risks into causes with early-warning signals and one preventive action with an owner and a by-when. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: reviews
  group_size: 4
  duration_minutes: 25
  setting: hybrid
  props: [failure-story card, root-cause card, early-warning-signal card, preventive-action card, owner-and-by-when card, blank cards]
  depth: tool-type
  language: en
  updated: 2026-10-09
---

# The Premortem

A review pointed at the future. Before you launch (or after a miss), the team assumes the project has already failed and writes the story of how — which surfaces the risks people were too polite to raise while it still felt optimistic. Causes get early-warning signals and one preventive action with an owner and a by-when.

## When to use this activity

- A plan that hasn't happened yet and a team too optimistic to name what could sink it.
- A review of something that just missed, where you want honesty rather than blame.
- You have 4–12 people and 25 minutes; online works if the three columns live on a shared board.

## What's in the folder

| File | Use |
|---|---|
| `the-premortem-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed, cut guides, card back, blank): a failure-story card, a root-cause card, an early-warning-signal card, a preventive-action card, an owner-and-by-when card, a blank card |
| `the-premortem-run-sheet.pdf` | Print edition: guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size of the print files in this folder — same content, bookmarks and linked contents in every edition |
| `the-premortem-guide.md` | Facilitator guide: objectives, when to use, setup, how to run it, the card, failure modes, variations, facilitation notes |
| `the-premortem-debrief.md` | Debrief: how to run it, reading the board, four debrief questions, failure-mode table |
| `the-premortem-start-here.md` | Quick start — pick a route, set the room, print list |
| `the-premortem-license.md` | Plain-language licence — what you can do, what you must keep |
| `the-premortem-activity-poster.pdf` | The whole session on one wall (A3): the backwards timeline, the flow, the two rules |

## How to run it

1. Declare the failure as certain: "It's three months from now and it failed — write how."
2. Everyone writes causes silently before anyone speaks.
3. Round-robin: read one cause each, post and cluster under Root causes.
4. For the top three causes, name an early-warning signal you'd notice in time.
5. For the top cause, agree one preventive action with an owner and a by-when.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/the-premortem/files/the-premortem.zip
unzip the-premortem.zip   # -> the-premortem/SKILL.md + every file + manifest
```

Unzipped you get a directory named `the-premortem` containing this SKILL.md, every file it references, and a manifest.

Only want some files — anonymous, CC BY 4.0:

```bash
# 1. get the printable cards
curl -O https://workshopskill.com/en/activities/the-premortem/files/the-premortem-prop-cards.pdf

# 2. get the wall poster
curl -O https://workshopskill.com/en/activities/the-premortem/files/the-premortem-activity-poster.pdf

# 3. get the debrief and the guide
curl -O https://workshopskill.com/en/activities/the-premortem/files/the-premortem-debrief.md
curl -O https://workshopskill.com/en/activities/the-premortem/files/the-premortem-guide.md
```

This session needs no online form and no account — three columns, cards, sticky notes. There is no pre/post measure; the artifact is the clustered causes with early-warning signals and one preventive action with an owner and a by-when.

Prep facts for the agent:
- 4–12 people around a plan that hasn't happened yet, or a review of one that just did.
- Flow sums: set the scene 3 + write the failure 7 + share & post 6 + signal it 5 + assign 4 = 25 minutes.
- No projector needed; the poster is optional and nothing requires a screen.
- Print at poker spec. One card sheet per person.

**Where the skill goes.** Drop the unzipped `the-premortem/` into your agent's skills directory and it loads automatically: Claude Code `~/.claude/skills/the-premortem/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/the-premortem/`, Qoder `~/.qoder/skills/the-premortem/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- If the causes are all safe and obvious, ask "if this fails and you'd get blamed — what was it?" and write that one.
- A signal nobody owns won't fire; name a watcher for each of the top three.
- If it drifts into blaming another team, park it as a named dependency with an owner who'll raise it elsewhere.

## Remix: make it yours

Want this folder under your own brand, or packaged as your own marketplace product? The license file spells out what you may do: rename the card prompts, reprint the cards and poster at spec, and keep the CC BY attribution line — then use, sell, and redistribute it freely.

## Attribution

Filed by hand and checked folder-to-folder — the script, timings, and prop dimensions agree with each other. CC BY 4.0 free — run it, copy it, rebrand it for your own workshop; keep the attribution line and the premortem stays open.
