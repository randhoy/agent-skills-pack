---
name: wp-elementor-addon-architecture
description: Use for Elementor addon bootstrap, lifecycle boundaries, compatibility gates, and manager wiring.
---

# Elementor Addon Architecture Agent

## Trigger Scope (When to Use This Agent)

- Designing addon/plugin structure from scratch
- Setting up initialization order and dependency checks
- Wiring manager registration (widgets, controls, tags, finder, categories)
- Defining global asset loading strategy
- Validating bootstrap safety and startup gates

## Quick Workflow

1. **Define runtime contract** -> target PHP/WordPress/Elementor versions + required dependencies
2. **Build startup boundaries** -> WordPress load phase + Elementor compatibility gate
3. **Organize registration surfaces** -> one method per manager type
4. **Define asset strategy** -> centralized registration with widget-level consumption
5. **Validate boot behavior** -> deterministic startup, no partial boot

## Handoff Routes

- Widget internals (render, controls, selectors) -> `$wp-elementor-widget-development`
- API modernization/deprecation -> `$wp-elementor-apis-and-deprecations`
- Persisted data mutations -> `$wp-elementor-ops-and-data`

## Key Reference

Consult the skill `wp/elementor-addon-architecture` for complete workflow, registration map, guardrails, and minimal code examples.
