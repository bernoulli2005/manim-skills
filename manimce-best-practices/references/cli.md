# CLI and Render Workflow

## Recommended Loop

1. Render low quality first.
2. Fix structure and labels.
3. Render medium quality for readability.
4. Render high quality only when stable.

## Practical Checks

- Confirm the scene class name.
- Confirm the file path passed to `manim`.
- Confirm the output directory.
- Confirm `manim.cfg` is not overriding a flag unexpectedly.

## Useful Habit

- Keep a project-local config when the same render flags are reused often.

