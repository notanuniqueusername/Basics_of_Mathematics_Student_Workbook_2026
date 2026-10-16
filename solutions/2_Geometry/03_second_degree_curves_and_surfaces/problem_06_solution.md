# Exercise 6. Shifted Ellipse

## The question

Reduce
$$4x^2+9y^2-16x+18y-11=0$$
to canonical form. Give the center and semiaxis lengths. Check that substituting the coordinates of the center into the left-hand side gives a value consistent with the form you obtained.

## Before calculating: account for outside coefficients

Complete the square inside each coordinate group, then multiply the compensating constants by the outside coefficient. A shifted ellipse is recognized after dividing by a positive right-hand side.

A translated ellipse has form $(x-h)^2/a^2+(y-k)^2/b^2=1$. Its center is $(h,k)$ and its semiaxes are the positive square roots of the denominators. The denominator under a squared coordinate determines that coordinate's scale; one should not assign the longer semiaxis by an assumed naming convention for $a$ or $b$.

## 1. Complete the squares

$$4(x^2-4x)+9(y^2+2y)-11=0,$$

$$4[(x-2)^2-4]+9[(y+1)^2-1]-11=0.$$

The constants are $-16-9-11=-36$, so

$$4(x-2)^2+9(y+1)^2=36.$$

Divide by $36$:

$$\boxed{\frac{(x-2)^2}{9}+\frac{(y+1)^2}{4}=1}.$$

## 2. Read the ellipse

The center is $\boxed{(2,-1)}$, with horizontal semiaxis $\boxed{3}$ and vertical semiaxis $\boxed{2}$. The axis endpoints are $(5,-1),(-1,-1),(2,1),(2,-3)$.

The center is inside the ellipse, not on it. Its canonical left-hand side is $0$, whereas points on the boundary have value $1$.

## 3. Derive the semiaxes and all four endpoints

At the center height $y=-1$, the second square vanishes, leaving $(x-2)^2/9=1$. Thus $x-2=\pm3$, giving $(-1,-1)$ and $(5,-1)$, each three units horizontally from the center.

At the center's horizontal coordinate $x=2$, the first square vanishes, leaving $(y+1)^2/4=1$. Hence $y+1=\pm2$, giving $(2,-3)$ and $(2,1)$, each two units vertically from the center.

This derives the endpoint list rather than only reading it off. The enclosing rectangle is $-1\le x\le5$, $-3\le y\le1$, and the longer axis is horizontal. The original polynomial is exactly $36$ times the normalized ellipse left side minus $36$, explaining its negative value at the center.

## 4. Verification

At the center, the original left-hand side is

$$4\cdot2^2+9(-1)^2-16\cdot2+18(-1)-11=16+9-32-18-11=-36.$$

This matches $4(x-2)^2+9(y+1)^2-36$ at $(2,-1)$, which is also $-36$. There is no reason for this value to be zero at the center. At the endpoint $(5,-1)$, the original expression gives $100+9-80-18-11=0$, checking a boundary point as well.
