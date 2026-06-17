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

