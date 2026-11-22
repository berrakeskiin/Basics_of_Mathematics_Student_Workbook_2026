# Exercise 14. Closest Point on a Line

## Problem Statement

Given a point $`P=(4,1)`$ and a line through the origin with direction $`v=(1,2)`$. Using projection, find the closest point on the line, the distance from $`P`$ to the line, and verify that the appropriate vector is perpendicular to the direction of the line.

## Theoretical Background and Concepts

- The closest point $`Q`$ on the line $`\{tv\}`$ to $`P`$ is the projection $`Q=\mathrm{proj}_v P=\dfrac{P\cdot v}{v\cdot v}v`$.
- The shortest connection $`\overrightarrow{QP}=P-Q`$ is perpendicular to the line; the distance is $`\|P-Q\|`$.

## Detailed Step-by-Step Solution

```math
P\cdot v=4+2=6,\qquad v\cdot v=5,\qquad Q=\frac65(1,2)=\left(\frac65,\ \frac{12}5\right).
```

```math
\overrightarrow{QP}=P-Q=\left(4-\frac65,\ 1-\frac{12}5\right)=\left(\frac{14}5,\ -\frac75\right).
```

```math
d=\|\overrightarrow{QP}\|=\frac15\sqrt{14^2+7^2}=\frac{\sqrt{245}}5=\frac{7\sqrt5}5=\frac7{\sqrt5}\approx3.13.
```

**Perpendicularity:** $`\overrightarrow{QP}\cdot v=\frac{14}5-\frac{14}5=0`$ ✓.

## Verification and Consistency Checks

- Line equation: points $`t(1,2)`$ satisfy $`2x-y=0`$. Point–line distance formula: $`\dfrac{|2\cdot4-1|}{\sqrt{2^2+1^2}}=\dfrac7{\sqrt5}`$ ✓.
- Any other point, e.g. $`(1,2)`$, is farther: $`\|(3,-1)\|=\sqrt{10}\approx3.16>3.13`$ ✓.
