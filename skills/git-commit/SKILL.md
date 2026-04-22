---
name: git-commit
description: Generates a git commit message based on current staged or unstaged changes. Use when the user wants to commit, asks for a commit message, or says "help me write a commit".
---

# Git Commit Message Generator

## Convention

Use Conventional Commits format:

```
<type>(<scope>): <subject>

<body>

<footer>
```

**type** must be one of:
- `feat` — new feature
- `fix` — bug fix
- `refactor` — code change that neither fixes a bug nor adds a feature
- `perf` — performance improvement
- `test` — adding or updating tests
- `docs` — documentation only
- `chore` — build process, dependency updates, tooling

## Rules

- `subject`: max 50 characters, imperative mood ("add" not "added"), no period
- `body`: explain *why*, not *what* — the diff already shows what changed. Wrap at 72 chars.
- `footer`: use for breaking changes (`BREAKING CHANGE: <description>`) or issue references (`Closes #123`)
- body and footer are optional for small, self-explanatory changes

## Process

1. Run `git diff --staged` to see staged changes
2. If nothing is staged, run `git diff` to see unstaged changes
3. Read `~/.claude/context/projects.md` if the change touches service boundaries
4. Generate the commit message

## Output

Provide:
1. **Recommended** commit message (most accurate)
2. **Alternative 1** (different type or framing if applicable)
3. **Alternative 2** (shorter version if the recommended is long)

Format each as a code block so it can be copied directly.
Briefly explain why you chose the recommended type and scope.
