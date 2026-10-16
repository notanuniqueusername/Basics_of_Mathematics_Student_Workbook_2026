# Exercise 5. A 3×3 Matrix

## The question

Use Gauss–Jordan elimination to find the inverse of
$$A=\begin{pmatrix}1&1&0\\0&1&1\\1&0&1\end{pmatrix}.$$
Check the result by multiplication.

## Before calculating: the concepts

Reduce $[A\mid I]$ to $[I\mid A^{-1}]$. Apply every operation to the entire augmented row.

## 1. Plan the three-pivot reduction

The first two pivots are already $1$. Remove the bottom-left entry first. The next replacement removes the entry $-1$ beneath the second pivot and leaves a third pivot equal to $2$. Normalize that pivot before using it to clear the entries above it.

## 2. Show every augmented matrix

Start with

$$\left[\begin{array}{ccc|ccc}1&1&0&1&0&0\\0&1&1&0&1&0\\1&0&1&0&0&1\end{array}\right].$$

Use $R_3\leftarrow R_3-R_1$ on both halves:

$$\left[\begin{array}{ccc|ccc}1&1&0&1&0&0\\0&1&1&0&1&0\\0&-1&1&-1&0&1\end{array}\right].$$

Now $R_3\leftarrow R_3+R_2$ clears the second-column entry:

$$\left[\begin{array}{ccc|ccc}1&1&0&1&0&0\\0&1&1&0&1&0\\0&0&2&-1&1&1\end{array}\right].$$

Divide row three by $2$ to make its pivot $1$:

$$\left[\begin{array}{ccc|ccc}1&1&0&1&0&0\\0&1&1&0&1&0\\0&0&1&-1/2&1/2&1/2\end{array}\right].$$

Subtract row three from row two. Its right half becomes $(0,1,0)-(-1/2,1/2,1/2)=(1/2,1/2,-1/2)$:

$$\left[\begin{array}{ccc|ccc}1&1&0&1&0&0\\0&1&0&1/2&1/2&-1/2\\0&0&1&-1/2&1/2&1/2\end{array}\right].$$

Finally use $R_1\leftarrow R_1-R_2$:

$$\left[\begin{array}{ccc|ccc}1&0&0&1/2&-1/2&1/2\\0&1&0&1/2&1/2&-1/2\\0&0&1&-1/2&1/2&1/2\end{array}\right].$$

Read the right half:

$$\boxed{A^{-1}=\frac12\begin{pmatrix}1&-1&1\\1&1&-1\\-1&1&1\end{pmatrix}}.$$

## 3. Explain the final backward steps

Once row three has been divided by $2$, its left half is $(0,0,1)$. Subtract it from row two to remove the third-column entry there. Then subtract the updated row two from row one to remove its second-column entry. These operations must also act on all three entries of the right half.

## 4. Verification

Write the integer numerator as $N$. Direct row-by-column multiplication gives

$$AN=\begin{pmatrix}1+1&-1+1&1-1\\1-1&1+1&-1+1\\1-1&-1+1&1+1\end{pmatrix}=2I.$$

Check the other order too:

$$NA=\begin{pmatrix}1+1&1-1&-1+1\\1-1&1+1&1-1\\-1+1&-1+1&1+1\end{pmatrix}=2I.$$

Since $A^{-1}=N/2$, both products with the candidate inverse equal $I$. The factor $1/2$ is essential: the numerator matrix by itself would give $2I$, not $I$.
