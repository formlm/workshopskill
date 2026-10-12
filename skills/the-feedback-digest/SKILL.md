---
name: the-feedback-digest
description: A 20-minute, 1–2 person self-assessment tool. Collect the feedback you've actually received, sort it into Already knew / Surprised me / I'll dismiss, read the surprised pile as your blindspot, then write one honest sentence the evidence supports and one action that follows from the surprise. Poker-spec cards and an A3 poster included; no account, no projector.
version: 2.1.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: self-assessment
  group_size: 1
  duration_minutes: 20
  setting: hybrid
  props: [sorting cards, sentence card, action card, blank cards]
  depth: tool-type
  language: en
  updated: 2026-10-09
---

# The Feedback Digest

You collect the feedback you've actually received — from reviews, Slack, 1:1s, emails — and sort it into three piles: things you already knew, things that surprised you, and things you're going to dismiss. The surprised pile is the point: it's the part of how you land that you can't see from the inside. Then you write one sentence about yourself the whole set supports, and one action that follows from the surprise.

## When to use this activity

- Anyone who gets a lot of feedback but can't say what it actually adds up to about them.
- After a review cycle, when a fresh pile of comments is still too close to sort honestly.
- You have 20 minutes, alone or with one other person digesting their own feedback.

## What's in the folder

| File | Use |
|---|---|
| `the-feedback-digest-prop-cards.pdf` | Poker-spec print deck (63.5 × 88.9 mm, bleed, cut guides, back, blanks): three sorting cards (Already knew · Surprised me · I'll dismiss), "the sentence the evidence supports," "one action from the surprised pile" |
| `the-feedback-digest-run-sheet.pdf` | Print edition: facilitator guide + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper for this folder's print files — same content, every version bookmarked with a linked contents page |
| `the-feedback-digest-guide.md` | Facilitator guide: goal, setup, minute script, ground rules, variations |
| `the-feedback-digest-debrief.md` | Debrief questions + three rescues |
| `the-feedback-digest-start-here.md` | Start here — pick a route, set the room, print checklist |
| `the-feedback-digest-license.md` | Plain-language license — what you can do, what you must keep |
| `the-feedback-digest-activity-poster.pdf` | The whole digest on one wall (A3): the three piles, the minute flow, the two rules. |

## How to run it

1. Write each piece of feedback you've received recently on its own card — verbatim where you can.
2. Sort every card into Already knew, Surprised me, or I'll dismiss (dismiss only with a reason).
3. Read the surprised pile for what keeps repeating — that pattern is the blindspot.
4. Write one honest sentence the whole set supports, and one action that follows from the surprise.

## Run this activity with an agent

A facilitator can hand the whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/the-feedback-digest/files/the-feedback-digest.zip
unzip the-feedback-digest.zip   # -> the-feedback-digest/SKILL.md + every file + manifest
```

You get a directory named `the-feedback-digest` with this SKILL.md, every file it references, a manifest.

Want just some files — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/the-feedback-digest/files/the-feedback-digest-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/the-feedback-digest/files/the-feedback-digest-activity-poster.pdf

# 3. Get the debrief and the guide
curl -O https://workshopskill.com/en/activities/the-feedback-digest/files/the-feedback-digest-debrief.md
curl -O https://workshopskill.com/en/activities/the-feedback-digest/files/the-feedback-digest-guide.md
```

This digest needs no online form and no account — a pile of real feedback and a few cards. There is no pre/post measure; the artifact is the three piles, the named blindspot, one honest sentence, and one action.

Prep facts for the agent:
- 1–2 people, each digesting their own received feedback.
- Flow sums to: gather 6 + sort 6 + read the surprise 4 + sentence & action 4 = 20 minutes.
- No projector; the poster is optional and nothing needs a screen.
- Print at poker spec. One deck per person.

**Where the skill goes.** Drop the unzipped `the-feedback-digest/` into your agent's skills directory to auto-load it: Claude Code `~/.claude/skills/the-feedback-digest/` (or `.claude/skills/` in a project), OpenAI Codex `~/.codex/skills/the-feedback-digest/`, Qoder `~/.qoder/skills/the-feedback-digest/`. No skills directory? Paste this file into the conversation and ask the agent to follow it. Step-by-step for each agent: https://workshopskill.com/en/skill-guides/

## Facilitator notes

- The "already knew" pile is the comfortable one, not the useful one — keep pointing at the surprised pile.
- Every dismissal needs a spoken one-sentence reason; where there isn't one, it's the blindspot hiding.
- The action should come from the surprise, not from the confirmation, or nothing will change.

## Adapt it: make it yours

Want to rebrand this folder or package it as your own shelf product? The white-label guide in the folder (the "white-label & marketplace guide" row in the file list) spells out renaming the card faces, the card and poster print specs, and the packaging steps. Keep the CC BY attribution line and you're free to use, sell, and redistribute.

## Credit

Hand-filed file by file, and cross-checked inside the folder — script, timings, and prop sizes agree with each other. CC BY 4.0, free — run it, copy it, rebrand it for your own workshop; keep the attribution line and this digest stays open.
