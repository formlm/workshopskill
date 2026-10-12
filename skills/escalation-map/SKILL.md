---
name: escalation-map
description: A 25-minute, 4-12 person conflict post-mortem that plots the arc of a getting-hot disagreement as a heat ladder — Warm, Heated, Boiling, Point of no return — writes what could have kept each rung one degree cooler, and circles the earliest cheap move. Names stay off the wall; the map is about the shape of getting hot. Printable poker rung cards and an A3 poster; no account, no projector.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: conflict
  group_size: 4
  duration_minutes: 25
  setting: hybrid
  props: [poker rung cards, one-degree-cooler card, blank cards]
  depth: tool-type
  language: en
  updated: 2026-10-09
---

# Escalation Map

A team plots the arc of a conflict as a heat ladder — from calm, to tension, to blowup, to the point where it wasn't recoverable the same way. At each rung, they name what could have kept it one degree cooler, and mark the earliest rung where a small move was cheapest. No culprit is on the map; only the shape of getting hot.

## When to use this activity

- A dispute has left the room picking sides, and no one can see how it got this hot.
- You want a shared post-mortem of a conflict that doesn't turn into a blame contest.
- You have 4–12 people and 25 minutes; remote works on a shared board.

## What is in the folder

| File | Purpose |
|---|---|
| `escalation-map-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): four rung cards (Warm / Heated / Boiling / Point of no return), a one-degree-cooler card, a blank card |
| `escalation-map-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC |
| `escalation-map-guide.md` | Run sheet: objectives, setup, minute-by-minute script, grouping rules, variations |
| `escalation-map-debrief.md` | Debrief questions + reading the ladder + three failure-mode rescues |
| `escalation-map-start-here.md` | Start here — pick your lane, file map, print list |
| `escalation-map-license.md` | License in plain language — what you may do, what you must keep |
| `escalation-map-activity-poster.pdf` | The whole post-mortem on one wall (A3): meta, the run of show, the four rungs, the earliest-cheap-move prompt. |

## Running it

1. Draw the four-rung ladder; set the rule — no names, no "who started it", only the shape.
2. Place what actually happened on each rung of heat, start-to-end.
3. On each rung, write what could have kept it one rung lower — cheap, not heroic.
4. Circle the earliest rung with a real move: the intervention point the map is for.
5. Each person names, out loud, one thing they will do at their own earliest rung next time.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/escalation-map/files/escalation-map.zip
unzip escalation-map.zip   # -> escalation-map/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `escalation-map` holding this SKILL.md, every file it references, and a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/escalation-map/files/escalation-map-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/escalation-map/files/escalation-map-activity-poster.pdf

# 3. Get the debrief and the run sheet
curl -O https://workshopskill.com/en/activities/escalation-map/files/escalation-map-debrief.md
curl -O https://workshopskill.com/en/activities/escalation-map/files/escalation-map-guide.md
```

This post-mortem needs no online form and no account — four rung cards, a ladder on the wall, sticky notes. There is no measured pre/post; the artifact is the map with its circled earliest-cheap-rung and each person's named next-time move.

Useful preparation facts for the agent:
- 4–12 people around one real, past conflict; keep names off the wall.
- Agenda math: frame 3 + plot 6 + one-degree-cooler 6 + earliest-cheap 5 + bridge 5 = 25 minutes.
- No projector needed; the poster is optional and nothing requires a screen.
- Print at poker. One set of four rung cards, one move card and blanks per group.

**Where to put the skill.** Drop the unzipped `escalation-map/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/escalation-map/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/escalation-map/`, Qoder `~/.qoder/skills/escalation-map/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- If the map only fills rungs 3–4, the team is skipping the early, cheap part — push honestly for rung 1.
- The strongest moment is realising a 30-second, costless move at rung 2 was never tried because everyone was saving for the rungs below.
- Force cheap moves (a question, a day's delay, one offline hop), not heroic "have a big talk" answers.

## Remix: make it yours

Want to rebrand this folder or package it for your own shelf? The license file (`escalation-map-license.md`) spells out the tiers, and `escalation-map-prop-cards.pdf` carries the print specs (poker trim, bleed, corner radius, gsm). Keep the CC BY attribution line and you're free to use it, sell it, or redistribute it.

## Attribution

Filed by hand and checked folder against folder — script, timings and prop sizes agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and this map stays open.
