---
name: draw-what-i-mean
description: A 12-minute, pairs (2 people) describe-and-draw tool that runs three rounds — free words, a shared shape-word card, then open clarifying questions — to show that instruction precision and a shared shorthand beat a confident description. Printable poker-spec cards and an A3 poster; no account, no projector.
version: 2.1.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: communication
  group_size: 2
  duration_minutes: 12
  setting: hybrid
  props: [poker picture cards, shared shape-word card, A4 sketch sheet per drawer]
  depth: tool-type
  language: en
  updated: 2026-10-08
---

# Draw What I Mean

Back to back, one partner describes a small composed picture — a few shapes in a fixed arrangement — and the other draws only from the words. Run three rounds (free, shared word card, open questions) and compare. The gap between the picture and the drawing is the lesson about instruction precision and shared vocabulary.

## When to use this tool

- A team builds from verbal or half-specified briefs and keeps shipping the wrong thing.
- You want a fast, hands-on demo of why a shared vocabulary and clarifying questions matter more than talking clearly.
- You have 12 minutes and pairs of two; no art skill needed — line shapes, not portraits.

## What is in the folder

| File | Purpose |
|---|---|
| `draw-what-i-mean-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): picture cards for the describer, one shared shape-word card, a blank authoring card |
| `draw-what-i-mean-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 document |
| `draw-what-i-mean-run-sheet-Letter.pdf` | US Letter paper size for the print document — same content, bookmarks and a linked TOC |
| `draw-what-i-mean-guide.md` | Run sheet: objectives, setup with a materials table, minute-by-minute script, failure modes and rescues, variations |
| `draw-what-i-mean-debrief.md` | 6 debrief questions with what each targets + reading the three comparisons + three failure modes of the debrief |
| `draw-what-i-mean-start-here.md` | Start here — pick your lane, file map, print list |
| `draw-what-i-mean-license.md` | License in plain language — what you may do, what you must keep |
| `draw-what-i-mean-activity-poster.pdf` | The whole tool on one wall (A3): meta, the three rounds, the bridge, watch-outs. |

## Running it

1. Pairs sit back to back; the drawer gets a blank sketch sheet, the describer a picture card face down.
2. Round 1 — free: describer talks, drawer draws from words only. Compare; note the drift.
3. Round 2 — vocabulary: same pair, new card, both may use the shared shape-word card. Compare.
4. Round 3 — questions: new card, the drawer may ask any clarifying question. Compare.
5. Bridge: one line each — which round closed the most gap, and what your work calls that.

## Run this tool with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/draw-what-i-mean/files/draw-what-i-mean.zip
unzip draw-what-i-mean.zip   # -> draw-what-i-mean/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `draw-what-i-mean` holding this SKILL.md, every file it references, and a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/draw-what-i-mean/files/draw-what-i-mean-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/draw-what-i-mean/files/draw-what-i-mean-activity-poster.pdf

# 3. Get the debrief and the run sheet
curl -O https://workshopskill.com/en/activities/draw-what-i-mean/files/draw-what-i-mean-debrief.md
curl -O https://workshopskill.com/en/activities/draw-what-i-mean/files/draw-what-i-mean-guide.md
```

This tool needs no online form and no account — it is paper and a pen. There is no measured pre/post; the artifact is the comparison between the picture card and the drawing.

Useful preparation facts for the agent:
- One pair is 2 people seated back to back; run many pairs at once with the same card set.
- Agenda math: setup 1 + three rounds 3+3+3 + compare/bridge 2 = 12 minutes.
- No projector needed; nothing in the folder requires a screen.
- Print at poker. One picture card per pair per round, one shared shape-word card per pair.

**Where to put the skill.** Drop the unzipped `draw-what-i-mean/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/draw-what-i-mean/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/draw-what-i-mean/`, Qoder `~/.qoder/skills/draw-what-i-mean/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- The strongest moment is comparing round 1 to round 2 — same describer, same effort, only the shared vocabulary changed.
- If a describer reaches over to draw, hold back-to-back: words only, the drawer keeps the pen.
- The strongest transfer question: "What is the shape-word card in your real work — and who isn't allowed to reach for it?"

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings and prop sizes agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and this tool stays open.
