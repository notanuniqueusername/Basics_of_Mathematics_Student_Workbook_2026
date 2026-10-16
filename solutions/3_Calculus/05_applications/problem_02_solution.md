# Problem 2. Maximum Area of a Rectangle

## The question

A rectangle has perimeter $40$.

1. Write its area as a function of the length of one side.
2. Determine the domain of this function resulting from the geometry of the problem.
3. Find the dimensions that give the maximum area.
4. Justify that the point found actually gives a maximum.

## Before calculating: eliminate one side with the constraint

Let $x,y$ be positive side lengths. Perimeter $40$ means $2x+2y=40$, so $y=20-x$. A rectangle must have both sides positive; zero-length boundary cases are degenerate and are used only for comparison.

An optimization model needs both an objective and the constraint that removes extra variables. Differentiating an area formula before enforcing the perimeter would leave two independent variables and would not answer the constrained question. The physical domain also excludes negative or zero side lengths even though the resulting polynomial is defined for all real inputs.

## 1. Build the objective and domain

$$\boxed{A(x)=x(20-x)=20x-x^2},\qquad\boxed{0<x<20}.$$

Area has squared length units, with side lengths in the same units as the perimeter.

## 2. Find and verify the optimum

$$A'(x)=20-2x=0\Longrightarrow x=10.$$

Then $y=20-10=10$. The derivative is positive for $x<10$ and negative for $x>10$, so this is the unique global maximum on the physical domain. Also $A''=-2<0$ and the area tends to zero at both domain boundaries.

$$\boxed{\text{Dimensions }10\times10,\qquad A_{\max}=100}.$$

## 3. Explain the square condition through balanced side changes

With $y=20-x$, increasing one side forces the other to decrease by the same amount. Near a candidate pair, the area change from a small increment $h$ is

$$(x+h)(20-x-h)-x(20-x)=h(20-2x)-h^2.$$

At $x=10$, the linear term vanishes and every nonzero sufficiently small change gives the negative amount $-h^2$. Away from $10$, a suitable sign of small $h$ makes the linear term positive and increases the area.

This increment argument explains the derivative condition geometrically: the marginal gain from lengthening one side must balance the loss from shortening the other. The equal-sided optimum is therefore a consequence of the constraint and objective, not an assumption about the desired rectangle.

## 4. Independent verification and interpretation

Complete the square:

$$A(x)=100-(x-10)^2\le100.$$

Equality occurs only at $x=10$, proving the global bound without calculus. The perimeter check is $2\cdot10+2\cdot10=40$. Nearby rectangles $9\times11$ and $8\times12$ have areas $99$ and $96$, confirming the predicted decline away from the square. The model, not differentiation alone, explains why a square is permitted and why the optimizing dimensions meet the original constraint.
