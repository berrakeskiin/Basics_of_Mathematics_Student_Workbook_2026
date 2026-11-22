# Exercise 8. Row Operations and Their Reversibility

## Problem Statement

For

```math
A=\begin{pmatrix}1&2&-1\\2&4&1\\-1&1&3\end{pmatrix}
```

perform, in order: (1) $`R_2\leftarrow R_2-2R_1`$, (2) $`R_3\leftarrow R_3+R_1`$, (3) interchange $`R_2`$ and $`R_3`$.
Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

## Theoretical Background and Concepts

There are three elementary row operations, and each one is reversible by an operation of the same type:
- adding a multiple of a row, $`R_i\leftarrow R_i+kR_j`$, is reversed by $`R_i\leftarrow R_i-kR_j`$;
- swapping rows, $`R_i\leftrightarrow R_j`$, is reversed by doing the same swap again;
- scaling a row, $`R_i\leftarrow cR_i`$ with $`c\neq0`$, is reversed by $`R_i\leftarrow \frac1c R_i`$.

Because they are reversible, row operations never lose information. That is why elimination can be used to solve systems.

## Detailed Step-by-Step Solution

**Step 1:** $`R_2\leftarrow R_2-2R_1`$: $`(2,4,1)-2(1,2,-1)=(0,0,3)`$

```math
\begin{pmatrix}1&2&-1\\0&0&3\\-1&1&3\end{pmatrix}
```

**Step 2:** $`R_3\leftarrow R_3+R_1`$: $`(-1,1,3)+(1,2,-1)=(0,3,2)`$

```math
\begin{pmatrix}1&2&-1\\0&0&3\\0&3&2\end{pmatrix}
```

**Step 3:** $`R_2\leftrightarrow R_3`$

```math
\begin{pmatrix}1&2&-1\\0&3&2\\0&0&3\end{pmatrix}
```

(upper triangular form)

**Reversing operations:**
1. $`R_2\leftarrow R_2-2R_1`$ is reversed by $`R_2\leftarrow R_2+2R_1`$.
2. $`R_3\leftarrow R_3+R_1`$ is reversed by $`R_3\leftarrow R_3-R_1`$.
3. $`R_2\leftrightarrow R_3`$ is reversed by $`R_2\leftrightarrow R_3`$ (the same swap).

To get back to $`A`$ from the final matrix, apply the reverses in **opposite order**: first swap $`R_2,R_3`$, then $`R_3\leftarrow R_3-R_1`$, then $`R_2\leftarrow R_2+2R_1`$.

## Verification and Consistency Checks

- Undoing: final matrix → swap → $`\begin{pmatrix}1&2&-1\\0&0&3\\0&3&2\end{pmatrix}`$ → $`R_3-R_1=(-1,1,3)`$ → $`R_2+2R_1=(2,4,1)`$, which gives back $`A`$. ✓
- Determinant check: $`\det A=1(12-1)-2(6+1)+(-1)(2+4)=11-14-6=-9`$. Adding a multiple of a row does not change the determinant, and a swap changes the sign, so the final matrix should have determinant $`+9`$: $`1\cdot3\cdot3=9`$. ✓
