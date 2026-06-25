---
name: wix-blog-pipeline
description: Prepare sanitized Wix blog publishing workflows from public topic inputs, article outlines, markdown content, SEO metadata, and upload checklists. Use when Codex needs to turn a content idea into a Wix-ready publishing package without accessing live credentials, private APIs, production CMS data, or unpublished internal assets.
---

# Wix Blog Pipeline

## Safety Boundary

Work only with user-provided content, public references, and sanitized exports. Do not request or expose API keys, cookies, account IDs, CMS tokens, local paths, customer data, or unpublished production content.

If publishing, scheduling, or editing a live site is required, stop and ask for an explicit production-safe workflow outside this public skill.

## Safe Inputs

- public topic or keyword
- article outline or source notes
- public reference URLs
- markdown content
- desired call to action

## What It Produces

A Wix-ready publishing package with title, slug, excerpt, SEO metadata, tags, body content, manual upload steps, and safety notes.

## Workflow

1. Clarify the target audience, search intent, primary keyword, and desired call to action.
2. Prepare a compact article structure with title, slug, excerpt, headings, FAQ candidates, and internal-link suggestions.
3. Produce Wix-ready markdown or rich-text sections. Keep copy skimmable and avoid filler.
4. Prepare metadata: SEO title, meta description, canonical intent, image alt text, and tags.
5. Run a final public-safe checklist:
   - No credentials or internal URLs.
   - No private customer names or account identifiers.
   - No local filesystem paths.
   - No claims that require private proof unless the user supplies public evidence.

## Output

Return a publishing package:

- `title`
- `slug`
- `excerpt`
- `seo_title`
- `meta_description`
- `tags`
- `body`
- `manual_wix_steps`
- `safety_notes`
