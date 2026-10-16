# Exercise 12. Intersection Line of Two Planes

## The question

Find a parametric equation of the line that is the intersection of
$$x+y+z=3,\qquad x-y+z=1.$$
Find its direction vector in two ways: from the system of equations and from the cross product of the normal vectors. Compare the results.

## Before calculating: solve the shared equations

Nonparallel planes intersect in a line. Its points satisfy both equations, while its direction is perpendicular to both plane normals.

A direction of the intersection line must be tangent to both planes, hence perpendicular to both normals. Their nonzero cross product gives such a direction, while solving the two equations supplies one anchor point. These roles are distinct: a correct direction alone would leave infinitely many parallel candidate lines.

## 1. Solve for the intersection

Subtract the second equation from the first:

$$(x+y+z)-(x-y+z)=3-1\quad\Longrightarrow\quad2y=2,$$

so $y=1$. The first then gives $x+z=2$. Choose $x=t$ and obtain $z=2-t$:

$$\boxed{(x,y,z)=(0,1,2)+t(1,0,-1),\quad t\in\mathbb R}.$$

From this system-based parametrization, the direction is $v=(1,0,-1)$.

## 2. Obtain the direction from normals

$$n_1=(1,1,1),\qquad n_2=(1,-1,1),$$

Apply the component formula $(a_2b_3-a_3b_2,\ a_3b_1-a_1b_3,\ a_1b_2-a_2b_1)$:

$$n_1\times n_2=\bigl(1\cdot1-1\cdot(-1),\ 1\cdot1-1\cdot1,\ 1\cdot(-1)-1\cdot1\bigr).$$

The components are $1-(-1)=2$, $1-1=0$, and $-1-1=-2$, respectively. Hence

$$n_1\times n_2=(2,0,-2)=2(1,0,-1)=2v.$$

The proportional directions describe the same line; direction vectors need not have equal lengths.

## 3. Explain why the solution has exactly one free parameter

Subtracting the two plane equations fixes $y=1$. Their remaining independent condition is $x+z=2$, leaving one coordinate free. Choosing $x=t$ gives the anchor $(0,1,2)$ at $t=0$ and the direction $(1,0,-1)$.

One could instead choose $z=s$, giving $(x,y,z)=(2-s,1,s)=(2,1,0)+s(-1,0,1)$. This appears different but is the same line: $s=2-t$ matches the coordinates, and the new direction is the negative of the first. The cross-product result $(2,0,-2)$ also describes this same direction line, explaining why proportional rather than identical vectors are the correct comparison.

## 4. Verification

For the general point $(t,1,2-t)$,

$$t+1+(2-t)=3,\qquad t-1+(2-t)=1.$$

Both plane equations hold for every $t$. Also $n_1\cdot v=1-1=0$ and $n_2\cdot v=1-1=0$, confirming the direction lies in both planes. The nonzero cross product rules out parallel planes.
