# Exercise 10. Inverse of a Diagonal Matrix

## The question

Given
$$D=\begin{pmatrix}2&0&0\\0&-3&0\\0&0&5\end{pmatrix},\qquad E=\begin{pmatrix}2&0&0\\0&0&0\\0&0&5\end{pmatrix}.$$
Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

## Before calculating: the concepts

A diagonal matrix is invertible exactly when every diagonal entry is nonzero. Its inverse contains their reciprocals.

## 1. Inspect the diagonal entries

A diagonal matrix sends each coordinate to that coordinate multiplied by its diagonal entry. Nonzero factors can be undone by reciprocals. A zero factor sends a whole coordinate direction to zero and cannot be undone.

## 2. Decide existence and give the inverse

For $D$, all three diagonal entries $2,-3,5$ are nonzero. Recover the coordinates by dividing by those numbers:

$$\boxed{D^{-1}=\begin{pmatrix}1/2&0&0\\0&-1/3&0\\0&0&1/5\end{pmatrix}}.$$

The negative sign of $-3$ remains in its reciprocal $-1/3$.

For $E$, the middle diagonal entry is $0$. In particular,

$$E\begin{pmatrix}x\\y\\z\end{pmatrix}=\begin{pmatrix}2x\\0\\5z\end{pmatrix}.$$

The output contains no information about $y$, so that coordinate cannot be recovered. Thus $\boxed{E\text{ is not invertible}}$. Neither conclusion requires Gauss–Jordan elimination.

## 3. Explain the singular matrix geometrically

The matrix $E$ sends all vectors $(0,s,0)^T$ to zero. Different values of $s$ therefore give the same output. No inverse transformation can determine which of those inputs was used. By contrast, each coordinate of $D$ can be recovered separately.

## 4. Verification

Multiplying diagonal matrices multiplies corresponding diagonal entries:

$$DD^{-1}=\begin{pmatrix}2(1/2)&0&0\\0&(-3)(-1/3)&0\\0&0&5(1/5)\end{pmatrix}=I_3,$$

and $D^{-1}D=I_3$ as well.

For $E$, the nonzero vector $(0,1,0)^T$ is sent to zero, confirming the failure of an inverse. The determinant test agrees: $\det D=2(-3)5=-30\ne0$, whereas $\det E=2\cdot0\cdot5=0$.
