---
name: manim-updaters
description: Manim skill for continuous motion, ValueTracker patterns, always_redraw, and updater-based dynamic scenes.
---

# Manim Updaters

## Overview

Use this skill when objects need to stay linked after creation: moving labels, live values, pointer lines, animated diagrams, or any content that must update continuously while another value changes.

## Use This Skill For

- `add_updater` and updater callbacks
- `always_redraw`
- `always`
- `ValueTracker`
- Live coordinates, labels, and dynamic geometry
- Avoiding stale visuals in scenes with continuous change

## Core Rule

If an object must keep reflecting another object or variable, do not manually re-create it every frame unless that is the simplest correct option. Use an updater or `always_redraw`.

## Choosing a Pattern

- Use `add_updater` when an object should mutate in place over time.
- Use `always_redraw` when an object is easiest to express as "rebuild this every frame."
- Use `ValueTracker` when the thing changing is a numeric parameter rather than a visible object.
- Use `always` for a simple perpetual method call pattern.

## Best Practices

- Keep updater functions small and deterministic.
- Read the current state inside the updater instead of caching values too early.
- Keep the geometry readable even while it changes.
- Prefer mobject updaters over scene-level hacks for things that must stay in sync.
- Remove updaters when the object no longer needs to be dynamic.

## Common Patterns

- A dot following a curve while a tracker advances.
- A label attached to a moving point.
- A number display that reflects a tracker.
- A dynamically sized brace or highlight that follows a target object.

## Cautions

- Continuous motion can become visually noisy if too many objects update at once.
- Some renderers and scene setups expose updater behavior differently, so test the exact render path you intend to ship.
- If a derived object gets out of sync, rewrite it as `always_redraw` before adding more manual bookkeeping.

## References

- [Updater reference guide](references/updaters.md)

