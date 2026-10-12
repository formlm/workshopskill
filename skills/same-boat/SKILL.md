---
name: same-boat
description: A 20-minute, 6-16 person conflict reframe where two sides at odds each list only what they will both lose if the dispute keeps running, and the overlap becomes one shared "same boat" card — moving from "against them" to "beside them, facing the same problem", with a separate "still different" card for genuine disagreement. Printable poker cards and an A3 poster; no account, no projector.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: conflict
  group_size: 6
  duration_minutes: 20
  setting: hybrid
  props: ["poker write cards", "shared \"same boat\" card", "\"still different\" card"]
  depth: tool-type
  language: en
  updated: 2026-10-09
---

# Same Boat

Two groups at odds each write down what they will **both** lose if the dispute keeps running — not what the other side is doing wrong. They read each other's lists, and the overlapping losses go on one shared "same boat" card. The move from "against them" to "beside them, facing the same problem" is the technique.

## When to use this activity

- Two teams or sub-groups have settled into blame and the argument loops the same three grievances.
- The conflict is real but the framing is positional — everyone can name the other's faults and nothing of the shared cost.
- You have twenty minutes and can seat the two sides apart but in one room (or two breakouts that reconvene).

## What is in the folder

| File | Purpose |
|---|---|
| `same-boat-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): a large shared "same boat" card, per-side write cards, a "still different" card |
| `same-boat-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC |
| `same-boat-guide.md` | Run sheet: objectives, setup, minute-by-minute script, grouping rules, variations |
| `same-boat-debrief.md` | Debrief questions + reading the shared card + three failure-mode rescues |
| `same-boat-start-here.md` | Start here — pick your lane, file map, print list |
| `same-boat-license.md` | License in plain language — what you may do, what you must keep |
| `same-boat-activity-poster.pdf` | The whole reframe on one wall (A3): meta, the run of show, the "both lose" rule, the reframe prompt. |

## Running it

1. Seat the two sides apart; state the rule — describe only what BOTH lose, never "they do X".
2. Each side writes its "both lose" list, separately, for five minutes.
3. Each reads its list aloud; overlaps go on the shared "same boat" card.
4. Around the shared items only: what would change if you treated that as the problem, not each other?
5. Keep a "still different" card for real disagreements so nothing is papered over.
6. Bridge: each side names one shared loss to act on together this week.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/same-boat/files/same-boat.zip
unzip same-boat.zip   # -> same-boat/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `same-boat` holding this SKILL.md, every file it references, and a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/same-boat/files/same-boat-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/same-boat/files/same-boat-activity-poster.pdf

# 3. Get the debrief and the run sheet
curl -O https://workshopskill.com/en/activities/same-boat/files/same-boat-debrief.md
curl -O https://workshopskill.com/en/activities/same-boat/files/same-boat-guide.md
```

This reframe needs no online form and no account — cards and two lists. There is no measured pre/post; the artifact is the shared "same boat" card and the kept-honest "still different" card.

Useful preparation facts for the agent:
- The two sides write separately, then reconvene to compare; seat them apart but in one room.
- Agenda math: frame 2 + write 5 + compare 7 + reframe 4 + bridge 2 = 20 minutes.
- No projector needed; the poster is optional and nothing requires a screen.
- Print at poker. One write card per side, one shared "same boat" card, one "still different" card.

**Where to put the skill.** Drop the unzipped `same-boat/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/same-boat/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/same-boat/`, Qoder `~/.qoder/skills/same-boat/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- Interrupt gently when a side writes "what they're doing wrong" — the rule is only shared losses; force concrete costs (a date, a sum, a name).
- The strongest moment is when one side hears a worry it had kept silent read aloud by the other.
- Same boat, different oars: naming a joint loss is not agreeing on everything — keep the "still different" list visible.

## Remix: make it yours

Want to rebrand this folder or package it for your own shelf? The license file (`same-boat-license.md`) spells out the tiers, and `same-boat-prop-cards.pdf` carries the print specs (poker trim, bleed, corner radius, gsm). Keep the CC BY attribution line and you're free to use it, sell it, or redistribute it.

## Attribution

Filed by hand and checked folder against folder — script, timings and prop sizes agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and this reframe stays open.
