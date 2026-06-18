---
name: manim-graphing
description: Manim graphing and coordinate-system workflows for Axes, NumberPlane, NumberLine, FunctionGraph, ParametricFunction, ImplicitFunction, ComplexPlane, PolarPlane, and chart-style visualizations.
---

# Manim Graphing

## Overview

Use this skill when the scene is built around axes, curves, coordinate systems, or plotted data. It covers 2D and 3D coordinate tools, graph helpers, and the most common plotting patterns in Manim.

## Use This Skill For

- `Axes`, `NumberPlane`, `ThreeDAxes`
- `NumberLine`, `ComplexPlane`, `PolarPlane`
- `FunctionGraph`, `ParametricFunction`, `ImplicitFunction`
- Graph labels, secant lines, areas, and coordinate readouts
- Logarithmic scales
- Coordinate conversion helpers like `coords_to_point`

## Core Approach

1. Choose the coordinate system that matches the idea.
   - Cartesian, polar, complex, or 3D.
2. Define ranges deliberately.
   - Keep the visible range focused on the explanation.
3. Build the graph from the system.
   - Add labels, markers, and annotations only after the base structure is readable.
4. Use helpers for derived geometry.
   - Areas, tangent lines, secants, and coordinate markers should be generated from the axes, not guessed by hand.

## Coordinate Systems

- `Axes`
  - The default choice for Cartesian plots.
- `NumberPlane`
  - Best when you want a full background grid.
- `ThreeDAxes`
  - Use for 3D coordinates and spatial diagrams.
- `ComplexPlane`
  - Use for complex numbers and complex-plane visualizations.
- `PolarPlane`
  - Use for radial or angular representations.
- `NumberLine`
  - Best for scalar emphasis or 1D motion.

## Graphing Rules

- Use `FunctionGraph` for standard function curves.
- Use `ParametricFunction` for paths defined parametrically.
- Use `ImplicitFunction` for level-set style plots.
- Use `LogBase` when the graph requires logarithmic scaling.
- Use helper methods for labels and tangent or secant constructions when they reinforce the math.

## Practical Advice

- Keep the axes and labels legible.
- Avoid overloading a graph with too many markers.
- If the graph is dynamically changing, pair it with updaters or `always_redraw`.
- The graph should teach the relationship, not just display the equation.

## Common Graph Recipes

- Plot a function, label the curve, then shade a region of interest.
- Show a point moving along a curve while a coordinate readout updates.
- Compare two curves on the same axes with different styles.
- Use a number line for scalar progression or one-dimensional motion.
- Use a complex plane for rotation-and-scaling narratives.

## Coordinate Selection

- Choose `Axes` for standard algebra, calculus, and general explainer plots.
- Choose `NumberPlane` when the grid is part of the visual language.
- Choose `ComplexPlane` when the story is about complex numbers or transformations.
- Choose `PolarPlane` when radial or angular meaning is central.
- Choose `ThreeDAxes` only if 3D geometry is essential to the explanation.

## Debugging Hints

- If a graph is clipped, expand the coordinate range before adjusting decorations.
- If labels overlap, move the labels after the graph is correct.
- If a dynamic graph flickers, rebuild the derived object with `always_redraw`.
- If the scene feels busy, reduce the number of annotations before changing the plot itself.

## References

- [Coordinate system reference](references/graphing.md)
