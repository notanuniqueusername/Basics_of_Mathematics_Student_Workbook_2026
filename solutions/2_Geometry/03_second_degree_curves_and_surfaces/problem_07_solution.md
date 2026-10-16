# Exercise 7. Classifying a Second-Degree Equation

## The question

Determine the type of object described by:
1. $4x^2+9y^2=36$,
2. $x^2-y^2=1$,
3. $x^2-4y=0$,
4. $x^2+y^2+1=0$.

In the last case, explain why there are no real points.

## Before calculating: normalize and check real existence

Signs and the number of squared coordinates suggest a curve type, but real existence must still be checked. In particular a sum of real squares cannot be negative.

Classification depends on both the squared-term pattern and the right-hand side after rearrangement. A sum of positive squares equal to a positive number gives a real bounded curve; equal to zero it may reduce to a point; equal to a negative number it has no real points. Algebraic resemblance alone does not establish a real geometric object.

## 1. Normalize the four equations

1. Divide $4x^2+9y^2=36$ by $36$:

$$\frac{x^2}{9}+\frac{y^2}{4}=1.$$

This is an ellipse centered at the origin with semiaxes $3$ and $2$.

2. The equation $x^2-y^2=1$ is a horizontal hyperbola, with vertices $(\pm1,0)$ and asymptotes $y=\pm x$.

3. Rearrange $x^2-4y=0$ as $y=x^2/4$. This is a parabola with vertex $(0,0)$, axis $x=0$, opening upward.

4. Rearrange the last equation as $x^2+y^2=-1$. Since $x^2+y^2\ge0$ for real coordinates, it has no real points. It is not a real circle with a negative radius.

## 2. Explain the recognition mechanism

The first two have two squared terms, with equal signs in the ellipse and opposite signs in the hyperbola. The third has only one squared variable and a linear other variable. The fourth resembles a circle algebraically but fails the nonnegative-radius-squared condition.

## 3. Make the scales and feasible coordinates explicit

For the ellipse, setting $y=0$ gives $x=\pm3$ and setting $x=0$ gives $y=\pm2$, confirming its unequal semiaxes. For the hyperbola, rearrangement gives $y^2=x^2-1$, so $|x|\ge1$ and the branches lie outside the central gap.

For the parabola, $y=x^2/4\ge0$, with symmetry under $x\mapsto-x$ and no restriction on $x$. It opens upward, unlike a form with $y^2$ and a linear $x$ term.

For the empty equation, the obstruction is not a missing convenient test point: the inequality $x^2+y^2+1\ge1$ rules out every real pair simultaneously. A finite search for points would not supply that proof.

## 4. Verification

Real points include $(3,0)$ for the ellipse, $(1,0)$ for the hyperbola, and $(2,1)$ for the parabola; substitution gives $36$, $1$, and $4-4=0$, respectively. For the last equation, its left-hand side is at least $1$, with minimum $1$ at $(0,0)$, so it cannot vanish anywhere in the real plane.
