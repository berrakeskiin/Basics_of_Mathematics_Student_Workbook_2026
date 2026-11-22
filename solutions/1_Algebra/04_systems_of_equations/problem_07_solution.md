# Exercise 7. Choosing a Method Deliberately

## Problem Statement

For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix $`\begin{cases}2x-y=3,\\4y=8;\end{cases}`$
2. three systems $`Ax=b_i`$ with the same invertible $`A`$, when $`A^{-1}`$ is already known;
3. one $`3\times3`$ system without a given inverse, where the goal is only one solution vector.

Carry out case 1 completely; for cases 2 and 3 describe the plan and which part is reusable or unnecessary.

## Theoretical Background and Concepts

- **Back-substitution** solves a triangular system directly, from the last equation upwards.
- **Using $`A^{-1}`$:** $`x_i=A^{-1}b_i`$; once $`A^{-1}`$ is known, each new right-hand side costs only one matrix–vector product.
- **Gaussian elimination** is the cheapest general method for a single system; computing $`A^{-1}`$ costs more than solving one system.

## Detailed Step-by-Step Solution

**Case 1 — back-substitution** (the matrix is already triangular, so no elimination is needed):
- $`4y=8\Rightarrow y=2`$
- $`2x-y=3\Rightarrow 2x=5\Rightarrow x=\frac52`$

```math
(x,y)=\left(\tfrac52,\ 2\right).
```

**Case 2 — multiply by the known inverse:** compute $`x_1=A^{-1}b_1`$, $`x_2=A^{-1}b_2`$, $`x_3=A^{-1}b_3`$. The expensive part (finding $`A^{-1}`$) is already done and is **reused** three times; elimination would have to be repeated (or done on $`[A\mid b_1\ b_2\ b_3]`$ at once). Equivalently, $`X=A^{-1}[\,b_1\ b_2\ b_3\,]`$.

**Case 3 — Gaussian elimination on $`[A\mid b]`$:** there is only one right-hand side and no inverse is given. Computing $`A^{-1}`$ would be **unnecessary** extra work (Gauss–Jordan on $`[A\mid I]`$ is about three times as much work as solving one system). Elimination plus back-substitution gives the answer directly.

## Verification and Consistency Checks

- Case 1: $`2\cdot\frac52-2=3`$ ✓ and $`4\cdot2=8`$ ✓.
- The choice depends on the structure (triangular, number of right-hand sides, whether $`A^{-1}`$ is known), not on the name of the method.
