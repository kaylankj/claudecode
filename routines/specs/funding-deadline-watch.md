---
name: funding-deadline-watch
description: Daily funding/grant deadline countdown with urgent flags for The Well Place
---

Autonomous DAILY scheduled run for Kaylan Jackson (The Well Place). Goal: make sure no funding/grant deadline hits 0 days unseen.

STEPS:
1. Read /Users/kaylan/Desktop/the well place/AI Team/KAYLAN_STATE.md for the current funding pipeline, plus any "Funding Briefing - *.docx/.md" files in /Users/kaylan/Desktop/the well place/ (workspace root).
2. Build a countdown table of every live opportunity that has a deadline: name | amount | deadline date | days remaining (compute from today) | fit score | current status. Sort by days remaining ascending.
3. Flag anything ≤7 days as 🔴 URGENT with the exact next action (submit, confirm registration, or file an extension) and any fee/no-fee note.
4. For any deadline within 14 days, use WebSearch to confirm it still stands (grant pages change/close).
5. Known recurring ones to always check if still open: NSF SBIR Phase I (full proposal deadlines), Google for Startups Black Founders Fund, SCRA SC Launch, AT&T She's Connected, HLTH, TiE, Evolve, Visionaries, Black Ambition Alumni Edge follow-on.
6. Write the report to /Users/kaylan/Desktop/the well place/AI Team/Routine Reports/funding-deadline-watch/<YYYY-MM-DD>.md (create the folder if needed) and finish with a 3-line summary of the most urgent items.

GUARDRAILS — unattended run: NEVER submit, send, apply, spend, or change settings on Kaylan's behalf. Draft and notify ONLY; every external action stays hers. Label any drafts "Drafted by Claude." Voice: 0 em dashes, 0 banned words, keep patent details out of public-facing copy. If a connector or file is unavailable this run, note it and continue rather than failing.