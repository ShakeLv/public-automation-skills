---
name: stripe-ops-review
description: Analyze sanitized Stripe revenue, subscription, invoice, payment, refund, churn, and cohort exports. Use when Codex needs to produce Stripe data analysis without accessing live Stripe credentials, customer PII, payment methods, webhooks, or production account settings.
---

# Stripe Data Analysis

## Safety Boundary

Use only sanitized CSVs, spreadsheets, or pasted tables. Do not request secret keys, webhook secrets, customer emails, card data, bank details, account IDs, tax IDs, or live dashboard access.

Do not cancel, refund, retry, modify, or create subscriptions from this public skill.

## Workflow

1. Identify the export type: subscriptions, invoices, payments, refunds, products, coupons, or events.
2. Normalize dates, currency, status labels, plan names, and customer grouping.
3. Calculate only from available fields:
   - gross revenue
   - refunds
   - net revenue
   - active subscriptions
   - churned subscriptions
   - failed payments
   - plan mix
   - cohort movement
4. Flag data gaps before drawing conclusions.
5. Produce a concise revenue or billing analysis with next checks.

## Output

Return:

- `metrics`
- `trend_summary`
- `cohort_or_plan_notes`
- `exceptions`
- `data_quality_notes`
- `questions_for_operator`
- `manual_followups`
