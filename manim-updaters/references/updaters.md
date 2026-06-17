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

