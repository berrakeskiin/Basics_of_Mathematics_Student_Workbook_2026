# Exercise 13. Does Every Equation Add New Information?

## Problem Statement

Consider the system

```math
x_1+x_2=10,\qquad x_2+x_3=8,\qquad x_1-x_3=2.
```

Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

## Theoretical Background and Concepts

- An equation is **redundant** if it is a linear combination of the others; it adds no new condition.
- In elimination, a redundant equation becomes a row $`[0\ 0\ 0\mid0]`$.

## Detailed Step-by-Step Solution

```math
\left[\begin{array}{ccc|c}1&1&0&10\\0&1&1&8\\1&0&-1&2\end{array}\right]\xrightarrow{R_3-R_1}\left[\begin{array}{ccc|c}1&1&0&10\\0&1&1&8\\0&-1&-1&-8\end{array}\right]\xrightarrow{R_3+R_2}\left[\begin{array}{ccc|c}1&1&0&10\\0&1&1&8\\0&0&0&0\end{array}\right].
```

The third row became $`0=0`$: the third equation is redundant. Indeed:

```math
(x_1+x_2)-(x_2+x_3)=x_1-x_3\quad\text{and}\quad 10-8=2,
```

so equation 3 = equation 1 $`-`$ equation 2.

**Solution:** $`x_3=t`$ is free, $`x_2=8-t`$, $`x_1=10-x_2=2+t`$:

```math
(x_1,x_2,x_3)=(2+t,\ 8-t,\ t),\qquad t\in\mathbb R.
```

Only two of the three equations are needed; the solution set is a line.

## Verification and Consistency Checks

Take $`t=3`$: $`(5,5,3)`$.
- $`5+5=10`$ ✓
- $`5+3=8`$ ✓
- $`5-3=2`$ ✓
