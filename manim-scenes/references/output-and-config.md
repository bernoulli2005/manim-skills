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

