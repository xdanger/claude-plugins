# Claude Code Plugins Marketplace

A personal, public collection of Claude Code plugins for cross-project sharing and management.

## Available Plugins

| Plugin                             | Description                                                   | Type    |
| ---------------------------------- | ------------------------------------------------------------- | ------- |
| [notion](./plugins/notion)         | Notion MCP server using STDIO mode (workaround for OAuth bug) | MCP     |
| [github](./plugins/github)         | GitHub MCP server via GitHub Copilot API                      | MCP     |
| [git-commit](./plugins/git-commit) | Slash command for Gitmoji + Conventional Commits              | Command |

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
    ├── git-commit/
    │   ├── commands/
    │   │   └── git-commit.md   # Slash command
    │   ├── plugin.json
    │   └── README.md
    └── notion/
        ├── .mcp.json
        ├── plugin.json
        └── README.md
```

## Usage

### MCP Plugins

Copy the `.mcp.json` content to your project's `.mcp.json` or global `~/.claude/.mcp.json`.

### Slash Commands

Symlink to your commands directory:

```bash
# User-level (all projects)
ln -s /path/to/claude-plugins/plugins/git-commit/commands/git-commit.md ~/.claude/commands/

# Project-level
ln -s /path/to/claude-plugins/plugins/git-commit/commands/git-commit.md .claude/commands/
```

## Environment Variables

MCP plugins require specific environment variables. See individual plugin READMEs:

- **notion**: `NOTION_TOKEN`
- **github**: `GITHUB_PAT`

## License

MIT
