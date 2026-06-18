# Graphing Reference

Manim provides a family of coordinate-system mobjects for plots and numeric diagrams.

## Main Coordinate Systems

- `Axes`: standard 2D axes
- `NumberPlane`: Cartesian plane with background lines
- `ThreeDAxes`: 3D coordinate axes
- `ComplexPlane`: plane specialized for complex numbers
- `PolarPlane`: polar coordinate background
- `NumberLine`: 1D axis-like representation

## Graph Primitives

- `FunctionGraph`: graph of a function over an x-range
- `ParametricFunction`: curve defined parametrically
- `ImplicitFunction`: contour-style curve defined by `f(x, y) = 0`

## Common Helpers

- `coords_to_point` / `c2p`: convert coordinates into scene points
- `get_graph_label`: place a label near a graph
- `get_area`: draw area under a curve
- `get_secant_slope_group`: visualize slope and delta changes
- `get_vertical_line` and related helpers: attach markers to graph points
- `get_T_label`: create a labeled point marker tied to a graph

## Logarithmic Scaling

- `LogBase` supports logarithmic graph scaling.
- Use it when the data spans orders of magnitude or the mathematical story is logarithmic.

## Best Practices

- Keep coordinate ranges tight enough to support the narration.
- Avoid unnecessary precision in labels.
- Use graph helpers instead of manually drawing repeated geometry.
- When the graph changes during the scene, let the coordinate system drive the derived elements.

## Example Graph Workflows

- Plot a function, label the curve, then shade a region of interest.
- Show a point moving along a curve while a coordinate readout updates.
- Compare two curves on the same axes with different styles.
- Use a number line for scalar progression or one-dimensional motion.
- Use a complex plane for rotation-and-scaling narratives.

## Data Presentation Notes

- Prefer explicit labels over visual guesswork.
- Keep the legend or key minimal and close to the plotted content.
- Use color consistently across related objects and labels.
- If the axes are decorative as well as functional, keep them visually light.

## Debugging Hints

- If a graph label is mispositioned, anchor it relative to the graph point rather than the raw scene point.
- If a dynamic graph flickers, use a more stable updater pattern or rebuild the derived object with `always_redraw`.
- If the coordinate system feels crowded, simplify the range before simplifying the visuals.
