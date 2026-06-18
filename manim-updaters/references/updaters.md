# Updater Reference

Updaters let mobjects respond continuously as the scene progresses.

## Main Tools

- `add_updater`: attach a function that runs as the scene updates
- `clear_updaters`: remove attached updater functions
- `always`: keep a method call active
- `always_redraw`: rebuild a mobject every frame
- `ValueTracker`: hold a numeric value that can drive motion

## Typical Use Cases

- Follow a moving object with a label or line
- Update text as a numeric value changes
- Keep a highlight aligned to a moving target
- Redraw a plot-derived object as parameters change

## Good Practices

- Prefer updater logic that is easy to reason about.
- Use trackers for numbers, not as a replacement for scene structure.
- If the scene only needs a final state, use a discrete animation instead of an updater.

## Debugging

- If an element does not track correctly, check whether the updater reads current state or stale cached state.
- If several objects depend on the same value, centralize that value in a tracker.
- If an updater is hard to maintain, switch to `always_redraw` or a simpler animation sequence.

## Example Patterns

- Attach a label to a moving point and keep the label offset stable.
- Drive the endpoint of a line from a tracker so the length changes live.
- Redraw a brace or highlight around a changing region.
- Keep a numeric readout synchronized with a parameter sweep.

## Operational Notes

- Prefer updaters when the relationship between objects matters more than the exact animation path.
- Prefer direct animations when the final state is all the viewer needs.
- Keep one source of truth for each changing quantity.

## Debugging Hints

- If a live object jitters, simplify the geometry or reduce the number of dependent updates.
- If a label jumps, make sure its anchor point stays stable.
- If a tracker-driven object behaves oddly, inspect the tracker value before animating.
- If an updater chain becomes hard to reason about, replace one layer with a more explicit animation.
