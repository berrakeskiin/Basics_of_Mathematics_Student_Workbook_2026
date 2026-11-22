# Exercise 15. Complete Classification of a Line Relative to a Plane

## Problem Statement

Let

```math
L:p+tv,\qquad \Pi:n\cdot x=d.
```

State the conditions distinguishing the three cases: one intersection point, parallel with no common points, and the line contained in the plane. Then illustrate each case with your own simple numerical example.

## Theoretical Background and Concepts

Substitute $`x=p+tv`$ into $`n\cdot x=d`$:

```math
n\cdot p+t\,(n\cdot v)=d\quad\Longleftrightarrow\quad t\,(n\cdot v)=d-n\cdot p.
```

## Detailed Step-by-Step Solution

**Classification:**

1. $`n\cdot v\neq0`$: exactly one solution $`t=\dfrac{d-n\cdot p}{n\cdot v}`$, so **one intersection point**.
2. $`n\cdot v=0`$ and $`n\cdot p\neq d`$: the equation becomes $`0=d-n\cdot p\neq0`$, no solution, so the line is **parallel with no common points**.
3. $`n\cdot v=0`$ and $`n\cdot p=d`$: the equation becomes $`0=0`$ for every $`t`$, so the **line lies in the plane**.

Geometrically: $`n\cdot v=0`$ means the direction is perpendicular to the normal (parallel to the plane); $`n\cdot p=d`$ means the starting point lies in the plane.

**Examples** with the plane $`z=0`$ ($`n=(0,0,1)`$, $`d=0`$):

1. $`p=(0,0,1)`$, $`v=(0,0,1)`$: $`n\cdot v=1\neq0`$; $`1+t=0\Rightarrow t=-1`$, point $`(0,0,0)`$.
2. $`p=(0,0,1)`$, $`v=(1,0,0)`$: $`n\cdot v=0`$, $`n\cdot p=1\neq0`$; all points have $`z=1`$, no intersection.
3. $`p=(0,0,0)`$, $`v=(1,0,0)`$: $`n\cdot v=0`$, $`n\cdot p=0=d`$; the line is the $`x`$-axis, which lies in the plane $`z=0`$.

## Verification and Consistency Checks

- The three conditions are mutually exclusive and cover all possibilities ($`n\cdot v`$ is either zero or not; if zero, $`n\cdot p`$ equals $`d`$ or not). ✓
- Each example satisfies exactly one condition, and the direct check ($`z`$-coordinate along the line) agrees with the classification. ✓
