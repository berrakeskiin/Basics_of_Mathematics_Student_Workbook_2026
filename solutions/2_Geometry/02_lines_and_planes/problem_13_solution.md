# Exercise 13. Closest Point on a Plane

## Problem Statement

Find the point on the plane $`x+2y+2z=4`$ closest to $`P=(3,0,0)`$. Give the distance and check that the segment joining the two points is perpendicular to the plane.

## Theoretical Background and Concepts

- The closest point $`Q`$ is the orthogonal projection: move from $`P`$ along the normal $`n=(1,2,2)`$ until the plane is reached.
- Distance: $`d=\dfrac{|ax_0+by_0+cz_0-d|}{\|n\|}`$.

## Detailed Step-by-Step Solution

Line through $`P`$ along $`n`$: $`(3+t,\ 2t,\ 2t)`$. Substitute:

```math
(3+t)+2(2t)+2(2t)=4\ \Rightarrow\ 3+9t=4\ \Rightarrow\ t=\frac19.
```

```math
Q=\left(3+\tfrac19,\ \tfrac29,\ \tfrac29\right)=\left(\tfrac{28}9,\ \tfrac29,\ \tfrac29\right).
```

**Distance:**

```math
d=\|Q-P\|=\frac19\|(1,2,2)\|=\frac19\cdot3=\frac13.
```

## Verification and Consistency Checks

- $`Q`$ on the plane: $`\frac{28}9+\frac49+\frac49=\frac{36}9=4`$ ✓.
- $`\overrightarrow{PQ}=\frac19(1,2,2)`$ is parallel to $`n`$, so the segment is perpendicular to the plane ✓.
- Formula: $`\frac{|3+0+0-4|}{\sqrt{1+4+4}}=\frac13`$ ✓.
