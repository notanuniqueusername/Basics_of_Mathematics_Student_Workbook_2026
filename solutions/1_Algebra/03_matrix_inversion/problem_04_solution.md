# Exercise 4. Gauss–Jordan

## The question

Find $A^{-1}$ using the Gauss–Jordan method for
$$A=\begin{pmatrix}1&2\\3&5\end{pmatrix}.$$
Show the augmented matrix $[A\mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

## Before calculating: the concepts

Gauss–Jordan applies each row operation to both halves of the augmented matrix.

## 1. Set up the augmented matrix

The identity on the right has the same number of rows as $A$. It records what happens when the chosen row operations are applied to $I$. First remove the $3$ below the leading $1$, then normalize the second pivot, and finally clear the entry above that pivot.

## 2. Carry out the Gauss–Jordan steps

Attach the identity to the right of $A$:

$$\left[\begin{array}{cc|cc}1&2&1&0\\3&5&0&1\end{array}\right].$$

First use $R_2\leftarrow R_2-3R_1$. On the left, $(3,5)-3(1,2)=(0,-1)$; on the right, $(0,1)-3(1,0)=(-3,1)$. Thus

$$\left[\begin{array}{cc|cc}1&2&1&0\\0&-1&-3&1\end{array}\right].$$

Normalize the second pivot with $R_2\leftarrow-R_2$:

$$\left[\begin{array}{cc|cc}1&2&1&0\\0&1&3&-1\end{array}\right].$$

Finally use $R_1\leftarrow R_1-2R_2$. The new right row is $(1,0)-2(3,-1)=(-5,2)$:

$$\left[\begin{array}{cc|cc}1&0&-5&2\\0&1&3&-1\end{array}\right].$$

The left half is now $I$, so $\boxed{A^{-1}=\begin{pmatrix}-5&2\\3&-1\end{pmatrix}}$.

## 3. Read the inverse from the right half

After the first operation, the second row on the left is $(0,-1)$. Multiplication by $-1$ changes that pivot to $1$. Subtracting twice the new second row from the first removes the remaining $2$ above it. At this point the entire left half, not just its diagonal, is the identity.

## 4. Verification

Check both product orders:

$$AA^{-1}=\begin{pmatrix}1(-5)+2\cdot3&1\cdot2+2(-1)\\3(-5)+5\cdot3&3\cdot2+5(-1)\end{pmatrix}=\begin{pmatrix}1&0\\0&1\end{pmatrix},$$

$$A^{-1}A=\begin{pmatrix}(-5)1+2\cdot3&(-5)2+2\cdot5\\3\cdot1+(-1)3&3\cdot2+(-1)5\end{pmatrix}=\begin{pmatrix}1&0\\0&1\end{pmatrix}.$$

To explain why the method works, let $F$ be the product of the elementary matrices representing the row operations. The augmented matrix becomes $[FA\mid F]$. Obtaining $FA=I$ forces $F=A^{-1}$, so the right half records the inverse rather than an unrelated matrix.
