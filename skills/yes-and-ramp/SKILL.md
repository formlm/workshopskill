---
name: yes-and-ramp
description: A 15-minute, 4-12 person creativity drill where a group builds one idea by each person saying "yes, and…" and adding a turn — accepts only, never "but" — so a plain seed climbs a ramp until it's unrecognisable, training building-on-others over editing-them. Printable poker prompt cards and an A3 poster; no account, no projector.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: creativity
  group_size: 4
  duration_minutes: 15
  setting: hybrid
  props: [poker seed + rule cards, a ramp-log sheet]
  depth: tool-type
  language: en
  updated: 2026-10-11
---

# Yes-And Ramp

A group builds one idea by going around and adding to it — each person starts from what the last said ("yes, and…"), never replacing it ("yes, but"). One ordinary seed climbs an accepts-only ramp until the group can't recognise where it started. The rule trains building-on-others over editing-them.

## When to use this activity

- Idea meetings collapse into "that won't work" before anything gets built on.
- You want fifteen minutes of generative momentum to open a design or naming session.
- You have 4–12 people comfortable speaking in a round; it runs on a call too.

## What is in the folder

| File | Purpose |
|---|---|
| `yes-and-ramp-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): seed-prompt cards, the "yes, and — no but" rule card, a ramp-log card, blank seed faces |
| `yes-and-ramp-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC |
| `yes-and-ramp-guide.md` | Run sheet: objectives, setup, minute-by-minute script, grouping rules, variations |
| `yes-and-ramp-debrief.md` | Debrief questions + reading the ramp back + three failure-mode rescues |
| `yes-and-ramp-start-here.md` | Start here — pick your lane, file map, print list |
| `yes-and-ramp-license.md` | License in plain language — what you may do, what you must keep |
| `yes-and-ramp-activity-poster.pdf` | The whole drill on one wall (A3): meta, the run of show, the one rule, the read-back prompt. |

## Running it

1. Write a deliberately ordinary seed on a card or the board.
2. Go around: each person says "yes, and…" and adds one turn. Keep a running note so the ramp is visible.
3. Loop the round two and three times so it climbs several stories.
4. Read the whole ramp back from the first line; compare it to the seed.
5. Bridge: one line each on where the real "that won't work" reflex cost you a ramp like this.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/yes-and-ramp/files/yes-and-ramp.zip
unzip yes-and-ramp.zip   # -> yes-and-ramp/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `yes-and-ramp` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/yes-and-ramp/files/yes-and-ramp-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/yes-and-ramp/files/yes-and-ramp-activity-poster.pdf

# 3. Get the debrief and the run sheet
curl -O https://workshopskill.com/en/activities/yes-and-ramp/files/yes-and-ramp-debrief.md
curl -O https://workshopskill.com/en/activities/yes-and-ramp/files/yes-and-ramp-guide.md
```

This drill needs no online form and no account — a seed, a round and a log. There is no measured pre/post; the artifact is the ramp itself and the read-back that shows how far accepts-only building carried it.

Useful preparation facts for the agent:
- One round of 4–12 people; go around two or three times so the ramp climbs.
- Agenda math: seed 1 + ramp 7 + two loops 2 + read-back 4 + bridge 1 = 15 minutes.
- No projector needed; the poster is optional and nothing requires a screen.
- Print at poker. One seed card per ramp, one rule card for the room, one log sheet.

**Where to put the skill.** Drop the unzipped `yes-and-ramp/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/yes-and-ramp/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/yes-and-ramp/`, Qoder `~/.qoder/skills/yes-and-ramp/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- If someone slips a "but," do a light-touch reset — "yes, AND, go again" — the reflex is the lesson, don't shame it.
- The strongest moment is the read-back, hearing how far one ordinary seed travelled.
- Keep your own additions concrete, not clever — you set the register for the round.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings and prop sizes agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and this drill stays open.
