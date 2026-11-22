# Exercise 2. Gaussian Elimination — One Solution

## Problem Statement

Solve using Gaussian elimination:

```math
\begin{cases}x+y+z=6,\\2x-y+z=3,\\x+2y-z=2.\end{cases}
```

After solving, substitute the result into all equations and check consistency.

## Theoretical Background and Concepts

- **Gaussian elimination:** use row operations on the augmented matrix $`[A\mid b]`$ to reach row echelon form, then solve from the bottom up (back-substitution).
- Row operations do not change the set of solutions.

## Detailed Step-by-Step Solution

```math
\left[\begin{array}{ccc|c}1&1&1&6\\2&-1&1&3\\1&2&-1&2\end{array}\right]
```

$`R_2\leftarrow R_2-2R_1`$, $`R_3\leftarrow R_3-R_1`$:

```math
\left[\begin{array}{ccc|c}1&1&1&6\\0&-3&-1&-9\\0&1&-2&-4\end{array}\right]
```

$`R_2\leftrightarrow R_3`$, then $`R_3\leftarrow R_3+3R_2`$:

```math
\left[\begin{array}{ccc|c}1&1&1&6\\0&1&-2&-4\\0&0&-7&-21\end{array}\right]
```

Back-substitution:
- $`-7z=-21\Rightarrow z=3`$
- $`y-2z=-4\Rightarrow y=-4+6=2`$
- $`x+y+z=6\Rightarrow x=6-2-3=1`$

**Solution:** $`(x,y,z)=(1,2,3)`$.

## Verification and Consistency Checks

- $`1+2+3=6`$ ✓
- $`2\cdot1-2+3=3`$ ✓
- $`1+2\cdot2-3=2`$ ✓

All three equations are satisfied, and the echelon form has 3 pivots, so the solution is unique.
