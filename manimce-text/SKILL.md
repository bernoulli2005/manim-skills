---
name: manimce-text
description: Manim Community Edition text and math guidance for Text, MarkupText, Paragraph, Tex, MathTex, labels, derivations, and mixed prose-plus-math layouts.
---

# ManimCE Text

## Overview

Use this skill for text-heavy ManimCE work: prose, labels, captions, formulas, derivations, and mixed text-plus-math layouts.

## Use This Skill For

- `Text`
- `MarkupText`
- `Paragraph`
- `Tex`
- `MathTex`
- label-heavy diagrams
- derivations and formula reveals

## Selection Rules

- Use `Text` for ordinary prose.
- Use `MarkupText` only when inline styling is useful.
- Use `Paragraph` for stacked multi-line blocks.
- Use `Tex` for LaTeX-rendered text that is not purely symbolic.
- Use `MathTex` for symbolic math and equation-heavy content.

## Layout Rules

- Keep text readable at render scale.
- Keep labels short near dense geometry.
- Place formulas close to the objects they explain.
- Stage long derivations rather than crowding one frame.
- Use hierarchy: title, subtitle, annotation, detail.

## Common Mistakes

- Using `MathTex` everywhere.
- Making labels too small.
- Letting text collide with diagrams.
- Mixing too many font styles without a clear hierarchy.

## References

- [Text and LaTeX notes](references/text.md)

