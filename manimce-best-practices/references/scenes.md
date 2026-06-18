# Scene Structure

## Recommended Scene Shape

- Keep `construct()` readable.
- Break repeated logic into helper methods.
- Add objects before animating them when that improves readability.
- Use `wait()` to let the viewer process the current frame.

## Scene Design Rules

- One scene should usually teach one local idea.
- If the scene needs too many concepts, split it.
- Keep the scene order aligned with the narrative order.
- Use scene names that reveal purpose, not implementation detail.

## Common Pitfalls

- Too many simultaneous changes.
- Too much hidden state in helper methods.
- Mixing unrelated visual languages in one scene.
- Letting a single scene become a full video dump.

## Good Scene Shapes

- title -> setup -> transformation -> summary
- question -> diagram -> proof step -> conclusion
- graph -> highlight -> interpretation -> takeaway

