# Public Automation Skills

Sanitized Codex skills for content operations, growth analysis, ad-health review, billing review, data analysis, and backlink submission workflows.

This repository is intentionally **not** a production automation repo. It contains reusable agent instructions and public-safe operating patterns only.

## Skills

| Skill | What it is for |
| --- | --- |
| `wix-blog-draft-ops` | Turn a content idea into a Wix-ready draft packet. |
| `trend-signal-tracker` | Collect public trend signals and convert them into growth or content hypotheses. |
| `ads-health-monitor` | Review sanitized ad performance exports and flag anomalies. |
| `stripe-ops-review` | Analyze sanitized Stripe-like billing and subscription exports. |
| `growth-data-analysis` | Turn sanitized growth datasets into findings and next tests. |
| `backlink-submission-ops` | Find, qualify, and track public backlink or directory submissions. |

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
  wix-blog-draft-ops/
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
