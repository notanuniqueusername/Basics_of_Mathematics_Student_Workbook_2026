# Exercise 4. Triangular Matrix

## The question

Without expanding the determinant, compute
$$\det\begin{pmatrix}2&4&1\\0&-3&5\\0&0&7\end{pmatrix}.$$
State the rule for an arbitrary triangular matrix and explain it using this example.

## Before calculating: the concepts

The determinant of any upper or lower triangular $n\times n$ matrix is the product of its diagonal entries: $\det T=\prod_{i=1}^n t_{ii}$.

## 1. Recognize triangular structure

Check the entries below the main diagonal: all three are zero. The diagonal is $2,-3,7$, while the entries $4,1,5$ lie above it. Those off-diagonal entries do not enter the product rule for a triangular determinant.

## 2. Use the diagonal product

The matrix is upper triangular because all entries below the diagonal are zero. Its diagonal entries are $2,-3,7$, so without expansion,

$$\boxed{\det T=2\cdot(-3)\cdot7=-42}.$$

For any $n\times n$ upper or lower triangular matrix,

$$\det T=t_{11}t_{22}\cdots t_{nn}.$$

To see why, use the determinant permutation formula. A term selects one entry from every row and every column. For an upper triangular matrix, a nonzero selected entry in row $i$ must have column index at least $i$. Since the selected column indices must together be $1,\ldots,n$, every one must equal its row index. Thus only the diagonal term can survive. The lower triangular case reverses the inequality.

## 3. Explain why the shortcut applies

A triangular matrix may have arbitrary entries on one side of its diagonal. It need not be diagonal. Its determinant still depends only on the diagonal entries; a zero diagonal entry would make this product zero, and hence make the matrix singular.

## 4. Verification

**Sign and magnitude.** There is one negative diagonal factor, so the determinant must be negative; its magnitude is $2\cdot3\cdot7=42$.

**Invertibility.** In $Tx=0$, the last equation gives $7x_3=0$, hence $x_3=0$. The second then gives $-3x_2=0$, hence $x_2=0$. The first gives $2x_1=0$, hence $x_1=0$. The homogeneous system has only the zero solution, agreeing with the nonzero determinant. No determinant expansion is needed for either check.
