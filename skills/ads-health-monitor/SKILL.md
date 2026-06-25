---
name: ads-health-monitor
description: Audit and manage sanitized Google Ads performance workflows, including campaign health, search terms, conversion movement, spend anomalies, and proposed changes. Use when Codex needs to inspect exported ad data or prepare a Google Ads management plan without accessing live accounts, credentials, customer IDs, or production settings.
---

# Google Ads Management

## Safety Boundary

Use sanitized exports only. Never expose customer IDs, account IDs, billing details, OAuth tokens, conversion IDs, tracking templates, internal dashboards, or production screenshots.

Do not change bids, budgets, targeting, conversion goals, tags, imports, scripts, or campaigns from this public skill. Any live-account change must be written as a proposed action requiring human approval.

## Safe Inputs

- sanitized Google Ads exports
- aggregate campaign, search term, location, or device tables
- manually pasted daily movement summaries
- public landing page or offer context

## What It Produces

An account health review with anomalies, waste or opportunity areas, likely causes, and a proposed action queue that requires human approval before any live change.

## Workflow

1. Confirm the export schema, date range, currency, and attribution window.
2. Check account health:
   - spend trend
   - conversion trend
   - CPA or ROAS movement
   - campaign outliers
   - search term waste
   - location or device anomalies
3. Diagnose likely causes:
   - traffic mix changed
   - conversion tracking shifted
   - budget limited
   - learning phase
   - query quality changed
   - landing page or offer mismatch
4. Write proposed actions as a review queue:
   - pause or exclude
   - split or merge
   - adjust budget
   - update keyword/search term rules
   - inspect conversion setup
5. Separate facts, interpretation, and suggested actions.

## Output

Return:

- `account_snapshot`
- `anomalies`
- `waste_or_opportunity`
- `likely_causes`
- `proposed_actions`
- `requires_human_approval`
