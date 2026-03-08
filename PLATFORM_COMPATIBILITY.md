# Platform Compatibility

This pack is prepared for multiple agent ecosystems.

## OpenAI-style skill loading

- Path pattern: `skills/<domain>/<skill-name>/SKILL.md`
- UI metadata: `skills/<domain>/<skill-name>/agents/openai.yaml`
- Included index and manifest:
  - `skills/INDEX.md`
  - `skills/manifest.json`

## Anthropic (Claude Code) compatibility

- Subagent wrappers are provided in:
  - `.claude/agents/wp-elementor-addon-architecture.md`
  - `.claude/agents/wp-elementor-widget-development.md`
  - `.claude/agents/wp-elementor-apis-and-deprecations.md`
  - `.claude/agents/wp-elementor-ops-and-data.md`
- These wrappers reference the corresponding skills under `skills/wp/*`.

## Antigravity compatibility

- Skills are mirrored to:
  - `.agent/skills/wp/<skill-name>/SKILL.md`
- This keeps a dedicated `.agent/skills` namespace while preserving the same skill content.
