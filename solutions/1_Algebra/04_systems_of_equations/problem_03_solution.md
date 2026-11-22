# Exercise 3. Inconsistent System

## Problem Statement

Solve or show that the system is inconsistent:

```math
\begin{cases}x+2y=3,\\2x+4y=7.\end{cases}
```

Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

## Theoretical Background and Concepts

- If elimination produces a row $`[\,0\ \ 0\mid c\,]`$ with $`c\neq0`$, it means the equation $`0=c`$, which is false. Then the system is **inconsistent** (no solution).

## Detailed Step-by-Step Solution

```math
\left[\begin{array}{cc|c}1&2&3\\2&4&7\end{array}\right]\xrightarrow{R_2-2R_1}\left[\begin{array}{cc|c}1&2&3\\0&0&1\end{array}\right].
```

The second row means $`0\cdot x+0\cdot y=1`$, i.e. $`0=1`$, which is impossible. **The system has no solution.**

**Interpretation:** the left side of the second equation is exactly twice the left side of the first ($`2x+4y=2(x+2y)`$). If $`x+2y=3`$, then $`2x+4y`$ must be $`6`$, but the system demands $`7`$. Geometrically, these are two **parallel, distinct lines** ($`y=\frac{3-x}2`$ and $`y=\frac{7-2x}4`$ have the same slope $`-\frac12`$ but different intercepts $`\frac32`$ and $`\frac74`$).

## Verification and Consistency Checks

- $`\det\begin{pmatrix}1&2\\2&4\end{pmatrix}=0`$, so a unique solution is impossible; together with the contradiction this confirms "no solution". ✓
