---
name: manim-composer
description: Plan Manim explainer videos and 3Blue1Brown-style sequences from vague ideas, educational prompts, or visual metaphors. Use when the user wants a scene-by-scene plan, narrative hook, audience/focus clarification, or a visual outline before writing Manim code.
---

# Manim Composer

## Overview

Use this skill before writing code when the user has an idea but not a scene plan. Turn a vague concept into a concrete animation roadmap: audience, narrative hook, beat order, scene list, and required visuals.

## Use This Skill For

- Vague video ideas that need structure
- Educational or explainer videos
- "3Blue1Brown style" or "explain visually" requests
- Planning a Manim sequence before implementation
- Deciding what the scene should teach, not just what it should show

## Planning Workflow

1. Clarify the objective.
   - What idea should the viewer understand at the end?
   - What misconception should the video fix?
2. Identify the audience.
   - Assume level, background, and patience.
3. Find the narrative hook.
   - What makes this surprising, useful, or intuitive?
4. Break the idea into beats.
   - One beat per visual change or conceptual shift.
5. Map beats to scenes.
   - Keep each scene focused on one local question.
6. Note dependencies.
   - Variables, diagrams, formulas, assets, references, or data.

## Questions To Ask

- Who is the target viewer?
- What level of math/science knowledge should I assume?
- Is this proof-heavy, intuition-heavy, or application-heavy?
- How long should the final video feel?
- Should the style be calm and explanatory, or fast and dramatic?
- What is the single most important "aha" moment?

## Output Shape

Produce a plan with:

- one-sentence goal
- audience assumptions
- key insight
- scene-by-scene outline
- visual assets needed
- implementation notes for ManimCE

## Planning Rules

- Prefer concrete beats over abstract themes.
- Keep each scene visually simple.
- Make the first scene establish the problem or question quickly.
- Use the final scene to resolve the central idea, not to add new ones.
- If the idea needs too many concepts, split it into a series.

## References

- [Scene examples](references/scene-examples.md)
- [ManimCE implementation notes](references/version-notes.md)

