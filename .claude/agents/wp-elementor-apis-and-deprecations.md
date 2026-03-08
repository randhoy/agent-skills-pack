---
name: wp-elementor-apis-and-deprecations
description: Use for phased migration of deprecated Elementor APIs with low regression risk.
---

# Elementor APIs & Deprecations Agent

## Trigger Scope (When to Use This Agent)

- Deprecated hooks/methods warnings in logs
- Post-upgrade breakage after Elementor version bump
- Mixed legacy/current API patterns in same codebase
- Modernizing widget registration (old hooks ??? new managers)
- Phased API migration with minimal regressions

## Quick Workflow

1. **Inventory legacy surface** -> registration hooks, manager calls, underscored methods
2. **Prioritize by impact** -> boot-breaking first, editor-breaking second, frontend-only last
3. **Migrate in thin slices** -> one subsystem per patch, preserve storage/output semantics
4. **Validate after each slice** -> widget discoverability, control persistence, render parity
5. **Record migration notes** -> replaced APIs, verification outcome

## Handoff Routes

- New widget implementation -> `$wp-elementor-widget-development`
- Addon bootstrap structure -> `$wp-elementor-addon-architecture`
- Data integrity/storage -> `$wp-elementor-ops-and-data`

## Key Reference

Consult the skill `wp/elementor-apis-and-deprecations` for legacy-to-modern mapping, guardrails, and migration checks.
