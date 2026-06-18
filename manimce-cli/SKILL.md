---
name: manimce-cli
description: Manim Community Edition CLI and render workflow guidance for command usage, quality presets, output paths, config files, and debugging failed renders.
---

# ManimCE CLI

## Overview

Use this skill for the command-line and render workflow side of ManimCE. It covers commands, quality presets, project config, output locations, and basic render debugging.

## Use This Skill For

- running `manim`
- choosing quality presets
- using `manim.cfg`
- debugging missing or stale renders
- checking output paths and scene names

## Workflow

1. Render low quality first.
2. Fix structure, labels, and layout.
3. Render medium quality to check readability.
4. Render high quality only when stable.

## Rules

- Verify the scene class name before debugging anything else.
- Verify the file path passed to `manim`.
- Verify the output folder and `media` tree.
- Use project-local config when the same flags repeat often.

## Common Mistakes

- Debugging the scene before checking the CLI command.
- Forgetting that `manim.cfg` can override flags.
- Assuming the render output went where you expected.
- Jumping to high quality too early.

## References

- [CLI notes](references/cli.md)

