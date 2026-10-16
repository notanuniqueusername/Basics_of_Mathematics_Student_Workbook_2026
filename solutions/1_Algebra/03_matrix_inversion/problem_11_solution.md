# Exercise 11. Parameter and Invertibility

## The question

For
$$A(t)=\begin{pmatrix}1&t\\t&1\end{pmatrix}$$
find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

## Before calculating: the concepts

Find the allowed parameter values before using an inverse formula.

## 1. Find the excluded parameters

The determinant is the product of the diagonal entries minus the product of the off-diagonal entries: $1-t^2=(1-t)(1+t)$. These factors show both excluded values explicitly. The inverse formula is valid only after those values have been removed.

## 2. Derive the parameter-dependent inverse

Compute and factor the determinant:

$$\det A(t)=1\cdot1-t\cdot t=1-t^2=(1-t)(1+t).$$

It is nonzero exactly when $\boxed{t\ne1,-1}$. For those values apply the $2\times2$ formula:

$$\boxed{A(t)^{-1}=\frac1{1-t^2}\begin{pmatrix}1&-t\\-t&1\end{pmatrix}}.$$

At $t=1$, the two rows are $(1,1)$ and $(1,1)$. At $t=-1$, they are $(1,-1)$ and $(-1,1)$, so one is the negative of the other. Both exceptional matrices have dependent rows and no inverse. The zero denominator at those values reflects that failure of existence.

## 3. Explain the exceptional cases

At $t=1$, the vector $(1,-1)^T$ is sent to zero; at $t=-1$, the vector $(1,1)^T$ is sent to zero. These nonzero vectors demonstrate why the zero denominator corresponds to a nonexistent inverse, rather than a missing numerical simplification.

## 4. Verification

For every allowed $t$, multiply explicitly:

$$A(t)A(t)^{-1}=\frac1{1-t^2}\begin{pmatrix}1-t^2&-t+t\\t-t&1-t^2\end{pmatrix}=I.$$

The same calculation in the reversed order gives $I$.

At the excluded values, $A(1)(1,-1)^T=0$ and $A(-1)(1,1)^T=0$ with nonzero inputs, independently confirming singularity. At $t=0$, the formula gives $A(0)^{-1}=I$, agreeing with $A(0)=I$.
