---
name: backlink-submission-ops
description: Find, qualify, and track GitHub-first outreach opportunities such as awesome lists, AI tool repositories, developer directories, and community resource pages. Use when Codex needs to prepare pull request or submission materials without exposing private accounts, credentials, production analytics, or non-public company data.
---

# GitHub Outreach Ops

## Safety Boundary

Use public pages and public product descriptions only. Do not submit forms, open pull requests, send emails, or post comments unless the user explicitly approves the exact destination and content.

Do not expose private metrics, customer names, internal roadmap, tracking links with private parameters, credentials, or account-specific screenshots.

## Safe Inputs

- public GitHub repository URLs
- public product descriptions
- public submission rules
- sanitized outreach status tables

## What It Produces

A qualified outreach list, recommended submission path, public-safe PR or listing copy, required assets, and a status table.

## Workflow

1. Define the product category, audience, and acceptable outreach types.
2. Find public opportunities, GitHub first:
   - awesome lists
   - AI tool repositories
   - developer resource directories
   - community resource pages
   - product directories when they clearly fit the same audience
3. Score each opportunity:
   - relevance
   - authority
   - submission friction
   - policy fit
   - expected traffic quality
4. Prepare safe PR or submission copy with no private claims.
5. Track status: found, qualified, prepared, PR opened, submitted, accepted, rejected, follow-up.

## Output

Return:

- `opportunities`
- `qualification_notes`
- `submission_copy`
- `required_assets`
- `approval_needed`
- `tracking_table`
