# Agent Skills Pack

Portable skill pack for multiple domains (WordPress and non-WordPress).

## Structure

```text
github-publish-files/
  skills/
    <domain>/
      <skill-name>/
        SKILL.md
        agents/openai.yaml
  LICENSE
  ATTRIBUTION.md
  README.md
```

## Included Skills

- `wp/elementor-addon-architecture`
- `wp/elementor-widget-development`
- `wp/elementor-apis-and-deprecations`
- `wp/elementor-ops-and-data`

Detailed index: `skills/INDEX.md`  
Machine-readable manifest: `skills/manifest.json`

Add any other domain skills by placing them under `skills/<domain>/<skill-name>/`.

## Usage

Install each skill directory into your Codex skills root (for example `~/.codex/skills/<skill-name>`), then restart Codex UI/session to pick up new skills.

## Platform Targets

- OpenAI-style skills: `skills/`
- Anthropic wrappers: `.claude/agents/`
- Antigravity-style skills: `.agent/skills/`
- Details: [PLATFORM_COMPATIBILITY.md](PLATFORM_COMPATIBILITY.md)

## License

- Repository license: [GPL-2.0-or-later](LICENSE)
- Third-party attribution and adaptation notes: [ATTRIBUTION.md](ATTRIBUTION.md)
