# Problem 4. Area Between Curves

## The question

Find the area of the region bounded by the graphs
$$
y=x
$$
and
$$
y=x^2.
$$

First find the intersection points and justify which function is greater on the relevant interval.

## Before calculating: area requires upper minus lower

First locate the intersections and determine which graph is above the other. Integrating a difference over the wrong interval or in the wrong order can give an incorrect sign or an unbounded region.

The phrase “bounded by” requires finding the actual enclosed interval from curve intersections. The vertical-strip height is the upper ordinate minus the lower ordinate on that interval. It is not enough to choose subtraction order by how the functions were listed in the question; their relative sign must be established algebraically.

## 1. Determine the bounded region

Solve $x=x^2$:

$$x(x-1)=0\Longrightarrow x=0,1.$$

The intersection points are $(0,0)$ and $(1,1)$. On $0<x<1$, $x-x^2=x(1-x)>0$, so $y=x$ is above $y=x^2$.

## 2. Integrate the vertical strip heights

$$A=\int_0^1(x-x^2)\,dx=\left[\frac{x^2}{2}-\frac{x^3}{3}\right]_0^1=\frac12-\frac13.$$

Therefore $\boxed{A=1/6}$ square units. Each thin strip has width $dx$ and height $x-x^2$, which explains the integral rather than just supplying a formula.

## 3. Verify the same area with horizontal strips

Inside the bounded region, $0\le y\le1$. Solving the boundaries for $x$ gives $x=y$ on the line and $x=\sqrt y$ on the right-hand parabola branch. Since $\sqrt y\ge y$ in this range, a horizontal strip has width $\sqrt y-y$.

Thus a second construction gives

$$A=\int_0^1(\sqrt y-y)\,dy=\left[\frac23y^{3/2}-\frac{y^2}{2}\right]_0^1=\frac23-\frac12=\frac16.$$

This uses a different orientation of strips and agrees with the vertical-strip calculation. The negative root $x=-\sqrt y$ is not part of this region, which lies between the two nonnegative intersection points. That restriction follows from the geometry, not just the algebraic square-root equation.

## 4. Verification

The area under the upper line is $\int_0^1x\,dx=1/2$ and under the lower parabola is $\int_0^1x^2\,dx=1/3$, so their difference is $1/6$.

As a bound, $0\le x-x^2=1/4-(x-1/2)^2\le1/4$ on a unit-length interval. Hence $0\le A\le1/4$, consistent with $1/6$. The integrand vanishes at both intersections and is positive inside, matching a bounded nonnegative geometric area.
