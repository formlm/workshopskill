---
name: assumption-audit
description: A 20-minute, 3-8 person pass that surfaces the unwritten things a plan needs to be true, tags each as Evidence / To-verify / Fragile-if-false, and ranks the fragile ones down to the two or three that would actually break the plan — each with an owner and a date to check. Printable poker cards and an A3 poster; no account, no projector.
version: 2.0.0
license: CC-BY-4.0
allowed-tools: Read, Write, Bash(curl:*), Bash(unzip:*)
metadata:
  category: creativity
  group_size: 3
  duration_minutes: 20
  setting: hybrid
  props: [poker prompt + tag cards, who-checks-by-when card, blank assumption cards]
  depth: tool-type
  language: en
  updated: 2026-10-11
---

# Assumption Audit

A plan works only if a list of things nobody wrote down are true. The team surfaces those hidden assumptions, tags each one Evidence / To-verify / Fragile-if-false, and ranks them by how much the plan rests on it. What comes out is the two or three unexamined beliefs that would actually break the plan — each with an owner and a date to check.

## When to use this activity

- A plan looks solid and everyone agrees too quickly — usually because the load-bearing assumptions are invisible.
- You're about to commit time or money and want to know what the plan secretly depends on.
- You have 3–8 people who built or will run the plan and twenty minutes; it works on a call.

## What is in the folder

| File | Purpose |
|---|---|
| `assumption-audit-prop-cards.pdf` | Poker-spec print sheet (63.5 × 88.9 mm, bleed + cut guides, backs + blanks): an assumption-prompt card, three tag cards, a who-checks-by-when card, blanks |
| `assumption-audit-run-sheet.pdf` | The print edition: run sheet + debrief bound as one A4 document |
| `*-Letter.pdf` | US Letter paper size for the print documents in this folder — same content, bookmarks and a linked TOC |
| `assumption-audit-guide.md` | Run sheet: objectives, setup, minute-by-minute script, grouping rules, variations |
| `assumption-audit-debrief.md` | Debrief questions + reading the board + three failure-mode rescues |
| `assumption-audit-start-here.md` | Start here — pick your lane, file map, print list |
| `assumption-audit-license.md` | License in plain language — what you may do, what you must keep |
| `assumption-audit-activity-poster.pdf` | The whole audit on one wall (A3): meta, the run of show, the three tags, the owner-and-date prompt. |

## Running it

1. Put the plan up; define an assumption — something the plan needs true that isn't written in it.
2. Silent, then round-robin: every "the plan assumes…" on a card. Aim for 10–15; don't judge yet.
3. Tag each Evidence / To-verify / Fragile-if-false; rank the fragile ones by how much the plan rests on them.
4. For the top 2–3 fragile assumptions: who checks it, by when, and the fallback if it fails.
5. Read back: say the scariest assumption aloud; confirm the owner and the date.

## Run this activity with an agent

A facilitator can hand this whole folder to their AI agent. Install first — one command:

```bash
curl -LO https://workshopskill.com/en/activities/assumption-audit/files/assumption-audit.zip
unzip assumption-audit.zip   # -> assumption-audit/SKILL.md + all files + manifest
```

The zip unpacks to a directory named `assumption-audit` holding this SKILL.md, every file it references, a manifest.

Individual files, if you only need some — anonymous, CC BY 4.0:

```bash
# 1. Get the printable cards
curl -O https://workshopskill.com/en/activities/assumption-audit/files/assumption-audit-prop-cards.pdf

# 2. Get the wall poster
curl -O https://workshopskill.com/en/activities/assumption-audit/files/assumption-audit-activity-poster.pdf

# 3. Get the debrief and the run sheet
curl -O https://workshopskill.com/en/activities/assumption-audit/files/assumption-audit-debrief.md
curl -O https://workshopskill.com/en/activities/assumption-audit/files/assumption-audit-guide.md
```

This audit needs no online form and no account — cards and a wall. There is no measured pre/post; the artifact is the ranked list of fragile assumptions with an owner and a check-by date for each.

Useful preparation facts for the agent:
- 3–8 people who built or will run the plan; silent first so opinions don't anchor the list.
- Agenda math: frame 2 + surface 6 + tag & rank 5 + assign 5 + read back 2 = 20 minutes.
- No projector needed; the poster is optional and nothing requires a screen.
- Print at poker. One prompt card, three tag cards and blanks per group.

**Where to put the skill.** Drop the unzipped `assumption-audit/` directory into your agent's skills folder and it loads automatically: Claude Code `~/.claude/skills/assumption-audit/` (or `.claude/skills/` in the project), OpenAI Codex `~/.codex/skills/assumption-audit/`, Qoder `~/.qoder/skills/assumption-audit/`. No skills folder in your agent? Paste this file into the chat and ask the agent to follow it. Per-agent walkthroughs: https://workshopskill.com/en/skill-guides/

## Facilitation notes

- Keep the distinction sharp: a risk might happen; an assumption is believed true right now — ask "what do we assume here?"
- Force a ranking of the fragile ones; "everything is critical" means nothing was examined.
- End on owners and dates before the point of no return, or the audit was theatre.

## Remix: make it yours

## Attribution

Filed by hand and checked folder against folder — script, timings and prop sizes agree. Free under CC BY 4.0 — run it, copy it, rebrand it for your own workshop; keep the attribution and this audit stays open.
