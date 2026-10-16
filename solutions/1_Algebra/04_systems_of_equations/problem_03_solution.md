# Exercise 3. Inconsistent System

## The question

Solve or show that the system is inconsistent:
$$\begin{cases}x+2y=3,\\2x+4y=7.\end{cases}$$
Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

## Before calculating: the concepts

An augmented row with zero coefficients and a nonzero right-hand side is a contradiction.

## 1. Compare the coefficient rows

The second coefficient row is twice the first. To preserve consistency, its constant would also have to be twice the first constant. Twice $3$ is $6$, whereas the second right-hand side is $7$. Elimination makes this mismatch explicit.

## 2. Expose the contradiction in the augmented matrix

Write

$$\left[\begin{array}{cc|c}1&2&3\\2&4&7\end{array}\right].$$

Replace $R_2$ by $R_2-2R_1$. Its coefficient entries become $2-2\cdot1=0$ and $4-2\cdot2=0$, while its right-hand side becomes $7-2\cdot3=1$. Therefore

$$\left[\begin{array}{cc|c}1&2&3\\0&0&1\end{array}\right].$$

Read the last row as an equation:

$$0x+0y=1\quad\Longleftrightarrow\quad 0=1.$$

This contradiction is independent of $x$ and $y$. There is no pair that can satisfy it, so $\boxed{\text{the system has no solution}}$.

## 3. Interpret the last row

The row $(0,0\mid1)$ does not describe a free variable. It describes an impossible equation. A free variable can occur in a consistent system, whereas this row rules out every candidate pair. Geometrically, the two equations describe distinct parallel lines.

## 4. Verification

Check the contradiction directly in the original equations. Any pair satisfying $x+2y=3$ must also satisfy

$$2x+4y=2(x+2y)=2\cdot3=6.$$

The other equation demands $2x+4y=7$, so the two requirements cannot both hold. Geometrically, the lines are $y=3/2-x/2$ and $y=7/4-x/2$: the same slope but different intercepts. Thus they are parallel and distinct, agreeing with the absence of an intersection.
