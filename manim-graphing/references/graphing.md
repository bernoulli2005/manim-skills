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

