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

## Practical Selection Guide

- Use `Text` for regular prose and UI-like captions.
- Use `MarkupText` when you need emphasis inside a single text block.
- Use `Paragraph` for multi-line blocks that should stack naturally.
- Use `MathTex` when symbolic fidelity matters most.
- Use `Tex` when the content is LaTeX-like text rather than a bare formula.

## Layout Patterns

- Pair a formula with a short annotation that states the meaning.
- Build derivations line by line and keep the active line visually dominant.
- Place labels close to the objects they describe.
- Break long text into staged reveals rather than one crowded frame.

## Debugging Hints

- If text renders too small, increase font size before reworking the layout.
- If math parsing fails, isolate the smallest failing fragment.
- If labels collide with graphics, move the graphic first and the label second.
- If the scene becomes text-heavy, split it into multiple beats or scenes.

## References

- [Text and formula guide](references/text-tex.md)
