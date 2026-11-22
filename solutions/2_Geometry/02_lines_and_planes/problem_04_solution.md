# Exercise 4. Plane Through Three Points

## Problem Statement

Find the equation of the plane through $`A=(1,0,0)`$, $`B=(0,1,0)`$, $`C=(0,0,1)`$. First construct two vectors lying in the plane, and then use the cross product. Check the resulting equation on all three points.

## Theoretical Background and Concepts

- $`\overrightarrow{AB}`$ and $`\overrightarrow{AC}`$ lie in the plane; $`n=\overrightarrow{AB}\times\overrightarrow{AC}`$ is perpendicular to both, so it is a normal vector.
- Then the plane is $`n\cdot(X-A)=0`$.

## Detailed Step-by-Step Solution

```math
\overrightarrow{AB}=(-1,1,0),\qquad \overrightarrow{AC}=(-1,0,1).
```

```math
n=\overrightarrow{AB}\times\overrightarrow{AC}=\big(1\cdot1-0\cdot0,\ 0\cdot(-1)-(-1)\cdot1,\ (-1)\cdot0-1\cdot(-1)\big)=(1,1,1).
```

```math
1\cdot(x-1)+1\cdot y+1\cdot z=0\quad\Rightarrow\quad x+y+z=1.
```

## Verification and Consistency Checks

- $`A`$: $`1+0+0=1`$ ✓; $`B`$: $`0+1+0=1`$ ✓; $`C`$: $`0+0+1=1`$ ✓.
- $`n\cdot\overrightarrow{AB}=-1+1+0=0`$ and $`n\cdot\overrightarrow{AC}=-1+0+1=0`$ ✓.
- Intercept form: $`\frac x1+\frac y1+\frac z1=1`$, consistent with the points on the axes.
