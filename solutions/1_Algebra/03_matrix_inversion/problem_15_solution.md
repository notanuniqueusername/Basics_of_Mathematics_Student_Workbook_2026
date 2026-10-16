# Exercise 15. Two Methods for Solving the Same System

## The question

For
$$A=\begin{pmatrix}2&1\\1&3\end{pmatrix},\qquad b=\begin{pmatrix}7\\8\end{pmatrix}$$
solve $Ax=b$ in two ways:

1. using $A^{-1}b$,
2. using Gaussian elimination.

Compare both solutions, the number of essential steps, and state which method was simpler in this example.

## Before calculating: the concepts

The inverse method computes a whole inverse; elimination works directly with the given right-hand side.

## 1. Separate the two solution routes

Both routes use the same coefficient matrix and right-hand side. The determinant is $5$, so the inverse exists and the solution is unique. In the inverse route, construct $A^{-1}$ before multiplying by $b$. In elimination, attach $b$ as a single augmented column and work directly on it.

## 2. Solve by inverse and by elimination

**Method 1: inverse multiplication.** For a $2\times2$ matrix, use

$$\begin{pmatrix}a&b\\c&d\end{pmatrix}^{-1}=\frac1{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix},\qquad ad-bc\ne0.$$

The determinant of $A$ is $2\cdot3-1\cdot1=5$. Exchange its diagonal entries $2,3$, negate its off-diagonal entries $1,1$, and divide by $5$ to obtain

$$A^{-1}=\frac15\begin{pmatrix}3&-1\\-1&2\end{pmatrix}.$$

Then

$$x=A^{-1}b=\frac15\begin{pmatrix}3\cdot7+(-1)8\\(-1)7+2\cdot8\end{pmatrix}=\frac15\begin{pmatrix}13\\9\end{pmatrix}=\begin{pmatrix}13/5\\9/5\end{pmatrix}.$$

**Method 2: Gaussian elimination.** Start with

$$\left[\begin{array}{cc|c}2&1&7\\1&3&8\end{array}\right].$$

Use $R_2\leftarrow R_2-\frac12R_1$. The new second row is $(0,3-1/2\mid8-7/2)=(0,5/2\mid9/2)$:

$$\left[\begin{array}{cc|c}2&1&7\\0&5/2&9/2\end{array}\right].$$

Back substitution gives

$$\frac52x_2=\frac92\Longrightarrow x_2=\frac95,\qquad 2x_1+\frac95=7\Longrightarrow x_1=\frac{7-9/5}{2}=\frac{13}{5}.$$

Both methods produce $\boxed{x=(13/5,9/5)^T}$.

## 3. Compare the essential work fairly

Count an essential stage as one complete mathematical task, rather than one scalar arithmetic operation. On this convention each route has three stages, but the stages do different amounts of work:

| Method | Stage 1 | Stage 2 | Stage 3 |
|---|---|---|---|
| Inverse | Compute $\det A$ | Construct all four entries of $A^{-1}$ | Multiply $A^{-1}$ by $b$ |
| Elimination | Perform one augmented-row replacement | Solve for $x_2$ | Back-substitute for $x_1$ |

For a more detailed comparison, count scalar additions/subtractions, multiplications, and divisions, treating unary sign changes and writing known zeros as free. Evaluate the inverse entries individually; for elimination, compute the multiplier and update only the remaining coefficient and right-hand side.

| Calculation | Additions/subtractions | Multiplications | Divisions | Total |
|---|---:|---:|---:|---:|
| Determinant $2\cdot3-1\cdot1$ | 1 | 2 | 0 | 3 |
| Four inverse entries | 0 | 0 | 4 | 4 |
| Matrix-vector product | 2 | 4 | 0 | 6 |
| **Inverse method** | **3** | **6** | **4** | **13** |
| Multiplier $m=1/2$ | 0 | 0 | 1 | 1 |
| Updates $3-m\cdot1$, $8-m\cdot7$ | 2 | 2 | 0 | 4 |
| Solve $x_2=(9/2)/(5/2)$ | 0 | 0 | 1 | 1 |
| Back-substitute $x_1=(7-1\cdot x_2)/2$ | 1 | 1 | 1 | 3 |
| **Elimination method** | **3** | **3** | **3** | **9** |

These counts use a stated entrywise procedure; simplifying multiplications by $1$ or keeping the inverse factored can change the exact arithmetic count. They are not universal complexity constants.

**Gaussian elimination is simpler in this example:** there is one right-hand side and no inverse supplied, so it finds the two required coordinates directly with one row replacement and back substitution. Computing an entire inverse supplies more information than this one system needs. If $A^{-1}$ were already known, its construction cost would disappear; with many right-hand sides, that previous work could also be reused.

## 4. Verification

Substitute into both original equations:

$$2\left(\frac{13}{5}\right)+\frac95=\frac{26+9}{5}=7,$$

$$\frac{13}{5}+3\left(\frac95\right)=\frac{13+27}{5}=8.$$

To check the inverse method separately, $AA^{-1}=\frac15\begin{pmatrix}6-1&-2+2\\3-3&-1+6\end{pmatrix}=I$. Thus the methods agree and the result satisfies the original system. Uniqueness follows from $\det A=5\ne0$.
