# Exercise 10. Projection of a Point onto a Plane

## Problem Statement

Find the orthogonal projection of $`P=(2,1,3)`$ onto the plane $`x+y+z=3`$, and then find the reflection of $`P`$ across this plane. Check that the midpoint of the segment joining the point and its reflection lies on the plane.

## Theoretical Background and Concepts

- Move from $`P`$ along the normal $`n=(1,1,1)`$: the line $`P+t\,n`$ meets the plane at the projection $`P'`$.
- The reflection is $`P''=P+2(P'-P)`$ (go twice as far); $`P'`$ is then the midpoint of $`PP''`$.

## Detailed Step-by-Step Solution

Line through $`P`$ along $`n`$: $`(2+t,\ 1+t,\ 3+t)`$. Substitute into the plane:

```math
(2+t)+(1+t)+(3+t)=3\ \Rightarrow\ 6+3t=3\ \Rightarrow\ t=-1.
```

**Projection:**

```math
P'=(2-1,\ 1-1,\ 3-1)=(1,0,2).
```

**Reflection** ($`t=-2`$):

```math
P''=(2-2,\ 1-2,\ 3-2)=(0,-1,1).
```

## Verification and Consistency Checks

- $`P'`$ on the plane: $`1+0+2=3`$ ✓.
- Midpoint of $`PP''`$: $`\left(\frac{2+0}2,\ \frac{1-1}2,\ \frac{3+1}2\right)=(1,0,2)=P'`$, and it lies on the plane ✓.
- $`P-P'=(1,1,1)`$ is parallel to $`n`$, so the segment is perpendicular to the plane ✓. Distance $`=\sqrt3`$, which matches $`\frac{|2+1+3-3|}{\sqrt3}=\sqrt3`$ ✓.
