# Exercise 12. Formula for a Matrix Power

## The question

Let

$$A=\begin{pmatrix}1&1\\0&1\end{pmatrix}.$$

Compute $A^2$, $A^3$, $A^4$, and use them to conjecture a formula for $A^n$. Then assume the formula holds for $n$, multiply by $A$, and show that this gives exactly the formula for $n+1$.

## Before calculating: the plan

This exercise has two separate stages, and they play different roles.

1. **Discover** a pattern from a few computed cases. This only produces a *guess*.
2. **Prove** the guess by showing that if it holds for $n$, it must also hold for $n+1$. Since it holds for $n=1$, it then holds for $n=2$, then $n=3$, and so on for every $n$. This is **induction**.

Checking one more case, say $n=5$, would add confidence but never prove the formula for all $n$. The inductive step is what covers every $n$ at once.

## 1. Compute $A^2$

$$A^2=AA=\begin{pmatrix}1\cdot1+1\cdot0 & 1\cdot1+1\cdot1\\ 0\cdot1+1\cdot0 & 0\cdot1+1\cdot1\end{pmatrix}=\begin{pmatrix}1&2\\0&1\end{pmatrix}.$$

## 2. Compute $A^3$

Use $A^3=A^2A$:

$$A^3=\begin{pmatrix}1&2\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}=\begin{pmatrix}1&1+2\\0&1\end{pmatrix}=\begin{pmatrix}1&3\\0&1\end{pmatrix}.$$

## 3. Compute $A^4$

Use $A^4=A^3A$:

$$A^4=\begin{pmatrix}1&3\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}=\begin{pmatrix}1&1+3\\0&1\end{pmatrix}=\begin{pmatrix}1&4\\0&1\end{pmatrix}.$$

## 4. Conjecture

Collecting the results:

$$A^1=\begin{pmatrix}1&1\\0&1\end{pmatrix},\quad A^2=\begin{pmatrix}1&2\\0&1\end{pmatrix},\quad A^3=\begin{pmatrix}1&3\\0&1\end{pmatrix},\quad A^4=\begin{pmatrix}1&4\\0&1\end{pmatrix}.$$

The diagonal stays $1$, the lower-left entry stays $0$, and the upper-right entry equals the exponent. So we conjecture

$$A^n=\begin{pmatrix}1&n\\0&1\end{pmatrix}\qquad(n\ge1).$$

## 5. Proof by induction

**Base case.** For $n=1$ the formula gives $\begin{pmatrix}1&1\\0&1\end{pmatrix}=A$. ✓

**Inductive step.** Assume that for some $n$,

$$A^n=\begin{pmatrix}1&n\\0&1\end{pmatrix}.$$

Then $A^{n+1}=A^nA$, so

$$A^{n+1}=\begin{pmatrix}1&n\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}=\begin{pmatrix}1\cdot1+n\cdot0 & 1\cdot1+n\cdot1\\ 0\cdot1+1\cdot0 & 0\cdot1+1\cdot1\end{pmatrix}=\begin{pmatrix}1&n+1\\0&1\end{pmatrix}.$$

This is exactly the formula with $n$ replaced by $n+1$. Since the formula holds for $n=1$ and passing from $n$ to $n+1$ always works, it holds for every $n\ge1$. $\blacksquare$

## 6. Why the pattern appears

Multiplying by $A$ on the right adds the first column to the second column, since the second column of $XA$ is $X\begin{pmatrix}1\\1\end{pmatrix}$, which is column 1 plus column 2 of $X$. Each multiplication therefore adds $1$ to the upper-right entry and changes nothing else.

The same result follows from Exercise 11's decomposition $A=I+N$ with $N^2=0$:

$$A^n=(I+N)^n=I+nN=\begin{pmatrix}1&n\\0&1\end{pmatrix},$$

because every term containing $N^2$ or higher vanishes.

## 7. Verification

**Different grouping.** By associativity, $A^4=A^2A^2$ must agree with the step-by-step result:

$$A^2A^2=\begin{pmatrix}1&2\\0&1\end{pmatrix}\begin{pmatrix}1&2\\0&1\end{pmatrix}=\begin{pmatrix}1&4\\0&1\end{pmatrix}.\ ✓$$

**Law of exponents.** The formula should satisfy $A^mA^n=A^{m+n}$:

$$\begin{pmatrix}1&m\\0&1\end{pmatrix}\begin{pmatrix}1&n\\0&1\end{pmatrix}=\begin{pmatrix}1&m+n\\0&1\end{pmatrix}.\ ✓$$

**Determinant check.** $\det A^n=(\det A)^n=1$, and the formula gives $1\cdot1-n\cdot0=1$. ✓
