# Exercise 3. When Does the Inverse Not Exist?

## The question

For
$$A=\begin{pmatrix}2&4\\1&2\end{pmatrix}$$
explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

## Before calculating: the concepts

A zero determinant and dependent rows each imply noninvertibility.

## 1. Use the determinant criterion

The determinant calculation tests invertibility numerically. If it is zero, the $2\times2$ inverse formula would involve division by zero, so that formula cannot produce an inverse. This is a failure of existence, rather than a reason to seek a different formula.

## 2. Give two explanations of noninvertibility

**Determinant argument.** Compute

$$\det A=2\cdot2-4\cdot1=4-4=0.$$

A square matrix with zero determinant has no inverse. In particular, the $2\times2$ inverse formula cannot be used because its denominator would be zero.

**Row-dependence argument.** The rows satisfy

$$(2,4)=2(1,2),\qquad R_1=2R_2.$$

Eliminate the repeated information:

$$\begin{pmatrix}2&4\\1&2\end{pmatrix}\xrightarrow{R_1\leftarrow R_1-2R_2}\begin{pmatrix}0&0\\1&2\end{pmatrix}.$$

There cannot be a pivot in both rows. The transformation loses a direction of information, so it cannot be undone. Both arguments yield $\boxed{A^{-1}\text{ does not exist}}$.

## 3. Relate the two explanations

The row dependence explains the zero determinant: replacing $R_1$ by $R_1-2R_2$ produces a zero row. It also means the two rows describe the same linear information at different scales. An inverse cannot recover information that the transformation has lost.

## 4. Verification

The nonzero vector $v=(-2,1)^T$ is sent to zero:

$$Av=\begin{pmatrix}2(-2)+4\cdot1\\1(-2)+2\cdot1\end{pmatrix}=\begin{pmatrix}0\\0\end{pmatrix}.$$

If an inverse $C$ existed, then $v=CAv=C0=0$, contradicting $v\ne0$. This checks the conclusion through the defining property of an inverse. It also gives a concrete example of the information loss identified by the dependent rows.
