# Problem 11. Derivative from the Definition

## The question

Using only
$$f'(x)=\lim_{h\to0}\frac{f(x+h)-f(x)}h,$$
find the derivative of $f(x)=x^2$. Compare the result with the power rule and indicate where the limit is used in the calculation.

## Before calculating: start from the definition only

The derivative is the limit of secant slopes. Keep $h\ne0$ during cancellation and let $h\to0$ only after simplifying the quotient; substituting $h=0$ initially would give $0/0$.

The derivative definition takes a limit with the base point $x$ held fixed and the increment $h$ varying toward zero. These symbols play different roles. Algebraic cancellation is performed only for nonzero $h$, which is exactly the condition in a punctured limit; the final limit can exist even though the original quotient is undefined at $h=0$.

## 1. Expand the increment

For $f(x)=x^2$,

$$f(x+h)-f(x)=(x+h)^2-x^2=x^2+2xh+h^2-x^2=2xh+h^2.$$

## 2. Form the quotient and take its limit

For $h\ne0$,

$$\frac{f(x+h)-f(x)}h=\frac{2xh+h^2}h=2x+h.$$

Now use the limit:

$$\boxed{f'(x)=\lim_{h\to0}(2x+h)=2x}.$$

Expansion and cancellation are exact algebraic steps. The transition from $2x+h$ to $2x$ is where the limiting operation is actually used.

## 3. Connect secant lines with the limiting tangent

The secant through $(x,x^2)$ and $(x+h,(x+h)^2)$ has slope $2x+h$. As the second point moves toward the first from either side, this slope approaches $2x$.

The resulting tangent line at a general contact argument $a$ is

$$y-a^2=2a(x-a),\qquad y=2ax-a^2.$$

Its difference from the parabola is $x^2-(2ax-a^2)=(x-a)^2$, a nonnegative error that vanishes quadratically at contact. This explains geometrically what the derivative calculation achieved and checks that the slope formula works for every contact point, including the horizontal tangent at $a=0$. No differentiation rule was needed to derive the slope; the power-rule comparison comes only afterward.

## 4. Compare and verify

The power rule predicts $(x^2)'=2x$, agreeing with the result derived independently from the definition. At $x=3$, the secant slopes are $6+h$, tending to $6$ from both sides. At $x=0$, they are $h$, tending to zero.

For any fixed $x$, the difference between a secant slope and the proposed derivative is $|(2x+h)-2x|=|h|$. Taking $0<|h|<\varepsilon$ proves the limit directly for every real $x$.
