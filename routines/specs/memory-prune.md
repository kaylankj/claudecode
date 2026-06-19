---
name: memory-prune
description: Weekly check + trim of MEMORY.md so it stays under its size cap
---

Autonomous WEEKLY scheduled run (Sunday night) for Kaylan Jackson. Context: her auto-memory index MEMORY.md keeps blowing past its size cap (has hit ~37KB; target is lean, ideally under ~18KB).

STEPS:
1. Read /Users/kaylan/.claude/projects/-Users-kaylan/memory/MEMORY.md and report its current size in KB and line count.
2. If it is over ~18KB or noticeably bloated: identify duplicate, stale, or superseded entries and PROPOSE a trimmed version (move durable detail into the individual memory files it links to, keep MEMORY.md to one tight line per memory).
3. Write the proposed trimmed MEMORY.md to /Users/kaylan/Desktop/the well place/AI Team/Routine Reports/memory-prune/<YYYY-MM-DD>_MEMORY-proposed.md (create folder if needed) — do NOT overwrite the live MEMORY.md.
4. Also note any individual memory file in that memory/ folder that looks stale or wrong and should be reviewed.
5. Finish with: current size, whether a trim is recommended, and where the proposed version was saved.

GUARDRAILS — unattended run: do NOT overwrite or delete the live MEMORY.md or any memory file; only write a PROPOSED version to the report folder for Kaylan to approve. If a file is unavailable, note it and continue.