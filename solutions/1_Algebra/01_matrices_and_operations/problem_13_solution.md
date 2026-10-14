# Exercise 13. A Recurrence Written in Matrix Form

## The question

Let

$$F=\begin{pmatrix}1&1\\1&0\end{pmatrix}.$$

Compute $F^2$, $F^3$, $F^4$, $F^5$ and compare the entries with the sequence $0,1,1,2,3,5,8,\ldots$. Then compute $F\begin{pmatrix}a\\b\end{pmatrix}$ and explain how this multiplication performs one recurrence step.

## Before calculating: the idea

The sequence is the Fibonacci sequence, defined by

$$f_0=0,\quad f_1=1,\quad f_{n+1}=f_n+f_{n-1}.$$

Each term is the sum of the two before it. The claim to test is that the matrix $F$ packages this rule, so that powers of $F$ produce Fibonacci numbers.

## 1. Compute the powers

Each power is the previous one times $F$.

$$F^2=FF=\begin{pmatrix}1\cdot1+1\cdot1 & 1\cdot1+1\cdot0\\ 1\cdot1+0\cdot1 & 1\cdot1+0\cdot0\end{pmatrix}=\begin{pmatrix}2&1\\1&1\end{pmatrix}.$$

$$F^3=F^2F=\begin{pmatrix}2&1\\1&1\end{pmatrix}\begin{pmatrix}1&1\\1&0\end{pmatrix}=\begin{pmatrix}2+1&2+0\\1+1&1+0\end{pmatrix}=\begin{pmatrix}3&2\\2&1\end{pmatrix}.$$

$$F^4=F^3F=\begin{pmatrix}3&2\\2&1\end{pmatrix}\begin{pmatrix}1&1\\1&0\end{pmatrix}=\begin{pmatrix}3+2&3+0\\2+1&2+0\end{pmatrix}=\begin{pmatrix}5&3\\3&2\end{pmatrix}.$$

$$F^5=F^4F=\begin{pmatrix}5&3\\3&2\end{pmatrix}\begin{pmatrix}1&1\\1&0\end{pmatrix}=\begin{pmatrix}5+3&5+0\\3+2&3+0\end{pmatrix}=\begin{pmatrix}8&5\\5&3\end{pmatrix}.$$

## 2. Compare with the sequence

With $f_0=0,\ f_1=1,\ f_2=1,\ f_3=2,\ f_4=3,\ f_5=5,\ f_6=8$:

| Power | Matrix | In terms of $f_n$ |
|---|---|---|
| $F^1$ | $\begin{pmatrix}1&1\\1&0\end{pmatrix}$ | $\begin{pmatrix}f_2&f_1\\f_1&f_0\end{pmatrix}$ |
| $F^2$ | $\begin{pmatrix}2&1\\1&1\end{pmatrix}$ | $\begin{pmatrix}f_3&f_2\\f_2&f_1\end{pmatrix}$ |
| $F^3$ | $\begin{pmatrix}3&2\\2&1\end{pmatrix}$ | $\begin{pmatrix}f_4&f_3\\f_3&f_2\end{pmatrix}$ |
| $F^4$ | $\begin{pmatrix}5&3\\3&2\end{pmatrix}$ | $\begin{pmatrix}f_5&f_4\\f_4&f_3\end{pmatrix}$ |
| $F^5$ | $\begin{pmatrix}8&5\\5&3\end{pmatrix}$ | $\begin{pmatrix}f_6&f_5\\f_5&f_4\end{pmatrix}$ |

The pattern is

$$F^n=\begin{pmatrix}f_{n+1}&f_n\\f_n&f_{n-1}\end{pmatrix}.$$

The matrix is symmetric, the off-diagonal entries are $f_n$, and the diagonal holds the neighbouring terms.

## 3. One recurrence step

Compute $F$ times a general vector:

$$F\begin{pmatrix}a\\b\end{pmatrix}=\begin{pmatrix}1\cdot a+1\cdot b\\1\cdot a+0\cdot b\end{pmatrix}=\begin{pmatrix}a+b\\a\end{pmatrix}.$$

Read the vector $\begin{pmatrix}a\\b\end{pmatrix}$ as a pair of consecutive terms, with $a$ the newer one and $b$ the older one. Then:

- the first entry $a+b$ is the **sum of the two terms**, which is the next term of the sequence,
- the second entry $a$ is the **newer term kept**, which becomes the "older" term of the new pair.

So one multiplication by $F$ moves the window of two consecutive terms one step forward. Starting from $\begin{pmatrix}f_1\\f_0\end{pmatrix}=\begin{pmatrix}1\\0\end{pmatrix}$:

$$F\begin{pmatrix}1\\0\end{pmatrix}=\begin{pmatrix}1\\1\end{pmatrix},\quad F\begin{pmatrix}1\\1\end{pmatrix}=\begin{pmatrix}2\\1\end{pmatrix},\quad F\begin{pmatrix}2\\1\end{pmatrix}=\begin{pmatrix}3\\2\end{pmatrix},\ \ldots$$

These are the pairs $\begin{pmatrix}f_2\\f_1\end{pmatrix},\begin{pmatrix}f_3\\f_2\end{pmatrix},\begin{pmatrix}f_4\\f_3\end{pmatrix},\ldots$. In general,

$$F\begin{pmatrix}f_n\\f_{n-1}\end{pmatrix}=\begin{pmatrix}f_{n+1}\\f_n\end{pmatrix},\qquad\text{so}\qquad F^n\begin{pmatrix}1\\0\end{pmatrix}=\begin{pmatrix}f_{n+1}\\f_n\end{pmatrix}.$$

## 4. Why the powers contain Fibonacci numbers

The last formula says that $F^n\begin{pmatrix}1\\0\end{pmatrix}$ is the first column of $F^n$. So the first column of $F^n$ is $\begin{pmatrix}f_{n+1}\\f_n\end{pmatrix}$, matching the table. The second column is the first column of $F^{n-1}$, which gives $\begin{pmatrix}f_n\\f_{n-1}\end{pmatrix}$, because $F^n=F^{n-1}F$ and the second column of $F$ is... more simply, because multiplying a matrix on the right by $F$ sends columns $(c_1,c_2)$ to $(c_1+c_2,\ c_1)$, shifting the old first column into the second place.

This is an induction in disguise. If $F^n=\begin{pmatrix}f_{n+1}&f_n\\f_n&f_{n-1}\end{pmatrix}$, then

$$F^{n+1}=F^nF=\begin{pmatrix}f_{n+1}+f_n & f_{n+1}\\ f_n+f_{n-1} & f_n\end{pmatrix}=\begin{pmatrix}f_{n+2}&f_{n+1}\\f_{n+1}&f_n\end{pmatrix}.$$

## 5. Verification

**Determinant check.** $\det F=-1$, so $\det F^n=(-1)^n$. The formula gives

$$f_{n+1}f_{n-1}-f_n^2=(-1)^n.$$

For $n=5$: $8\cdot3-5^2=24-25=-1=(-1)^5$. ✓ For $n=4$: $5\cdot2-3^2=10-9=1=(-1)^4$. ✓

**Different grouping.** By associativity, $F^5=F^2F^3$:

$$\begin{pmatrix}2&1\\1&1\end{pmatrix}\begin{pmatrix}3&2\\2&1\end{pmatrix}=\begin{pmatrix}6+2&4+1\\3+2&2+1\end{pmatrix}=\begin{pmatrix}8&5\\5&3\end{pmatrix}.\ ✓$$

**Sum rule.** In each $F^n$, the first row sums to the next Fibonacci number: for $F^5$, $8+5=13=f_7$. ✓
