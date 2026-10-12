---
name: the-third-story
description: A 25-minute, 4–10 person conflict tool. Two sides at odds each tell, in the third person, the story a neutral observer would tell about what's happening between them — what a camera would see, not who's right. Then both name the need under each position and commit one move that serves a shared need. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: conflict
  group_size: 4
  duration_minutes: 25
  setting: hybrid
  props: [third-person card, camera-view card, need-under-position card, shared-need-move card, blank cards]
  depth: tool-type
  language: en
  updated: 2026-10-09
---

# The Third Story

When two sides are at odds, each is sure their version is the obvious truth. This moves the room off "my story versus yours" onto a shared, observable scene: each side tells, in the third person, the story a neutral observer would tell about what is happening between them. Then both look for the need under each position, and commit one move that serves a need they share.

## When to use this activity

- A live disagreement where each side has told its first story so often it now sounds like fact.
- A split that's starting to name villains and you want to catch it before it hardens.
- You have 4–10 people and 25 minutes; it runs on a shared board online.

## What's in the folder

| File | Use |
|---|---|
| `the-third-story-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed, cut guides, back, blank): a "tell it in the third person" card, a "what a camera would see" card, a "the need under my position" card, a "one shared-need move" card |
| `the-third-story-run-sheet.pdf` | Print edition: facilitator guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper for this folder's print files — same content, every version bookmarked with a linked contents page |
| `the-third-story-guide.md` | Facilitator guide: goal, setup, minute script, ground rules, variations |
| `the-third-story-debrief.md` | Debrief questions + three rescues |
| `the-third-story-start-here.md` | Start here — pick a route, set the room, print checklist |
| `the-third-story-license.md` | Plain-language license — what you can do, what you must keep |
| `the-third-story-activity-poster.pdf` | The whole reframe on one wall (A3): the two columns, the minute flow, the two rules. |

## How to run it

1. Frame the disagreement as a shared object; set the rule — third person only, describe what a camera would see.
2. Each side writes and reads the story a neutral observer would tell about the clash. Post both.
3. Read both together; mark the shared scene and the exact sentence where they diverge.
4. Each side names one need under its position; where they overlap, commit one move + owner + date.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/the-third-story/files/the-third-story.zip
unzip the-third-story.zip   # -> the-third-story/SKILL.md + every file + manifest
```

You get a directory named `the-third-story` with this SKILL.md, every file it references, and a manifest.

Want just some files — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/the-third-story/files/the-third-story-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/the-third-story/files/the-third-story-activity-poster.pdf

# 3. Get the debrief and the guide
curl -O https://workshopskill.com/en/activities/the-third-story/files/the-third-story-debrief.md
curl -O https://workshopskill.com/en/activities/the-third-story/files/the-third-story-guide.md
```

This reframe needs no online form and no account — two columns on a wall and cards. There is no pre/post measure; the artifact is the two third stories, the named divergence, and one dated shared-need move.

Prep facts for the agent:
- 4–10 people, ideally the two sides of a real disagreement plus one or two neutrals.
- Flow sums to: frame 3 + tell third stories 8 + compare 6 + need + move 8 = 25 minutes.
- No projector; the poster is optional and nothing needs a screen.
- Print at poker spec. One set of prompt cards per side.

**Where the skill goes.** Drop the unzipped `the-third-story/` into your agent's skills directory to auto-load it: Claude Code `~/.claude/skills/the-third-story/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/the-third-story/`, Qoder `~/.qoder/skills/the-third-story/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Step-by-step for each agent: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- The instant a side names a villain, it's the first story again — ask for the sentence as pure camera footage.
- The shared scene is the real output; keep pointing at what both agree a camera would capture.
- If the needs genuinely don't overlap, say so and shift the move to an explicit trade, not a false resolution.

## Adapt it: make it yours

Want to rebrand this folder or package it as your own shelf product? The license file (`the-third-story-license.md`) spells out the tiers, and `the-third-story-prop-cards.pdf` carries the print specs (poker trim, bleed, corner radius, gsm). Keep the CC BY attribution line and you're free to use it, sell it, and redistribute it.

## Credit

Hand-filed file by file, and cross-checked inside the folder — script, timings, and prop sizes agree with each other. CC BY 4.0, free — run it, copy it, rebrand it for your own workshop; keep the attribution line and this reframe stays open.
