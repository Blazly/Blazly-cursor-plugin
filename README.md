# Blazly for Cursor

Run Blazly's SEO, GEO and AEO agents from Cursor: site audits, keyword research, ranking opportunities, backlinks, competitor research, AI visibility, brand sentiment, Search Console and GA4 insights, blog writing, and publishing to WordPress, Webflow or your own site.

## What's included

- **MCP server** (`mcp.json`): connects Cursor to Blazly at `https://app.blazly.ai/mcp`.
- **Skill** (`skills/blazly-seo-geo`): tells the agent which Blazly tool fits each request, how to wait for long-running tasks and how to publish safely.

## Requirements

- A Blazly account on the Basic plan or above ([sign up](https://app.blazly.ai)).
- A project in Blazly with your website.
- A Blazly API key for that project.

## Setup

1. In Blazly, open your project and go to **Connect AI tools**.
2. Click **Create key** and copy it. The key starts with `blz_` and is shown only once.
3. Install the Blazly plugin from the Cursor Marketplace.
4. In the Cursor dashboard, open **Plugins**, find Blazly, click **Configure**, and paste the key into **Blazly API key**.
5. In Cursor, make sure the Blazly MCP server is turned on.

Each key is tied to one Blazly project. To work on another project, create a key in that project and update the plugin configuration.

## Example prompts

- "Run a full SEO audit on my site and summarize the top fixes by impact."
- "Find realistic ranking opportunities for my site around invoicing software."
- "How does my site show up in AI answers for our main product category?"
- "Write a GEO article on 'free generative engine optimization tool' and publish it to WordPress as a draft."
- "Which Search Console queries lost the most clicks in the last 28 days?"
- "Schedule a weekly keyword check for my main topic every Monday at 9am."

## Tools

| Tool | What it does |
| --- | --- |
| `get_project` | Shows the connected project: website, brand and integrations |
| `keyword_research` | Volume, difficulty, CPC, trend and related keywords |
| `site_audit` | Technical and on-page SEO audit (200+ checks) |
| `write_seo_blog` | Long-form SEO/AEO article in your brand voice |
| `write_geo_blog` | Article built to be cited by AI assistants |
| `humanize_text` | Rewrites copy so it reads naturally |
| `find_ranking_opportunities` | Winnable long-tail keywords |
| `find_backlinks` | Editorial backlink prospects |
| `serp_tracking` | Top Google rankings for a domain |
| `ai_visibility` | Presence in Google AI Overview, ChatGPT, Claude, Gemini and Grok |
| `brand_sentiment` | How AI assistants describe your brand |
| `competitor_research` | Competitors vs your site on SEO and AI visibility |
| `prompt_research` | AI-search volume for a prompt |
| `local_seo_audit` | Google Business Profile and local SEO checklist |
| `find_b2b_leads` | Companies and contacts for an ideal customer profile |
| `search_console_and_analytics` | Answers from your Search Console and GA4 data |
| `get_task_result` | Result of a long-running task |
| `publish_post` | Publishes to WordPress, Webflow or a custom site |
| `schedule_task` | Schedules work once, daily or weekly |
| `list_scheduled_tasks` | Lists scheduled tasks |
| `cancel_scheduled_task` | Cancels a scheduled task |

Agent runs use Blazly credits from your plan, the same as in the Blazly app. Long tasks return a `task_id`; the agent checks back with `get_task_result` until the result is ready.

## Security

Your API key is stored in your Cursor plugin configuration, never in this repository. Revoke a key at any time in Blazly under **Connect AI tools**.

## Support

- Website: [blazly.ai](https://www.blazly.ai)
- Email: [jerry@blazly.ai](mailto:jerry@blazly.ai)

## License

MIT
