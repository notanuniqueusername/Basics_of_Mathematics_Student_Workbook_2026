# Exercise 3. Swapping Two Rows

## The question

For
$$A=\begin{pmatrix}1&2&0\\0&3&1\\2&1&1\end{pmatrix}$$
compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.

First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

## Before calculating: the concepts

Swapping two rows multiplies the determinant by $-1$. Cofactor signs along the first row are $+,-,+$.

## 1. Compute before swapping

First find the determinant of the original matrix. Expansion along its first row is short because the third entry is zero, so only two cofactors contribute. Remember that the second cofactor is subtracted.

## 2. Form the swapped matrix and predict its determinant

Expand along the first row. Its third entry is zero, and the cofactor signs are $+,-,+$:

$$\det A=1\det\begin{pmatrix}3&1\\1&1\end{pmatrix}-2\det\begin{pmatrix}0&1\\2&1\end{pmatrix}+0.$$

Compute the two minors separately:

$$3\cdot1-1\cdot1=2,\qquad 0\cdot1-1\cdot2=-2.$$

Therefore $\det A=1(2)-2(-2)=\boxed{6}$.

Swapping rows one and two gives

$$B=\begin{pmatrix}0&3&1\\1&2&0\\2&1&1\end{pmatrix}.$$

Before calculating its determinant, predict $\boxed{\det B=-\det A=-6}$ because exactly one row swap was performed.

## 3. Explain the sign change

A single row swap reverses the orientation represented by a determinant, so the sign changes once. It does not multiply the magnitude by any additional factor. The independent calculation of $B$ below is a check of the prediction, rather than the reason for making it.

## 4. Verification

Expand $B$ along its first row, retaining the negative cofactor sign at position $(1,2)$:

$$\det B=0-3\det\begin{pmatrix}1&0\\2&1\end{pmatrix}+1\det\begin{pmatrix}1&2\\2&1\end{pmatrix}.$$

Hence

$$\det B=-3(1\cdot1-0\cdot2)+(1\cdot1-2\cdot2)=-3-3=-6.$$

This confirms the sign prediction. Swapping those same rows back would change $-6$ to $6$, recovering the original determinant.
