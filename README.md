# Lifeline Australia Notion Assistant

A prompt and some context to help AIs like Claude use Lifeline Australia's Notion workspace to search, fetch, and manage documentation.

If using another AI agent, just rename CLAUDE.md to AGENTS.md.

## Overview

This repository provides a command-line interface for working with LLA's Notion workspace. It uses the Notion MCP plugin to enable searching pages, fetching content, and creating/updating documentation.

## Notion Integration

This tool integrates with LLA's Notion workspace via the Notion MCP plugin. Available tools include:

- **Search**: `mcp__plugin_Notion_notion__notion-search` - Search for pages and databases
- **Fetch**: `mcp__plugin_Notion_notion__notion-fetch` - Retrieve full page content
- **Create**: `mcp__plugin_Notion_notion__notion-create-pages` - Create new pages
- **Update**: `mcp__plugin_Notion_notion__notion-update-page` - Update existing pages

> **Note**: These tools are deferred and must be loaded via `ToolSearch` before use.

### Key Notion Pages

| Resource | Description |
|----------|-------------|
| [Digital Products Map](https://www.notion.so/2edd91c9531880b682e2ed178c2c5f9f) | Central documentation hub for LLA's digital products |
| [Projucts Database](https://www.notion.so/1b029157de124cedbe571e0892a96f6e) | Database tracking all digital products and projects |

### Product Documentation

| Product | Documentation URL |
|---------|-------------------|
| Service Finder | https://www.notion.so/c9fed4396188410d9d4c6400ee5064f7 |
| Support Finder | https://www.notion.so/2af407bf9b0f44ecb47cedce4f22529c |
| Shift Starter | https://www.notion.so/174d91c95318800eb44bde38a6114144 |
| Beyond Now | https://www.notion.so/521b0a980fb94dd28e056b82d6450a7a |
| 13 YARN | https://www.notion.so/8170a7d385424d9c8307fc9ad07de19d |
| CISS Tools | https://www.notion.so/2f0d91c9531880e686a5eaed5c3e0a2b |

## Documentation

- **[CLAUDE.md](./CLAUDE.md)** - Detailed guide for working with Notion, including search tips, common acronyms, and external systems
- **[lla-context.md](./lla-context.md)** - Comprehensive glossary of Lifeline Australia terminology, frameworks, and service definitions
