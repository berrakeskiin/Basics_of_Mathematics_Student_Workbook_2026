# Exercise 9. Distances

## Problem Statement

Compute: (1) the distance from $`P=(2,3)`$ to the line $`3x+4y-10=0`$; (2) the distance from $`Q=(2,-1,3)`$ to the plane $`2x-2y+z-4=0`$. Compare the two formulas and explain their common connection with the normal direction.

## Theoretical Background and Concepts

```math
d(P,\ ax+by+c=0)=\frac{|ax_0+by_0+c|}{\sqrt{a^2+b^2}},\qquad d(Q,\ ax+by+cz+d=0)=\frac{|ax_0+by_0+cz_0+d|}{\sqrt{a^2+b^2+c^2}}.
```

## Detailed Step-by-Step Solution

**1. Point–line:**

```math
d=\frac{|3\cdot2+4\cdot3-10|}{\sqrt{9+16}}=\frac{|6+12-10|}{5}=\frac85=1.6.
```

**2. Point–plane:**

```math
d=\frac{|2\cdot2-2\cdot(-1)+3-4|}{\sqrt{4+4+1}}=\frac{|4+2+3-4|}{3}=\frac53.
```

**Common idea:** both formulas are the same: substitute the point into the equation and divide by the length of the normal vector $`n`$ ($`(3,4)`$ or $`(2,-2,1)`$). The shortest path from a point to a line (in 2D) or a plane (in 3D) goes **along the normal**. The numerator measures how far the point is from satisfying the equation, and dividing by $`\|n\|`$ turns this into an actual length.

## Verification and Consistency Checks

- (1) Foot of the perpendicular: $`P-\frac{8}{25}(3,4)=(1.04,\ 1.72)`$, and $`3\cdot1.04+4\cdot1.72=3.12+6.88=10`$ ✓; the step length is $`\frac8{25}\cdot5=1.6`$ ✓.
- (2) Foot: $`Q-\frac59(2,-2,1)`$; its length is $`\frac59\cdot3=\frac53`$ ✓.
