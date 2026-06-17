---
name: manim-text-tex
description: Manim text and formula rendering for Text, MarkupText, Paragraph, Tex, MathTex, captions, labels, derivations, and mixed prose-plus-math layouts.
---

# Manim Text and TeX

## Overview

Use this skill when the scene needs readable prose, labels, captions, formulas, or mixed text-and-math content. This skill helps choose the right text system and avoid common rendering mistakes.

## Use This Skill For

- `Text` for ordinary text
- `MarkupText` for text with styling markup
- `Paragraph` for multi-line text blocks
- `Tex` and `MathTex` for LaTeX rendering
- Combining labels, formulas, and annotations in the same scene

## Selection Rules

- Use `Text` for regular language text.
- Use `MathTex` for math expressions where symbol-level control matters.
- Use `Tex` when you want LaTeX-rendered text that is not strictly a standalone math expression.
- Use `MarkupText` when the content needs inline styling.

## Practical Guidance

- Keep simple text simple.
- Use LaTeX only when it adds real typesetting value.
- Use raw strings for formulas when it makes escape handling clearer.
- Keep labels short when they sit inside dense diagrams.
- Match font size and color to the visual hierarchy of the scene.

## Common Patterns

- Title + subtitle layout
- Formula reveal with accompanying plain-language explanation
- Annotation labels on axes, arrows, or highlighted objects
- Step-by-step derivation where each line is introduced cleanly

## Pitfalls

- Putting every line into LaTeX when plain text would be easier to maintain.
- Using text that is too small to read after render compression.
- Letting formulas collide with surrounding graphics.
- Mixing too many font styles without a deliberate hierarchy.

## References

- [Text and formula guide](references/text-tex.md)
