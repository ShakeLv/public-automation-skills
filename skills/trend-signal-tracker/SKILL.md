---
name: trend-signal-tracker
description: Collect and summarize public trend signals from search results, social discussions, directories, changelogs, GitHub repositories, and news-like sources. Use when Codex needs to identify public growth or content opportunities without using private analytics, paid account data, or production credentials.
---

# Trend Signal Tracker

## Safety Boundary

Use public sources or user-provided sanitized exports only. Do not use private dashboards, hidden community logs, customer data, personal inboxes, paid tools, or authenticated accounts unless the user explicitly provides a sanitized export.

## Workflow

1. Define the market, audience, and time window.
2. Gather signals from public sources:
   - search results and related queries
   - GitHub repositories and issues
   - product directories
   - public community posts
   - changelogs and release notes
3. Cluster signals into themes. Separate durable demand from short-lived noise.
4. Score each theme:
   - audience relevance
   - urgency
   - content angle
   - distribution path
   - evidence quality
5. Produce suggested next actions: article ideas, landing page tests, outreach targets, or monitoring queries.

## Output

Return:

- `top_signals`
- `evidence`
- `why_it_matters`
- `content_angles`
- `growth_tests`
- `risks_or_unknowns`
