# Exercise 5. Row Echelon Form and Number of Solutions

## The question

For the augmented matrix
$$\left[\begin{array}{ccc|c}1&2&-1&3\\0&1&2&1\\0&0&0&0\end{array}\right]$$
determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

## Before calculating: the concepts

Pivot columns determine dependent variables; nonpivot columns correspond to free variables in a consistent echelon system.

## 1. Read the echelon form

The leading entries occur in columns one and two. Column three has no pivot, so $z$ is free. The zero last row has zero on the right as well, so it introduces no contradiction and no additional equation.

## 2. Express the pivot variables in terms of the free variable

Translate each nonzero row into its equation:

$$x+2y-z=3,\qquad y+2z=1.$$

The last row is $0=0$ and adds no restriction. The first leading entry is in column one and the second in column two; column three has no pivot. Choose $z=s$ as the single free variable.

Use the second equation first:

$$y+2s=1\quad\Longrightarrow\quad y=1-2s.$$

Then use the first:

$$x+2(1-2s)-s=3\quad\Longrightarrow\quad x+2-5s=3\quad\Longrightarrow\quad x=1+5s.$$

Therefore

$$\boxed{(x,y,z)=(1+5s,1-2s,s),\quad s\in\mathbb R}.$$

## 3. Explain why there is exactly one parameter

Choose $z=s$. The second row determines $y=1-2s$, and the first then determines $x=1+5s$. Once $s$ is chosen, neither of the other variables is free. Two pivots among three variables leave one degree of freedom, rather than two or three.

## 4. Verification

Substitute without fixing the parameter:

$$(1+5s)+2(1-2s)-s=1+5s+2-4s-s=3,$$

$$(1-2s)+2s=1.$$

The last row remains $0=0$. For example, $s=1$ gives $(6,-1,1)$, and $6+2(-1)-1=3$, $-1+2\cdot1=1$. There are two pivots among three variables, hence exactly one freely selectable coordinate. This distinguishes the harmless zero row from a contradiction such as $(0,0,0\mid1)$.
