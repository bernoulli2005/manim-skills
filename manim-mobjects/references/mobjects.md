# Mobjects and Layout

Mobjects are the basic building blocks of Manim animations. They represent any object that can appear on screen.

## Key Concepts

- `Mobject` is the common base class.
- `VMobject` is the vectorized variant used for many drawable shapes.
- Many higher-level objects, including graphs, tables, and axes, are still mobjects.

## Creation and Display

- Create mobjects first.
- Add them to a scene with `add()` if they should appear immediately.
- Remove them with `remove()` when they should disappear without an animation.

## Layout Methods

- `move_to`: absolute positioning
- `shift`: relative offset
- `scale`: resize uniformly or with vectors where appropriate
- `next_to`: place an object adjacent to another
- `to_edge`: anchor an object to a screen edge
- `arrange`: lay out a group in a row, column, or more complex order

## Grouping

- Use grouping when several objects should move together.
- Group containers are useful for labels, diagrams, and repeated motifs.
- Keep group boundaries meaningful so later animation steps stay simple.

## Styling

- Stroke controls the outline.
- Fill controls the interior.
- Opacity is useful for layering and spotlight effects.
- Consistent styling makes the viewer learn the visual system faster.

## Transforms

- Transform-related animations work best when the source and target have compatible structure.
- Use vector shapes when you expect smooth interpolation.
- If a mobject needs to change continuously, consider an updater rather than repeated manual transforms.

## Practical Heuristics

- Use the simplest shape that communicates the idea.
- Do not overcompose a scene with too many nested groups unless the hierarchy is deliberate.
- Keep labels close to what they describe.
- Prefer semantic names like `title`, `axes`, `legend`, `highlight`, `marker`.

