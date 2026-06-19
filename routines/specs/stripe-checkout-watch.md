---
name: stripe-checkout-watch
description: Weekly check that Stripe is live and buy-links/checkout actually work
---

Autonomous WEEKLY scheduled run (Fridays) for Kaylan Jackson (The Well Place). Context: Stripe reads as LIVE but the checkout/payment-link plumbing has had gaps — owed kits exist but $0 is moving through Stripe ("$1,188" = owed kits, NOT Stripe balance). Goal: catch broken checkout before it costs a sale.

STEPS:
1. Read /Users/kaylan/Desktop/the well place/AI Team/KAYLAN_STATE.md for current Stripe status, owed kits, and pricing (Snapshot $97, Blueprint $297, Intensive $997; tinctures/add-ons as listed).
2. If Stripe connectors are available: confirm the account is live (acct_1PTmPLEbNCGxt0Oa), list active payment links/products, and note balance + active subscriptions. Otherwise work from the state file.
3. Cross-check: does every product Kaylan is actively selling have a working payment link? Flag any product with no link or an inactive one.
4. List any owed-kit/customer that has no corresponding invoice or payment link.
5. Write to /Users/kaylan/Desktop/the well place/AI Team/Routine Reports/stripe-checkout-watch/<YYYY-MM-DD>.md (create folder if needed) and finish with any checkout gap that could be losing money.

GUARDRAILS — unattended run: NEVER create/modify products, payment links, invoices, refunds, or charge anyone. Inspect and notify ONLY. If a connector/file is unavailable, note it and continue.