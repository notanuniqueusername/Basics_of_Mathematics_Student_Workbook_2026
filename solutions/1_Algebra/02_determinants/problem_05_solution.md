# Exercise 5. Row Operations

## The question

For
$$A=\begin{pmatrix}1&2&3\\2&1&0\\-1&4&2\end{pmatrix}$$
find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

## Before calculating: the concepts

Row replacement $R_i\leftarrow R_i+cR_j$ with $i\ne j$ preserves the determinant. A triangular determinant is the product of the diagonal entries.

## 1. Plan the elimination

The first pivot is already $1$. Use it to remove the entries $2$ and $-1$ underneath it. Choose row replacements rather than row scalings so that every intermediate matrix has exactly the same determinant as the original.

## 2. Create zeros and track the determinant

Each operation below is a row replacement and preserves the determinant.

First remove the $2$ below the first pivot:

$$R_2\leftarrow R_2-2R_1=(2,1,0)-(2,4,6)=(0,-3,-6).$$

The matrix becomes

$$\begin{pmatrix}1&2&3\\0&-3&-6\\-1&4&2\end{pmatrix}.$$

Next remove the $-1$ in the first column:

$$R_3\leftarrow R_3+R_1=(-1,4,2)+(1,2,3)=(0,6,5).$$

Now the matrix is $\begin{pmatrix}1&2&3\\0&-3&-6\\0&6&5\end{pmatrix}$. Finally,

$$R_3\leftarrow R_3+2R_2=(0,6,5)+(0,-6,-12)=(0,0,-7).$$

We reach the upper triangular matrix

$$U=\begin{pmatrix}1&2&3\\0&-3&-6\\0&0&-7\end{pmatrix},\qquad \boxed{\det A=\det U=1(-3)(-7)=21}.$$

## 3. Read the final determinant

After the first column is cleared, use the second pivot to clear the remaining entry below the diagonal. The diagonal product may be used only after the matrix is triangular. No correction for a row swap or row scaling is necessary here because neither operation was used.

## 4. Verification

A direct cofactor check on the original matrix gives

$$\det A=1\begin{vmatrix}1&0\\4&2\end{vmatrix}-2\begin{vmatrix}2&0\\-1&2\end{vmatrix}+3\begin{vmatrix}2&1\\-1&4\end{vmatrix}.$$

The minors are $2$, $4$, and $8-(-1)=9$, respectively. Therefore $\det A=2-8+27=21$, matching elimination. The two negative final pivots also explain why the result is positive.
