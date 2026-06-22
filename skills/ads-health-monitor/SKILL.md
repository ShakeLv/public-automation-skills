---
name: ads-health-monitor
description: Review sanitized advertising performance exports for spend, conversion, attribution, campaign, keyword, location, and anomaly patterns. Use when Codex needs to inspect CSV or spreadsheet-like ad data without connecting to live ad accounts, changing bids, reading production credentials, or modifying campaigns.
---

# Ads Health Monitor

## Safety Boundary

Analyze sanitized exports only. Never change campaigns, bids, budgets, targeting, conversion goals, tags, or account settings from this skill. Never expose customer IDs, account IDs, billing IDs, API keys, OAuth tokens, tracking templates, or internal dashboards.

## Workflow

1. Confirm the export schema and date range.
2. Check basic health:
   - spend trend
   - conversion trend
   - CPA or ROAS movement
   - impression and click anomalies
   - campaign or keyword outliers
3. Compare segments when available:
   - campaign
   - channel
   - geography
   - device
   - search term or keyword
4. Separate observation from recommendation. Do not overreact to small samples.
5. Produce a read-only action plan. Mark any live-account change as requiring explicit human review.

## Output

Return:

- `summary`
- `anomalies`
- `likely_causes`
- `checks_to_run_next`
- `recommended_actions`
- `do_not_change_without_review`
