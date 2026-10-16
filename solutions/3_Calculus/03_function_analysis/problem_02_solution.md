# Problem 2. A Parabola from the Perspective of the Derivative

## The question

For $f(x)=x^2-4x+1$, find the minimum using the derivative. Compare the result with the vertex form and explain why both approaches lead to the same point.

## Before calculating: use a derivative sign change

A differentiable function has a local minimum where its derivative changes from negative to positive. To establish a global minimum, also consider the whole domain or an exact lower bound.

A critical point is only a candidate until its surrounding derivative sign or another argument establishes its type. The quadratic's full real domain makes a global statement straightforward: the derivative pattern covers every real input, and the completed square supplies an exact lower bound attained at one point.

## 1. Find and classify the critical point

$$f'(x)=2x-4=2(x-2).$$

The unique zero is $x=2$. For $x<2$, $f'<0$; for $x>2$, $f'>0$. The function decreases then increases, so it has a minimum at

$$\boxed{x=2,\qquad f(2)=4-8+1=-3}.$$

Because these intervals exhaust the real domain, it is a global minimum. Alternatively $f''=2>0$ confirms the upward curvature.

## 2. Compare with vertex form

Complete the square:

$$f(x)=x^2-4x+1=(x-2)^2-3.$$

Since $(x-2)^2\ge0$, its least value is $-3$, achieved exactly at $x=2$. Both methods identify the same vertex $\boxed{(2,-3)}$.

## 3. Relate the vertex shift to the derivative calculation

Writing $u=x-2$ turns the function into $u^2-3$. The horizontal shift moves the vertex from $x=0$ to $x=2$, and the vertical shift moves its height from $0$ to $-3$. Neither changes the upward-opening curvature.

Its derivative with respect to $x$ is $2u\,du/dx=2(x-2)$ because $du/dx=1$. Thus the critical equation is precisely the condition that the shifted horizontal coordinate be zero. The algebraic and calculus methods are not competing coincidences: both locate where the nonnegative square has its smallest value. They also establish uniqueness, since $(x-2)^2=0$ only when $x=2$.

## 4. Verification

The derivative from vertex form is $2(x-2)$, agreeing with the original differentiation. Symmetric values $f(1)=f(3)=-2$ exceed $-3$, and the exact gap is $f(x)-f(2)=(x-2)^2\ge0$ for every $x$. The derivative explains how the function approaches and leaves the minimum; the completed square explains its height and symmetry directly.
