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

## PART 2 — PROPOSED NEW ROUTINES (gaps visible in your state file)

> ⚪ These are *suggestions* drawn from recurring loops in KAYLAN_STATE.md.
> Keep, cut, or edit. Nothing here is built yet.

### 💼 Business
| Proposed | Suggested cadence | Why (the loop it closes) |
|---|---|---|
| `funding-deadline-watch` | daily | Funding deadlines keep going to 0 days (Evolve $50K, Visionaries, TiE, HLTH, AT&T). A daily countdown + "submit/extend by" alert |
| `ip-deadline-watch` | weekly | 2 trademark Office Actions due **2026-07-20** (NANONUTRITION + High Exosome Diet); patent/PCT windows. Surfaces what's due before it lapses |
| `publishing-unblock` | daily | The #1 lever flagged repeatedly: *publishing is the bottleneck, not drafting.* Watches Repurpose.io health + the unsent draft pile (52 drafts, 8 AUTO) and nudges 1 send |
| `client-pipeline-sweep` | weekly | Notion Client Pipeline keeps going empty; warm follow-ups for kit recipients + leads |
| `stripe-checkout-watch` | weekly | Stripe reads live but checkout plumbing has gaps ($0 despite owed kits). Confirms buy-links actually work |

### 🏠 Personal
| Proposed | Suggested cadence | Why |
|---|---|---|
| `willie-va-tracker` | weekly | VA claim 127839356 (Step 3/8); sleep-apnea C&P exam ~6/29 is the last holdup; back-pay accruing. Tracks QTC/VA next-actions |
| `health-followups` | weekly | Open medical loops: seizure eval (30+ days), comprehensive blood draw + thyroid panel before deadlines, echo/EF before any stress protocol |
| `credit-rebuild` | monthly | July post-Paris plan: pay-for-delete $637 OIS collection, bureau freezes, Ollo app. Keeps the steps moving |
| `family-calendar-sync` | daily | Family cal (kkelsey143) keeps disconnecting so trips/events don't show on the work calendar |

### ⚙️ Infrastructure
| Proposed | Suggested cadence | Why |
|---|---|---|
| `memory-prune` | weekly | `MEMORY.md` keeps blowing past its size cap (37KB, over again). Auto-trim + archive |
| `otter-backfill-watch` | weekly | ~80 never-synced Otter transcripts backlog; drains it in batches |

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
