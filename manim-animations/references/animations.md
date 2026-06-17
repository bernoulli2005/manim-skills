# Animation Reference

Manim animations are the mechanisms that change mobjects over time.

## Main Families

- Direct appearance and disappearance: `FadeIn`, `FadeOut`, `Write`, `Create`
- Morphing and replacement: `Transform`, `ReplacementTransform`
- Emphasis: `Indicate`, `Flash`, `Circumscribe`
- Motion along paths or methods: `.animate`, `MoveAlongPath`
- Composition: `AnimationGroup`, `LaggedStart`, `Succession`

## Choosing the Right Tool

- Use `Create` for drawing a shape into existence.
- Use `Write` for text or formula reveals.
- Use `FadeIn` / `FadeOut` when the object should simply appear or vanish.
- Use `Transform` when identity should persist across a shape change.
- Use `.animate` when you are animating a direct property or method call and the intent is obvious.

## Timing Rules

- Keep `run_time` aligned with the complexity of what the viewer has to parse.
- Faster motion works for obvious transitions.
- Slower motion works for structural changes or dense math.

## Practical Advice

- Do not use a fancy animation if a simple one communicates the same idea.
- When a transition feels messy, simplify the source and target mobjects rather than forcing the animation class to do all the work.
- Staggered reveals are helpful for lists, diagrams, and network structures.

