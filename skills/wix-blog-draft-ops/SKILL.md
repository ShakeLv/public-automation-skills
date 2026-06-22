---
name: wix-blog-draft-ops
description: Prepare sanitized Wix blog draft workflows from public topic inputs, outlines, markdown drafts, SEO metadata, and upload checklists. Use when Codex needs to turn a content idea into a Wix-ready draft plan without accessing live credentials, private APIs, production CMS data, or unpublished internal assets.
---

# Wix Blog Draft Ops

## Safety Boundary

Work only with user-provided drafts, public references, and sanitized exports. Do not request or expose API keys, cookies, account IDs, CMS tokens, local paths, customer data, or unpublished production content.

If publishing, scheduling, or editing a live site is required, stop and ask for an explicit production-safe workflow outside this public skill.

## Workflow

1. Clarify the target audience, search intent, primary keyword, and desired call to action.
2. Draft a compact outline with title, slug, excerpt, headings, FAQ candidates, and internal-link suggestions.
3. Produce Wix-ready markdown or rich-text sections. Keep copy skimmable and avoid filler.
4. Prepare metadata: SEO title, meta description, canonical intent, image alt text, and tags.
5. Run a final public-safe checklist:
   - No credentials or internal URLs.
   - No private customer names or account identifiers.
   - No local filesystem paths.
   - No claims that require private proof unless the user supplies public evidence.

## Output

Return a draft packet:

- `title`
- `slug`
- `excerpt`
- `seo_title`
- `meta_description`
- `tags`
- `body`
- `manual_wix_steps`
- `safety_notes`
