---
name: memory-prune
description: Weekly trim-check of the TWP brain-vault MEMORY.md (iCloud) so it stays under cap
---

Autonomous WEEKLY scheduled run (Sunday night) for Kaylan Jackson. Goal: keep her TWP brain-vault MEMORY.md from blowing past its size cap (target lean, ideally under ~18KB; it has hit ~48KB).

PRIMARY TARGET: /Users/kaylan/Library/Mobile Documents/com~apple~CloudDocs/TWP_Memory/memory/MEMORY.md

STEPS:
1. Read the primary target above and report its size in KB + line count.
2. ALSO note (do not edit) two sibling copies that exist and can drift out of sync — flag if their sizes/dates differ from the primary, since multiple copies is a source-of-truth risk:
   - /Users/kaylan/Library/CloudStorage/GoogleDrive-kkelsey143@gmail.com/My Drive/TWP_Memory/memory/MEMORY.md
   - /Users/kaylan/Library/Mobile Documents/com~apple~CloudDocs/TWP_Memory_OLD_iCloud_BACKUP/memory/MEMORY.md
3. If the primary is over ~18KB or clearly bloated: identify duplicate, stale, or superseded entries and PROPOSE a trimmed version (push durable detail down into the individual linked memory files, keep MEMORY.md to one tight line per memory).
4. Write the proposed trimmed file to /Users/kaylan/Desktop/the well place/AI Team/Routine Reports/memory-prune/<YYYY-MM-DD>_MEMORY-proposed.md — do NOT overwrite any live MEMORY.md.
5. Finish with: primary size, whether a trim is recommended, whether the three copies are in sync, and where the proposal was saved.

GUARDRAILS — unattended run: do NOT overwrite or delete ANY MEMORY.md or memory file; only write a PROPOSED version to the report folder for Kaylan to approve. If a file is unavailable, note it and continue.