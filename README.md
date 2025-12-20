# Claude Code Plugins Marketplace

A personal, public collection of Claude Code plugins for cross-project sharing and management.

## Available Plugins

| Plugin                     | Description                                                   | Type |
| -------------------------- | ------------------------------------------------------------- | ---- |
| [notion](./plugins/notion) | Notion MCP server using STDIO mode (workaround for OAuth bug) | MCP  |
| [github](./plugins/github) | GitHub MCP server via GitHub Copilot API                      | MCP  |

## Structure

```
.
├── .claude-plugin/
│   └── marketplace.json    # Plugin registry
└── plugins/
    ├── github/
    │   ├── .mcp.json       # MCP server config
    │   ├── plugin.json     # Plugin metadata
    │   └── README.md
    └── notion/
        ├── .mcp.json
        ├── plugin.json
        └── README.md
```

## Usage

### Option 1: Copy MCP config

Copy the `.mcp.json` content to your project's `.mcp.json` or global `~/.claude/.mcp.json`.

### Option 2: Reference via symlink

```bash
ln -s /path/to/claude-plugins/plugins/notion/.mcp.json ~/.claude/mcp/notion.json
```

## Environment Variables

Each plugin requires specific environment variables. See individual plugin READMEs for details:

- **notion**: `NOTION_TOKEN`
- **github**: `GITHUB_PAT`

## License

MIT
