---
name: manim-animations
description: Manim animation selection for `.animate`, Create, FadeIn, FadeOut, Write, Transform, ReplacementTransform, rate functions, timing, and multi-step choreography.
---

# Manim Animations

## Overview

Use this skill when the task is about motion itself: which animation class to use, how to stage transitions, and how to choreograph a scene. This skill complements the scene and mobject skills.

## Use This Skill For

- Choosing between `.animate` and explicit animation classes
- Using `Create`, `FadeIn`, `FadeOut`, `Write`, `Transform`, and related classes
- Coordinating multiple animations in one `play()`
- Adjusting run time and rate functions
- Building multi-step transitions and choreography

## Decision Rules

- Use `.animate` for direct method-driven changes when the intent is simple.
- Use named animation classes when the transition itself matters.
- Use `Transform` when the same concept should morph.
- Use `ReplacementTransform` when the old object should be replaced by the new one.
- Use `FadeIn` and `FadeOut` for presence changes.
- Use `Write` when text should appear as if it is being written.

## Choreography

1. Group related actions into one `play()` call when they happen together.
2. Use separate `play()` calls when the viewer should perceive distinct beats.
3. Prefer readable timing over overly compressed motion.
4. Make the slowest element set the pace when multiple things must be understood together.

## Timing

- Use `run_time` to control the duration of a transition.
- Use easing or rate functions when the motion should feel natural or stylized.
- Keep timing consistent across repeated motifs unless contrast is intentional.

## Composition Patterns

- `AnimationGroup` for concurrent actions.
- `LaggedStart` for cascaded or staggered reveals.
- `Succession` for sequential steps.
- `Wait` for intentional pauses.

## Advanced Notes

- Some mobjects define custom animation behavior.
- Animation overrides can make a mobject respond specially to a class of animations.
- When animation choices become hard to read, simplify the motion design before adding more complexity.

## Example Sequences

- Intro: `FadeIn` title, `Create` diagram, `Write` labels.
- Comparison: `Transform` old diagram into new diagram, then `Indicate` the changed part.
- Emphasis: `Circumscribe` a region, `Flash` a point, then continue.
- Progressive reveal: use `LaggedStart` to introduce elements one by one.

## Debugging Hints

- If the animation feels too fast, increase `run_time` before adding effects.
- If two objects should move together, group them into the same animation call.
- If a transform looks broken, simplify the source and target shapes.
- If emphasis feels noisy, remove extra effects and keep one primary highlight.

## References

- [Animation reference guide](references/animations.md)
