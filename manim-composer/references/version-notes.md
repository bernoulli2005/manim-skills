# ManimCE Version Notes

These notes keep planning grounded in Manim Community Edition behavior.

## What To Check

- Which API version the code targets
- Whether the project relies on `Scene`, `MovingCameraScene`, or `ThreeDScene`
- Whether the scene uses newer helpers or older naming patterns
- Whether any examples came from ManimGL and need translation

## Practical Differences To Watch

- Do not copy code from a different Manim variant without checking the API.
- Verify animation helper names, camera helpers, and text rendering behavior.
- Verify CLI flags and output paths before assuming the plan is correct.

## Planning Guidance

- Prefer CE-native patterns when the user asks for Manim Community Edition.
- If the reference material seems variant-specific, call that out explicitly.
- When in doubt, plan the scene in terms of visual intent first, then validate the exact API later.

