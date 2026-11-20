---
name: blazly-seo-geo
description: Run Blazly SEO, GEO and AEO agents from Cursor. Use when the user asks for a site audit, keyword research, ranking opportunities, backlinks, competitor research, AI visibility or brand sentiment, Search Console or GA4 data, writing or humanizing a blog article, publishing a post, or scheduling recurring marketing work.
---

# Blazly SEO and GEO agents

Blazly tools come from the `blazly` MCP server. Each connection is tied to one Blazly project, which already knows the website, brand and connected integrations.

## Before running agents

- Call `get_project` first when you need the project's website, brand or which integrations are connected.
- Tools that take a website default to the project website, so omit `website_url` unless the user names a different site.

## Picking a tool

| User wants | Tool |
| --- | --- |
| Technical and on-page SEO issues | `site_audit` |
| Volume and difficulty for a keyword | `keyword_research` |
| Keywords the site can realistically rank for | `find_ranking_opportunities` |
| Current Google rankings for a domain | `serp_tracking` |
| Link building prospects | `find_backlinks` |
| Comparison with competitors | `competitor_research` |
| How the site shows up in AI answers | `ai_visibility` |
| How AI assistants describe the brand | `brand_sentiment` |
| How often a prompt is asked in AI assistants | `prompt_research` |
| Real Search Console or GA4 numbers | `search_console_and_analytics` |
| A long-form SEO or AEO article | `write_seo_blog` |
| An article built to be cited by AI assistants | `write_geo_blog` |
| Make copy read more naturally | `humanize_text` |
| Google Business Profile and local SEO | `local_seo_audit` |
| Companies and contacts for an ideal customer profile | `find_b2b_leads` |
| Put an article live on the site | `publish_post` |
| Run work later or on a repeat | `schedule_task`, `list_scheduled_tasks`, `cancel_scheduled_task` |

## Long-running tasks

Audits and blog writers can take several minutes. When a tool returns `status: "running"` with a `task_id`, tell the user it is in progress, then call `get_task_result` with that `task_id` every 30 to 60 seconds until `status` is `done` or `failed`.

## Publishing

- `publish_post` needs WordPress, Webflow or a custom website connected in Blazly. If none is connected, ask the user to connect one under Integrations in Blazly.
- Pass the `article` returned by `write_seo_blog` or `write_geo_blog` (`title`, `html`, `meta_description`, `slug`).
- Confirm with the user before publishing live; use `status: "draft"` when they haven't asked to go live.

## Credits

Every agent run spends Blazly credits from the user's plan, the same as in the Blazly app. Avoid re-running an agent just to re-read a result; use `get_task_result` instead.
