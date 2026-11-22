# Exercise 14. Contrast: Intersection and Parallelism

## Problem Statement

From the point $`P=(0,0,1)`$, two lines are drawn with direction vectors $`v_1=(2,1,-1)`$ and $`v_2=(2,1,0)`$. For each line, analyze its position relative to the plane $`z=0`$. For the line that intersects the plane, find the intersection point. For the other line, explain how you can recognize parallelism without solving an equation.

## Theoretical Background and Concepts

- The plane $`z=0`$ has normal $`n=(0,0,1)`$.
- $`v\cdot n\neq0`$: one intersection point; $`v\cdot n=0`$: parallel (or contained, if $`P`$ is in the plane).

## Detailed Step-by-Step Solution

**Line 1:** $`v_1\cdot n=-1\neq0`$, so it intersects the plane in one point. Parametrization $`(2t,\ t,\ 1-t)`$; the condition $`z=0`$ gives $`1-t=0\Rightarrow t=1`$:

```math
\text{intersection point}=(2,1,0).
```

**Line 2:** $`v_2\cdot n=0`$: the $`z`$-coordinate of the direction is $`0`$, so moving along the line never changes $`z`$. Every point has $`z=1`$, and since $`P`$ is not in the plane ($`z=1\neq0`$), the line is **parallel to the plane and never meets it** (it stays at distance 1 above it).

**Recognition without solving:** it is enough to look at the third coordinate of the direction vector ($`v\cdot n`$). Although $`v_1`$ and $`v_2`$ differ only in this one coordinate, it decides everything.

## Verification and Consistency Checks

- $`(2,1,0)=P+1\cdot v_1`$ ✓ and $`z=0`$ ✓.
- Line 2: $`(2t,\ t,\ 1)`$, so $`z=1`$ for all $`t`$, and $`1=0`$ has no solution ✓.
