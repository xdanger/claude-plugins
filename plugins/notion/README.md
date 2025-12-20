# Notion MCP Server

Notion MCP server configuration using STDIO mode with `@notionhq/notion-mcp-server`.

## Prerequisites

1. Create a Notion Integration at https://www.notion.so/profile/integrations
2. Set environment variable:
   ```bash
   export NOTION_TOKEN="ntn_xxxxxxxxxxxxxx"
   ```
3. Grant Integration access to pages/databases in Notion (page `...` menu → Connections)

## Why STDIO instead of OAuth HTTP?

The official Notion plugin uses OAuth HTTP mode (`https://mcp.notion.com/mcp`), but there's a known issue where the OAuth flow succeeds but returns an invalid token (401). STDIO mode with Integration Token is more reliable.
