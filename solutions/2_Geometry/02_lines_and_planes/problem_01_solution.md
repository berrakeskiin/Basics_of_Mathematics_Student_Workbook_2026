# Exercise 1. Line Through Two Points

## Problem Statement

Find the equation of the line through $`A=(1,2)`$ and $`B=(4,-1)`$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

## Theoretical Background and Concepts

- **Parametric form:** $`X=A+t\,v`$, where $`v`$ is a direction vector (e.g. $`\overrightarrow{AB}`$).
- **General form:** $`ax+by+c=0`$, where $`n=(a,b)`$ is a **normal** vector (perpendicular to the line). In the plane, if $`v=(v_1,v_2)`$, then $`n=(v_2,-v_1)`$ is perpendicular to it.

## Detailed Step-by-Step Solution

**Direction vector:** $`v=\overrightarrow{AB}=(4-1,\ -1-2)=(3,-3)`$, or more simply $`(1,-1)`$.

**Parametric form:**

```math
(x,y)=(1,2)+t(1,-1),\quad\text{i.e.}\quad x=1+t,\ y=2-t,\ t\in\mathbb R.
```

**Normal vector:** $`n=(1,1)`$, since $`n\cdot v=1-1=0`$.

**General form:** $`1\cdot(x-1)+1\cdot(y-2)=0`$, i.e.

```math
x+y-3=0.
```

(Eliminating $`t`$ from the parametric form gives the same: $`x+y=(1+t)+(2-t)=3`$.)

## Verification and Consistency Checks

- $`A=(1,2)`$: $`1+2-3=0`$ ✓ (and $`t=0`$ in the parametric form).
- $`B=(4,-1)`$: $`4-1-3=0`$ ✓ (and $`t=3`$ gives $`(4,-1)`$).
