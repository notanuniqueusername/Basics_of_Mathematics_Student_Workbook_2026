# Exercise 14. Contrast: Intersection and Parallelism

## The question

From the point $P=(0,0,1)$, two lines are drawn with direction vectors
$$v_1=(2,1,-1),\qquad v_2=(2,1,0).$$
For each line, analyze its position relative to the plane $z=0$.

For the line that intersects the plane, find the intersection point. For the other line, explain how you can recognize parallelism without solving an equation.

## Before calculating: inspect the vertical component

The plane $z=0$ has normal $n=(0,0,1)$. For a line from $P$, the dot product $n\cdot v$ equals its vertical direction component. A nonzero value permits crossing; zero keeps the height constant.

A horizontal plane is especially transparent because its normal tests only the vertical coordinate. The other direction components affect where a crossing occurs horizontally, but cannot decide whether a constant-height line ever reaches a different height. This separates the crossing criterion from the later point calculation.

## 1. First direction: find the intersection

The first line is

$$L_1(t)=(0,0,1)+t(2,1,-1)=(2t,t,1-t).$$

Its normal dot product is $-1\ne0$. Setting $z=0$ gives $1-t=0$, hence $t=1$:

$$\boxed{L_1\cap\{z=0\}=\{(2,1,0)\}}.$$

## 2. Second direction: recognize parallelism

The second line is $L_2(t)=(2t,t,1)$. Its direction has vertical component zero, so $n\cdot v_2=0$. Its height is always $1$, and its anchor is not in $z=0$. Therefore $\boxed{L_2\text{ is parallel and disjoint from the plane}}$.

## 3. Compare the two trajectories coordinate by coordinate

Both lines have the same horizontal motion $(x,y)=(2t,t)$. Their only difference is height: $1-t$ for the first and $1$ for the second. At $t=1$, both reach horizontal position $(2,1)$, but their spatial points are $(2,1,0)$ and $(2,1,1)$.

Thus the direction change in just one coordinate switches the classification from a unique intersection to no intersection. There is no need to solve a simultaneous spatial system for the second line: its height is visibly incompatible with the plane. In normal-dot-product terms, the first line has slope $-1$ in the plane residual, whereas the second has slope zero and nonzero constant residual $1$.

## 4. Verification

At $t=1$, the first line gives exactly $(2,1,0)$, whose height is zero. For the second line, every displacement has the form $(2t,t,0)$ and therefore cannot change the original height $1$. This distinction separates containment from disjoint parallelism: if its anchor height had been zero, the same second direction would instead give a line contained in the plane.
