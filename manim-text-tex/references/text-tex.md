# Text and Formula Guide

Manim supports two main text pipelines:

- Pango-based text rendering for standard text
- LaTeX-based rendering for formulas and typeset math

## Text Without LaTeX

- Use `Text` for standard prose.
- Use `MarkupText` when you need styled spans.
- Use `Paragraph` for multi-line text blocks.
- Pango can render non-English alphabets and typical UI-like labels.

## Text With LaTeX

- Use `MathTex` for mathematical expressions.
- Use `Tex` when the content is better thought of as a LaTeX string rather than a bare formula.
- Use this route when mathematical notation must look polished and precise.

## Layout Advice

- Place text where it supports the story instead of centering everything by default.
- Keep formulas close to the objects they describe.
- Use consistent sizing and spacing across labels in the same scene.

## Good Habits

- Prefer the simplest text system that solves the problem.
- Keep equations readable at video scale.
- Break long derivations into staged reveals rather than a single crowded frame.

