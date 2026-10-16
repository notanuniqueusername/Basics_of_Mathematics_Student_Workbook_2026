# Exercise 8. Two Systems with the Same Coefficient Matrix

## The question

Solve by elimination the two systems
$$\begin{cases}2x+y=5,\\x-y=1,\end{cases}$$
$$\begin{cases}2x+y=1,\\x-y=4.\end{cases}$$
Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

## Before calculating: the concepts

The same row operations eliminate the same coefficient matrix, regardless of the right-hand side. Both right-hand sides may be processed together.

## 1. Keep both right-hand sides aligned

Both systems have coefficient matrix $\begin{pmatrix}2&1\\1&-1\end{pmatrix}$. Write their right-hand sides as two separate augmented columns. Carrying both columns through the same row operation solves the systems together without confusing which constants belong to which system.

## 2. Perform the shared elimination

Place the two right-hand sides in separate columns beside the shared coefficients:

$$\left[\begin{array}{cc|cc}2&1&5&1\\1&-1&1&4\end{array}\right].$$

Use $R_2\leftarrow R_2-\frac12R_1$. The coefficient row becomes $(0,-3/2)$. The right-hand sides become $1-5/2=-3/2$ and $4-1/2=7/2$:

$$\left[\begin{array}{cc|cc}2&1&5&1\\0&-3/2&-3/2&7/2\end{array}\right].$$

For the first system,

$$-\frac32y=-\frac32\Longrightarrow y=1,\qquad 2x+1=5\Longrightarrow x=2.$$

For the second system,

$$-\frac32y=\frac72\Longrightarrow y=-\frac73,\qquad 2x-\frac73=1\Longrightarrow x=\frac53.$$

Thus the solutions, in the stated order, are $\boxed{(2,1)}$ and $\boxed{(5/3,-7/3)}$. The elimination multiplier and coefficient pivots are identical; only the constants and resulting coordinates differ.

## 3. Identify the reusable part of the calculation

The multiplier $1/2$ and the coefficient pivots depend only on the common matrix $A$. For any right-hand side $b=(b_1,b_2)^T$, the same row replacement produces

$$2x+y=b_1,\qquad-\frac32y=b_2-\frac12b_1.$$

Therefore the shared solution procedure is

$$y=\frac{b_1-2b_2}{3},\qquad x=\frac{b_1-y}{2}=\frac{b_1+b_2}{3}.$$

Substituting the two supplied right-hand sides into these formulas reproduces the two computed pairs. This separates the fixed coefficient work from the changing data: a new right-hand side changes the transformed constants and final coordinates, but does not require choosing new elimination multipliers. Keeping both right-hand sides in one augmented calculation makes that reuse explicit.

## 4. Verification

For the first system,

$$2(2)+1=5,\qquad 2-1=1.$$

For the second,

$$2\left(\frac53\right)-\frac73=\frac{10-7}{3}=1,\qquad \frac53-\left(-\frac73\right)=\frac{12}{3}=4.$$

Each pair satisfies its own two original equations. Both coefficient pivots, $2$ and $-3/2$, are nonzero, so both solutions are unique. Processing the two constants together has reused elimination without treating them as two equations belonging to a single unknown vector.
