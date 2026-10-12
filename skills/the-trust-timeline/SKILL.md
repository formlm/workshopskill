---
name: the-trust-timeline
description: A 25-minute, 4–10 person trust tool. A team lays its shared history on a line — moments trust grew, broke, and got repaired — reads the pattern of what breaks and rebuilds trust here, and picks one live break to repair with an owner and a check-in date. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.1.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: trust
  group_size: 4
  duration_minutes: 25
  setting: hybrid
  props: [grew card, broke card, repaired card, repair-that-worked card, live-break card, blank cards]
  depth: tool-type
  language: en
  updated: 2026-10-10
---

# The Trust Timeline

A team lays its shared history on a line — the moments trust grew, the moments it broke, the moments it got repaired — to see the pattern of how trust actually works here, then picks one live break to repair. Trust isn't declared; it accumulates in moments, and it's repairable, not fragile.

## When to use this activity

- A team with history where trust has quietly accumulated breaks that nobody has looked at together.
- After a rupture you want to repair on purpose rather than let it pile up.
- You have 4–10 people and 25 minutes; online works if the timeline lives on a shared board.

## What's in the folder

| File | Use |
|---|---|
| `the-trust-timeline-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed, cut guides, card back, blank): grew / broke / repaired marker cards, a "the repair that worked" card, a "one live break to fix" card, a blank card |
| `the-trust-timeline-run-sheet.pdf` | Print edition: guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size of the print files in this folder — same content, bookmarks and linked contents in every edition |
| `the-trust-timeline-guide.md` | Run sheet: objectives, when to use, setup, minute-by-minute script, the card, failure modes, variations |
| `the-trust-timeline-debrief.md` | Debrief: how to run it, six numbered questions with what each targets, and the failure modes of the debrief |
| `the-trust-timeline-start-here.md` | Quick start — pick a route, set the room, print list |
| `the-trust-timeline-license.md` | Plain-language licence — what you can do, what you must keep |
| `the-trust-timeline-activity-poster.pdf` | The whole session on one wall (A3): the timeline, the flow, the two rules |

## How to run it

1. Draw a horizontal timeline with three lanes: Grew · Broke · Repaired.
2. Everyone posts real moments across the lanes, placed roughly when they happened.
3. Read the pattern aloud: what does trust break on here, and what repair keeps working?
4. Pick one live break the team volunteers to fix — never assign it.
5. Name a repair action, an owner, and a check-in date.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/the-trust-timeline/files/the-trust-timeline.zip
unzip the-trust-timeline.zip   # -> the-trust-timeline/SKILL.md + every file + manifest
```

Unzipped you get a directory named `the-trust-timeline` containing this SKILL.md, every file it references, a manifest.

Only want some files — anonymous, CC BY 4.0:

```bash
# 1. get the printable cards
curl -O https://workshopskill.com/en/activities/the-trust-timeline/files/the-trust-timeline-prop-cards.pdf

# 2. get the wall poster
curl -O https://workshopskill.com/en/activities/the-trust-timeline/files/the-trust-timeline-activity-poster.pdf

# 3. get the debrief and the guide
curl -O https://workshopskill.com/en/activities/the-trust-timeline/files/the-trust-timeline-debrief.md
curl -O https://workshopskill.com/en/activities/the-trust-timeline/files/the-trust-timeline-guide.md
```

This session needs no online form and no account — a line, three lanes, cards. There is no pre/post measure; the artifact is the shared timeline plus one live break with a repair, an owner, and a check-in date.

Prep facts for the agent:
- 4–10 people who share a history; safety is modeled, not demanded.
- Flow sums: draw the line 2 + post moments 8 + read the pattern 7 + repair one 8 = 25 minutes.
- No projector needed; the poster is optional and nothing requires a screen.
- Print at poker spec. One card sheet per person.

**Where the skill goes.** Drop the unzipped `the-trust-timeline/` into your agent's skills directory and it loads automatically: Claude Code `~/.claude/skills/the-trust-timeline/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/the-trust-timeline/`, Qoder `~/.qoder/skills/the-trust-timeline/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- If nobody will post a break, go first about an event, not a person — safety is modeled.
- If every break on the line is old and resolved, that's a dodge; ask what's still open.
- If a break names someone, strip the name and describe what happened and what it cost.

## Remix: make it yours

Want this folder under your own brand, or packaged as your own marketplace product? Keep the CC BY attribution line and you are free to use, sell, and redistribute it.

## Attribution

Filed by hand and checked folder-to-folder — the script, timings, and prop dimensions agree with each other. CC BY 4.0 free — run it, copy it, rebrand it for your own workshop; keep the attribution line and the timeline stays open.
