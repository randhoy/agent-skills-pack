# Agent Skills Pack

Cross-platform skills pack for WordPress/Elementor workflows.

## Quick Start

1. Clone this repository.
2. Pick your platform (Codex/OpenAI, Claude, Antigravity).
3. Copy the relevant skill folders to your platform skills location.

Detailed compatibility guide: [PLATFORM_COMPATIBILITY.md](PLATFORM_COMPATIBILITY.md)

## Included Skills

| Skill | Purpose |
|---|---|
| `wp/elementor-addon-architecture` | Addon bootstrap, lifecycle gates, manager wiring |
| `wp/elementor-widget-development` | Controls, render/content template parity, selector patterns |
| `wp/elementor-apis-and-deprecations` | Legacy -> modern API migration with low regression |
| `wp/elementor-ops-and-data` | Backup-first content/meta operations and verification loop |

Skill index: `skills/INDEX.md`  
Machine-readable manifest: `skills/manifest.json`

## Install By Platform

### OpenAI/Codex Style

Source of truth: `skills/wp/<skill-name>/`

- Includes `SKILL.md`
- Includes `agents/openai.yaml`

### Anthropic (Claude)

Source of truth: `.claude/agents/*.md`

- Ready-to-use wrapper agents:
  - `wp-elementor-addon-architecture`
  - `wp-elementor-widget-development`
  - `wp-elementor-apis-and-deprecations`
  - `wp-elementor-ops-and-data`

Marketplace metadata:
- `.claude-plugin/marketplace.json`
- Use this when distributing through Claude plugin/marketplace flows.

### Antigravity Style

Source of truth: `.agent/skills/wp/<skill-name>/SKILL.md`

Notes:
- For Antigravity, the `.agent/skills/` namespace is the key requirement.
- No extra marketplace manifest is required in this pack.

## Folder Layout

```text
agent-skills-pack/
  skills/
    wp/
      <skill-name>/
        SKILL.md
        agents/openai.yaml
  .claude/agents/
    wp-*.md
  .agent/skills/wp/
    <skill-name>/SKILL.md
  LICENSE
  ATTRIBUTION.md
  PLATFORM_COMPATIBILITY.md
  README.md
```

## Extend The Pack

Add new skills under `skills/<domain>/<skill-name>/`, then optionally mirror them to:
- `.claude/agents/` (Anthropic wrappers)
- `.agent/skills/<domain>/` (Antigravity namespace)

## License

- Repository license: [GPL-2.0-or-later](LICENSE)
- Third-party attribution and adaptation notes: [ATTRIBUTION.md](ATTRIBUTION.md)

## Project Governance

- Contribution guide: [CONTRIBUTING.md](CONTRIBUTING.md)
- Changelog: [CHANGELOG.md](CHANGELOG.md)
