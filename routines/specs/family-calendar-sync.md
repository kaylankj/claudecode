---
name: family-calendar-sync
description: Daily check that family events are visible on the work calendar; flags disconnects
---

Autonomous DAILY scheduled run for Kaylan Jackson. Context: her family/personal calendar (account kkelsey143) keeps disconnecting, so trips, flights, and personal events don't show on her primary work calendar and she gets surprised.

STEPS:
1. Read /Users/kaylan/Desktop/the well place/AI Team/KAYLAN_STATE.md for known upcoming personal events (flights, baby shower, eye exams, appointments, travel).
2. If Google Calendar connectors are available, list events for the next 14 days across all accessible calendars; otherwise work from the state file.
3. Cross-check: are the known personal/family events (from the state file) actually present on the work calendar? List any that are MISSING or that appear only on the family calendar.
4. If the family calendar (kkelsey143) appears disconnected/inaccessible, flag it clearly with the one-line fix ("reconnect kkelsey143 in calendar settings") — do not attempt to reconnect it yourself.
5. Write to /Users/kaylan/Desktop/the well place/AI Team/Routine Reports/family-calendar-sync/<YYYY-MM-DD>.md (create folder if needed) and finish with: today's events + anything missing from the work calendar.

GUARDRAILS — unattended run: NEVER create, move, delete, or accept calendar events, and never change connection settings. Report and notify ONLY. If a connector/file is unavailable, note it and continue.