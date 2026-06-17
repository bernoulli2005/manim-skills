---
name: manim-mobjects
description: Manim skill for creating, styling, grouping, positioning, and transforming mobjects and vectorized objects.
---

# Manim Mobjects

## Overview

Use this skill when the task is about the objects you place on screen: shapes, groups, labels, vector objects, positioning, styling, and structural composition. This is the right skill for constructing the visual language of a scene.

## Use This Skill For

- Creating circles, squares, arrows, lines, and other shapes
- Grouping objects with `VGroup` or similar containers
- Positioning content with `move_to`, `shift`, `next_to`, `to_edge`, and `arrange`
- Styling fills, strokes, colors, and opacity
- Transforming objects from one shape to another
- Understanding when to use `Mobject` vs `VMobject`

## Core Model

- `Mobject` is the base abstraction for displayable objects.
- Most visible shapes are subclasses of `Mobject`.
- `VMobject` is the vectorized form used for many drawable shapes.
- A plain `Mobject` is usually not what you want unless you are building infrastructure.

## Working Pattern

1. Create the object.
2. Group related objects.
3. Align and position them.
4. Style them.
5. Add them to the scene or animate them.

## Positioning

- Use `move_to` for absolute placement.
- Use `shift` for relative movement.
- Use `next_to` for labels, callouts, and nearby annotations.
- Use `to_edge` for title cards or fixed framing.
- Use `arrange` or `arrange_in_grid` for structured layouts.
- Use alignment helpers when multiple objects must share a baseline, edge, or center.

## Styling

- Choose stroke and fill separately when you need clear contrast.
- Keep line widths and font sizes readable at video scale.
- Favor consistent palette choices across a scene.
- Use opacity deliberately for emphasis, layering, or de-emphasis.

## Transformation Strategy

- Use a direct transform when the source and target concepts are related.
- Use `ReplacementTransform` when the old object should visibly become the new one.
- Use copying when one object should persist while another branch evolves.
- If a shape is generated procedurally, keep it structurally compatible with the target transform.

## Common Primitives

- `Circle`, `Square`, `Rectangle`, `RoundedRectangle`
- `Line`, `Arrow`, `DoubleArrow`
- `Dot`, `Triangle`, `Polygon`
- `Tex`, `MathTex`, `Text`, `MarkupText`
- `Axes`, `NumberPlane`, `Graph`, `Table`

## Practical Advice

- Prefer semantic grouping over one giant monolithic object.
- Name intermediate objects clearly so later animations stay readable.
- Use vectorized shapes when you want smooth transforms and clean scaling.
- Keep layout logic separate from animation logic when possible.

## References

- [Building blocks tutorial](references/mobjects.md)

