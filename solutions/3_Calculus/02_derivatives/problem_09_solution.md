# Problem 9. A Logarithm and the Chain Rule

## The question

For
$$f(x)=\ln(x^2+1)$$
compute the derivative. Then determine the sign of $f'(x)$ for $x<0$, $x=0$, and $x>0$, and describe qualitatively how the function behaves around zero.

## Before calculating: a positive logarithm argument

The chain rule for logarithms is $(\ln g)'=g'/g$ wherever $g>0$. Since $x^2+1\ge1$, this logarithm is defined and differentiable for every real $x$.

A logarithmic derivative formula is valid only where its argument is positive. Here $x^2+1$ never approaches a forbidden sign, so the formula applies on a single connected domain $\mathbb R$. The positive denominator then makes the sign chart especially simple: it preserves the numerator's sign rather than introducing additional sign-change intervals.

## 1. Compute the derivative

Set $g=x^2+1$, so $g'=2x$. Then

$$\boxed{f'(x)=\frac{2x}{x^2+1}}.$$

## 2. Analyze its sign

The denominator is always positive, so only the numerator matters:

| $x$ | $(-\infty,0)$ | $0$ | $(0,\infty)$ |
|---|---|---|---|
| $f'(x)$ | Negative | $0$ | Positive |
| $f$ | Decreasing | Minimum | Increasing |

Thus the graph descends toward $(0,0)$ and rises afterward. The tangent at zero is horizontal. The function is even because replacing $x$ by $-x$ leaves $x^2+1$ unchanged.

## 3. Explain the shape through the inside and outside functions

The inner function $x^2+1$ decreases toward $1$ as $x$ moves from the negative axis to zero, then increases from $1$ afterward. The logarithm is strictly increasing on positive inputs, so composing it preserves that decrease-then-increase pattern.

This geometric composition argument agrees with the derivative chart without computing another derivative. It also explains why the minimum value is $\ln1=0$ and why the graph is symmetric about the vertical axis.

At zero the formula gives a zero slope, but the surrounding signs establish the minimum. At any other input, the numerator $2x$ is nonzero, so there are no other stationary points. The derivative therefore gives both the local turning behavior and the uniqueness of that turning point.

## 4. Verification

The logarithm is increasing and $x^2+1\ge1$, so $f(x)=\ln(x^2+1)\ge\ln1=0$, with equality only at $x=0$. This confirms the global minimum independently of the derivative sign chart.

At $x=-1$ and $x=1$, the derivative values are $-1$ and $1$, confirming the signs on either side. Also $f'(-x)=-f'(x)$, as expected for the derivative of an even differentiable function.
