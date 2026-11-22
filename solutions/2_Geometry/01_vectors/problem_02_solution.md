# Exercise 2. Distance as the Length of a Vector

## Problem Statement

The points are $`A=(1,2,3)`$ and $`B=(4,-2,6)`$. (1) Construct $`\overrightarrow{AB}`$. (2) Compute its length. (3) Compute the distance between the points using the coordinate formula. (4) Explain why both calculations give the same result.

## Theoretical Background and Concepts

- $`\overrightarrow{AB}=B-A`$ (end minus start).
- Length: $`\|w\|=\sqrt{w_1^2+w_2^2+w_3^2}`$ (Pythagorean theorem in 3D).
- Distance formula: $`d(A,B)=\sqrt{(b_1-a_1)^2+(b_2-a_2)^2+(b_3-a_3)^2}`$.

## Detailed Step-by-Step Solution

1. $`\overrightarrow{AB}=(4-1,\ -2-2,\ 6-3)=(3,-4,3)`$.
2. $`\|\overrightarrow{AB}\|=\sqrt{3^2+(-4)^2+3^2}=\sqrt{9+16+9}=\sqrt{34}\approx5.83`$.
3. $`d(A,B)=\sqrt{(4-1)^2+(-2-2)^2+(6-3)^2}=\sqrt{34}`$.
4. The distance formula is exactly the length of the difference vector $`B-A`$: its coordinates are the differences of the coordinates. So the two calculations are the same computation written in two ways.

## Verification and Consistency Checks

- $`\overrightarrow{BA}=(-3,4,-3)`$ has the same length $`\sqrt{34}`$, as distance does not depend on direction. ✓
- $`A+\overrightarrow{AB}=(1+3,2-4,3+3)=(4,-2,6)=B`$ ✓.
