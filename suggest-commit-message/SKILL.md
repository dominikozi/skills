---
name: suggest-commit-message
description: Review repository changes and suggest a clear Conventional Commit message.
---

Review the current repository changes and propose an accurate commit message.

## Workflow

1. Inspect the repository state with `git status`.
2. Review staged changes with `git diff --staged`.
3. Review unstaged changes with `git diff` when they may also be part of the commit.
4. Check recent commit messages with `git log -10 --oneline` to understand the repository's existing style.
5. Identify the main purpose of the changes, not just the files that were modified.
6. Do not modify files, stage changes, create commits, or push anything.
7. Use Conventional Commits format `<type>(<optional scope>): <description>`.
