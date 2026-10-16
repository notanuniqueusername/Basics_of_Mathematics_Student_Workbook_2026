# Exercise 8. Linear Combination and Checking the Result

## The question

Check whether $w=(5,1)$ can be written as
$$w=au+bv,$$
where $u=(1,1)$ and $v=(2,-1)$. If so, find $a,b$, reconstruct $w$ from them, and explain the geometric meaning of the existence of such coefficients.

## Before calculating: equate vector coordinates

The equation $w=au+bv$ is equivalent to one scalar equation per coordinate. Finding such coefficients determines whether the target belongs to the span of the two given directions.

A vector equation imposes simultaneous coordinate conditions: the same coefficients $a,b$ must work in both positions. Solving only the first coordinate would leave many candidates and would not establish representability. The coefficient matrix has $u$ and $v$ as its columns, linking this exercise directly to the column interpretation of matrix multiplication.

## 1. Form and solve the system

$$a(1,1)+b(2,-1)=(a+2b,a-b)=(5,1).$$

Therefore

$$a+2b=5,\qquad a-b=1.$$

Subtract the second equation from the first: $3b=4$, so $b=4/3$. Then $a=1+b=7/3$. Thus

$$\boxed{w=\frac73u+\frac43v}.$$

## 2. Explain existence and uniqueness

The two directions are not parallel: the determinant of their column matrix is

$$\det\begin{pmatrix}1&2\\1&-1\end{pmatrix}=-1-2=-3\ne0.$$

They therefore span the entire plane. Every plane vector, including this $w$, has a unique expression as their linear combination. Geometrically, the scaled displacement $au$ followed by $bv$ reaches $w$.

## 3. Connect the coefficient calculation with the column picture

The vector equation can be written

$$\begin{pmatrix}1&2\\1&-1\end{pmatrix}\begin{pmatrix}a\\b\end{pmatrix}=\begin{pmatrix}5\\1\end{pmatrix}.$$

Its determinant is $-3$, so the inverse exists and equals

$$\frac1{-3}\begin{pmatrix}-1&-2\\-1&1\end{pmatrix}.$$

Applying it to the target gives

$$\begin{pmatrix}a\\b\end{pmatrix}=\frac1{-3}\begin{pmatrix}-5-2\\-5+1\end{pmatrix}=\begin{pmatrix}7/3\\4/3\end{pmatrix}.$$

This checks the earlier elimination by a different matrix method. Geometrically, the columns are independent directions, and the coefficient vector tells how far to travel along each to reach $w$. The existence and uniqueness are consequences of those directions, not a special coincidence of this target vector.

## 4. Verification

Reconstruct both coordinates explicitly:

$$\frac73(1,1)+\frac43(2,-1)=\left(\frac73+\frac83,\frac73-\frac43\right)=(5,1).$$

The second equation also yields $a-b=7/3-4/3=1$, so no sign was lost in using the negative second coordinate of $v$.
