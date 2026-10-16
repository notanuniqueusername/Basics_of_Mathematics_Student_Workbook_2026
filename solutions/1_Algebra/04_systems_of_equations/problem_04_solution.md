# Exercise 4. Infinitely Many Solutions

## The question

Solve
$$\begin{cases}x+y+z=2,\\2x+2y+2z=4,\\x-y+z=0.\end{cases}$$
Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

## Before calculating: the concepts

A consistent system with a free variable has infinitely many solutions. A zero augmented row adds no restriction.

## 1. Remove the repeated information

The second equation is twice the first, including its right-hand side, so it will become a zero row. Subtracting the first equation from the third instead removes $x$ and $z$, leaving an equation that determines $y$.

## 2. Reduce and introduce a free variable

Start with

$$\left[\begin{array}{ccc|c}1&1&1&2\\2&2&2&4\\1&-1&1&0\end{array}\right].$$

The replacement $R_2\leftarrow R_2-2R_1$ produces a zero row:

$$\left[\begin{array}{ccc|c}1&1&1&2\\0&0&0&0\\1&-1&1&0\end{array}\right].$$

Next $R_3\leftarrow R_3-R_1$ gives row three $(0,-2,0\mid-2)$. Swap rows two and three to put the zero row last:

$$\left[\begin{array}{ccc|c}1&1&1&2\\0&-2&0&-2\\0&0&0&0\end{array}\right].$$

The second row gives $y=1$, and the first becomes $x+z=1$. Column three has no pivot, so choose the free variable $z=s$:

$$\boxed{(x,y,z)=(1-s,1,s),\quad s\in\mathbb R}.$$

The row swap preserves the solution set; unlike determinant calculations, no sign adjustment to the solutions is involved.

## 3. Describe the whole solution set

With $y=1$, the first equation becomes $x+z=1$. Either $x$ or $z$ may be chosen freely; choosing $z=s$ makes $x=1-s$. The parameter must range over all real numbers to describe every solution. Different parameter values give different third coordinates, so the family contains infinitely many distinct points.

## 4. Verification

Check the whole family in the original equations:

$$(1-s)+1+s=2,$$

$$2(1-s)+2\cdot1+2s=2-2s+2+2s=4,$$

$$(1-s)-1+s=0.$$

Every real $s$ works. As the requested concrete example, $s=0$ gives $(1,1,0)$, for which the left-hand sides are $2$, $4$, and $0$. Distinct choices of $s$ give distinct third coordinates, so there really are infinitely many solutions. Conversely, elimination forced $y=1$ and $x=1-z$, so the family includes every solution.
