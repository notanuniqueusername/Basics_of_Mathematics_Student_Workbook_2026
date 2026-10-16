# Exercise 1. From a System to a Matrix

## The question

Write the system
$$\begin{cases}2x-y+z=4,\\x+3y-2z=1,\\3x+y+z=7.\end{cases}$$
in the form $Ax=b$.
Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

## Before calculating: the concepts

In $A\mathbf{x}=b$, each row of $A$ lists the coefficients of one equation in the same variable order.

## 1. Fix the order of the unknowns

Use the same order $x,y,z$ in every row. A coefficient is the number multiplying that variable, including its sign. The first equation contributes $(2,-1,1)$, the second contributes $(1,3,-2)$, and the third contributes $(3,1,1)$. The constants belong in a separate column vector.

## 2. Write the three matrix components

Read the coefficients in the fixed order $x,y,z$:

| Equation | Coefficient of $x$ | Coefficient of $y$ | Coefficient of $z$ | Constant |
|---|---|---|---|---|
| $2x-y+z=4$ | $2$ | $-1$ | $1$ | $4$ |
| $x+3y-2z=1$ | $1$ | $3$ | $-2$ | $1$ |
| $3x+y+z=7$ | $3$ | $1$ | $1$ | $7$ |

An omitted numerical coefficient means $1$; a minus sign by itself means $-1$. Put the coefficient columns into $A$, the unknowns into a column vector, and the constants into $b$:

$$\boxed{A=\begin{pmatrix}2&-1&1\\1&3&-2\\3&1&1\end{pmatrix},\quad \mathbf{x}=\begin{pmatrix}x\\y\\z\end{pmatrix},\quad b=\begin{pmatrix}4\\1\\7\end{pmatrix}}.$$

The requested matrix equation is

$$\boxed{\begin{pmatrix}2&-1&1\\1&3&-2\\3&1&1\end{pmatrix}\begin{pmatrix}x\\y\\z\end{pmatrix}=\begin{pmatrix}4\\1\\7\end{pmatrix}}.$$

Bold $\mathbf{x}$ denotes the whole unknown vector, distinguishing it from the first scalar coordinate $x$.

## 3. Check the dimensions and correspondence

The coefficient matrix is $3\times3$, the unknown vector is $3\times1$, and their product is $3\times1$, matching the right-hand side. The first row-column product gives the first equation, and the same correspondence holds for rows two and three. No solving is required: this task asks for a change of notation.

## 4. Verification

Multiply the left-hand side to recover the scalar equations:

$$A\mathbf{x}=\begin{pmatrix}2\cdot x+(-1)y+1\cdot z\\1\cdot x+3y+(-2)z\\3x+1\cdot y+1\cdot z\end{pmatrix}=\begin{pmatrix}2x-y+z\\x+3y-2z\\3x+y+z\end{pmatrix}.$$

Equating these entries with $4,1,7$ gives exactly the original three equations, including both negative coefficients. The dimensions also agree: $(3\times3)(3\times1)=3\times1$. No equation was added or removed, and the unknown order is identical in every row.
