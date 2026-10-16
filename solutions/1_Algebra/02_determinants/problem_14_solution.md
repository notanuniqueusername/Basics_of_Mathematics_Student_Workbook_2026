# Exercise 14. A System of Equations and the Determinant

## The question

Consider the system $Ax=b$, where
$$A=\begin{pmatrix}1&2\\k&4\end{pmatrix}.$$
For which values of $k$ does the system have exactly one solution for every $b$? For the remaining value, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example for which it has no solution.

## Before calculating: the concepts

$Ax=b$ has exactly one solution for every right-hand side precisely when $A$ is invertible. At a singular value, consistency depends on $b$.

## 1. Apply the criterion for all right-hand sides

The phrase “for every $b$” calls for invertibility of the coefficient matrix. Compute its determinant first. Then handle the singular parameter separately; a singular system can be consistent for some right-hand sides and inconsistent for others.

## 2. Find the parameter cases and construct examples

Compute

$$\det A=1\cdot4-2k=4-2k=2(2-k).$$

Thus $\boxed{k\ne2}$ gives an invertible matrix, and hence exactly one solution for every $b$.

At $k=2$, writing $b=(b_1,b_2)^T$ gives

$$x+2y=b_1,\qquad 2x+4y=b_2.$$

Subtract twice the first equation from the second: $0=b_2-2b_1$.

**Compatible example:** choose $b=(1,2)^T$. Only $x+2y=1$ remains, so $y=s$ and $x=1-2s$ for every real $s$.

**Incompatible example:** choose $b=(1,3)^T$. The reduced equation is $0=3-2=1$, so no solution exists.

## 3. Explain the distinction at the singular value

When $k=2$, the second left-hand side is twice the first. A compatible right-hand side must have the same relation. Compatibility leaves one free variable, whereas failure of that relation produces a contradiction. Neither choice gives a unique solution at this parameter.

## 4. Verification

For the infinite family, substitute into both equations:

$$(1-2s)+2s=1,\qquad 2(1-2s)+4s=2.$$

For instance, $s=0$ and $s=1$ give distinct solutions $(1,0)$ and $(-1,1)$.

For the inconsistent example, the first equation forces the second left-hand side to equal $2$, so it cannot equal $3$. Finally, when $k\ne2$, elimination gives $(4-2k)y=b_2-kb_1$, determining $y$ uniquely and then $x=b_1-2y$, explicitly confirming uniqueness for every $b$.
