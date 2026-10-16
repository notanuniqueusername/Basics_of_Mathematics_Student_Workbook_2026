# Exercise 10. A Polynomial Through Three Points

## The question

Find a polynomial $p(x)=ax^2+bx+c$ whose graph passes through $(0,1)$, $(1,3)$, and $(2,9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

## Before calculating: the concepts

Substituting each point into $p(x)=ax^2+bx+c$ produces a linear equation in the unknown coefficients.

## 1. Convert points into equations

The inputs $0,1,2$ are known numbers, while $a,b,c$ are the unknowns. Each point provides one equation by imposing $p(x)=y$. Start with the point at $x=0$ because its squared and linear terms vanish, immediately determining $c$.

## 2. Solve for the polynomial coefficients

Impose the three point conditions separately:

$$p(0)=a\cdot0^2+b\cdot0+c=1\quad\Longrightarrow\quad c=1,$$

$$p(1)=a+b+c=3,$$

$$p(2)=4a+2b+c=9.$$

These form a linear system in $a,b,c$, even though the polynomial is quadratic in its input $x$. Substitute $c=1$ into the last two equations:

$$a+b=2,\qquad 4a+2b=8.$$

Subtract twice the first equation from the second:

$$2a=4\Longrightarrow a=2.$$

Then $b=2-a=0$. Consequently

$$\boxed{p(x)=2x^2+1}.$$

## 3. Explain why a quadratic gives a linear coefficient system

The data values $0,1,2$ are fixed inputs. Squaring them gives the known numbers $0,1,4$; it does not square the unknown coefficient $a$. Thus every equation is linear in the unknowns $a,b,c$.

In matrix form, with coefficient order $a,b,c$,

$$\begin{pmatrix}0&0&1\\1&1&1\\4&2&1\end{pmatrix}\begin{pmatrix}a\\b\\c\end{pmatrix}=\begin{pmatrix}1\\3\\9\end{pmatrix}.$$

The coefficient determinant is

$$1\det\begin{pmatrix}1&1\\4&2\end{pmatrix}=2-4=-2\ne0.$$

Consequently the three data points determine a unique coefficient vector. This independently explains the uniqueness seen in elimination. The result has $a=2\ne0$, so it is genuinely a quadratic rather than a lower-degree polynomial that happens to fit the points.

## 4. Verification

Check all three prescribed points using the final polynomial:

$$p(0)=2\cdot0^2+1=1,$$

$$p(1)=2\cdot1^2+1=3,$$

$$p(2)=2\cdot2^2+1=8+1=9.$$

All points lie on its graph. The solution is unique because $c$ was forced by the first point, the elimination forced $a=2$, and then $b=0$ was forced. Thus the calculation did not merely construct one polynomial among several possible quadratics.
