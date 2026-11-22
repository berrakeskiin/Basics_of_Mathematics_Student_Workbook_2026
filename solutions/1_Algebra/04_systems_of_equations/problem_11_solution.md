# Exercise 11. A Parameter in a System of Three Equations

## Problem Statement

Analyze the number of solutions depending on $`t`$:

```math
\begin{cases}x+y+z=1,\\x+ty+z=2,\\x+y+tz=3.\end{cases}
```

Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

## Theoretical Background and Concepts

- During elimination we divide by pivots. If a pivot depends on $`t`$, the values of $`t`$ that make it zero must be treated **separately**.
- A row $`[0\ 0\ 0\mid c\neq0]`$ means no solution; a full set of nonzero pivots means a unique solution.

## Detailed Step-by-Step Solution

```math
\left[\begin{array}{ccc|c}1&1&1&1\\1&t&1&2\\1&1&t&3\end{array}\right]\xrightarrow{R_2-R_1,\ R_3-R_1}\left[\begin{array}{ccc|c}1&1&1&1\\0&t-1&0&1\\0&0&t-1&2\end{array}\right].
```

The matrix is triangular with pivots $`1,\ t-1,\ t-1`$, so $`\det A=(t-1)^2`$.

**Case $`t\neq1`$** (we may divide by $`t-1`$):

```math
y=\frac1{t-1},\qquad z=\frac2{t-1},\qquad x=1-y-z=1-\frac3{t-1}=\frac{t-4}{t-1}.
```

**Exactly one solution.**

**Case $`t=1`$** (the division step is not allowed): the second row becomes $`[0\ 0\ 0\mid1]`$, i.e. $`0=1`$. **No solution.** (Indeed, for $`t=1`$ all three left sides equal $`x+y+z`$, but the right sides are $`1,2,3`$.)

The case "infinitely many solutions" does not occur for any $`t`$.

## Verification and Consistency Checks

Take $`t=2`$: $`y=1`$, $`z=2`$, $`x=-2`$.
- $`-2+1+2=1`$ ✓
- $`-2+2\cdot1+2=2`$ ✓
- $`-2+1+2\cdot2=3`$ ✓
