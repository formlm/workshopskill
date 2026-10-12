---
name: paper-plane-intros
description: A 15-minute, 8-20 person icebreaker where everyone writes one non-obvious line about themselves, folds it into a paper plane and throws it across the room, then finds the author and asks a real follow-up question — a physical remix plus a genuine exchange that mixes a room past its usual clusters. Printable instruction cards and an A3 poster; no account, no projector.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: icebreakers
  group_size: 8
  duration_minutes: 15
  setting: hybrid
  props: [poker instruction + follow-up cards, one A4 sheet per person, open floor]
  depth: tool-type
  language: en
  updated: 2026-10-09
---

# Paper Plane Intros

Everyone writes one non-obvious line about themselves, folds it into a paper plane, throws it across the room, then hunts down the author and asks a real follow-up question. The throw forces the room past the people it already sat next to; the follow-up is what turns a parlor trick into two people who know something real about each other.

## When to use this activity

- A group keeps clustering with the same faces and you want strangers introduced, not just warmed up.
- You have fifteen minutes and a little open floor; the movement is the point.
- Remote: everyone "throws" into a shared channel and the group finds the author.

## What is in the folder

| File | Purpose |
|---|---|
| `paper-plane-intros-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): instruction card, follow-up-question card, gallery card, blank faces |
| `paper-plane-intros-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC |
| `paper-plane-intros-guide.md` | Run sheet: objectives, setup, minute-by-minute script, grouping rules, variations |
| `paper-plane-intros-debrief.md` | Debrief questions + reading what came back + three failure-mode rescues |
| `paper-plane-intros-start-here.md` | Start here — pick your lane, file map, print list |
| `paper-plane-intros-license.md` | License in plain language — what you may do, what you must keep |
| `paper-plane-intros-activity-poster.pdf` | The whole icebreaker on one wall (A3): meta, the run of show, the two rules, the follow-up prompt. |

## Running it

1. Each person writes one non-obvious line on a plain A4 sheet — no name on the outside.
2. Fold a plane; on your count, everyone throws across the room. Each person catches one that isn't theirs.
3. Read the line you caught aloud, find the author, and ask them one real follow-up question.
4. Round two: a second, deeper line, refold, rethrow, repeat.
5. Gallery: each person names the plane they caught and the one thing they learned about its author.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/paper-plane-intros/files/paper-plane-intros.zip
unzip paper-plane-intros.zip   # -> paper-plane-intros/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `paper-plane-intros` holding this SKILL.md, every file it references, and a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/paper-plane-intros/files/paper-plane-intros-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/paper-plane-intros/files/paper-plane-intros-activity-poster.pdf

# 3. Get the debrief and the run sheet
curl -O https://workshopskill.com/en/activities/paper-plane-intros/files/paper-plane-intros-debrief.md
curl -O https://workshopskill.com/en/activities/paper-plane-intros/files/paper-plane-intros-guide.md
```

This icebreaker needs no online form and no account — plain paper, a room and a question. There is no measured pre/post; the artifact is the cross-room mixing and the conversations it started.

Useful preparation facts for the agent:
- 8–20 people, one plain A4 sheet each, and enough open floor to throw safely.
- Agenda math: write 2 + fold & throw 2 + read & find 5 + round two 4 + gallery 2 = 15 minutes.
- No projector needed; nothing in the folder requires a screen.
- Print at poker spec. One instruction card and one follow-up card for the room.

**Where to put the skill.** Drop the unzipped `paper-plane-intros/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/paper-plane-intros/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/paper-plane-intros/`, Qoder `~/.qoder/skills/paper-plane-intros/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- Read the "nothing obvious" rule twice and give a concrete example before anyone throws.
- If a person grabs back their own plane, they must throw it on and catch a different one.
- Model one real follow-up question before round one — the pair who goes deeper sets the tone the room can hear.

## Remix: make it yours

Want to rebrand this folder or package it for your own shelf? Under CC BY you can swap the instruction-card faces, the card and poster art, and the packaging yourself. Keep the attribution line and you're free to use it, sell it, or redistribute it.

## Attribution

Filed by hand and checked folder against folder — script, timings and prop sizes agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and this icebreaker stays open.
