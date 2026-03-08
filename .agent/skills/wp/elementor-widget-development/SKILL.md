---
name: elementor-widget-development
description: Engineer Elementor widgets for any WordPress project. Use for control modeling, frontend rendering, editor preview parity, selector logic, and widget-level dependency loading.
---

# Elementor Widget Development

## Core (Universal)

### Trigger Scope

Use this skill when the task is widget internals:
- building/refactoring widget classes
- mapping controls to visual output
- fixing `render()` and `content_template()` mismatch
- optimizing widget-specific JS/CSS dependencies

### Workflow

1. Define widget contract.
- required identity methods
- control model with explicit defaults

2. Implement control surface.
- section structure
- responsive and conditional behavior

3. Implement frontend rendering.
- deterministic output from sanitized settings
- explicit output escaping

4. Implement editor rendering.
- mirror frontend intent in `content_template()`
- keep branch parity where possible

5. Verify behavior.
- empty/default/custom states
- editor/frontend parity

### Control And Selector Patterns

- Prefer `{{WRAPPER}}`-scoped selectors for style controls.
- Use control placeholders by data shape:
- `{{VALUE}}` for scalar controls (text/color/select/switcher).
- `{{SIZE}}{{UNIT}}` for slider-like controls.
- `{{TOP}}{{UNIT}} {{RIGHT}}{{UNIT}} {{BOTTOM}}{{UNIT}} {{LEFT}}{{UNIT}}` for dimensions.
- `{{URL}}` for media/url bindings.
- For repeater rows, use the row `_id` and `{{CURRENT_ITEM}}`-style targeting patterns.

### Guardrails

- Do not rely on implicit defaults for critical output.
- Do not output raw setting values without escaping.
- Do not enqueue heavy assets globally when widget-level dependency is possible.
- Avoid unnecessary DOM wrappers.

### Extended Cases

- If widget includes rich form behavior (validation/actions/record processing), route to `$elementor-forms`.
- If control injection into third-party widgets is needed, use element hooks before/after section boundaries.

### Minimal Example

```php
class Card_Widget extends \Elementor\Widget_Base {
    public function get_name(): string { return 'card_widget'; }
    public function get_title(): string { return esc_html__( 'Card', 'vendor-kit' ); }
    public function get_categories(): array { return [ 'basic' ]; }
    public function get_script_depends(): array { return [ 'vendor-card' ]; }
    protected function register_controls(): void {}
    protected function render(): void {}
    protected function content_template(): void {}
}
```
