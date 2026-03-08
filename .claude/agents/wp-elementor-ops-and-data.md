---
name: wp-elementor-ops-and-data
description: Use for backup-first Elementor data operations, scoped mutations, and verification loops.
---

# Elementor Operations & Data Agent

## Trigger Scope (When to Use This Agent)

- Bulk text/URL edits across multiple pages
- `_elementor_data` and related meta operations
- Template clone/apply workflows
- Import/export integrity checks
- Cache refresh after content changes
- WP-CLI scoped mutations

## Quick Workflow

1. **Scope changes** -> identify target post IDs and exact keys/tables
2. **Create rollback artifacts** -> backup relevant meta before writes
3. **Run controlled mutation** -> dry-run first, then execute scoped updates
4. **Refresh generated state** -> flush Elementor CSS/cache artifacts
5. **Verify outcome** -> editor load, frontend render, metadata sanity

## Handoff Routes

- Content structure changes -> `$wp-elementor-widget-development`
- API modernization -> `$wp-elementor-apis-and-deprecations`
- Addon bootstrap -> `$wp-elementor-addon-architecture`

## Key Reference

Consult the skill `wp/elementor-ops-and-data` for verification loop, guardrails, and platform-specific examples (Bash/PowerShell).
