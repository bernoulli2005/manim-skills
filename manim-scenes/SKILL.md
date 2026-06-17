---
name: manim-scenes
description: Scene-level Manim skill for construct methods, play/wait/add/remove flow, sections, and camera-driven scene structure.
---

# Manim Scenes

## Overview

Use this skill when the task is about how a Manim scene is structured: `construct()`, scene methods, render flow, sections, and camera behavior. It is the right skill for deciding how a script should be organized around one or more scenes.

## Use This Skill For

- Writing or refactoring `Scene` subclasses
- Organizing a file with multiple scenes
- Using `add`, `remove`, `play`, and `wait`
- Breaking a scene into narrative beats or sections
- Choosing between standard, moving-camera, and 3D scene types
- Understanding scene-level rendering and output behavior

## Reference Workflow

1. Put the animation logic in `construct()`.
   - Treat `construct()` as the scene script.
   - Use helper methods only to keep `construct()` readable.
2. Add static content with `add()`.
   - Use this for objects that should appear without animation.
3. Animate changes with `play()`.
   - Use one or more animations in a single call when they belong together.
4. Pause with `wait()`.
   - Use it to separate beats or allow the viewer to read a frame.
5. Remove content with `remove()` or transform it away.
   - Prefer explicit transitions over abrupt state changes unless the cut is intentional.

## Scene Types

- `Scene`
  - The default choice for most animations.
  - Best for linear explanations and general motion.
- `MovingCameraScene`
  - Use when content should be reframed dynamically.
  - Helpful for zooming into dense diagrams or code-like layouts.
- `ThreeDScene`
  - Use for 3D geometry and camera movement in 3D space.
  - Keep the composition simple and readable; 3D scenes become hard to follow quickly.
- `VoiceoverScene`
  - Use only when the project explicitly includes voiceover timing.

## Scene-Level Best Practices

- Keep each scene focused on one idea.
- Prefer a small number of clear transitions.
- Use scene sections when a long explanation benefits from logical breaks.
- Avoid mixing too many unrelated visual motifs in one scene.
- Reuse helper methods for repeated framing, title cards, or layout blocks.
- When rendering multiple scenes from one file, make the file order and scene names deliberate.

## Camera Notes

- Use camera-aware scenes when the framing is part of the story.
- Keep camera movement slower than object motion unless the cut is supposed to feel energetic.
- In 3D scenes, keep axis orientation and object placement consistent so the viewer does not lose spatial reference.

## Rendering Notes

- The scene file can contain multiple scenes, but each scene should still be independently understandable.
- If a scene becomes unwieldy, split it into smaller scenes rather than overloading one `construct()`.
- The output folder structure matters when debugging missing videos or partial renders.

## References

- [Official Scene API](references/scenes.md)
- [Output and config overview](references/output-and-config.md)

