---
name: repo-workflow
description: Use when working in this repository to follow shared project workflow, relative paths, repository conventions, and safe handling of machine-specific settings.
---

# Repo Workflow

## Purpose

Follow this repository's shared workflow while keeping all paths portable across different computers.

## Core Rules

- Treat the repository root as the base path.
- Prefer relative paths such as `docs/spec.md`, `.codex/skills/repo-workflow/SKILL.md`, and `scripts/build.ps1`.
- Do not hard-code user-specific paths such as `C:\Users\name\...`.
- Do not commit API keys, tokens, passwords, local credentials, or machine-specific config.
- If a task needs a local path, ask the user or read it from an ignored local config file.

## Before Changing Files

1. Inspect the current repo structure.
2. Check whether matching conventions already exist.
3. Keep edits scoped to the requested task.
4. Preserve unrelated user changes.

## Recommended Layout

Use this structure when adding Codex skills to the repo:

```text
.codex/
  skills/
    skill-name/
      SKILL.md
      agents/
        openai.yaml
      references/
      scripts/
      assets/
```

Only create optional folders when they are useful for the skill.

## Machine-Specific Settings

Use ignored local files for per-computer values:

```text
.codex/local/
```

Examples:

- local workspace paths
- private tokens
- machine-specific tool locations
- temporary generated files

## Success Criteria

- The same repo works on different computers.
- Shared behavior is version-controlled.
- Private or machine-specific data stays out of git.
- Instructions remain short enough to be easy to maintain.
