---
name: trend-signal-tracker
description: Monitor public SEO and AI trend feeds, dedupe topics, score opportunities, and prepare content or growth actions from sanitized snapshots. Use when Codex needs to run an AI-hotspot or SEO trend-monitor workflow without exposing private APIs, cloud storage, CMS IDs, production paths, or credentials.
---

# SEO Trend Monitor

## Safety Boundary

Use public pages, public APIs, or user-provided sanitized snapshots only. Do not expose live API endpoints, cloud bucket names, CMS post IDs, account IDs, local paths, cookies, tokens, or production logs.

Do not publish, claim, modify, or reconcile live production state from this public skill. Produce a plan or sanitized output packet only.

## Workflow

1. Load trend candidates from a public source or sanitized snapshot.
2. Normalize each candidate:
   - title
   - source URL
   - source type
   - timestamp
   - short summary
   - product or market angle
3. Dedupe against prior public topics. Treat close paraphrases as the same topic.
4. Score each candidate:
   - relevance to target audience
   - recency
   - evidence quality
   - search or social demand
   - content angle
   - distribution fit
5. Select the best topics and generate a publish-ready planning packet:
   - headline angle
   - keyword
   - slug
   - article thesis
   - supporting sources
   - risk notes
6. Return status in a table. Mark topics as `candidate`, `selected`, `drafted`, `published`, `skipped`, or `failed`.

## Output

Return:

- `top_topics`
- `dedupe_notes`
- `scores`
- `content_angles`
- `distribution_plan`
- `status_table`
- `safety_notes`
