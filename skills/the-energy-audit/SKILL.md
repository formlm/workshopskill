---
name: the-energy-audit
description: A 15-minute, solo-or-pair self-assessment tool. List the recurring things you actually do in a normal week, mark each + (gives energy) / − (drains) / = (neutral), name the biggest drain you keep choosing and the biggest + you keep skipping, and commit one dated swap. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.1.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: self-assessment
  group_size: 1
  duration_minutes: 15
  setting: hybrid
  props: [sign cards, chosen-drain card, starved-plus card, swap-and-date card]
  depth: tool-type
  language: en
  updated: 2026-10-09
---

# The Energy Audit

You cannot redirect a week you cannot see. List the recurring things you actually do, mark each by what it does to your energy — gives (+), drains (−), neutral (=) — then find the biggest drain you keep choosing and the biggest + you keep skipping, and commit to one dated swap. An energy audit is not time management; it is noticing what your time costs and returns.

## When to use this activity

- A busy person who insists they have "no time for anything they enjoy" and can't say where the week went.
- Before a role change or a burnout conversation — you need evidence, not a vibe.
- You have 15 minutes, alone or in a pair; it runs offline on a desk or online on a shared board.

## What's in the folder

| File | Use |
|---|---|
| `the-energy-audit-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed, cut guides, back, blank): a gives (+) card, a drains (−) card, a neutral (=) card, "the drain I keep choosing," "the + I keep skipping," "one swap + date" |
| `the-energy-audit-run-sheet.pdf` | Print edition: facilitator guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper for this folder's print files — same content, every version bookmarked with a linked contents page |
| `the-energy-audit-guide.md` | Facilitator guide: goal, setup, minute script, rules, variations |
| `the-energy-audit-debrief.md` | Debrief questions + three rescues |
| `the-energy-audit-start-here.md` | Start here — pick a route, set the room, print checklist |
| `the-energy-audit-license.md` | Plain-language license — what you can do, what you must keep |
| `the-energy-audit-activity-poster.pdf` | The whole audit on one wall (A3): the three signs, the minute flow, the two rules. |

## How to run it

1. List every recurring thing you actually did in a normal week — activities, not outcomes.
2. Mark each +, −, or = fast; the first mark is the honest one.
3. Circle the biggest − you keep choosing, and the biggest + you keep cutting.
4. Commit one swap — drop/halve one −, add back one + — with a date, and say it out loud.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/the-energy-audit/files/the-energy-audit.zip
unzip the-energy-audit.zip   # -> the-energy-audit/SKILL.md + every file + manifest
```

You get a directory named `the-energy-audit` with this SKILL.md, every file it references, a manifest.

Want just some files — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/the-energy-audit/files/the-energy-audit-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/the-energy-audit/files/the-energy-audit-activity-poster.pdf

# 3. Get the debrief and the guide
curl -O https://workshopskill.com/en/activities/the-energy-audit/files/the-energy-audit-debrief.md
curl -O https://workshopskill.com/en/activities/the-energy-audit/files/the-energy-audit-guide.md
```

This audit needs no online form and no account — a list of your week and a pen. There is no pre/post measure; the artifact is the marked-up week, the two things it named, and one dated swap.

Prep facts for the agent:
- 1 person (solo, or a pair each auditing their own week); honest, not impressive.
- Flow sums to: list 5 + mark 4 + spot 3 + swap 3 = 15 minutes.
- No projector; the poster is optional and nothing needs a screen.
- Print at poker spec. One sheet of sign + prompt cards per person.

**Where the skill goes.** Drop the unzipped `the-energy-audit/` into your agent's skills directory to auto-load it: Claude Code `~/.claude/skills/the-energy-audit/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/the-energy-audit/`, Qoder `~/.qoder/skills/the-energy-audit/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Step-by-step for each agent: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- If the whole page is −, they listed obligations, not activities — push for the concrete Tuesday call, not "reporting."
- The most useful line is a + that was hard to mark — permission they didn't think they had.
- Make the swap small enough to survive a bad week. One kept swap beats ten grand plans.

## Adapt it: make it yours

Want to rebrand this folder or package it as your own shelf product? The white-label guide in the folder (the "white-label & marketplace guide" row in the file list) spells out renaming the card faces, the card and poster print specs, and the packaging steps. Keep the CC BY attribution line and you're free to use, sell, and redistribute.

## Credit

Hand-filed file by file, and cross-checked inside the folder — script, timings, and prop sizes agree with each other. CC BY 4.0, free — run it, copy it, rebrand it for your own workshop; keep the attribution line and this audit stays open.
