# Problem 14. A Piecewise-Defined Function

## The question

Let
$$f(x)=\begin{cases}x+1,&-1\le x<1,\\2,&1\le x\le3.\end{cases}$$
Sketch the graph, decide where to split the integral, compute
$$\int_{-1}^{3}f(x)\,dx$$
and verify the result geometrically.

## Before calculating: split where the formula changes

The function switches at $x=1$. Its first branch rises from $0$ to $2$, and its second is the constant height $2$. The branches meet there, so there is no jump, but different antiderivative formulas are still needed on the two intervals.

A piecewise formula determines where an integral must be split, even if the pieces join continuously. The splitting is about which expression is valid on each subinterval. Values at finitely many individual endpoints do not affect a Riemann integral, so the strict versus nonstrict inequality at the join does not create an additional area term.

## 1. Sketch and split

```text
 f(x)
 2 |        *-----------* (3,2)
   |       / (1,2)
 0 |  *---/-----------------> x
    (-1,0)
```

The point $(1,2)$ belongs to the second branch; the first branch has the same limiting height. A single endpoint's assignment does not change the integral.

$$\int_{-1}^3f(x)\,dx=\int_{-1}^1(x+1)\,dx+\int_1^3 2\,dx.$$

## 2. Evaluate the pieces

$$\int_{-1}^1(x+1)\,dx=\left[\frac{x^2}{2}+x\right]_{-1}^1=\frac32-\left(-\frac12\right)=2,$$

$$\int_1^3 2\,dx=[2x]_1^3=6-2=4.$$

Hence $\boxed{\int_{-1}^3f(x)\,dx=6}$.

## 3. Construct a continuous accumulation check across the join

An antiderivative on the first piece is $G(x)=(x+1)^2/2$, chosen so $G(-1)=0$. At $x=1$ it gives $G(1)=2$. Continuing accumulation on the constant second piece gives

$$G(x)=\begin{cases}(x+1)^2/2,&-1\le x\le1,\\2+2(x-1)=2x,&1\le x\le3.\end{cases}$$

The formulas agree at the join and have derivative $x+1$ and $2$ on their respective interiors. Hence the total accumulation is $G(3)-G(-1)=6-0=6$.

This checks the split-integral result using a single continuous accumulated-area function. It also makes visible why unrelated primitive constants on the two pieces must be coordinated before treating them as one function across the join.

## 4. Geometric verification

The rising part bounds a triangle of base $2$ and height $2$, area $2$. The constant part bounds a rectangle of width $2$ and height $2$, area $4$. Their total is $6$, agreeing with the integral. Both regions lie above the axis, so no signed-area correction is needed. The graph and split together explain why integrating either branch over the whole interval would be incorrect.
