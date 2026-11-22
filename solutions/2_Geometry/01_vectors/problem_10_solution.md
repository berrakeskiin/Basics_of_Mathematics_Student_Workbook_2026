# Exercise 10. Triangle Area from Vectors

## Problem Statement

The points $`A=(0,0,0)`$, $`B=(2,1,0)`$, $`C=(1,3,2)`$ form a triangle. Construct $`\overrightarrow{AB}`$ and $`\overrightarrow{AC}`$, compute the area of the parallelogram using the cross product, and then find the area of the triangle. Explain the factor $`\frac12`$.

## Theoretical Background and Concepts

- Area of the parallelogram spanned by $`a,b`$: $`\|a\times b\|`$.
- The diagonal $`BC`$ cuts the parallelogram $`ABDC`$ into two congruent triangles, so the area of triangle $`ABC`$ is $`\frac12\|\overrightarrow{AB}\times\overrightarrow{AC}\|`$.

## Detailed Step-by-Step Solution

```math
\overrightarrow{AB}=(2,1,0),\qquad \overrightarrow{AC}=(1,3,2).
```

```math
\overrightarrow{AB}\times\overrightarrow{AC}=(1\cdot2-0\cdot3,\ 0\cdot1-2\cdot2,\ 2\cdot3-1\cdot1)=(2,-4,5).
```

```math
\text{parallelogram}=\sqrt{2^2+(-4)^2+5^2}=\sqrt{45}=3\sqrt5\approx6.71.
```

```math
\text{triangle}=\frac12\cdot3\sqrt5=\frac{3\sqrt5}{2}\approx3.35.
```

**Factor $`\frac12`$:** the triangle is exactly half of the parallelogram built on the same two edges.

## Verification and Consistency Checks

- $`(2,-4,5)\cdot(2,1,0)=4-4+0=0`$ and $`(2,-4,5)\cdot(1,3,2)=2-12+10=0`$ ✓ (perpendicular to both edges).
- Lagrange: $`\|AB\|^2\|AC\|^2-(AB\cdot AC)^2=5\cdot14-5^2=45`$ ✓.
