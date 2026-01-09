---
allowed-tools: Bash(git add:*), Bash(git status:*), Bash(git commit:*), Bash(gh:issue view)
description: Create a git commit with Gitmoji and Conventional Commits
---

## Context

- Current git status: !`git status`
- Current git diff (staged and unstaged changes): !`git diff HEAD`
- Current branch: !`git branch --show-current`
- Recent commits: !`git log --oneline -10`

## Your task

Based on the above changes, create a single git commit following Gitmoji and Conventional Commits specification.

### Execution Steps

1. Run `git diff --cached` to review all staged changes (ignore unstaged files)
2. If `$ARGUMENTS` is provided, run `gh issue view $ARGUMENTS` to get issue details
3. Analyze changes and determine:
   - **type**: feat/fix/docs/style/refactor/perf/test/build/ci/chore/revert
   - **scope**: Extract from issue or branch name (optional)
   - **gitmoji**: Choose emoji matching the change nature
   - **breaking**: Whether there's a breaking change
4. Generate commit message in this format:

**First line (subject):**
```
<emoji> <type>(<scope>)<exclamation-if-breaking>: <description> (#<issue_id>)
```

Example: `✨ feat(auth)! support user login (#1234)`

**Key points:**
- description in English, imperative mood (add/fix/update), max 50 characters
- Add exclamation mark after type if breaking change

**Body (after blank line):**
```
- <emoji> change description 1
- <emoji> change description 2
- <emoji> change description 3
```

**For breaking changes, append:**
```
💥 BREAKING CHANGE:
- breaking change description
```

5. After committing, run `git status` to confirm

### Guidelines

- Output only the commit message, no explanations
- Message must accurately reflect "why" and "what" of changes
- Use active voice, avoid redundant phrases
- If no staged files, output warning message
- Stage additional changes if needed using `git add`

You have the capability to call multiple tools in a single response. Stage and create the commit using a single message. Do not use any other tools or do anything else besides git operations needed for the commit.
