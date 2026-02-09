# Lifeline Australia Notion Assistant - Team Reference

## About This Tool

This repository provides a command-line interface for interacting with Lifeline Australia's (LLA) Notion workspace. The Digital Product team uses Notion extensively for documentation, and this tool enables searching, fetching, and managing that content programmatically.

## Notion Workspace Access

This repo has access to LLA's Notion workspace via the Notion MCP plugin. Use the following tools:

- `mcp__plugin_Notion_notion__notion-search` - Search for pages/databases
- `mcp__plugin_Notion_notion__notion-fetch` - Fetch full page content by URL or ID
- `mcp__plugin_Notion_notion__notion-create-pages` - Create new pages
- `mcp__plugin_Notion_notion__notion-update-page` - Update existing pages

**Important:** These tools are deferred and must be loaded via `ToolSearch` before use:
```
ToolSearch query: "+notion fetch search"
```

## Key Notion Pages

### Digital Products Map
**URL:** https://www.notion.so/2edd91c9531880b682e2ed178c2c5f9f

Central documentation hub for LLA's digital products. 

### Product Documentation Pages (in Digital Product Wiki)
| Product | Home Page URL |
|---------|--------------|
| Service Finder | https://www.notion.so/c9fed4396188410d9d4c6400ee5064f7 |
| Support Finder | https://www.notion.so/2af407bf9b0f44ecb47cedce4f22529c |
| Shift Starter | https://www.notion.so/174d91c95318800eb44bde38a6114144 |
| Beyond Now | https://www.notion.so/521b0a980fb94dd28e056b82d6450a7a |
| 13 YARN | https://www.notion.so/8170a7d385424d9c8307fc9ad07de19d |
| CISS Tools | https://www.notion.so/2f0d91c9531880e686a5eaed5c3e0a2b |

### Projucts Database
**URL:** https://www.notion.so/1b029157de124cedbe571e0892a96f6e

Database tracking all digital products and projects. Note the intentional misspelling "Projucts" - this is the actual name used in Notion as a portmanteau of 'Product' and 'Project'.

## Key People

| Name | Role | Products |
|------|------|----------|
| Ben Ferrari | Product Lead | Service Finder, Support Finder, lifeline.org.au |
| Toby Reid | Tech Lead | All products |
| Satish Shrestha | Former Product Manager | Beyond Now, Shift Starter |
| Mark Manners | Product Manager | Shift Starter, Support Finder, CISS Tools |
| Dane Glerum | Former Head of Digital Product | 13 YARN oversight |
| Marcel Jacobs | Design Lead | Various products |
| Andy Hearne | UX Designer | Shift Starter |

## Common Acronyms & Terms

| Term | Meaning |
|------|---------|
| CS | Crisis Supporter (volunteer) |
| ISS | In-Shift Supervisor |
| CISS | Crisis In-Shift Supervisor tools |
| HS | Help Seeker (person calling/contacting Lifeline) |
| HAD/HADS | Human Assisted Digital Services (text/chat) |
| STS | Specialised Telephone Services (MensLine, SuicideLine, etc.) |
| L&D | Learning and Development |
| WFM | Workforce Management |
| Flippy Dippys | Paper-based referral lists |
| Midas | Project name for new lifeline.org.au platform |
| Zipper | Project name for Beyond Now |
| Unify | Project combining CISS Tools, Shift Starter, Support Finder |

## Working with Notion Content

### Search Tips
- Use semantic queries: "Service Finder infrastructure" rather than exact phrases
- Filter by date range for recent documents: `filters: { created_date_range: { start_date: "2025-01-01" } }`
- Search within a page using `page_url` parameter

### Fetching Pages
- Always fetch a page before updating to understand current structure
- Use the Notion-flavored Markdown spec (fetch `notion://docs/enhanced-markdown-spec` resource)

### Creating/Updating Pages
- Use `page_id` for parent when creating sub-pages
- For databases, fetch first to get the `data-source-url` (collection://...)
- Hyperlink to source documentation where possible

### Data Reliability
- Documents may not be regularly verified - prioritise newer information
- When information conflicts, use the most recent document
- Better to leave fields empty than hallucinate information

## External Systems

| System | Purpose | Access |
|--------|---------|--------|
| Jira | Task tracking (MIDAS project, Product Discovery) | lifelineaustralia.atlassian.net |
| Figma | Design files | figma.com |
| GitHub | Code repos (service-finder, support-finder) | github.com/lifelineau |
| Bitbucket | Code repos (lifeline.org.au, Beyond Now) | bitbucket.org/lifelineau |
| Sentry | Error monitoring | lifeline-au.sentry.io |
| Better Stack | Uptime monitoring | uptime.betterstack.com |
| Algolia | Search | dashboard.algolia.com |
| Sanity | CMS for Service/Support Finder | *.sanity.studio |

## Organisational Context

See `lla-context.md` for comprehensive organisational terminology, frameworks, and service definitions.
