# Exercise 13. Undoing a Composite Transformation

## Problem Statement

The matrices

```math
S=\begin{pmatrix}2&0\\0&1\end{pmatrix},\qquad H=\begin{pmatrix}1&1\\0&1\end{pmatrix}
```

describe nonuniform scaling and shear. For $`T=HS`$, find $`T^{-1}`$ in two ways: (1) compute $`T`$, then its inverse; (2) use $`(HS)^{-1}=S^{-1}H^{-1}`$. Compare the results. Also compute $`H^{-1}S^{-1}`$ and verify that the incorrect order gives a different matrix. Explain the rule "when undoing a composition of operations, we undo them from the end".

## Theoretical Background and Concepts

- $`Tx=H(Sx)`$: first scaling $`S`$, then shear $`H`$.
- $`(HS)^{-1}=S^{-1}H^{-1}`$.
- $`S^{-1}=\begin{pmatrix}\frac12&0\\0&1\end{pmatrix}`$, $`H^{-1}=\begin{pmatrix}1&-1\\0&1\end{pmatrix}`$ (shear back).

## Detailed Step-by-Step Solution

**Way 1:**

```math
T=HS=\begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}2&0\\0&1\end{pmatrix}=\begin{pmatrix}2&1\\0&1\end{pmatrix},\qquad \det T=2,
```

```math
T^{-1}=\frac12\begin{pmatrix}1&-1\\0&2\end{pmatrix}=\begin{pmatrix}\frac12&-\frac12\\0&1\end{pmatrix}.
```

**Way 2:**

```math
S^{-1}H^{-1}=\begin{pmatrix}\frac12&0\\0&1\end{pmatrix}\begin{pmatrix}1&-1\\0&1\end{pmatrix}=\begin{pmatrix}\frac12&-\frac12\\0&1\end{pmatrix}.
```

Both ways give the same $`T^{-1}`$.

**Incorrect order:**

```math
H^{-1}S^{-1}=\begin{pmatrix}1&-1\\0&1\end{pmatrix}\begin{pmatrix}\frac12&0\\0&1\end{pmatrix}=\begin{pmatrix}\frac12&-1\\0&1\end{pmatrix}\neq T^{-1}.
```

**The rule:** $`T`$ first scales and then shears. To return, we must first remove the **last** operation (the shear, $`H^{-1}`$) and only then the first one (the scaling, $`S^{-1}`$). Written as a product acting on $`x`$, this is $`S^{-1}H^{-1}x`$.

## Verification and Consistency Checks

```math
TT^{-1}=\begin{pmatrix}2&1\\0&1\end{pmatrix}\begin{pmatrix}\frac12&-\frac12\\0&1\end{pmatrix}=\begin{pmatrix}1&-1+1\\0&1\end{pmatrix}=I.
```

✓ With the wrong order: $`T\cdot H^{-1}S^{-1}=\begin{pmatrix}1&-1\\0&1\end{pmatrix}\neq I`$. ✓
