# Exercise 11. Shortening the Calculation with Row Operations

## The question

Compute
$$\det\begin{pmatrix}1&2&3\\1&3&4\\1&4&6\end{pmatrix}$$
by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

## Before calculating: the concepts

Adding a multiple of a different row does not change the determinant. Create zeros below successive pivots, then multiply the diagonal entries.

## 1. Exploit the shared first entry

All three first-column entries equal $1$. Subtracting row one from rows two and three therefore creates two zeros immediately. These operations preserve the determinant and simplify the remaining $2\times2$ part.

## 2. Eliminate in two stages

Subtract the first row from the second:

$$R_2\leftarrow R_2-R_1=(0,1,1),\qquad \begin{pmatrix}1&2&3\\0&1&1\\1&4&6\end{pmatrix}.$$

Subtract the unchanged first row from the third:

$$R_3\leftarrow R_3-R_1=(0,2,3),\qquad \begin{pmatrix}1&2&3\\0&1&1\\0&2&3\end{pmatrix}.$$

Finally remove the $2$ below the second pivot:

$$R_3\leftarrow R_3-2R_2=(0,2,3)-(0,2,2)=(0,0,1).$$

Every operation is a determinant-preserving row replacement. Consequently

$$\boxed{\det A=\det\begin{pmatrix}1&2&3\\0&1&1\\0&0&1\end{pmatrix}=1\cdot1\cdot1=1}.$$

## 3. Explain what was preserved

A row replacement adds a multiple of a different row without changing the determinant. This differs from multiplying a row by a number. Even though the coefficients $-1$ and $-2$ appear in the replacements, there is no extra determinant factor to record.

## 4. Verification

A cofactor check on the original first row gives

$$\det A=1(3\cdot6-4\cdot4)-2(1\cdot6-4\cdot1)+3(1\cdot4-3\cdot1).$$

The three minors are $2$, $2$, and $1$, so the result is $2-4+3=1$. This agrees with the triangular product and confirms that no row-operation factor or sign was omitted.
