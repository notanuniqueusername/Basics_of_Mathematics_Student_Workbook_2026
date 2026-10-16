# Exercise 12. A Parameter Revealed by a Row Operation

## The question

For
$$A(t)=\begin{pmatrix}1&2&3\\2&4&t\\0&1&1\end{pmatrix}$$
find the values of $t$ for which the matrix is not invertible.

Before computing the determinant, perform the operation
$$R_2\leftarrow R_2-2R_1$$
and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

## Before calculating: the concepts

Row replacement preserves a determinant. A parameter value gives noninvertibility exactly when the determinant vanishes.

## 1. Perform the prescribed replacement first

Twice row one is $(2,4,6)$. Subtracting it from row two removes the first two entries and leaves $t-6$ as the only potentially nonzero entry of that row. This exposes the exceptional parameter before any long expansion.

## 2. Extract the determinant from the new structure

Perform the required operation before computing any determinant:

$$R_2\leftarrow R_2-2R_1=(2,4,t)-(2,4,6)=(0,0,t-6).$$

It preserves the determinant and gives

$$\det A(t)=\det\begin{pmatrix}1&2&3\\0&0&t-6\\0&1&1\end{pmatrix}.$$

Expand down the first column; its only nonzero entry has positive cofactor sign:

$$\det A(t)=1\det\begin{pmatrix}0&t-6\\1&1\end{pmatrix}=0\cdot1-(t-6)\cdot1=6-t.$$

Therefore $\det A(t)=0$ exactly when $\boxed{t=6}$. The minus sign in the $2\times2$ formula is essential: the determinant is $6-t$, rather than $t-6$.

## 3. Interpret the exceptional value in the original matrix

The transformed row vanishes exactly when $t=6$. In the original matrix this means row two is exactly twice row one. For any other value the determinant is nonzero, so there are no further singular cases to consider.

## 4. Verification

At $t=6$, the original second row is $(2,4,6)=2(1,2,3)$, so it is dependent on the first and the replaced row is zero.

For a compact check of the formula, expand the transformed matrix along row two. Its only nonzero entry is in position $(2,3)$, with sign $(-1)^{2+3}=-1$. Its minor is $\begin{pmatrix}1&2\\0&1\end{pmatrix}$, of determinant $1$. Thus $\det A(t)=-(t-6)\cdot1=6-t$, confirming both the root and the sign.
