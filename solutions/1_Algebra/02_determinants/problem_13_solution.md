# Exercise 13. Determinant by Elimination

## The question

Compute the determinant
$$A=\begin{pmatrix}1&2&3\\2&5&7\\1&0&2\end{pmatrix}$$
using elimination. Record the effect of every row operation used on the value of the determinant.

## Before calculating: the concepts

Row replacements leave the determinant unchanged; the determinant of the final upper triangular matrix is its diagonal product.

## 1. Choose determinant-preserving operations

The first pivot is $1$, so the two entries beneath it can be removed without fractions or swaps. After that, the second pivot is also $1$. Record each replacement explicitly so the relationship between the original and final determinants stays clear.

## 2. Reduce to an upper triangular matrix

Remove the entry below the first pivot in row two:

$$R_2\leftarrow R_2-2R_1=(2,5,7)-(2,4,6)=(0,1,1).$$

This replacement leaves the determinant unchanged. Next,

$$R_3\leftarrow R_3-R_1=(1,0,2)-(1,2,3)=(0,-2,-1),$$

again with no determinant change. The matrix is now

$$\begin{pmatrix}1&2&3\\0&1&1\\0&-2&-1\end{pmatrix}.$$

Use the second pivot to remove $-2$:

$$R_3\leftarrow R_3+2R_2=(0,-2,-1)+(0,2,2)=(0,0,1).$$

This also preserves the determinant. Hence

$$\boxed{\det A=\det\begin{pmatrix}1&2&3\\0&1&1\\0&0&1\end{pmatrix}=1}.$$

## 3. Finish only after checking the diagonal

The final diagonal has three entries equal to $1$. Its product is therefore $1$. The operations used have not changed the determinant, so this product is the original determinant itself, with no sign correction.

## 4. Verification

Check with a first-row cofactor expansion of the original matrix:

$$\det A=1(5\cdot2-7\cdot0)-2(2\cdot2-7\cdot1)+3(2\cdot0-5\cdot1).$$

This is $10-2(-3)+3(-5)=10+6-15=1$. The agreement checks the original arithmetic independently of the elimination sequence.
