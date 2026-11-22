# Exercise 3. Swapping Two Rows

## Problem Statement

For

```math
A=\begin{pmatrix}1&2&0\\0&3&1\\2&1&1\end{pmatrix}
```

compute $`\det A`$. Then form $`B`$ by swapping the first and second rows of $`A`$. First predict $`\det B`$ using a determinant property, then verify by calculation.

## Theoretical Background and Concepts

- Swapping two rows **changes the sign** of the determinant: $`\det B=-\det A`$.
- Cofactor expansion along the first row: $`\det A=a_{11}C_{11}+a_{12}C_{12}+a_{13}C_{13}`$, with signs $`+,-,+`$.

## Detailed Step-by-Step Solution

**$`\det A`$** (expansion along the first row):

```math
\det A=1\cdot\det\begin{pmatrix}3&1\\1&1\end{pmatrix}-2\cdot\det\begin{pmatrix}0&1\\2&1\end{pmatrix}+0=1\cdot(3-1)-2\cdot(0-2)=2+4=6.
```

**Prediction:** $`B`$ is obtained by one row swap, so $`\det B=-\det A=-6`$.

**Verification:**

```math
B=\begin{pmatrix}0&3&1\\1&2&0\\2&1&1\end{pmatrix},
```

```math
\det B=0\cdot(2-0)-3\cdot(1\cdot1-0\cdot2)+1\cdot(1\cdot1-2\cdot2)=0-3-3=-6.
```

The prediction is confirmed.

## Verification and Consistency Checks

- Sarrus' rule for $`A`$: $`(1\cdot3\cdot1+2\cdot1\cdot2+0)-(0+1\cdot1\cdot1+2\cdot0\cdot1)=7-1=6`$. ✓
- $`\det B=-6=-\det A`$, consistent with the row-swap property. ✓
