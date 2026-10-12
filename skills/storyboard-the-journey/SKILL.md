---
name: storyboard-the-journey
description: A 25-minute, 4-12 person mapping tool that lays one person's end-to-end experience out as a strip of storyboard panels, marks each with a high / low / hope, and draws the experience line through them — so a team argues about the same valley instead of its own box. Printable poker panel cards and an A3 poster; no account, no projector.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: creativity
  group_size: 4
  duration_minutes: 25
  setting: hybrid
  props: [poker panel + marker cards, a journey-prompt card, blank panels]
  depth: tool-type
  language: en
  updated: 2026-10-11
---

# Storyboard the Journey

A group draws a person's end-to-end experience as a strip of storyboard panels — what they do, see, feel at each step — then marks every panel with a high, a low, and a hope, and draws the experience line through them. The wall becomes one shared map, so the team spots the dip nobody owned.

## When to use this activity

- A team optimises pieces (a screen, a form, a policy) without seeing the whole arc the person moves through.
- You want a shared, concrete picture of an experience before arguing about fixes.
- You have 4–12 people and 25 minutes; it works on a shared board online.

## What is in the folder

| File | Purpose |
|---|---|
| `storyboard-the-journey-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): a journey-prompt card, high/low/hope marker cards, a draw-the-line card, blank panels |
| `storyboard-the-journey-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC |
| `storyboard-the-journey-guide.md` | Run sheet: objectives, setup, minute-by-minute script, grouping rules, variations |
| `storyboard-the-journey-debrief.md` | Debrief questions + reading the wall + three failure-mode rescues |
| `storyboard-the-journey-start-here.md` | Start here — pick your lane, file map, print list |
| `storyboard-the-journey-license.md` | License in plain language — what you may do, what you must keep |
| `storyboard-the-journey-activity-poster.pdf` | The whole map on one wall (A3): meta, the run of show, the three marks, the draw-the-line prompt. |

## Running it

1. Bind one person and one journey; agree the start and the end.
2. Sketch a left-to-right row of panels — what they do, see, feel at each step. Rough only.
3. On each panel add a high, a low, a hope; then draw the experience line through them.
4. Look where the line dips hardest and where hopes pile up; circle the two or three places worth a move.
5. For each circle: who could own a change, and what it would take.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/storyboard-the-journey/files/storyboard-the-journey.zip
unzip storyboard-the-journey.zip   # -> storyboard-the-journey/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `storyboard-the-journey` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/storyboard-the-journey/files/storyboard-the-journey-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/storyboard-the-journey/files/storyboard-the-journey-activity-poster.pdf

# 3. Get the debrief and the run sheet
curl -O https://workshopskill.com/en/activities/storyboard-the-journey/files/storyboard-the-journey-debrief.md
curl -O https://workshopskill.com/en/activities/storyboard-the-journey/files/storyboard-the-journey-guide.md
```

This mapping tool needs no online form and no account — a row of panels, three marks, and a marker to draw the line. There is no measured pre/post; the artifact is the shared journey map and the two or three circled valleys it points at.

Useful preparation facts for the agent:
- 4–12 people; bind one journey per strip, keep sketches rough.
- Agenda math: bound 3 + panel 9 + mark 7 + cluster 4 + name-the-move 2 = 25 minutes.
- No projector needed; the poster is optional and nothing requires a screen.
- Print at poker. One prompt card, a row of blank panels, and the marker cards per group.

**Where to put the skill.** Drop the unzipped `storyboard-the-journey/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/storyboard-the-journey/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/storyboard-the-journey/`, Qoder `~/.qoder/skills/storyboard-the-journey/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- Anchor on one named person; if a panel is an internal handoff, it's off the map — draw the person's journey, not your process.
- The strongest moment is seeing a big dip nobody owned, because each team only saw its own box.
- Draw the line, don't just list steps — the shape points at the valley a feature list never shows.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings and prop sizes agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and this map stays open.
