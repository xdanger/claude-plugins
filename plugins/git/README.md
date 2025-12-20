# Git Commands

Git slash commands for Gitmoji + Conventional Commits workflow.

## Installation

```bash
# Add marketplace
/plugin marketplace add xdanger/claude-plugins

# Install plugin
/plugin install git@xdanger-claude-marketplace
```

## Commands

| Command       | Description                                                 |
| ------------- | ----------------------------------------------------------- |
| `/git:commit` | Generate commit message with Gitmoji + Conventional Commits |

## Usage

```
/git:commit [issue_number]
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
