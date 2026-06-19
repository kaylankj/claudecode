---
name: app-health-check
description: Weekly health check on the Vessel app + Supabase backend
---

Autonomous WEEKLY scheduled run (Tuesdays) for Kaylan Jackson (The Well Place). Goal: keep the Vessel app + its backend healthy and shippable. This is an INSPECTION/STATUS check — do not run builds, deploys, or migrations.

KNOWN FACTS (verify/update from the state file each run):
- App: Vessel (Expo project @kaylankj/the-well-place; active ship branch ship/vault-wiring-testflight; main lags behind).
- App Store Connect: App ID 6781328209, bundle com.thewellplace.vessel, Team AQ5Q4TYBTD, builds submitted under Apple ID kaylankelsey@ymail.com. Last known: v1.4.0 build 1 delivered to Apple.
- Backend: Supabase project cqwjwfqxiakmlasybmdi (has flashed INACTIVE/paused before — flag if paused). Edge functions: oura-oauth, admin-load-client, parse-lab-report. Migrations 007 (Oura tokens) + 008 (lab columns) were PENDING link+push — track whether applied.
- Health bars: test suite was 1093/1093 green, tsc strict clean, 0 em dashes / 0 banned words. RLS account isolation verified (auth.uid() = user_id on every health table).
- Anthropic Console credits were low (~$4.23) — flag if low; the app uses ANTHROPIC_API_KEY as a Supabase secret.
- Repo lives in the ourwellplace Google Drive copy, NOT Desktop.

STEPS:
1. Read /Users/kaylan/Desktop/the well place/AI Team/KAYLAN_STATE.md for the latest app/backend status.
2. Produce a status board: TestFlight build state, Supabase active/paused, migrations applied?, test suite status, open blockers (e.g., lab-parser wiring, data-loader build, Apple ID cleanup, web/laptop build), Anthropic credit level.
3. Flag anything 🔴 (paused backend, failing build, low credits) with the one fix action.
4. Write to /Users/kaylan/Desktop/the well place/AI Team/Routine Reports/app-health-check/<YYYY-MM-DD>.md (create folder if needed) and finish with the top app blocker this week.

GUARDRAILS — unattended run: NEVER run builds, submit to TestFlight, deploy edge functions, push migrations, or change Supabase/Apple settings. Inspect and notify ONLY. If a connector/file is unavailable, note it and continue.