# Exercise 2. Formula for a 2×2 Matrix

## The question

Find the inverse of
$$A=\begin{pmatrix}3&2\\5&4\end{pmatrix}$$
using the formula for a $2\times2$ matrix. At the end, check the result by computing one product with $A$.

## Before calculating: the concepts

For $M=\begin{pmatrix}a&b\\c&d\end{pmatrix}$, $M^{-1}=\frac1{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$ if $ad-bc\ne0$.

## 1. Check the denominator first

Read $a=3$, $b=2$, $c=5$, and $d=4$. The inverse formula requires $ad-bc\ne0$, so its denominator must be checked before dividing. A common error is to negate the diagonal entries instead of swapping them; only the off-diagonal entries are negated.

## 2. Build the inverse using the formula

For $A=\begin{pmatrix}a&b\\c&d\end{pmatrix}$, first compute $\Delta=ad-bc$. Here

$$\Delta=3\cdot4-2\cdot5=12-10=2\ne0.$$

The inverse therefore exists. Swap $a$ and $d$, negate $b$ and $c$, and divide the entire matrix by $\Delta$:

$$\boxed{A^{-1}=\frac12\begin{pmatrix}4&-2\\-5&3\end{pmatrix}=\begin{pmatrix}2&-1\\-5/2&3/2\end{pmatrix}}.$$

The reciprocal factor applies to every entry, including the negative ones.

## 3. Explain the factor outside the matrix

The factor $1/2$ multiplies every entry of the numerator matrix. It may stay outside the matrix during the multiplication check. The numerator product must therefore be $2I$, which becomes $I$ after multiplying by $1/2$.

## 4. Verification

Calculate a full product, retaining the factor outside until the end:

$$AA^{-1}=\frac12\begin{pmatrix}3\cdot4+2(-5)&3(-2)+2\cdot3\\5\cdot4+4(-5)&5(-2)+4\cdot3\end{pmatrix}=\frac12\begin{pmatrix}2&0\\0&2\end{pmatrix}=I.$$

An additional scalar check is

$$\det(A^{-1})=2\cdot\frac32-(-1)\left(-\frac52\right)=3-\frac52=\frac12=\frac1{\det A}.$$

The product verifies the inverse itself; the determinant check is a useful consistency test but would not prove the inverse on its own.
