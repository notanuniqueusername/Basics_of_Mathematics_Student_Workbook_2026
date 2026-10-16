# Exercise 12. Homogeneous System

## The question

Solve
$$\begin{cases}x+2y-z=0,\\2x+4y-2z=0,\\x-y+2z=0.\end{cases}$$
Give all solutions in parametric form and explain why $(0,0,0)$ always satisfies a homogeneous system.

## Before calculating: the concepts

A homogeneous system has zero right-hand side. It always admits the zero vector; free variables can produce further solutions.

## 1. Use the homogeneous structure

Every right-hand side is zero, so row replacements keep that column zero. The second equation is twice the first and therefore contributes no new restriction. Subtracting the first equation from the third reveals the relation between $y$ and $z$.

## 2. Reduce and parameterize all solutions

Write the augmented matrix:

$$\left[\begin{array}{ccc|c}1&2&-1&0\\2&4&-2&0\\1&-1&2&0\end{array}\right].$$

Use $R_2\leftarrow R_2-2R_1$ and then $R_3\leftarrow R_3-R_1$:

$$\left[\begin{array}{ccc|c}1&2&-1&0\\0&0&0&0\\0&-3&3&0\end{array}\right].$$

Swap the lower rows to place the zero row last. The second nonzero row is $-3y+3z=0$, hence $y=z$. Choose $z=s$. The first row then gives

$$x+2s-s=0\quad\Longrightarrow\quad x=-s.$$

Therefore

$$\boxed{(x,y,z)=(-s,s,s)=s(-1,1,1),\quad s\in\mathbb R}.$$

There are two pivots and one free variable, giving a line of solutions through the origin.

## 3. Distinguish the zero solution from the full family

Setting $s=0$ gives the zero vector, which always solves a homogeneous system. Here the free variable also allows nonzero solutions, such as $(-1,1,1)$ at $s=1$. In vector form the whole solution set is $s(-1,1,1)$, a line through the origin.

## 4. Verification

Check the whole family:

$$x+2y-z=-s+2s-s=0,$$

$$2x+4y-2z=-2s+4s-2s=0,$$

$$x-y+2z=-s-s+2s=0.$$

At $s=0$ the zero vector is recovered. More generally, a homogeneous system has the form $Av=0$, and $A0=0$ for any matrix $A$, explaining why the zero vector always works. At $s=1$, $(-1,1,1)$ gives a nonzero solution here. Conversely, the reduced equations force $y=z$ and $x=-z$, so no solutions are missing from the family.
