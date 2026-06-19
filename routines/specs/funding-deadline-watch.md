---
name: funding-deadline-watch
description: Daily funding/grant deadline countdown with urgent flags for The Well Place
---

Autonomous DAILY scheduled run for Kaylan Jackson (The Well Place). Goal: make sure no funding/grant deadline hits 0 days unseen — AND that the amounts/eligibility she's acting on are actually correct.

STEPS:
1. Read /Users/kaylan/Desktop/the well place/AI Team/KAYLAN_STATE.md for the current funding pipeline, plus any "Funding Briefing - *.docx/.md" files in /Users/kaylan/Desktop/the well place/ (workspace root).
2. Build a countdown table of every live opportunity that has a deadline: name | amount | deadline date | days remaining (compute from today) | fit score | current status. Sort by days remaining ascending.
3. VERIFY-BEFORE-FLAGGING (critical): for anything ≤14 days OR that you'd rank as a top-3 "hottest," use WebSearch/WebFetch to confirm against the OFFICIAL source: (a) the exact dollar amount, (b) the real deadline, (c) key eligibility (esp. minimum annual revenue, location, ownership, years operating). If the verified figure differs from the state file, FLAG THE DISCREPANCY explicitly (e.g. "state file says $50K; official source says $5,000 — corrected") and rank by the VERIFIED amount, not the state-file number. Known prior error: "Evolve" = Entreprenista Evolve Grant, $5,000 (NOT $50K), requires $100K+ annual revenue — Kaylan may be ineligible.
4. Eligibility gate: if Kaylan clearly fails a hard requirement (e.g. revenue floor she doesn't meet — her revenue is ~$45K-90K), mark it ⚠️ LIKELY INELIGIBLE so she doesn't waste time, rather than listing it as urgent.
5. Flag verified opportunities ≤7 days as 🔴 URGENT with the exact next action and any fee/no-fee note.
6. Always-check recurring set if still open: NSF SBIR Phase I, Google for Startups Black Founders Fund, SCRA SC Launch, AT&T She's Connected, HLTH, TiE.
7. Write the report to /Users/kaylan/Desktop/the well place/AI Team/Routine Reports/funding-deadline-watch/<YYYY-MM-DD>.md (create the folder if needed) and finish with a 3-line summary of the most urgent VERIFIED + ELIGIBLE items.

GUARDRAILS — unattended run: NEVER submit, send, apply, spend, or change settings on Kaylan's behalf. Draft and notify ONLY; every external action stays hers. Label any drafts "Drafted by Claude." Voice: 0 em dashes, 0 banned words, keep patent details out of public-facing copy. If a connector or file is unavailable, note it and continue rather than failing.