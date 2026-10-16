# Problem 1. Derivative of a Polynomial and the Slope of a Tangent Line

## The question

For
$$f(x)=3x^5-2x^3+7x-4$$
find $f'(x)$. Then compute $f'(0)$ and $f'(1)$, determine the signs of the obtained values, and explain what they say about the slope of the tangent line to the graph at these two points.

## Before calculating: differentiate term by term

Use $(x^m)'=mx^{m-1}$, the constant-multiple and sum rules, and the fact that a constant differentiates to zero. The derivative at a point is the slope of the tangent there.

The power rule applies to each monomial, and linearity allows the resulting derivatives to be added. The value $f'(x_0)$ describes vertical change per unit horizontal change near $x_0$, whereas $f(x_0)$ describes the point's height. A negative function value can therefore coexist with a positive tangent slope, as it does here at zero.

## 1. Compute the derivative

$$f'(x)=3\cdot5x^4-2\cdot3x^2+7-0=\boxed{15x^4-6x^2+7}.$$

The exponent decreases by one in each power term, whereas the constant term $-4$ disappears.

## 2. Evaluate the tangent slopes

$$\boxed{f'(0)=7>0},\qquad\boxed{f'(1)=15-6+7=16>0}.$$

Both tangents rise from left to right. The tangent at $x=1$ is steeper because its slope is larger. Since $f(0)=-4$ and $f(1)=4$, their equations are $y=7x-4$ and $y-4=16(x-1)$, respectively.

## 3. Connect the derivative values with local linear models

At $x_0=0$, the point is $(0,-4)$ and the slope is $7$, so the first-order model is $f(h)\approx-4+7h$. The exact remainder is

$$f(h)-(-4+7h)=3h^5-2h^3.$$

Dividing by $h$ leaves $3h^4-2h^2\to0$, which is precisely why that line is tangent.

At $x_0=1$, the model is $4+16h$. Expansion gives remainder $24h^2+28h^3+15h^4+3h^5$, again negligible compared with $h$. Thus the computed slopes are not merely numbers from a formula; they are the coefficients of the best first-order descriptions at the two specified points. The larger slope $16$ means a greater local rise for the same small positive horizontal increment.

## 4. Verification

At zero, the difference quotient simplifies exactly:

$$\frac{f(h)-f(0)}h=3h^4-2h^2+7\longrightarrow7.$$

At one, expansion gives

$$\frac{f(1+h)-f(1)}h=16+24h+28h^2+15h^3+3h^4\longrightarrow16.$$

These checks use the derivative definition and agree with both computed slopes. Positive derivative describes the local slope; it does not by itself mean the function's value is positive, as $f(0)=-4$ illustrates.
