---
name: the-values-sort
description: A 20-minute, 1–8 person self-assessment tool that makes choosing values expensive. You sort a value-card deck into Core / Important / Not mine with a hard cap of five on Core, cut to five, then check one real recent decision against them and close one gap. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.1.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: self-assessment
  group_size: 1
  duration_minutes: 20
  setting: hybrid
  props: [zone cards, the-test card, value cards, blank cards]
  depth: tool-type
  language: en
  updated: 2026-10-09
---

# The Values Sort

You can name "nice" values all day; you only find out what you actually value when you're forced to choose. Sort a deck of value cards into Core / Important / Not mine — Core capped at five — then check one real recent decision against your five and close one gap. A value that costs nothing isn't yours.

## When to use this activity

- You keep saying one thing matters and your decisions quietly say otherwise.
- A career or life crossroads where you need to know what you'd actually pay for, not what sounds good.
- A team that wants to surface the value clashes underneath its friction. Works solo at a desk or with 1–8 people for 20 minutes.

## What's in the folder

| File | Use |
|---|---|
| `the-values-sort-prop-cards.pdf` | Poker-spec print deck (63.5 × 88.9 mm, bleed, cut guides, card back, blank): three zone cards, a "The test" card, a starter set of value cards, and blanks to write your own |
| `the-values-sort-run-sheet.pdf` | Print edition: guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size of the print files in this folder — same content, bookmarks and linked contents in every edition |
| `the-values-sort-guide.md` | Run sheet: goal, setup, minute-by-minute, grouping rules, variants |
| `the-values-sort-debrief.md` | Debrief questions + read the five + three rescues |
| `the-values-sort-start-here.md` | Quick start — pick a route, set the room, print list |
| `the-values-sort-license.md` | Plain-language licence — what you can do, what you must keep |
| `the-values-sort-activity-poster.pdf` | The whole session on one wall (A3): the three piles, the flow, the two rules |

## How to run it

1. Deal the value cards; sort each into Core, Important, or Not mine. Core is capped at five.
2. If Core overflowed, cut it to exactly five — the stings are the signal. Write your five.
3. Pick one real decision from the last month and lay it next to your five: what did it honor, what did it trade away?
4. Name one change to close a gap, write it on a blank card, and date it.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/the-values-sort/files/the-values-sort.zip
unzip the-values-sort.zip   # -> the-values-sort/SKILL.md + every file + manifest
```

Unzipped you get a directory named `the-values-sort` containing this SKILL.md, every file it references, a manifest.

Only want some files — anonymous, CC BY 4.0:

```bash
# 1. get the printable card deck
curl -O https://workshopskill.com/en/activities/the-values-sort/files/the-values-sort-prop-cards.pdf

# 2. get the wall poster
curl -O https://workshopskill.com/en/activities/the-values-sort/files/the-values-sort-activity-poster.pdf

# 3. get the debrief and the guide
curl -O https://workshopskill.com/en/activities/the-values-sort/files/the-values-sort-debrief.md
curl -O https://workshopskill.com/en/activities/the-values-sort/files/the-values-sort-guide.md
```

This session needs no online form and no account — three piles, a deck, a blank card. There is no pre/post measure; the artifact is your five core values, one decision tested against them, and one dated change.

Prep facts for the agent:
- 1–8 people; runs solo at a desk or as a peer group each sorting their own.
- Flow sums: sort 4 + cut to five 4 + the test 6 + close a gap 6 = 20 minutes.
- No projector needed; the poster is optional and nothing requires a screen.
- Print at poker spec. Print the deck sheet twice for a group.

**Where the skill goes.** Drop the unzipped `the-values-sort/` into your agent's skills directory and it loads automatically: Claude Code `~/.claude/skills/the-values-sort/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/the-values-sort/`, Qoder `~/.qoder/skills/the-values-sort/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- If someone can't cut to five, make them anyway — the pain of the cut is the finding.
- If every value feels "important," move more into Not mine until Core gets uncomfortable; comfort means no choosing.
- Push the test toward a decision with real tension; a choice where everyone got what they wanted proves nothing.

## Remix: make it yours

Want this folder under your own brand, or packaged as your own marketplace product? The white-label guide in this folder (the "white-label & marketplace guide" row in the file list) covers renaming the zones, swapping the value deck, the card and poster print specs, and packaging steps. Keep the CC BY attribution line and you are free to use, sell, and redistribute it.

## Attribution

Filed by hand and checked folder-to-folder — the script, timings, and prop dimensions agree with each other. CC BY 4.0 free — run it, copy it, rebrand it for your own workshop; keep the attribution line and the sort stays open.
