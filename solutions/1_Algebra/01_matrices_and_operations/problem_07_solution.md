# Exercise 7. Identity Matrix, Zero Matrix, and Powers

## The question

We are given

$$A=\begin{pmatrix}2&1\\0&2\end{pmatrix}.$$

Compute $AI$, $IA$, $A+0$, $A^2$, $A^3$. Explain the roles of $I$ and $0$, and describe the pattern in the successive powers of $A$.

## Before calculating: the neutral elements

Matrices have two special "do nothing" elements, one for each operation.

- The **identity matrix** $I$ is neutral for multiplication. For $2\times2$ matrices,
$$I=\begin{pmatrix}1&0\\0&1\end{pmatrix}.$$
It has ones on the diagonal and zeros elsewhere, and it plays the role of the number $1$.
- The **zero matrix** $0$ is neutral for addition. For $2\times2$ matrices,
$$0=\begin{pmatrix}0&0\\0&0\end{pmatrix}.$$
It plays the role of the number $0$.

Both must have the same size as $A$ for the operations to be defined, so here they are $2\times2$.

## 1. Compute $AI$ and $IA$

$$AI=\begin{pmatrix}2\cdot1+1\cdot0 & 2\cdot0+1\cdot1\\ 0\cdot1+2\cdot0 & 0\cdot0+2\cdot1\end{pmatrix}=\begin{pmatrix}2&1\\0&2\end{pmatrix}=A.$$

$$IA=\begin{pmatrix}1\cdot2+0\cdot0 & 1\cdot1+0\cdot2\\ 0\cdot2+1\cdot0 & 0\cdot1+1\cdot2\end{pmatrix}=\begin{pmatrix}2&1\\0&2\end{pmatrix}=A.$$

## 2. Compute $A+0$

$$A+0=\begin{pmatrix}2+0&1+0\\0+0&2+0\end{pmatrix}=\begin{pmatrix}2&1\\0&2\end{pmatrix}=A.$$

## 3. Compute $A^2$

$$A^2=AA=\begin{pmatrix}2\cdot2+1\cdot0 & 2\cdot1+1\cdot2\\ 0\cdot2+2\cdot0 & 0\cdot1+2\cdot2\end{pmatrix}=\begin{pmatrix}4&4\\0&4\end{pmatrix}.$$

## 4. Compute $A^3$

Use $A^3=A^2A$:

$$A^3=\begin{pmatrix}4&4\\0&4\end{pmatrix}\begin{pmatrix}2&1\\0&2\end{pmatrix}=\begin{pmatrix}4\cdot2+4\cdot0 & 4\cdot1+4\cdot2\\ 0\cdot2+4\cdot0 & 0\cdot1+4\cdot2\end{pmatrix}=\begin{pmatrix}8&12\\0&8\end{pmatrix}.$$

## 5. The roles of $I$ and $0$

- $I$ is the multiplicative neutral element: $AI=IA=A$. Multiplying by $I$ leaves every vector unchanged, so $I$ represents the transformation "do nothing". Unlike general matrices, $I$ commutes with everything, so $AI=IA$ holds here automatically.
- $0$ is the additive neutral element: $A+0=A$. It also has a second property, $A\cdot0=0$, so multiplying by $0$ destroys everything.

## 6. The pattern in the powers

Collecting the results:

$$A=\begin{pmatrix}2&1\\0&2\end{pmatrix},\quad A^2=\begin{pmatrix}4&4\\0&4\end{pmatrix},\quad A^3=\begin{pmatrix}8&12\\0&8\end{pmatrix}.$$

- The diagonal entries are $2,\,4,\,8$, that is $2^n$.
- The lower-left entry stays $0$.
- The upper-right entries are $1,\,4,\,12$. Writing them as $n\cdot2^{n-1}$ gives $1\cdot1=1$, $2\cdot2=4$, $3\cdot4=12$. ✓

This suggests

$$A^n=\begin{pmatrix}2^n & n\,2^{n-1}\\ 0 & 2^n\end{pmatrix}.$$

This is a conjecture from three cases, not a proof. A way to see why it holds: write $A=2I+N$ with $N=\begin{pmatrix}0&1\\0&0\end{pmatrix}$. Then $N^2=0$, and since $2I$ commutes with $N$, the binomial expansion stops after two terms:
$$A^n=(2I+N)^n=2^nI+n\,2^{n-1}N,$$
which is exactly the formula above.

## 7. Verification

**Check $A^3$ by a different grouping.** Multiplication is associative, so $A^3=AA^2$ must give the same result:

$$AA^2=\begin{pmatrix}2&1\\0&2\end{pmatrix}\begin{pmatrix}4&4\\0&4\end{pmatrix}=\begin{pmatrix}8&8+4\\0&8\end{pmatrix}=\begin{pmatrix}8&12\\0&8\end{pmatrix}.\ ✓$$

**Determinant check.** Since $\det(A^n)=(\det A)^n$ and $\det A=4$:

$$\det A^2=16=4\cdot4-4\cdot0,\qquad \det A^3=64=8\cdot8-12\cdot0.\ ✓$$

**Formula check.** For $n=3$ the formula gives $2^3=8$ on the diagonal and $3\cdot2^2=12$ in the corner, matching $A^3$. ✓
