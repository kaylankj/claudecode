# The Well Place — Routine Catalog (Master Map)

> Single source of truth for every scheduled routine in the AI Team.
> **Surface:** routines run in **Claude Cowork** (server-side). This file is the
> version-controlled *blueprint* — edit here, then stand the routine up in Cowork.
> Last mapped: 2026-06-19 (from KAYLAN_STATE.md).

**Legend** — Cadence · Surface · Status (🟢 live / 🟡 needs attention / ⚪ proposed)
**Lane** — 💼 Business · 🏠 Personal · ⚙️ Infrastructure

---

## PART 1 — EXISTING ROUTINES (already running in Cowork)

### Daily
| Routine | Time | Lane | What it does | Output | Status |
|---|---|---|---|---|---|
| `mordecai-daily` | ~AM | 💼 | The gate orchestrator. Sets "Today's 3," surfaces hottest funding + aging loops, flags drift | `AI Team/Mordecai/mordecai_YYYY-MM-DD.md` | 🟢 |
| `twp-mailerlite-daily` | ~5 AM | 💼 | Subscriber sync, draft staging, send-loop nudge, report | `MailerLite Reports/YYYY-MM-DD-mailerlite.md` | 🟢 |
| `grounding-sync-telegram` | daily | ⚙️ | Grounding/state sync to Telegram + Supabase | Supabase write | 🟡 confirm live write |
| `session-memory-sync` | ~10 PM | ⚙️ | Consolidates the day's sessions into the state file | `KAYLAN_STATE.md` | 🟢 |
| `state-verification-nightly` | nightly | ⚙️ | Pings every connector, writes drift report (green/yellow/red) | `AI Team/drift-YYYY-MM-DD.md` | 🟢 |
| `memory-icloud-sync-nightly` | nightly | ⚙️ | Syncs Obsidian TWP_Memory vault (now on Google Drive) | Drive vault | 🟡 verify path post-move |

### Weekly
| Routine | Day | Lane | What it does | Output | Status |
|---|---|---|---|---|---|
| `twp-morning-briefing` | Mon ~6 AM | 💼 | Week's top 5, calendar pileups, aging counters | `Daily Briefings/` | 🟢 |
| `twp-monday-podcast` (Monday Sprint) | Mon ~midday | 💼 | Podcast repurpose check + funding scout (net-new opps + reconfirm live) | `Funding Briefing - <date>.docx` | 🟢 |
| `twp-tuesday-writing` | Tue | 💼 | Drafts 1 Substack + 1 paired nurture email (voice-audited) | `Content Drafts/<date>_tuesday-writing/` | 🟢 |

### Biweekly / As-flagged
| Routine | Cadence | Lane | What it does | Output | Status |
|---|---|---|---|---|---|
| `twp-podcast-content-batch` | every other wk (ON weeks) | 💼 | Podcast → 3 social threads + captions + community prompts, logged to Notion | `Content Drafts/Podcast Batches/` | 🟡 source repeats until new ep |
| `twp-vessel-app-nightly-build` | nightly/as-flagged | 💼 | Vessel app build + ship work on `ship/vault-wiring-testflight` | git commits + state note | 🟢 |

### Referenced but unconfirmed (verify these exist as routines)
- **Book Launch Daily** — folder exists; is there a `book-launch-daily` routine?
- **Systems Health** — folder exists; tied to `state-verification`?
- **ClickUp sync** — `clickup_sync_logs/` exists; a `clickup-sync` routine?

---

## PART 1B — PORTED COWORK → CLAUDE CODE (2026-06-19, smart split)

> These 3 weekly content/scout routines were reconstructed as Claude Code tasks
> (they invoke the TWP skills: twp-auto-brain, twp-funding-scout, twp-substack,
> twp-brand-voice, twp-podcast). **⚠️ Disable the Cowork twins** so they don't double-run.
> The daily-critical / state-writing / app-build / infra routines in Part 1 STAY in Cowork.

| Routine | Schedule (local) | What it does | Status |
|---|---|---|---|
| `twp-monday-sprint` | Mon 12:06 PM | Funding scout (net-new + reconfirm) → Funding Briefing .docx + podcast repurpose check | 🟢 ported |
| `twp-tuesday-writing` | Tue 10:03 AM | Drafts 1 Substack + 1 paired nurture email in her voice (humanizer pass) | 🟢 ported |
| `twp-podcast-content-batch` | Thu 1:05 PM (self-gates) | Podcast→social batch ONLY when a genuinely new episode exists | 🟢 ported |

**Cowork twins to DISABLE:** `twp-monday-podcast` (Monday Sprint), `twp-tuesday-writing`, `twp-podcast-content-batch`.

