---
name: roleswap-argument
description: A 20-minute, 6–16 person conflict tool. Take a real disagreement in the room, then make each side argue the *other* side's position honestly — steel-man it, land one true thing in it, and name the shared need underneath both. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: conflict
  group_size: 6
  duration_minutes: 20
  setting: hybrid
  props: [your-side card, their-side card, steel-man card, what's-true card, shared-need card, swap-back card]
  depth: tool-type
  language: en
  updated: 2026-10-10
---

# Roleswap Argument

Most conflicts stall not because the facts are unknown, but because nobody on either side can state the other's position in a way that side would accept. This tool forces the swap: each side argues the *other* position honestly, steel-mans it, names one true thing in it, and surfaces the need both are really serving — then returns to its own side, changed.

## When to use this activity

- Two teams or two people stuck in a "we're right, they're wrong" loop that re-litigating the facts won't break.
- Before a contested decision, as cheap insurance against a choice the other side won't support.
- You have 6–16 people on two sides of a real disagreement and 20 minutes; it runs on a shared board online.

## What's in the folder

| File | Use |
|---|---|
| `roleswap-argument-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed, cut guides, back, blank): your-side, their-side, steel-man, what's-true, shared-need, swap-back cards |
| `roleswap-argument-run-sheet.pdf` | Print edition: facilitator guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper for this folder's print files — same content, every version bookmarked with a linked contents page |
| `roleswap-argument-guide.md` | Facilitator guide: goal, setup, minute script, ground rules, variations |
| `roleswap-argument-debrief.md` | Debrief questions + three rescues |
| `roleswap-argument-start-here.md` | Start here — pick a route, set the room, print checklist |
| `roleswap-argument-license.md` | Plain-language license — what you can do, what you must keep |
| `roleswap-argument-activity-poster.pdf` | The whole swap on one wall (A3): the two positions, the minute flow, the two rules. |

## How to run it

1. State both live positions in one honest sentence each — no caricature.
2. Each side argues the *other* position as someone who genuinely holds it.
3. Steel-man it: strengthen the other side's best case beyond what they gave you.
4. Each person names one thing genuinely true in the other position, then the group names the shared need; everyone returns to their own side and restates it, updated.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/roleswap-argument/files/roleswap-argument.zip
unzip roleswap-argument.zip   # -> roleswap-argument/SKILL.md + every file + manifest
```

You get a directory named `roleswap-argument` with this SKILL.md, every file it references, and a manifest.

Want just some files — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/roleswap-argument/files/roleswap-argument-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/roleswap-argument/files/roleswap-argument-activity-poster.pdf

# 3. Get the debrief and the guide
curl -O https://workshopskill.com/en/activities/roleswap-argument/files/roleswap-argument-debrief.md
curl -O https://workshopskill.com/en/activities/roleswap-argument/files/roleswap-argument-guide.md
```

This swap needs no online form and no account — two positions on a wall and an honest turn at the other side. There is no pre/post measure; the artifact is two positions everyone can state fairly, one true thing named in each, and the shared need underneath.

Prep facts for the agent:
- 6–16 people split into two sides of one real, safe-to-surface disagreement.
- Flow sums to: frame 4 + swap & argue 6 + steel-man 5 + land it 5 = 20 minutes.
- No projector; the poster is optional and nothing needs a screen.
- Print at poker spec. One set of role cards per pair of sides.

**Where the skill goes.** Drop the unzipped `roleswap-argument/` into your agent's skills directory to auto-load it: Claude Code `~/.claude/skills/roleswap-argument/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/roleswap-argument/`, Qoder `~/.qoder/skills/roleswap-argument/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Step-by-step for each agent: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- Argue to understand, not to win — a swap performed as parody hasn't happened; run it again as a believer would.
- Insist on one true thing in the other side before anyone returns to their own; the refusal to find one is itself the data.
- If the room is too hot for a public swap, do it in pairs with a neutral reader first.

## Adapt it: make it yours

Want to rebrand this folder or package it as your own shelf product? The license file (`roleswap-argument-license.md`) spells out the tiers, and `roleswap-argument-prop-cards.pdf` carries the print specs (poker trim, bleed, corner radius, gsm). Keep the CC BY attribution line and you're free to use it, sell it, and redistribute it.

## Credit

Hand-filed file by file, and cross-checked inside the folder — script, timings, and prop sizes agree with each other. CC BY 4.0, free — run it, copy it, rebrand it for your own workshop; keep the attribution line and this swap stays open.
