# Public Automation Skills

[English](README.md) / [中文](README.zh-CN.md)

Sanitized Codex skills for four public-safe automation workflows: content production, GitHub outreach, data management, and internal daily briefs.

This repository is intentionally **not** a production automation repo. It contains reusable agent instructions and public-safe operating patterns only.

The goal is simple: someone should be able to copy a skill folder, give it public or sanitized inputs, and get a useful output without knowing the original private environment.

## Workflows

### Content Production Pipeline

Use this workflow to turn public SEO and AI trend signals into publishable content assets.

Skills: `trend-signal-tracker`, `wix-blog-pipeline`

Safe inputs: public trend URLs, sanitized topic snapshots, article outlines, public reference links.

Output: ranked topic ideas, content angles, SEO metadata, and a Wix-ready publishing package.

### GitHub Outreach

Use this workflow to find GitHub-first distribution opportunities and prepare public-safe submission materials.

Skill: `github-outreach-ops`

Safe inputs: public repository URLs, public product descriptions, awesome-list rules, submission guidelines.

Output: qualified targets, recommended submission path, PR or listing copy, and a tracking table.

### Data Management

Use this workflow to review acquisition, revenue, and billing data without connecting to live production systems.

Skills: `ads-health-monitor`, `stripe-ops-review`, `growth-data-analysis`

Safe inputs: sanitized Google Ads exports, sanitized Stripe exports, aggregate growth tables, manually summarized metrics.

Output: metric snapshots, anomalies, likely causes, data quality notes, and proposed action queues.

### Internal Daily Brief

Use this workflow to turn daily market, ads, revenue, content, and outreach movement into a Slack-ready report.

Skill: `daily-growth-brief`

Safe inputs: sanitized daily notes, public market signals, aggregate Ads/Stripe movement, content status, outreach status.

Output: Slack-ready brief, numbers worth watching, queued actions, blockers, and data quality notes.

## Quick Start

Pick the workflow first, then load the matching skill folder.

```text
Use trend-signal-tracker to review these public AI/SEO trend candidates and pick five article angles.
```

```text
Use github-outreach-ops to qualify these GitHub awesome-list repositories and prepare safe PR copy.
```

```text
Use ads-health-monitor and stripe-ops-review to review these sanitized exports and prepare today's action queue.
```

```text
Use daily-growth-brief to turn today's market, Ads, Stripe, content, and outreach snapshots into a Slack-ready report.
```

## Skills

| Skill | What it is for |
| --- | --- |
| `trend-signal-tracker` | Monitor public SEO and AI trend feeds, dedupe topics, score opportunities, and prepare content plans. |
| `wix-blog-pipeline` | Turn a content idea into a Wix-ready publishing package. |
| `ads-health-monitor` | Prepare sanitized Google Ads management audits and proposed action queues. |
| `stripe-ops-review` | Analyze sanitized Stripe revenue, subscription, churn, and cohort exports. |
| `growth-data-analysis` | Turn sanitized growth datasets into findings and next tests. |
| `github-outreach-ops` | Find, qualify, and track GitHub-first outreach opportunities. |
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
  github-outreach-ops/
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
