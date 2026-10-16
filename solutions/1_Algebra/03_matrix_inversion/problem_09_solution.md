# Exercise 9. Matrix Equation

## The question

Given
$$A=\begin{pmatrix}1&2\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}3&1\\2&4\end{pmatrix}.$$
Solve the equation $AX=B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

## Before calculating: the concepts

For $AX=B$, use $A^{-1}$ on the left, since that places $A^{-1}$ next to $A$.

## 1. Choose the side before multiplying

Starting from $AX=B$, multiply the whole equation on the left by $A^{-1}$. Associativity gives $(A^{-1}A)X=A^{-1}B$, hence $IX=A^{-1}B$. Multiplying on the right would instead give $AXA^{-1}=BA^{-1}$ and would not isolate $X$.

## 2. Calculate the entries of the unknown matrix

Multiply on the left by $A^{-1}$:

$$A^{-1}(AX)=A^{-1}B\quad\Longrightarrow\quad (A^{-1}A)X=A^{-1}B\quad\Longrightarrow\quad X=A^{-1}B.$$

Construct the inverse by Gauss–Jordan elimination. The matrix $A$ adds twice the second coordinate to the first, so reverse that row addition on both halves of $[A\mid I]$:

$$\left[\begin{array}{cc|cc}1&2&1&0\\0&1&0&1\end{array}\right]\xrightarrow{R_1\leftarrow R_1-2R_2}\left[\begin{array}{cc|cc}1&0&1&-2\\0&1&0&1\end{array}\right].$$

The left half is $I$, so the right half is $A^{-1}$:

$$A^{-1}=\begin{pmatrix}1&-2\\0&1\end{pmatrix}.$$

Now calculate every entry of $X$:

$$X=\begin{pmatrix}1\cdot3+(-2)2&1\cdot1+(-2)4\\0\cdot3+1\cdot2&0\cdot1+1\cdot4\end{pmatrix}=\boxed{\begin{pmatrix}-1&-7\\2&4\end{pmatrix}}.$$

Multiplying on the right instead would give $AXA^{-1}=BA^{-1}$, which does not isolate $X$.

## 3. Explain the matrix product

Left multiplication by $\begin{pmatrix}1&-2\\0&1\end{pmatrix}$ subtracts twice row two of $B$ from row one and leaves row two unchanged. This gives $3-2\cdot2=-1$ and $1-2\cdot4=-7$ in the first row. The second row remains $(2,4)$.

## 4. Verification

Substitute the matrix into the original equation:

$$AX=\begin{pmatrix}1(-1)+2\cdot2&1(-7)+2\cdot4\\0(-1)+1\cdot2&0(-7)+1\cdot4\end{pmatrix}=\begin{pmatrix}3&1\\2&4\end{pmatrix}=B.$$

A column check gives the same result: $A(-1,2)^T=(3,2)^T$, the first column of $B$, and $A(-7,4)^T=(1,4)^T$, the second column of $B$. Thus both columns solve their required vector equations. Left multiplication by an invertible matrix also ensures the matrix solution is unique.
