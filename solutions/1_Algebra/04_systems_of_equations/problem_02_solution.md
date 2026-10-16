# Exercise 2. Gaussian Elimination — One Solution

## The question

Solve using Gaussian elimination:
$$\begin{cases}x+y+z=6,\\2x-y+z=3,\\x+2y-z=2.\end{cases}$$
After solving, substitute the result into all equations and check consistency.

## Before calculating: the concepts

Gaussian elimination preserves the solution set when row operations also act on the right-hand side. Back substitution solves an upper triangular system.

## 1. Choose the first pivot

The leading coefficient of the first equation is $1$. Use it to remove $x$ from the second and third equations. Apply exactly the same operations to the constants: $3-2\cdot6=-9$ and $2-6=-4$. This produces equations involving only $y$ and $z$.

## 2. Eliminate and back-substitute

Write the augmented matrix in variable order $x,y,z$:

$$\left[\begin{array}{ccc|c}1&1&1&6\\2&-1&1&3\\1&2&-1&2\end{array}\right].$$

Use $R_2\leftarrow R_2-2R_1$:

$$\left[\begin{array}{ccc|c}1&1&1&6\\0&-3&-1&-9\\1&2&-1&2\end{array}\right].$$

Then $R_3\leftarrow R_3-R_1$ gives

$$\left[\begin{array}{ccc|c}1&1&1&6\\0&-3&-1&-9\\0&1&-2&-4\end{array}\right].$$

To remove the $1$ beneath the second pivot, add one third of row two to row three:

$$R_3\leftarrow R_3+\frac13R_2,\qquad \left[\begin{array}{ccc|c}1&1&1&6\\0&-3&-1&-9\\0&0&-7/3&-7\end{array}\right].$$

Back-substitute from the last row upward:

$$-\frac73z=-7\Longrightarrow z=3,$$

$$-3y-z=-9\Longrightarrow -3y-3=-9\Longrightarrow y=2,$$

$$x+y+z=6\Longrightarrow x+2+3=6\Longrightarrow x=1.$$

Thus $\boxed{(x,y,z)=(1,2,3)}$.

## 3. Explain the last elimination step

After clearing the first column, the second row is $-3y-z=-9$ and the third is $y-2z=-4$. Add one third of row two to row three: the coefficient of $y$ becomes $1-1=0$, the coefficient of $z$ becomes $-2-1/3=-7/3$, and the constant becomes $-4-3=-7$. Thus $z=3$. Work upward to obtain $y=2$ and finally $x=1$.

## 4. Verification

Substitute into every original equation, rather than only the reduced system:

$$x+y+z=1+2+3=6,$$

$$2x-y+z=2\cdot1-2+3=3,$$

$$x+2y-z=1+2\cdot2-3=2.$$

All three constants match. The echelon matrix has three nonzero pivots $1,-3,-7/3$, so there is no free variable; this verifies uniqueness as well as existence. Its diagonal product is $7\ne0$, consistent with an invertible coefficient matrix because only determinant-preserving row replacements were used.
