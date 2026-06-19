---
name: email-health-check
description: Weekly MailerLite health: automation states, list growth, deliverability
---

Autonomous WEEKLY scheduled run (Wednesdays) for Kaylan Jackson (The Well Place). Goal: keep the email system healthy. This is about SYSTEM HEALTH (automations, list, deliverability) — the daily publishing-unblock routine already handles shipping individual drafts, so do NOT duplicate that.

KNOWN STATE (verify/update from the state file each run):
- Platform: MailerLite. ~84 subscribers. Last send was 2026-05-20 (has been weeks dark).
- 9 automations, historically ALL OFF. Two critical ones: Welcome (id 183551989667333445) and Identify Series [QUIZ] (id 189996317280306684) — both disabled, so quiz signups land in silence.
- The funnel depends on Welcome being ON: signups → Welcome Seq → Vessel Snapshot $97.

STEPS:
1. Read /Users/kaylan/Desktop/the well place/AI Team/KAYLAN_STATE.md for the latest MailerLite status.
2. If the MailerLite connector is available: report subscriber count + weekly delta, new/unsubscribed/bounced/spam counts, the enabled/disabled state of all automations (especially Welcome + [QUIZ]), and days since last campaign send. Otherwise work from the state file.
3. Flag 🔴: any critical automation still OFF, rising bounce/spam, or list shrinkage.
4. Deliverability sanity: note if sending has been dark long enough to risk list cool-down.
5. Write to /Users/kaylan/Desktop/the well place/AI Team/Routine Reports/email-health-check/<YYYY-MM-DD>.md (create folder if needed) and finish with the single highest-leverage email-system fix (likely: flip Welcome ON).

GUARDRAILS — unattended run: NEVER send campaigns, enable/disable automations, or edit subscribers. Inspect and notify ONLY; flipping toggles is Kaylan's tap. If a connector/file is unavailable, note it and continue.