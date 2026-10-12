---
name: the-reliability-ledger
description: A 25-minute, 4–10 person trust tool that treats trust as a record of kept promises. Each person writes two commitments ("I'll reliably…") and one need ("I quietly need…"), the group surfaces one broken-but-unspoken expectation, and they commit one repair with an owner and a check-in date. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.1.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: trust
  group_size: 4
  duration_minutes: 25
  setting: hybrid
  props: [commitment cards, need card, unspoken-expectation card, repair-action card, blank cards]
  depth: tool-type
  language: en
  updated: 2026-10-10
---

# The Reliability Ledger

A team makes its implicit contract explicit: what each person will reliably do, what each quietly needs from the others, and the one broken-but-unspoken expectation everyone had. Then they commit one repair with an owner and a check-in date. Trust here is a record of kept promises, not a feeling manufactured with games.

## When to use this activity

- A team with some history where expectations have quietly formed and a few have quietly broken.
- A group where trust is leaking through unspoken assumptions, not through any single betrayal.
- You have 4–10 people and 25 minutes; online works if the two columns live on a shared board.

## What's in the folder

| File | Use |
|---|---|
| `the-reliability-ledger-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed, cut guides, card back, blank): two "I'll reliably…" cards, a "I quietly need…" card, a "The unspoken one" card, a "Repair action" card, a blank card |
| `the-reliability-ledger-run-sheet.pdf` | Print edition: guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size of the print files in this folder — same content, bookmarks and linked contents in every edition |
| `the-reliability-ledger-guide.md` | Run sheet: objectives, when to use, setup, minute-by-minute script, the card, failure modes, variations |
| `the-reliability-ledger-debrief.md` | Debrief: how to run it, six numbered questions with what each targets, and the failure modes of the debrief |
| `the-reliability-ledger-start-here.md` | Quick start — pick a route, set the room, print list |
| `the-reliability-ledger-license.md` | Plain-language licence — what you can do, what you must keep |
| `the-reliability-ledger-activity-poster.pdf` | The whole session on one wall (A3): the two columns, the flow, the two rules |

## How to run it

1. Put two columns on a wall — Commitments and Needs — plus a spot for the unspoken one.
2. Each person writes two commitments ("I'll reliably…") and one need ("I quietly need…").
3. Read each card aloud and post it; no debate, just hearing.
4. As a group, name one broken-but-unspoken expectation and write it on the card.
5. Agree one repair action with an owner and a check-in date; each person adds one commitment to make it real.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/the-reliability-ledger/files/the-reliability-ledger.zip
unzip the-reliability-ledger.zip   # -> the-reliability-ledger/SKILL.md + every file + manifest
```

Unzipped you get a directory named `the-reliability-ledger` containing this SKILL.md, every file it references, a manifest.

Only want some files — anonymous, CC BY 4.0:

```bash
# 1. get the printable cards
curl -O https://workshopskill.com/en/activities/the-reliability-ledger/files/the-reliability-ledger-prop-cards.pdf

# 2. get the wall poster
curl -O https://workshopskill.com/en/activities/the-reliability-ledger/files/the-reliability-ledger-activity-poster.pdf

# 3. get the debrief and the guide
curl -O https://workshopskill.com/en/activities/the-reliability-ledger/files/the-reliability-ledger-debrief.md
curl -O https://workshopskill.com/en/activities/the-reliability-ledger/files/the-reliability-ledger-guide.md
```

This session needs no online form and no account — two columns, cards, a marker. There is no pre/post measure; the artifact is the ledger plus one repair action with an owner and a check-in date.

Prep facts for the agent:
- 4–10 people with enough shared history that expectations have quietly formed.
- Flow sums: write 7 + read & post 6 + surface the unspoken 6 + repair 6 = 25 minutes.
- No projector needed; the poster is optional and nothing requires a screen.
- Print at poker spec. One card sheet per person plus the unspoken and repair cards.

**Where the skill goes.** Drop the unzipped `the-reliability-ledger/` into your agent's skills directory and it loads automatically: Claude Code `~/.claude/skills/the-reliability-ledger/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/the-reliability-ledger/`, Qoder `~/.qoder/skills/the-reliability-ledger/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- If needs come out as complaints, rewrite each as "I need X by Y" before it goes on the wall.
- If the unspoken one names a person, reframe it as a shared pattern and move on before the room closes.
- If no one wants to commit, start with boring operational promises — safety is built by kept small promises, not confessions.

## Remix: make it yours

Want this folder under your own brand, or packaged as your own marketplace product? Keep the CC BY attribution line and you are free to use, sell, and redistribute it.

## Attribution

Filed by hand and checked folder-to-folder — the script, timings, and prop dimensions agree with each other. CC BY 4.0 free — run it, copy it, rebrand it for your own workshop; keep the attribution line and the ledger stays open.
