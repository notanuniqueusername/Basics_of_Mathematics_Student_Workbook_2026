# Exercise 1. Definition of the Inverse

## The question

For
$$A=\begin{pmatrix}2&1\\1&1\end{pmatrix},\qquad B=\begin{pmatrix}1&-1\\-1&2\end{pmatrix}$$
check, without using a formula, whether $B=A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

## Before calculating: the concepts

The inverse definition is $AB=BA=I$.

## 1. Set up the definition check

Both matrices are $2\times2$, so both products are defined and must be compared with $I_2=\begin{pmatrix}1&0\\0&1\end{pmatrix}$. Compute each entry by taking a row from the left factor and a column from the right factor. For example, $(AB)_{12}=2(-1)+1(2)=0$.

## 2. Compute both multiplication orders

Use the row-by-column rule for every entry of $AB$:

$$AB=\begin{pmatrix}2\cdot1+1(-1)&2(-1)+1\cdot2\\1\cdot1+1(-1)&1(-1)+1\cdot2\end{pmatrix}=\begin{pmatrix}1&0\\0&1\end{pmatrix}=I_2.$$

Now reverse the multiplication order and calculate again:

$$BA=\begin{pmatrix}1\cdot2+(-1)1&1\cdot1+(-1)1\\(-1)2+2\cdot1&(-1)1+2\cdot1\end{pmatrix}=\begin{pmatrix}1&0\\0&1\end{pmatrix}=I_2.$$

Both defining identities hold, so $\boxed{B=A^{-1}}$. This uses multiplication alone, as requested; no inverse formula is needed.

## 3. State what the products prove

The calculation checks the defining equations directly. There is no need to derive an inverse formula or compute a determinant first: the given candidate already supplies the matrix to test. Both orders return the original vector after the two corresponding transformations are composed.

## 4. Verification

**Check on a vector in both orders.** Take $v=(1,2)^T$. Then

$$Bv=\begin{pmatrix}1-2\\-1+4\end{pmatrix}=\begin{pmatrix}-1\\3\end{pmatrix},\qquad A(Bv)=\begin{pmatrix}-2+3\\-1+3\end{pmatrix}=\begin{pmatrix}1\\2\end{pmatrix}=v.$$

In the other order,

$$Av=\begin{pmatrix}2+2\\1+2\end{pmatrix}=\begin{pmatrix}4\\3\end{pmatrix},\qquad B(Av)=\begin{pmatrix}4-3\\-4+6\end{pmatrix}=v.$$

These checks illustrate the meaning of the two identity products: each transformation undoes the other. The full matrix products above establish this for every vector, not only the chosen example.
