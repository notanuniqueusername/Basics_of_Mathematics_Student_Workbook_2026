# Problem 6. Average Value of a Function

## The question

Compute the average value of the function
$$
f(x)=x^2
$$
on the interval $[0,3]$.

Find a point $c\in[0,3]$ for which $f(c)$ is equal to this average value, and interpret the result geometrically.

## Before calculating: average height preserves accumulated area

The average value on $[a,b]$ is $\bar f=(b-a)^{-1}\int_a^bf(x)\,dx$. Geometrically it is the height of a rectangle with the same width and area as the region under a nonnegative graph.

A continuous average is weighted by interval length through integration, not by selecting a finite collection of sample heights. Dividing by the interval length converts total area back to a height. The integral mean-value theorem guarantees that a continuous function attains that average somewhere, but finding the point still requires solving the corresponding equation and checking the domain.

## 1. Calculate the average

$$\int_0^3x^2\,dx=\left[\frac{x^3}{3}\right]_0^3=9.$$

Divide by interval length $3$:

$$\boxed{\bar f=\frac93=3}.$$

It is not the average of endpoint heights, $(0+9)/2=4.5$, because the graph is curved rather than linear.

## 2. Find the point taking this value

Solve $f(c)=3$:

$$c^2=3\Longrightarrow c=\pm\sqrt3.$$

Only the positive root lies in $[0,3]$, so $\boxed{c=\sqrt3}$.

## 3. Explain the equal-area rectangle and the selected point

The graph $y=x^2$ over $[0,3]$ bounds area $9$. Replacing its varying height by the constant $3$ over the same width preserves that area, since $3\cdot3=9$. The line $y=3$ meets the graph at $x=\sqrt3$ within the interval.

The equation $c^2=3$ also has the negative solution $-\sqrt3$, but it lies outside the specified averaging interval and must be discarded. Strict increase on $[0,3]$ shows there is exactly one admissible intersection.

For a numerical bound, the average height $3$ lies between $f(0)=0$ and $f(3)=9$, as any average of nonnegative heights bounded by those values must. It differs from the midpoint height $f(1.5)=2.25$, illustrating that averaging inputs before evaluating is not the same operation as averaging function values.

## 4. Verification and interpretation

The rectangle of width $3$ and height $3$ has area $9$, equal to the integral. Also $f(\sqrt3)=3$ and $0<\sqrt3<3$, verifying both the height condition and interval membership.

Because $f$ is continuous, its average lies between its minimum and maximum: $0\le3\le9$. Strict increase on $[0,3]$ makes the point $c$ unique. The integral mean-value principle guarantees existence in this continuous example, while solving the equation identifies the actual point.
