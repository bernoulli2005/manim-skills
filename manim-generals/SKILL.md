---
name: manim-generals
description: Broad Manim workflow skill for planning scenes, choosing render settings, and routing to the right Manim specialist skill.
---

# Manim Generals

## Overview

Use this skill for general Manim work: project setup, scene planning, render strategy, and choosing the right specialist skill for a task. It is the default entry point when the user is still deciding what kind of animation to build.

## When To Use

- Starting a new Manim project or script
- Planning a scene before writing code
- Choosing between `Scene`, `MovingCameraScene`, and `ThreeDScene`
- Deciding whether to use `Text`, `MathTex`, `Axes`, `updaters`, or animation classes
- Debugging render configuration, output folders, or command-line usage

## Core Workflow

1. Identify the animation goal.
   - Expository math, UI motion, geometric construction, charting, 3D scene, or text-heavy explanation.
2. Choose the specialist skill.
   - Scenes: scene lifecycle and structure
   - Mobjects: shapes and layout
   - Animations: transitions and timing
   - Updaters: continuous motion and trackers
   - Graphing: axes, plots, coordinate systems
   - Text/TeX: captions and formulas
3. Start with one minimal `Scene`.
   - Keep the first version small and renderable.
   - Add complexity only after the base scene works.
4. Validate the render path.
   - Confirm CLI flags, quality preset, and output location.
   - Use `manim.cfg` only when repeated renders need stable defaults.

## Decision Rules

- Use `Scene` when the content is mostly sequential.
- Use `MovingCameraScene` when the camera must follow content.
- Use `ThreeDScene` when the composition depends on 3D axes or camera motion.
- Use `Text` for regular text and `MathTex`/`Tex` for formulas.
- Use `Mobject` subclasses instead of raw `Mobject` unless you are building infrastructure.
- Use `.animate` for simple method-driven motion and explicit animation classes for named transitions or choreography.
- Use mobject updaters for continuously changing visuals. Prefer `always_redraw` when a derived mobject should be regenerated every frame.

## Render Strategy

- Render low quality first for iteration.
- Use higher quality only when the composition is stable.
- When a scene has several independent parts, split them into smaller scenes instead of one giant `construct()`.
- Prefer deterministic naming and small helper methods so the scene is easy to revisit.

## References

- [Scene workflow](../manim-scenes/references/scenes.md)
- [Mobject and layout guide](../manim-mobjects/references/mobjects.md)
- [Animation guide](../manim-animations/references/animations.md)
- [Updater guide](../manim-updaters/references/updaters.md)
- [Graphing guide](../manim-graphing/references/graphing.md)
- [Text and TeX guide](../manim-text-tex/references/text-tex.md)