---

## PART 2 — NEW ROUTINES (🟢 LIVE in Claude Code as of 2026-06-19)

> These run via the Claude Code `scheduled-tasks` engine on this Mac (while the app
> is open; if closed when due, they run on next launch). All are **draft-and-notify
> only** — none send, post, publish, or spend. Each writes a report to
> `Desktop/the well place/AI Team/Routine Reports/<name>/<date>.md`.
> Definitions: `~/.claude/scheduled-tasks/<name>/SKILL.md`.

### 💼 Business
| Routine | Schedule (local) | What it does | Status |
|---|---|---|---|
| `funding-deadline-watch` | daily 6:36 AM | Countdown of every live funding deadline; 🔴 flags ≤7 days; web-verifies <14-day ones | 🟢 |
| `publishing-unblock` | daily 7:01 AM | Watches the unsent draft pile + Repurpose.io health; surfaces ONE "ship today" pick | 🟢 |
| `ip-deadline-watch` | Mon 7:38 AM | TM Office Actions (due 2026-07-20) + patent/PCT windows; flags ≤30/≤14 days | 🟢 |
| `client-pipeline-sweep` | Wed 9:10 AM | Pipeline follow-up list + drafts top 3 warm follow-ups (not sent) | 🟢 |
| `stripe-checkout-watch` | Fri 8:05 AM | Confirms Stripe live + every active product has a working buy-link | 🟢 |

### 🏠 Personal
| Routine | Schedule (local) | What it does | Status |
|---|---|---|---|
| `family-calendar-sync` | daily 6:53 AM | Checks personal events are on the work cal; flags kkelsey143 disconnects | 🟢 |
| `willie-va-tracker` | Mon 8:06 AM | VA claim 127839356 next-actions; sleep-apnea C&P + 8/11 reimbursement | 🟢 |
| `health-followups` | Thu 8:08 AM | Open medical loops: seizure eval, comprehensive draw + thyroid, echo/EF | 🟢 |
| `credit-rebuild` | 1st of month 9 AM | Credit-rebuild steps: OIS pay-for-delete, freezes, Ollo; pulls score factors | 🟢 |

### ⚙️ Infrastructure
| Routine | Schedule (local) | What it does | Status |
|---|---|---|---|
| `memory-prune` | Sun 11:02 PM | Checks MEMORY.md size; writes a PROPOSED trim (never overwrites live) | 🟢 |
| `otter-backfill-watch` | Sat 10:07 AM | Reports the Otter→Notion backlog + recommends next batch (you trigger sync) | 🟢 |

---

## PART 2B — BUSINESS SYSTEM HEALTH CHECKS (🟢 LIVE in Claude Code, 2026-06-19)

> "Are we up to par?" inspection routines per asset. All draft-and-notify only.
> `business-pulse` is the weekly rollup that reads every other report.

| Routine | Schedule (local) | What it checks | Status |
|---|---|---|---|
| `app-health-check` | Tue 8:01 AM | Vessel app: TestFlight build, Supabase active/migrations, test suite, Anthropic credits | 🟢 |
| `website-health-check` | Tue 9:10 AM | thewellplace.co loads + known leaks (Recieve typo, BOOK NOW green, popup→MailerLite, brand) | 🟢 |
| `email-health-check` | Wed 8:08 AM | MailerLite automations (Welcome/[QUIZ]), list growth, bounces/spam, days dark | 🟢 |
| `social-media-health-check` | Thu 9:08 AM | IG/TikTok posted-this-week?, follower trend, ManyChat live, Repurpose.io fixed? | 🟢 |
| `business-pulse` | Fri 4:04 PM | Rollup scorecard across App/Web/Email/Social/Cash/Funding/Clients/IP + top 3 actions | 🟢 |

---

## PART 3 — YOUR ADDITIONS (brain-dump zone)

> Drop any routine you want here in one line. I'll formalize each into Part 1/2
> format and a Cowork-ready spec. Format: `name — cadence — what it should do`.

- _e.g. morning-text-digest — daily 7am — text me my Today's 3 + weather + first meeting_
-
-
-

---

## Build order (once Part 3 is filled)
1. Finalize this catalog (you edit Parts 2–3).
2. For each routine, write a Cowork spec: trigger/cadence, exact prompt, inputs (brain/state/Notion), outputs, guardrails (no send/post/spend without you).
3. Stand them up in Cowork one lane at a time (Business → Personal → Infra), verify each fires once before moving on.
4. Mirror each finalized spec into `routines/specs/<name>.md` for version control.
