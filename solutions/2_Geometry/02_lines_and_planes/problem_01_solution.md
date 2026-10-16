# Exercise 1. Line Through Two Points

## The question

Find the equation of the line through $A=(1,2)$ and $B=(4,-1)$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

## Before calculating: two descriptions of a line

A line through $A$ with nonzero direction $v$ is $A+tv$. In the plane, a perpendicular vector $n$ gives the equivalent equation $n\cdot(X-A)=0$.

In two dimensions, a direction vector tells how coordinates change along a line, while a normal vector is perpendicular to those changes. The normal's coefficients appear in general form $ax+by+c=0$. Its constant is set by a point on the line; perpendicularity determines orientation but not location.

## 1. Find a direction and parametric form

$$B-A=(4-1,-1-2)=(3,-3).$$

Use the simpler proportional direction $v=(1,-1)$:

$$\boxed{(x,y)=(1,2)+t(1,-1),\quad t\in\mathbb R}.$$

Thus $x=1+t$, $y=2-t$. A direction can be rescaled without changing the line, because the parameter ranges over all real numbers.

## 2. Obtain general form

Choose $n=(1,1)$, since $n\cdot v=1-1=0$. The normal equation is

$$(x-1)+(y-2)=0\quad\Longrightarrow\quad\boxed{x+y-3=0}.$$

Eliminating $t$ from the parametric equations also gives $y=3-x$, the same line.

## 3. Show the two forms describe exactly the same set

The parametric equations imply $x+y=3$, so every parameter gives a point of the general equation. Conversely, suppose $x+y=3$. Choose $t=x-1$. Then $x=1+t$ and $y=3-x=2-t$, recovering the parametric form. This proves equivalence in both directions, rather than merely checking two points.

Using the unscaled direction $(3,-3)$ would give $(x,y)=(1,2)+s(3,-3)$, with $t=3s$. The line is unchanged because $s$ and $t$ each range over all real numbers. Rescaling a direction changes its parameter speed, not the geometric set.

## 4. Verification

At $A$, $1+2-3=0$; at $B$, $4-1-3=0$. In parametric form, $t=0$ gives $A$, while $t=3$ gives $B$. For every $t$, $(1+t)+(2-t)=3$, so the whole parametrized line satisfies the general equation. The normal is perpendicular to the direction, not necessarily to either point's position vector.
