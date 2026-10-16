# Exercise 9. A System from a Sum Condition

## The question

Find numbers $x,y$ satisfying
$$x+y=10,\qquad 2x+5y=32.$$
Solve the system and explain geometrically why the solution is unique.

## Before calculating: the concepts

Two linear equations describe two lines. Nonparallel lines intersect in exactly one point.

## 1. Eliminate one unknown

The coefficient of $x$ in the second equation is twice its coefficient in the first. Subtract twice the first equation from the second, including the constants. The difference removes $x$ and isolates $y$ without fractions.

## 2. Find the numbers and interpret the two lines

Subtract twice the sum equation from the second condition:

$$(2x+5y)-2(x+y)=32-2\cdot10.$$

Simplify:

$$3y=12\quad\Longrightarrow\quad y=4.$$

Substitute into the first equation:

$$x+4=10\quad\Longrightarrow\quad x=6.$$

Thus $\boxed{(x,y)=(6,4)}$.

To interpret uniqueness geometrically, write the lines in slope-intercept form:

$$y=10-x,\qquad y=\frac{32}{5}-\frac25x.$$

Their slopes are $-1$ and $-2/5$, respectively. They are not parallel and therefore have exactly one intersection: the point just found.

## 3. Connect elimination with the geometry of the lines

The first equation determines $x=10-y$. Substituting that expression into the second gives

$$2(10-y)+5y=32\quad\Longrightarrow\quad20+3y=32.$$

The nonzero coefficient $3$ forces one value of $y$, and the first equation then forces one value of $x$. This is the algebraic counterpart of the two distinct slopes: the constraints are independent rather than parallel copies of the same condition.

If the second equation had instead been $2x+2y=32$, elimination would have produced the contradiction $20=32$. If its right-hand side were $20$, it would add no new condition. The actual coefficients avoid both exceptional cases, explaining why this problem has exactly one pair rather than none or infinitely many.

## 4. Verification

Substitute into both original conditions:

$$6+4=10,\qquad 2\cdot6+5\cdot4=12+20=32.$$

As an algebraic check of uniqueness,

$$\det\begin{pmatrix}1&1\\2&5\end{pmatrix}=1\cdot5-1\cdot2=3\ne0.$$

The invertible coefficient matrix agrees with the distinct-slope geometric argument. A sum condition alone would permit infinitely many pairs, but the second independent line selects exactly one of them.
