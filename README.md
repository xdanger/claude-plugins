# Claude Code Plugins Marketplace

A personal, public collection of Claude Code plugins for cross-project sharing and management.

## Available Plugins

| Plugin                     | Description                                                   | Type    |
| -------------------------- | ------------------------------------------------------------- | ------- |
| [notion](./plugins/notion) | Notion MCP server using STDIO mode (workaround for OAuth bug) | MCP     |
| [github](./plugins/github) | GitHub MCP server via GitHub Copilot API                      | MCP     |
| [git](./plugins/git)       | Git slash commands (Gitmoji + Conventional Commits)           | Command |

## Installation

```bash
# Add this marketplace
/plugin marketplace add xdanger/claude-plugins

# Install individual plugins
/plugin install notion@xdanger-claude-marketplace
/plugin install github@xdanger-claude-marketplace
/plugin install git@xdanger-claude-marketplace
```

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
    ├── git/
    │   ├── commands/
    │   │   └── commit.md   # /git:commit
    │   ├── plugin.json
    │   └── README.md
    └── notion/
        ├── .mcp.json
        ├── plugin.json
        └── README.md
```

## Environment Variables

MCP plugins require specific environment variables. See individual plugin READMEs:

- **notion**: `NOTION_TOKEN`
- **github**: `GITHUB_PAT`

## License

MIT
