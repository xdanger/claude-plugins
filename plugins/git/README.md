# Git Commands

Git slash commands for Gitmoji + Conventional Commits workflow and GitHub Issue lifecycle management.

## Installation

```bash
# Add marketplace
/plugin marketplace add xdanger/claude-plugins

# Install plugin
/plugin install git@xdanger-claude-marketplace
```

## Commands

| Command                 | Description                                              |
| ----------------------- | -------------------------------------------------------- |
| `/git:commit`           | Generate commit message (Gitmoji + Conventional Commits) |
| `/git:issue-create`     | Create a new GitHub Issue                                |
| `/git:issue-plan`       | Explore solution for an issue                            |
| `/git:issue-test`       | Generate tests for an issue                              |
| `/git:issue-review`     | Code review for an issue                                 |
| `/git:issue-commit`     | Commit with issue reference                              |
| `/git:squash-and-merge` | Squash and merge a PR                                    |

## Usage

```bash
# Simple commit
/git:commit

# Issue workflow
/git:issue-create <description>
/git:issue-plan <issue_number>
/git:issue-test <issue_number>
/git:issue-review <issue_number>
/git:issue-commit <issue_number>

# PR merge
/git:squash-and-merge <pr_number>
```

## Issue Lifecycle

1. **Create Issue** → `/git:issue-create`
2. **Plan Solution** → `/git:issue-plan`
3. **Generate Tests** → `/git:issue-test`
4. **Implement & Commit** → `/git:issue-commit`
5. **Code Review** → `/git:issue-review`
6. **Merge PR** → `/git:squash-and-merge`
