---
name: manimce-best-practices
description: Manim Community Edition implementation hub for scenes, camera, animations, text, lines, CLI workflow, and version-safe coding patterns. Use when writing or reviewing ManimCE code, debugging renders, or translating a plan into code, and route to tighter skills like manimce-camera, manimce-text, or manimce-cli when the task is specialized.
---

# ManimCE Best Practices

## Overview

Use this skill when you are implementing Manim Community Edition code or reviewing it for correctness. It focuses on practical coding rules, scene hygiene, camera usage, animation choice, text handling, line drawing, CLI use, and version-safe habits.

## Use This Skill For

- Writing ManimCE scenes from a plan
- Reviewing or refactoring existing Manim code
- Choosing between animation and updater patterns
- Debugging camera, text, line, or render issues
- Translating a composed plan into a working scene

## Implementation Workflow

1. Start from the visual goal.
   - Identify what the viewer should see first, second, and last.
2. Build the smallest working scene.
   - One object, one motion, one takeaway.
3. Add structure.
   - Group repeated logic, separate beats, and name helper methods.
4. Refine with camera and timing.
   - Use framing only when it helps the viewer read the scene.
5. Validate the render path.
   - Confirm CLI command, quality preset, and output location.

## Core Rules

- Prefer clarity over cleverness.
- Prefer explicit code over implicit side effects.
- Keep each scene narrowly focused.
- Reuse helper functions when the same layout or motion appears multiple times.
- Make the rendered result readable at video scale, not just in source code.

## Topic Guides

- [Scene structure](references/scenes.md)
- [Compatibility notes](references/version-notes.md)
- [Scene examples](references/scene-examples.md)
- For camera-specific work, use `manimce-camera`.
- For text-specific work, use `manimce-text`.
- For CLI-specific work, use `manimce-cli`.
- For animation-specific work, use `manim-animations`.
- For scene orchestration, use `manim-scenes`.
