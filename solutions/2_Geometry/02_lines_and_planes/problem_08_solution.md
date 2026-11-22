# Exercise 8. Intersection Point of a Line and a Plane

## Problem Statement

Find the intersection point of $`(x,y,z)=(1,0,2)+t(1,2,-1)`$ with the plane $`x+y+z=4`$. Check the result by substituting it into both descriptions.

## Theoretical Background and Concepts

- Substitute the parametric coordinates into the plane equation. This gives one linear equation for $`t`$.
- A unique $`t`$ exists because $`v\cdot n=1+2-1=2\neq0`$.

## Detailed Step-by-Step Solution

$`x=1+t,\ y=2t,\ z=2-t`$:

```math
(1+t)+2t+(2-t)=4\ \Rightarrow\ 3+2t=4\ \Rightarrow\ t=\frac12.
```

```math
(x,y,z)=\left(1+\tfrac12,\ 2\cdot\tfrac12,\ 2-\tfrac12\right)=\left(\tfrac32,\ 1,\ \tfrac32\right).
```

## Verification and Consistency Checks

- Plane: $`\frac32+1+\frac32=4`$ ✓.
- Line: $`\left(\frac32,1,\frac32\right)-(1,0,2)=\left(\frac12,1,-\frac12\right)=\frac12(1,2,-1)`$ ✓, so the point is on the line with $`t=\frac12`$.
