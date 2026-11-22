# Exercise 14. A Small Change in the Right-Hand Side

## Problem Statement

Compare the systems

```math
\begin{cases}x+y=2,\\2x-y=1,\\3x=3\end{cases}\qquad\text{and}\qquad\begin{cases}x+y=2,\\2x-y=1,\\3x=3.1.\end{cases}
```

Check the consistency of each system and explain why a small change in one number can change the type of the system.

## Theoretical Background and Concepts

- With 3 equations and 2 unknowns, the system is consistent only if the extra equation **agrees** with the others.
- Consistency is a yes/no property: either the equations agree exactly, or there is a contradiction. There is no "almost consistent".

## Detailed Step-by-Step Solution

The first two equations: adding them gives $`3x=3\Rightarrow x=1`$, then $`y=2-1=1`$. So they alone have the unique solution $`(1,1)`$.

**System 1:** the third equation $`3x=3`$ gives $`x=1`$, which agrees. **Consistent, unique solution $`(1,1)`$.** The third equation is actually the sum of the first two, so it is redundant.

**System 2:** the third equation gives $`x=\frac{3.1}3\approx1.033`$, but the first two require $`x=1`$. In elimination: $`R_3-(R_1+R_2)`$ gives $`0=3.1-3=0.1`$, a contradiction. **Inconsistent, no solution.**

**Why a small change matters:** the left side of equation 3 equals the sum of the left sides of equations 1 and 2. The system is consistent only if the right sides satisfy the **same** relation, $`b_3=b_1+b_2=3`$. Any change of $`b_3`$, however small, breaks this exact equality. Geometrically, three lines must pass through one common point; moving one line slightly makes them form a small triangle instead.

## Verification and Consistency Checks

- $`(1,1)`$ in system 1: $`2=2`$, $`1=1`$, $`3=3`$ ✓.
- $`(1,1)`$ in system 2: the third equation gives $`3\neq3.1`$ ✗, as expected.
