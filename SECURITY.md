# Security

This repository must remain public-safe.

## Do Not Commit

- credentials, secrets, cookies, API keys, OAuth tokens, or webhook secrets
- live account IDs, customer IDs, campaign IDs, billing IDs, or dashboard URLs
- internal endpoints, database schemas, server paths, or local filesystem paths
- customer PII, payment data, emails, IP addresses, device IDs, or raw user logs
- scripts that directly mutate live production systems

## Allowed Content

- sanitized workflow descriptions
- public-source research steps
- schemas with fictional field names
- example prompts that use synthetic data
- read-only analysis patterns

## Review Checklist

Before publishing changes:

1. Search for obvious secret patterns.
2. Search for local absolute paths.
3. Search for private domain names or internal hostnames.
4. Confirm every workflow is read-only unless it explicitly asks for human approval.
5. Confirm examples use synthetic or public data.
