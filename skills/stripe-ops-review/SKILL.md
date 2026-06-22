---
name: stripe-ops-review
description: Analyze sanitized Stripe-like subscription, invoice, payment, refund, churn, and revenue exports. Use when Codex needs to summarize billing operations or revenue movement without accessing live Stripe credentials, customer PII, payment methods, webhooks, or production account settings.
---

# Stripe Ops Review

## Safety Boundary

Use only sanitized CSVs, spreadsheets, or copied summaries. Do not request secret keys, webhook secrets, customer emails, card data, bank details, account IDs, tax IDs, or live dashboard access.

Do not cancel, refund, retry, modify, or create subscriptions from this public skill.

## Workflow

1. Identify the export type: subscriptions, invoices, payments, refunds, products, coupons, or events.
2. Normalize dates, currency, status labels, and plan names.
3. Calculate only from available fields:
   - gross revenue
   - refunds
   - net revenue
   - active subscriptions
   - churned subscriptions
   - failed payments
   - plan mix
4. Flag data gaps before drawing conclusions.
5. Produce a concise operating summary and follow-up questions.

## Output

Return:

- `metrics`
- `trend_summary`
- `exceptions`
- `data_quality_notes`
- `questions_for_operator`
- `manual_followups`
