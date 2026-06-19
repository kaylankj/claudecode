---
name: otter-backfill-watch
description: Weekly check on the Otter→Notion transcript backlog
---

Autonomous WEEKLY scheduled run (Saturdays) for Kaylan Jackson (The Well Place). Context: there is a backlog of ~80+ never-synced Otter.ai transcripts that should be drained into Notion in batches. The Otter.ai MCP connector is now live (preferred over Chrome scraping), and a dedup fix is in place (Notion IN-query dedup).

STEPS:
1. Read /Users/kaylan/Desktop/the well place/AI Team/KAYLAN_STATE.md for the latest Otter/Notion sync status and current backlog estimate (Notion Otter DB was ~892 rows).
2. If the Otter and Notion connectors are available: list recent Otter transcripts not yet in the Notion Otter DB, and report how many remain in the backlog. Otherwise work from the state file.
3. Recommend the next batch to sync (e.g., the oldest 10-20), but DO NOT perform the sync automatically — flag it for Kaylan to trigger with "run the Otter backfill."
4. Note any apparent duplicates that slipped through.
5. Write to /Users/kaylan/Desktop/the well place/AI Team/Routine Reports/otter-backfill-watch/<YYYY-MM-DD>.md (create folder if needed) and finish with the current backlog count + recommended next batch size.

GUARDRAILS — unattended run: NEVER write to Notion or delete Otter content; inspect and recommend ONLY. The actual backfill is a separate Kaylan-triggered session. If a connector/file is unavailable, note it and continue.