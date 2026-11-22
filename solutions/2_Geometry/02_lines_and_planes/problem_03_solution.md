# Exercise 3. Plane Through a Point with a Given Normal Vector

## Problem Statement

Find the equation of the plane through $`P=(1,-2,3)`$ and perpendicular to $`n=(2,1,-1)`$. Check the result by substituting $`P`$ and explain the role of the normal vector.

## Theoretical Background and Concepts

- A point $`X=(x,y,z)`$ lies in the plane $`\iff`$ the vector $`\overrightarrow{PX}`$ is perpendicular to $`n`$ $`\iff n\cdot(X-P)=0`$.
- This gives $`a(x-x_0)+b(y-y_0)+c(z-z_0)=0`$ with $`n=(a,b,c)`$.

## Detailed Step-by-Step Solution

```math
2(x-1)+1\cdot(y+2)-1\cdot(z-3)=0
```

```math
2x-2+y+2-z+3=0\quad\Rightarrow\quad 2x+y-z+3=0.
```

**Role of the normal vector:** $`n`$ fixes the "tilt" of the plane: all directions inside the plane are perpendicular to $`n`$. Its coordinates become the coefficients of $`x,y,z`$. The point $`P`$ then fixes **which** of the parallel planes with this normal we take (it determines the constant).

## Verification and Consistency Checks

- $`P`$: $`2\cdot1+(-2)-3+3=0`$ ✓.
- Another point: moving from $`P`$ by $`(1,0,2)`$ (perpendicular to $`n`$, since $`2+0-2=0`$) gives $`(2,-2,5)`$: $`4-2-5+3=0`$ ✓.
