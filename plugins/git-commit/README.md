# Git Commit Command

Slash command that generates commit messages following Gitmoji + Conventional Commits format.

## Usage

```
/git-commit [issue_number]
```

## Installation

Copy or symlink to your Claude commands directory:

```bash
# User-level (all projects)
ln -s /path/to/claude-plugins/plugins/git-commit/commands/git-commit.md ~/.claude/commands/

# Project-level
ln -s /path/to/claude-plugins/plugins/git-commit/commands/git-commit.md .claude/commands/
```

## Features

- Analyzes staged changes via `git diff --cached`
- Fetches issue details if issue number provided
- Generates commit message with:
  - Gitmoji prefix
  - Conventional Commits format (`type(scope): description`)
  - Breaking change notation
  - Issue reference

## Example Output

```
✨ feat(auth)!: support user login (#1234)

- ✨ add POST /v1/login endpoint
- ✨ introduce jwt for tokens
- ✅ add login tests

💥 BREAKING CHANGE:
- rename `AuthError` to `LoginError`
```
