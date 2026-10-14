# Exercise 11. When Do Matrices Commute?

## The question

We are given

$$A=\begin{pmatrix}1&1\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}a&b\\c&d\end{pmatrix}.$$

Find the conditions on $a,b,c,d$ under which $AB=BA$, and describe the general form of all such matrices $B$.

## Before calculating: the plan

By Exercise 4, we know that $AB=BA$ is not automatic. Two matrices are equal exactly when **all four entries agree**, so $AB=BA$ becomes a system of four equations in the unknowns $a,b,c,d$. We compute both products with a general $B$, then compare entry by entry.

## 1. Compute $AB$

Rows of $A$ paired with columns of $B$:

$$AB=\begin{pmatrix}1\cdot a+1\cdot c & 1\cdot b+1\cdot d\\ 0\cdot a+1\cdot c & 0\cdot b+1\cdot d\end{pmatrix}=\begin{pmatrix}a+c&b+d\\c&d\end{pmatrix}.$$

## 2. Compute $BA$

Rows of $B$ paired with columns of $A$:

$$BA=\begin{pmatrix}a\cdot1+b\cdot0 & a\cdot1+b\cdot1\\ c\cdot1+d\cdot0 & c\cdot1+d\cdot1\end{pmatrix}=\begin{pmatrix}a&a+b\\c&c+d\end{pmatrix}.$$

## 3. Compare entry by entry

| Position | $AB$ | $BA$ | Equation | Result |
|---|---|---|---|---|
| $(1,1)$ | $a+c$ | $a$ | $a+c=a$ | $c=0$ |
| $(1,2)$ | $b+d$ | $a+b$ | $b+d=a+b$ | $d=a$ |
| $(2,1)$ | $c$ | $c$ | $c=c$ | always true |
| $(2,2)$ | $d$ | $c+d$ | $d=c+d$ | $c=0$ |

The same information can be read from the difference:

$$AB-BA=\begin{pmatrix}c&d-a\\0&-c\end{pmatrix}.$$

This is the zero matrix exactly when $c=0$ and $d=a$. The entries $(1,1)$ and $(2,2)$ give the same condition, and $(2,1)$ gives none, so only **two independent conditions** remain.

## 4. The general form of $B$

The conditions are $c=0$ and $d=a$, while $a$ and $b$ are free:

$$B=\begin{pmatrix}a&b\\0&a\end{pmatrix},\qquad a,b\in\mathbb R.$$

So the matrices that commute with $A$ are exactly the **upper triangular matrices with equal diagonal entries**. There is a two-parameter family of them.

## 5. Why this form appears

Write $A=I+N$ with $N=\begin{pmatrix}0&1\\0&0\end{pmatrix}$. The identity commutes with every matrix, so

$$AB=BA\iff NB=BN.$$

Now compute:

$$NB=\begin{pmatrix}c&d\\0&0\end{pmatrix},\qquad BN=\begin{pmatrix}0&a\\0&c\end{pmatrix}.$$

Equating entries gives $c=0$, $d=a$, and $0=c$, the same conditions as before. This explains the shape of the answer: $N$ only "moves the second coordinate into the first," and a matrix that commutes with it must treat both coordinates in the same way on the diagonal and have no lower-left entry.

The answer can also be written as

$$B=aI+bN=(a-b)\,I+b\,A.$$

So every matrix that commutes with $A$ is a combination of $I$ and $A$ itself. This agrees with Exercise 7, where $A^2$ and $A^3$ had exactly this shape.

## 6. Verification

**A matrix of the found form.** Take $a=2$, $b=3$, so $B=\begin{pmatrix}2&3\\0&2\end{pmatrix}$:

$$AB=\begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}2&3\\0&2\end{pmatrix}=\begin{pmatrix}2&5\\0&2\end{pmatrix},\qquad BA=\begin{pmatrix}2&3\\0&2\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}=\begin{pmatrix}2&5\\0&2\end{pmatrix}.\ ✓$$

**A matrix that violates the condition.** Take $c=1$ with $B=\begin{pmatrix}1&0\\1&1\end{pmatrix}$:

$$AB=\begin{pmatrix}2&1\\1&1\end{pmatrix}\ne\begin{pmatrix}1&1\\1&2\end{pmatrix}=BA.\ ✓$$

This matches the difference formula: $AB-BA=\begin{pmatrix}c&d-a\\0&-c\end{pmatrix}=\begin{pmatrix}1&0\\0&-1\end{pmatrix}$ for these values, and indeed $\begin{pmatrix}2&1\\1&1\end{pmatrix}-\begin{pmatrix}1&1\\1&2\end{pmatrix}=\begin{pmatrix}1&0\\0&-1\end{pmatrix}$.
