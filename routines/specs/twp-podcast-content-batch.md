---
name: twp-podcast-content-batch
description: Biweekly podcast→social content batch (self-gates: only runs on a genuinely new episode)
---

Autonomous scheduled run (Thursdays) for Kaylan Jackson (The Well Place). This is the ported "podcast content batch." It is conceptually EVERY OTHER WEEK and should SELF-GATE: only produce a batch when there is a genuinely new podcast episode to pull from. DRAFTS ONLY.

FIRST: invoke `twp-auto-brain` to load voice + calibrations, and `twp-podcast` / `twp-content-repurposer` for the batch.

STEPS:
1. Read /Users/kaylan/Desktop/the well place/AI Team/KAYLAN_STATE.md and the most recent file in /Users/kaylan/Desktop/the well place/Content Drafts/Podcast Batches/ to find which episode the LAST batch used.
2. Determine if a genuinely NEW episode exists since that last batch (last published was Ep 2 on 2/1; Ep 3 "Science Proves God" was in scripting; Ep 4 "The High Exosome Diet" has been reused). If the source would REPEAT the last batch's episode, STOP: write "skipped — no new episode source" to the report and do not generate duplicate content.
3. If there IS a new episode: produce a batch from it — 3 social threads (mix of IG carousels + a text thread), IG + TikTok captions with hashtags (TikTok captions SUPER SHORT), ~5 community prompts, and 1 episode-discussion post for The Well Room + Wellspring.
4. Save to /Users/kaylan/Desktop/the well place/Content Drafts/Podcast Batches/<YYYY-MM-DD>_podcast-content-batch.md. If Notion is available, log rows to the Content Tracker as "Drafted by Claude."
5. Voice audit: 0 em dashes, 0 banned words, patent-quiet. Write a summary to /Users/kaylan/Desktop/the well place/AI Team/Routine Reports/twp-podcast-content-batch/<YYYY-MM-DD>.md.

NOTE: this REPLACES the Cowork "twp-podcast-content-batch" — disable that Cowork twin. Carry-forward lever: the bottleneck is publishing, not drafting — flag that in the report.

GUARDRAILS — unattended run: NEVER post or publish. Draft and notify ONLY. If a connector/skill/file is unavailable, note it and continue.