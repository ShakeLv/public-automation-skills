# Public Automation Skills

Sanitized Codex skills for four public-safe automation workflows: content production, GitHub outreach, data management, and internal daily briefs.

This repository is intentionally **not** a production automation repo. It contains reusable agent instructions and public-safe operating patterns only.

The goal is simple: someone should be able to copy a skill folder, give it public or sanitized inputs, and get a useful output without knowing the original private environment.

## Workflow Map

| Workflow | Skills | What it is for |
| --- | --- | --- |
| Content production pipeline | `trend-signal-tracker`, `wix-blog-pipeline` | Monitor SEO/AI trend signals, select topics, build content briefs, and prepare Wix-ready publishing assets. |
| GitHub outreach | `backlink-submission-ops` | Find relevant GitHub awesome lists, directories, and community repositories, then prepare safe PR/submission copy. |
| Data management | `ads-health-monitor`, `stripe-ops-review`, `growth-data-analysis` | Review sanitized Google Ads, Stripe, and growth exports, then turn data into findings and action queues. |
| Internal daily brief | `daily-growth-brief` | Turn market signals, ad movement, revenue signals, and growth notes into a Slack-ready daily report. |

## Quick Start

Pick the workflow first, then load the matching skill folder.

```text
Use trend-signal-tracker to review these public AI/SEO trend candidates and pick five article angles.
```

```text
Use backlink-submission-ops to qualify these GitHub awesome-list repositories and prepare safe PR copy.
```

```text
Use ads-health-monitor and stripe-ops-review to review these sanitized exports and prepare today's action queue.
```

```text
Use daily-growth-brief to turn today's market, Ads, Stripe, content, and outreach snapshots into a Slack-ready report.
```

## Input And Output Shape

| Workflow | Safe input | Output |
| --- | --- | --- |
| Content production pipeline | Public trend URLs, sanitized topic snapshots, article outlines | Topic scores, content angles, Wix-ready publishing package |
| GitHub outreach | Public repository URLs, public product description, submission rules | Qualified targets, PR/submission copy, tracking table |
| Data management | Sanitized Google Ads, Stripe, or growth exports | Metric snapshot, anomalies, likely causes, proposed actions |
| Internal daily brief | Sanitized daily notes from market monitoring, ads, revenue, content, and outreach | Slack-ready brief, action queue, blockers, data quality notes |

## Skills

| Skill | What it is for |
| --- | --- |
| `trend-signal-tracker` | Monitor public SEO and AI trend feeds, dedupe topics, score opportunities, and prepare content plans. |
| `wix-blog-pipeline` | Turn a content idea into a Wix-ready publishing package. |
| `ads-health-monitor` | Prepare sanitized Google Ads management audits and proposed action queues. |
| `stripe-ops-review` | Analyze sanitized Stripe revenue, subscription, churn, and cohort exports. |
| `growth-data-analysis` | Turn sanitized growth datasets into findings and next tests. |
| `backlink-submission-ops` | Find, qualify, and track GitHub-first outreach and public backlink submissions. |
| `daily-growth-brief` | Produce Slack-ready internal daily reports from sanitized market, ads, revenue, and growth snapshots. |

## Safety Model

These skills are designed for public use and portfolio display.

They do not contain:

- API keys, tokens, cookies, OAuth secrets, or credentials
- production account IDs, customer IDs, billing IDs, or dashboard links
- private database schemas, internal endpoints, or server paths
- customer PII, emails, payment details, raw event logs, or user-level identifiers
- production scripts that can mutate live systems

Each skill assumes one of three safe inputs:

1. public web information
2. user-provided sanitized exports
3. manually pasted summaries with sensitive fields removed

## Repository Structure

```text
skills/
  ads-health-monitor/
  backlink-submission-ops/
  growth-data-analysis/
  stripe-ops-review/
  trend-signal-tracker/
  wix-blog-pipeline/
  daily-growth-brief/
```

Each skill folder contains:

- `SKILL.md` for agent-facing instructions
- `agents/openai.yaml` for display metadata

## Usage

Copy any folder under `skills/` into your Codex skills directory, or reference the folder directly when asking an agent to follow that workflow.

Example:

```text
Use the growth-data-analysis skill to inspect this sanitized acquisition export and summarize the top three findings.
```

## Publication Note

This repo is public by design. If you adapt these skills for private production workflows, keep production connectors, credentials, account IDs, and live mutation steps in a private repository.
