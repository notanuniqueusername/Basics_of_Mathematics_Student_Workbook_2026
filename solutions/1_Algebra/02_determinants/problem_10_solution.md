# Exercise 10. Detecting Dependence

## The question

Without carrying out a full determinant calculation, explain why
$$\det\begin{pmatrix}1&2&3\\2&4&6\\0&1&5\end{pmatrix}=0.$$
Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

## Before calculating: the concepts

Linearly dependent rows force the determinant to vanish and prevent a square matrix from being invertible.

## 1. Look for an exact row relation

Compare the entries of the first two rows before expanding anything. Every entry of row two is twice the corresponding entry of row one. Thus $R_2-2R_1=0$ is an explicit dependence, not merely a visual resemblance.

## 2. Use the dependence to obtain a zero row

Compare the first two rows entry by entry:

$$2(1,2,3)=(2,4,6),\qquad R_2=2R_1.$$

This is the explicit dependence $R_2-2R_1=0$. Replace row two by that difference:

$$\begin{pmatrix}1&2&3\\2&4&6\\0&1&5\end{pmatrix}\longrightarrow\begin{pmatrix}1&2&3\\0&0&0\\0&1&5\end{pmatrix}.$$

The replacement preserves the determinant. A zero row forces the determinant to be zero, since every determinant term contains one entry from that row. Therefore $\boxed{\det A=0}$, so the matrix is not invertible. No full determinant expansion is required.

## 3. Connect dependence with loss of an inverse

An invertible square matrix must have independent rows. Here one row supplies no new information, so elimination cannot give a pivot in every row. This explains why the zero determinant and noninvertibility express the same underlying failure.

## 4. Verification

To check the loss of invertibility directly, choose $v=(7,-5,1)^T$. Then

$$Av=\begin{pmatrix}1\cdot7+2(-5)+3\cdot1\\2\cdot7+4(-5)+6\cdot1\\0\cdot7+1(-5)+5\cdot1\end{pmatrix}=\begin{pmatrix}0\\0\\0\end{pmatrix}.$$

An inverse would imply $v=A^{-1}Av=0$, contradicting $v\ne0$. This checks noninvertibility without calculating the determinant numerically.
