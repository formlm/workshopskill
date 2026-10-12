---
name: one-minute-meetup
description: A 15-minute, 6-20 person rotating-pairs energizer where each pair gets exactly one minute to find a surprising shared thing — three escalating timed rounds plus a one-line gallery — so a room of semi-strangers builds real common ground faster than an open mingle. Printable poker-spec cards and an A3 poster; no account, no projector.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: icebreakers
  group_size: 6
  duration_minutes: 15
  setting: hybrid
  props: [poker round-ask cards, per-person tally card, a chime]
  depth: tool-type
  language: en
  updated: 2026-10-09
---

# One-Minute Meetup

Pairs get exactly one minute to find a *surprising* thing they share — not their job, not their city. The chime ends the pair, everyone rotates. Three timed rounds with escalating asks, then a one-line gallery. The timer and the "surprising only" rule are what get a room past small talk.

## When to use this activity

- A room of semi-strangers is sticking to business cards and weather before a session that needs them to actually know each other.
- You have 15 minutes and want energy up and names learned fast.
- Remote: run it in breakout rooms with the same chime; it transfers cleanly.

## What is in the folder

| File | Purpose |
|---|---|
| `one-minute-meetup-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): three round-ask cards, a per-person tally card, blank ask faces |
| `one-minute-meetup-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC |
| `one-minute-meetup-guide.md` | Run sheet: objectives, setup, minute-by-minute script, grouping rules, variations |
| `one-minute-meetup-debrief.md` | Debrief questions + reading the tally cards + three failure-mode rescues |
| `one-minute-meetup-start-here.md` | Start here — pick your lane, file map, print list |
| `one-minute-meetup-license.md` | License in plain language — what you may do, what you must keep |
| `one-minute-meetup-activity-poster.pdf` | The whole energizer on one wall (A3): meta, the three rounds, the gallery, the two rules. |

## Running it

1. Everyone gets a tally card and a pen; pair off (odd person rotates in next round).
2. Round 1 — one minute: find a surprising shared thing. Chime, rotate.
3. Round 2 — one minute: find something neither of you told anyone. Chime, rotate.
4. Round 3 — one minute: find a thing that changes how you'd work together.
5. Gallery — go around, one line each: the match that surprised you most.
6. Bridge — one line: what you found out about someone you'd already "met".

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/one-minute-meetup/files/one-minute-meetup.zip
unzip one-minute-meetup.zip   # -> one-minute-meetup/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `one-minute-meetup` holding this SKILL.md, every file it references, and a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/one-minute-meetup/files/one-minute-meetup-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/one-minute-meetup/files/one-minute-meetup-activity-poster.pdf

# 3. Get the debrief and the run sheet
curl -O https://workshopskill.com/en/activities/one-minute-meetup/files/one-minute-meetup-debrief.md
curl -O https://workshopskill.com/en/activities/one-minute-meetup/files/one-minute-meetup-guide.md
```

This energizer needs no online form and no account — cards, a chime and a pen. There is no measured pre/post; the artifact is the gallery of surprising matches.

Useful preparation facts for the agent:
- Pairs rotate; for an odd head-count one person sits out round one and rotates in next.
- Agenda math: setup 2 + three rounds 3+3+3 + gallery 4 + bridge 1 = 15 minutes (well inside it).
- No projector needed; the poster is optional and nothing requires a screen.
- Print at poker. One tally card per person, one set of ask cards for the room.

**Where to put the skill.** Drop the unzipped `one-minute-meetup/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/one-minute-meetup/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/one-minute-meetup/`, Qoder `~/.qoder/skills/one-minute-meetup/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- The strongest moment is the gallery: "I had no idea you'd done that too," about someone met ten minutes ago.
- If pairs chat past the chime, hold the hard stop and run the rotation loud — the squeeze is the engine.
- The strongest transfer question: "What is one thing you'd normally never ask, that you now will?"

## Remix: make it yours

Want to rebrand this folder or package it for your own shelf? Under CC BY you can swap the ask-card faces, the card and poster art, and the packaging yourself. Keep the attribution line and you're free to use it, sell it, or redistribute it.

## Attribution

Filed by hand and checked folder against folder — script, timings and prop sizes agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and this energizer stays open.
