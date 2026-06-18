# Output and Config

Manim rendering is controlled by CLI flags and config files.

## Useful Defaults

- Start with low-quality renders while iterating.
- Move to higher quality after layout and timing are correct.
- Use `manim.cfg` when you want project-local defaults that apply to the whole folder.

## Config File Rules

- The file must be named `manim.cfg`.
- The file must contain a `[CLI]` section.
- Options in the config file use the long-form names of CLI flags.
- A folder-wide config file affects only scripts in that folder.

## Debugging Tips

- If the output is not where you expect, check the `media` tree first.
- If a scene is not rendering, verify the scene class name and the exact file path passed to the CLI.
- If repeated renders are tedious, move stable flags into `manim.cfg`.

## Practical Render Loop

1. Render low quality to verify structure.
2. Fix geometry, ordering, and labels.
3. Render medium quality to verify readability.
4. Render high quality only after the scene is stable.

## Common Flags To Stabilize

- Resolution and quality preset
- Output directory
- Background color
- Frame rate when timing matters

## Debugging Checklist

- Verify the scene class name exists.
- Verify the file path passed to the CLI is correct.
- Verify the `media` folder is not stale from an older render.
- Verify `manim.cfg` is not overriding the flag you expect.
