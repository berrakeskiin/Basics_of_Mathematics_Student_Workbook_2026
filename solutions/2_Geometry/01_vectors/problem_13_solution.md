# Exercise 13. Do Four Points Lie in One Plane?

## Problem Statement

Given $`A=(0,0,0)`$, $`B=(1,2,0)`$, $`C=(0,1,1)`$, $`D=(2,5,1)`$. (1) Construct $`\overrightarrow{AB}`$ and $`\overrightarrow{AC}`$. (2) Find $`n=\overrightarrow{AB}\times\overrightarrow{AC}`$. (3) Construct $`\overrightarrow{AD}`$ and check whether $`\overrightarrow{AD}\cdot n=0`$. (4) Decide whether $`D`$ lies in the plane of $`A,B,C`$ and justify the criterion.

## Theoretical Background and Concepts

- $`n=\overrightarrow{AB}\times\overrightarrow{AC}`$ is perpendicular to the plane $`ABC`$.
- **Criterion:** $`D`$ lies in that plane $`\iff\overrightarrow{AD}\perp n\iff\overrightarrow{AD}\cdot n=0`$ (the plane consists exactly of the points $`X`$ with $`\overrightarrow{AX}\cdot n=0`$).

## Detailed Step-by-Step Solution

1. $`\overrightarrow{AB}=(1,2,0)`$, $`\overrightarrow{AC}=(0,1,1)`$.
2. ```math
n=(2\cdot1-0\cdot1,\ 0\cdot0-1\cdot1,\ 1\cdot1-2\cdot0)=(2,-1,1).
```
3. $`\overrightarrow{AD}=(2,5,1)`$, and

```math
\overrightarrow{AD}\cdot n=2\cdot2+5\cdot(-1)+1\cdot1=4-5+1=0.
```

4. Since $`\overrightarrow{AD}\cdot n=0`$, the vector $`\overrightarrow{AD}`$ is perpendicular to the normal, so it lies in the plane. **All four points are coplanar.**

## Verification and Consistency Checks

- Direct confirmation: $`\overrightarrow{AD}=2\overrightarrow{AB}+\overrightarrow{AC}=(2,4,0)+(0,1,1)=(2,5,1)`$ ✓, so $`D`$ is reached by moving within the plane.
- The plane equation is $`2x-y+z=0`$; $`D`$: $`4-5+1=0`$ ✓.
