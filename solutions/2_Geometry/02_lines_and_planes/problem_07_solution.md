# Exercise 7. A Line Relative to a Plane

## Problem Statement

For

```math
L:(x,y,z)=(1,1,0)+t(1,-1,0),\qquad \Pi:x+y+z=2,
```

determine whether the line intersects the plane at one point, is parallel to it, or lies in it. Explain the role of the dot product of the direction vector and the normal vector.

## Theoretical Background and Concepts

Let $`v`$ be the direction of the line and $`n`$ the normal of the plane.
- $`v\cdot n\neq0`$: the line crosses the plane in **one point**.
- $`v\cdot n=0`$: the line is parallel to the plane; then it either lies **in** the plane (if one of its points does) or has **no** common point.

## Detailed Step-by-Step Solution

$`v=(1,-1,0)`$, $`n=(1,1,1)`$:

```math
v\cdot n=1-1+0=0.
```

So the line is parallel to the plane or lies in it. Check the point $`P_0=(1,1,0)`$: $`1+1+0=2`$ ✓. It lies in the plane.

**Conclusion:** the line **lies in the plane**.

Algebraically: substituting $`x=1+t,\ y=1-t,\ z=0`$ gives $`(1+t)+(1-t)+0=2`$, i.e. $`2=2`$ for every $`t`$.

**Role of $`v\cdot n`$:** it measures how much the line "moves in the direction of the normal". If it is $`0`$, moving along the line never changes the value of $`x+y+z`$, so the line can never cross the plane from one side to the other.

## Verification and Consistency Checks

- $`t=5`$: point $`(6,-4,0)`$, $`6-4+0=2`$ ✓.
