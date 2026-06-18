# Manim Skills

This repository packages a set of Codex skills for working with Manim Community Edition.

## What is in this repo

- `manim-generals`
- `manim-composer`
- `manimce-best-practices`
- `manimce-camera`
- `manimce-text`
- `manimce-cli`
- `manim-scenes`
- `manim-mobjects`
- `manim-animations`
- `manim-updaters`
- `manim-graphing`
- `manim-text-tex`

Each skill lives in its own folder and contains a `SKILL.md` entry point plus optional `references/` material.

## How to install

Use `npx skills` to install a specific skill from this repo.

```bash
npx skills add bernoulli2005/manim-skills/manim-generals
npx skills add bernoulli2005/manim-skills/manim-composer
npx skills add bernoulli2005/manim-skills/manimce-best-practices
npx skills add bernoulli2005/manim-skills/manimce-camera
npx skills add bernoulli2005/manim-skills/manimce-text
npx skills add bernoulli2005/manim-skills/manimce-cli
npx skills add bernoulli2005/manim-skills/manim-scenes
```

You can also install by full URL:

```bash
npx skills add https://github.com/bernoulli2005/manim-skills/tree/main/manim-generals
```

## Recommended workflow

1. Install `manim-generals` first for project planning and routing.
2. Add the specialist skill you need for the current task.
3. Keep the scene-specific work in the narrowest skill that matches the problem.

## Skill map

- `manim-generals`: entry point for planning, render strategy, and skill selection
- `manim-composer`: turn vague video ideas into a scene-by-scene plan
- `manimce-best-practices`: implementation guidance for Manim Community Edition
- `manimce-camera`: camera framing, zooms, and pans
- `manimce-text`: text, formulas, and label layout
- `manimce-cli`: command-line rendering and debug workflow
- `manim-scenes`: scene lifecycle, `construct()`, `play()`, `wait()`, and camera structure
- `manim-mobjects`: objects, layout, grouping, and transforms
- `manim-animations`: animation classes, `.animate`, timing, and choreography
- `manim-updaters`: trackers, `always_redraw`, and continuous motion
- `manim-graphing`: axes, plots, coordinate systems, and curve helpers
- `manim-text-tex`: text, LaTeX, formulas, and labels

## Notes

- These skills follow the open agent skills format.
- The repo is organized for reuse as a GitHub-hosted skills bundle.
- If you change a skill, restart Codex so it picks up the update.
