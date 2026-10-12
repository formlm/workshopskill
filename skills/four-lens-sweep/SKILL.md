---
name: four-lens-sweep
description: A 20-minute, 4-10 person way to review one idea four times — Facts, then Feelings, then Risks, then Upside — with everyone in the same lens at the same time, so a room looks at one object four ways instead of arguing positions. Printable poker lens cards and an A3 poster; no account, no projector.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: creativity
  group_size: 4
  duration_minutes: 20
  setting: hybrid
  props: [poker lens cards, four sticky columns, a marker]
  depth: tool-type
  language: en
  updated: 2026-10-11
---

# Four-Lens Sweep

One idea is reviewed four times in a row, each pass through a single lens — what's true (Facts), how it lands (Feelings), what could break (Risks), what it unlocks (Upside) — with the whole room in the same lens at once. The room looks at one object four ways instead of arguing positions.

## When to use this activity

- A promising idea is about to be killed or loved by gut in one pass, with no even look at it.
- Your team reviews by personality — the optimist, the doubter, the accountant — never all four at once.
- You have twenty minutes and one decision worth pressure-testing; it works on a call.

## What is in the folder

| File | Purpose |
|---|---|
| `four-lens-sweep-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): four lens cards, a column-label card, a blank lens face |
| `four-lens-sweep-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC |
| `four-lens-sweep-guide.md` | Run sheet: objectives, setup, minute-by-minute script, grouping rules, variations |
| `four-lens-sweep-debrief.md` | Debrief questions + reading the four columns + three failure-mode rescues |
| `four-lens-sweep-start-here.md` | Start here — pick your lane, file map, print list |
| `four-lens-sweep-license.md` | License in plain language — what you may do, what you must keep |
| `four-lens-sweep-activity-poster.pdf` | The whole sweep on one wall (A3): meta, the four lenses, the one-lens-at-a-time rule, the synthesis prompt. |

## Running it

1. Put one idea on the wall; state the rule — one lens at a time, everyone in sync.
2. Facts pass (4 min): only what's true and what we assume. Then Feelings pass (4 min): only reactions.
3. Risks pass (5 min): only failure points and early warnings — don't fix yet. Then Upside pass (4 min): only what it opens, no "buts".
4. Synthesise: read the four columns together and decide with the whole picture in view.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/four-lens-sweep/files/four-lens-sweep.zip
unzip four-lens-sweep.zip   # -> four-lens-sweep/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `four-lens-sweep` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/four-lens-sweep/files/four-lens-sweep-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/four-lens-sweep/files/four-lens-sweep-activity-poster.pdf

# 3. Get the debrief and the run sheet
curl -O https://workshopskill.com/en/activities/four-lens-sweep/files/four-lens-sweep-debrief.md
curl -O https://workshopskill.com/en/activities/four-lens-sweep/files/four-lens-sweep-guide.md
```

This sweep needs no online form and no account — four lens cards, four columns, a marker. There is no measured pre/post; the artifact is the four-column picture and the decision made from the whole of it.

Useful preparation facts for the agent:
- 4–10 people around one idea; the whole room changes lenses together, four passes.
- Agenda math: frame 1 + Facts 4 + Feelings 4 + Risks 5 + Upside 4 + synthesise 2 = 20 minutes.
- No projector needed; the poster is optional and nothing requires a screen.
- Print at poker. One set of four lens cards and four sticky columns for the wall.

**Where to put the skill.** Drop the unzipped `four-lens-sweep/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/four-lens-sweep/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/four-lens-sweep/`, Qoder `~/.qoder/skills/four-lens-sweep/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- Keep every pass single-lens and timeboxed — the discipline of not mixing lenses is the whole value.
- The strongest moment is a fact-flag that turns out to be a shared assumption everyone had treated as true.
- End on the upside pass on purpose; a review that finishes on risks reads as a downer and gets avoided.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings and prop sizes agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and this sweep stays open.
