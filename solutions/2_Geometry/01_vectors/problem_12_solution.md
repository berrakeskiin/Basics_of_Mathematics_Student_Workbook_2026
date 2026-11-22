# Exercise 12. A Normal Vector to a Plane

## Problem Statement

Given $`A=(1,0,2)`$, $`B=(2,1,0)`$, $`C=(0,3,1)`$. Construct two vectors lying in the plane, find a vector perpendicular to both, and check the perpendicularity using dot products.

## Theoretical Background and Concepts

- $`\overrightarrow{AB}`$ and $`\overrightarrow{AC}`$ lie in the plane through $`A,B,C`$.
- The cross product $`n=\overrightarrow{AB}\times\overrightarrow{AC}`$ is perpendicular to both, so it is a **normal vector** of the plane.

## Detailed Step-by-Step Solution

```math
\overrightarrow{AB}=B-A=(1,1,-2),\qquad \overrightarrow{AC}=C-A=(-1,3,-1).
```

```math
n=\overrightarrow{AB}\times\overrightarrow{AC}=\big(1\cdot(-1)-(-2)\cdot3,\ (-2)\cdot(-1)-1\cdot(-1),\ 1\cdot3-1\cdot(-1)\big)=(5,3,4).
```

**Checks:**
- $`n\cdot\overrightarrow{AB}=5+3-8=0`$ ✓
- $`n\cdot\overrightarrow{AC}=-5+9-4=0`$ ✓

(As a consequence, the plane is $`5(x-1)+3y+4(z-2)=0`$, i.e. $`5x+3y+4z=13`$.)

## Verification and Consistency Checks

- All three points satisfy $`5x+3y+4z=13`$: $`A`$: $`5+0+8=13`$ ✓; $`B`$: $`10+3+0=13`$ ✓; $`C`$: $`0+9+4=13`$ ✓.
