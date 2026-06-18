# Scene Workflow

Manim scenes are the top-level orchestration layer. A scene owns the timeline, the camera, and the list of mobjects that are currently present.

## Mental Model

- `Scene` is where the animation script lives.
- `construct()` is the main entry point.
- `add()` places mobjects into the scene without animating them.
- `remove()` takes mobjects out of the scene.
- `play()` runs one or more animations.
- `wait()` inserts time without changing state.

## Practical Pattern

Use a scene in this order:

1. Create the mobjects.
2. Add or animate the initial layout.
3. Introduce motion with `play()`.
4. Pause with `wait()` when the viewer needs time to read.
5. Transition to the next beat or next scene.

## Choosing Between Scene Types

- `Scene`: default for almost all tutorials, explainers, and diagrams.
- `MovingCameraScene`: best when a static camera is too restrictive for zooms or panning.
- `ThreeDScene`: best for 3D coordinate systems, rotations, and perspective changes.

## Common Pitfalls

- Doing too much inside one `construct()` without structure.
- Relying on implicit state changes when a real animation would be clearer.
- Forgetting to keep the scene logically linear for the viewer.
- Using camera motion where a simple layout change would be easier to follow.

## Scene Output

- Rendered files live under the project `media` directory by default.
- Scene names matter because the render output is keyed by the scene class.
- For repeated local tweaking, keep a stable folder layout and use a local config file instead of retyping CLI flags.

## Example Scene Structure

1. Establish the topic with a title or intro frame.
2. Introduce the main object or diagram.
3. Animate the core change or proof step.
4. Add an emphasis beat.
5. Close with a summary or takeaway.

## Camera Usage

- Use the camera to change framing, not to compensate for poor layout.
- Reserve zooms for moments where close inspection improves understanding.
- Keep camera moves smooth and purposeful.

## Minimal Scene Thinking

- Start with one object, one label, one transition.
- Add the next layer only after the base render is correct.
- Move repeated logic into helper methods once the structure is clear.
