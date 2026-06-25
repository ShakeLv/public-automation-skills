---
name: growth-data-analysis
description: Analyze sanitized growth datasets such as acquisition, activation, retention, content, referral, funnel, revenue, and cohort exports. Use when Codex needs to turn CSV or spreadsheet-like data into findings, charts, hypotheses, and next actions without reading production databases or private analytics systems.
---

# Growth Data Analysis

## Safety Boundary

Work from sanitized files or pasted tables. Do not connect to production databases, warehouses, analytics tools, internal APIs, or private dashboards. Do not expose user-level identifiers, emails, IP addresses, device IDs, payment identifiers, or raw event logs.

## Safe Inputs

- sanitized CSV or spreadsheet exports
- pasted aggregate tables
- public benchmark tables
- manually summarized growth metrics

## What It Produces

A concise analysis with data quality notes, key findings, supporting tables, interpretation, next tests, and caveats.

## Workflow

1. State the question in one sentence.
2. Inspect the schema, row count, date range, missing values, and obvious duplicates.
3. Choose the smallest analysis that answers the question:
   - funnel drop-off
   - cohort retention
   - channel comparison
   - content performance
   - revenue movement
   - anomaly scan
4. Separate metric movement from interpretation.
5. Return findings with confidence levels and next experiments.

## Output

Return:

- `question`
- `data_notes`
- `key_findings`
- `charts_or_tables`
- `interpretation`
- `next_tests`
- `caveats`
