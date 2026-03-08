# Contributing

## Scope

This repository stores portable agent skills. Keep changes focused on skill quality, compatibility, and maintainability.

## Required Skill Structure

Each skill must be placed at:

`skills/<domain>/<skill-name>/`

Required file:
- `SKILL.md`

Recommended file:
- `agents/openai.yaml`

## SKILL.md Rules

- Must include YAML frontmatter with:
  - `name`
  - `description`
- Keep instructions concise and implementation-focused.
- Avoid project-specific paths and assumptions in universal skills.
- Prefer ASCII unless non-ASCII is necessary.

## Adding A New Skill

1. Create folder: `skills/<domain>/<skill-name>/`
2. Add `SKILL.md` with valid frontmatter.
3. Add `agents/openai.yaml` (recommended).
4. Update:
   - `skills/INDEX.md`
   - `skills/manifest.json`
5. If needed, add mirrors:
   - `.claude/agents/`
   - `.agent/skills/<domain>/`

## Pull Request Checklist

- Skill path matches convention.
- Frontmatter has `name` and `description`.
- `skills/manifest.json` is valid and updated.
- `skills/INDEX.md` includes new skill.
- CI validation passes.
