# Claude Code Plugins Marketplace

## Project Overview

This repository contains reusable Claude Code plugins (Skills, Slash Commands, Hooks, MCP configurations) for cross-project sharing.

## Directory Structure

- `skills/` - Skill definitions (`.md` files with prompts and configurations)
- `commands/` - Slash command implementations
- `hooks/` - Hook scripts for event-driven automation
- `mcp/` - MCP server configurations

## Development Guidelines

### Skills

- One skill per file
- Clear, focused purpose
- Include usage examples in comments
- Use descriptive file names: `<action>-<target>.md`

### Naming Conventions

- Files: `kebab-case`
- Directories: lowercase
- Skills: `verb-noun` pattern (e.g., `git-commit`, `issue-review`)

### Testing

Before adding a new plugin:

1. Test in a real project context
2. Verify no conflicts with existing plugins
3. Document any dependencies

## Publishing

Plugins in this repo can be referenced via GitHub raw URLs or symlinked to local Claude Code configurations.
