# Exercise 2. Circle by Completing the Square

## The question

Reduce
$$x^2+y^2-6x+4y-3=0$$
to canonical form. Find the center and radius, then substitute two simple points from the circle into both forms of the equation.

## Before calculating: complete squares without changing the equation

Use $x^2-2hx=(x-h)^2-h^2$. Any constant introduced inside a square must be balanced elsewhere. A circle has canonical form $(x-h)^2+(y-k)^2=r^2$.

Completing the square uses the identity $(x-h)^2=x^2-2hx+h^2$. The added $h^2$ must also be subtracted so the expression remains exactly equal to the original. The center is the point at which both shifted coordinates vanish; it is inside the circle and is not normally a point satisfying the boundary equation.

## 1. Complete both squares

$$x^2-6x=(x-3)^2-9,\qquad y^2+4y=(y+2)^2-4.$$

Substitute into the original equation:

$$(x-3)^2-9+(y+2)^2-4-3=0.$$

Thus

$$\boxed{(x-3)^2+(y+2)^2=16}.$$

## 2. Read the geometry and choose points

The center is $\boxed{(3,-2)}$ and the radius is $\boxed{4}$. The sign in $y+2=y-(-2)$ puts the center below the $x$-axis.

Moving four units horizontally from the center gives two convenient circle points $P=(7,-2)$ and $Q=(-1,-2)$.

## 3. Explain how the constants determine radius and center

For the $x$ group, half of $-6$ is $-3$, so the shift is $x-3$ and the balancing constant is $-9$. For the $y$ group, half of $4$ is $2$, so the shift is $y+2$ and the balancing constant is $-4$. Together with the original $-3$, these give $-16$ outside the squares.

Moving that constant to the right yields radius squared $16$, hence radius $4$, not $16$. At the center $(3,-2)$, the original expression equals $-16$, which agrees with the translated expression $0+0-16$. This additional check catches a radius error even before checking the selected boundary points.

## 4. Verification in both forms

In canonical form, $P$ gives $(7-3)^2+0=16$, and $Q$ gives $(-1-3)^2+0=16$.

In the original expression,

$$P:\quad49+4-42-8-3=0,$$

$$Q:\quad1+4+6-8-3=0.$$

Finally, expanding the canonical equation gives $x^2-6x+9+y^2+4y+4=16$, or $x^2+y^2-6x+4y-3=0$, recovering every original coefficient and constant.
