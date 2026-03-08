---
name: wp-elementor-widget-development
description: Use for Elementor widget controls, render/content_template parity, and scoped dependencies.
---

# Elementor Widget Development Agent

## Trigger Scope (When to Use This Agent)

- Building/refactoring widget classes
- Mapping controls to visual output
- Fixing `render()` and `content_template()` mismatch
- Implementing control selectors (responsive, conditionals)
- Optimizing widget-specific JS/CSS dependencies
- Handling repeater rows and dynamic content

## Quick Workflow

1. **Define widget contract** -> required methods (name, title, categories) + control defaults
2. **Implement control surface** -> sections with responsive/conditional behavior
3. **Implement frontend render** -> sanitized settings + explicit escaping
4. **Implement editor template** -> content_template() mirrors frontend intent
5. **Verify behavior** -> empty/default/custom states + editor/frontend parity

## Handoff Routes

- Addon/plugin structure -> `$wp-elementor-addon-architecture`
- API modernization/deprecation -> `$wp-elementor-apis-and-deprecations`
- Content mutations -> `$wp-elementor-ops-and-data`

## Key Reference

Consult the skill `wp/elementor-widget-development` for control/selector patterns, escaping guardrails, and minimal examples.
