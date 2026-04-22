# Global Claude Instructions

## Context Files
Project architecture and per-repo documentation are stored in ~/.claude/context/.
- `projects.md` — overall system architecture, service relationships, upstream/downstream
- `repo-<name>.md` — per-repo details (architecture, conventions, constraints)

When working in a repo or when a task involves specific services, read the relevant context files before proceeding.

## General Conventions
- Prefer explicit over implicit
- Ask for clarification before making assumptions on ambiguous requirements
- When in doubt about project conventions, check the context files first
