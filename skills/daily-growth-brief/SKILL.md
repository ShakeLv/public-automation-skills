---
name: daily-growth-brief
description: Prepare a Slack-ready internal daily report from sanitized market monitoring, Google Ads, Stripe, growth, and content pipeline snapshots. Use when Codex needs to summarize daily movement without exposing private channels, webhooks, credentials, account IDs, customer PII, production dashboards, or live mutation steps.
---

# Daily Growth Brief

## Safety Boundary

Use sanitized summaries, exported tables, or public signals only. Do not include Slack webhooks, private channel IDs, account IDs, billing IDs, customer-level data, production dashboard URLs, credentials, cookies, or raw logs.

This public skill prepares a report. It does not post to Slack, change ads, modify billing systems, or reconcile production state unless the user explicitly moves to a private operational workflow.

## Safe Inputs

- sanitized market or SEO monitoring notes
- sanitized Google Ads movement summary
- sanitized Stripe revenue or subscription summary
- content pipeline status
- GitHub outreach status
- blockers or decisions needed

## What It Produces

A Slack-ready daily report with the day's meaningful changes, numbers worth watching, queued actions, blockers, and data quality notes.

## Workflow

1. Gather the day's safe inputs:
   - market or SEO trend highlights
   - Google Ads movement
   - Stripe revenue or subscription movement
   - content pipeline status
   - outreach status
   - blockers or decisions needed
2. Separate signal from noise. Keep only items that changed a decision, exposed a risk, or created a useful action.
3. Write the daily brief in this order:
   - headline
   - what changed
   - numbers worth watching
   - actions queued
   - asks or blockers
4. Keep the tone concise and operational. Avoid long analysis unless a decision depends on it.
5. Add safety notes when data was missing, delayed, sampled, or manually estimated.

## Output

Return:

- `slack_ready_brief`
- `metric_snapshot`
- `market_signals`
- `action_queue`
- `blockers`
- `data_quality_notes`
