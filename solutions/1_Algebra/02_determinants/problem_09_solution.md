# Exercise 9. Area and the Determinant

## Problem Statement

The vectors $`u=\begin{pmatrix}3\\1\end{pmatrix}`$, $`v=\begin{pmatrix}1\\4\end{pmatrix}`$ span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

## Theoretical Background and Concepts

- The area of the parallelogram spanned by $`u,v\in\mathbb R^2`$ is $`\left|\det[\,u\ v\,]\right|`$ (the vectors are the columns).
- The **sign** of the determinant gives the orientation: positive if turning from $`u`$ to $`v`$ is counterclockwise, negative if clockwise.

## Detailed Step-by-Step Solution

```math
\det[\,u\ v\,]=\det\begin{pmatrix}3&1\\1&4\end{pmatrix}=3\cdot4-1\cdot1=11.
```

**Area** $`=|11|=11`$.

**Reversed order:**

```math
\det[\,v\ u\,]=\det\begin{pmatrix}1&3\\4&1\end{pmatrix}=1\cdot1-3\cdot4=-11.
```

**Area** $`=|-11|=11`$.

**What changes and what does not:** swapping the two columns changes the **sign** of the determinant (the orientation is reversed), but the **area** is the absolute value, so it stays $`11`$. It is the same parallelogram.

## Verification and Consistency Checks

- Alternative formula: area $`=|u|\,|v|\sin\theta`$. $`|u|^2=10`$, $`|v|^2=17`$, $`u\cdot v=7`$, so $`(\text{area})^2=|u|^2|v|^2-(u\cdot v)^2=170-49=121`$, giving area $`=11`$. ✓
