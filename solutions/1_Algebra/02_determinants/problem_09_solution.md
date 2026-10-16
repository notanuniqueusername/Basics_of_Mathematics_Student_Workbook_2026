# Exercise 9. Area and the Determinant

## The question

The vectors
$$u=\begin{pmatrix}3\\1\end{pmatrix},\qquad v=\begin{pmatrix}1\\4\end{pmatrix}$$
span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

## Before calculating: the concepts

The area spanned by two plane vectors is $|\det[u\ v]|$. The determinant itself is signed and records orientation.

## 1. Put the vectors in columns

Use the first vector as column one and the second as column two. This fixes the order for the signed determinant. The area is obtained only after taking its absolute value, because geometric area cannot be negative.

## 2. Calculate the area in both vector orders

Place the ordered vectors in columns:

$$[u\ v]=\begin{pmatrix}3&1\\1&4\end{pmatrix}.$$

The signed determinant and geometric area are

$$\det[u\ v]=3\cdot4-1\cdot1=12-1=11,\qquad \boxed{\text{area}=|11|=11\text{ square units}}.$$

Now reverse the order:

$$[v\ u]=\begin{pmatrix}1&3\\4&1\end{pmatrix},\qquad \det[v\ u]=1\cdot1-3\cdot4=-11.$$

The sign reverses, while the area is $|-11|=11$. Relative to the usual orientation of the coordinate axes, the positive order $(u,v)$ is counterclockwise; the reversed order is clockwise.

## 3. Distinguish area and orientation

Reversing the two vectors swaps two columns. The determinant changes sign while its absolute value stays the same. The parallelogram is the same geometric region in either description; only the ordered description of its spanning vectors changes.

## 4. Verification

Use the independent identity $\text{area}^2=\|u\|^2\|v\|^2-(u\cdot v)^2$:

$$\|u\|^2=3^2+1^2=10,\quad \|v\|^2=1^2+4^2=17,\quad u\cdot v=3\cdot1+1\cdot4=7.$$

Thus $\text{area}^2=10\cdot17-7^2=170-49=121$, giving area $11$ after taking the nonnegative square root. Exchanging $u$ and $v$ leaves this expression unchanged, confirming that area does not depend on their order.
