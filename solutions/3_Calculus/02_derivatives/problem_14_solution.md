# Problem 14. Continuity and Differentiability of a Piecewise Function

## The question

Investigate the behavior at $x=0$ of
$$f(x)=\begin{cases}x^2,&x\ge0,\\ax,&x<0.\end{cases}$$
For which values of $a$ is the function continuous? For which values do the one-sided derivatives exist and agree? For which value of $a$ is the function differentiable? Explain why continuity alone is not sufficient.

## Before calculating: continuity and derivative use different limits

The value at the joining point is $f(0)=0$ because the nonnegative branch applies. Continuity compares nearby values with this value; differentiability compares the one-sided difference quotients with each other.

Continuity asks whether the two branches meet at the same height. Differentiability asks whether their first-order changes agree after meeting. The latter is stronger: equal values do not force equal slopes. At a joining point, one-sided difference quotients should use the actual assigned function value, which here comes from the $x\ge0$ branch.

## 1. Test continuity

For every real $a$,

$$\lim_{x\to0^-}ax=0,\qquad\lim_{x\to0^+}x^2=0=f(0).$$

Thus $\boxed{f\text{ is continuous at }0\text{ for every real }a}$.

## 2. Compute one-sided derivatives from the definition

For $h>0$,

$$\frac{f(h)-f(0)}h=\frac{h^2}h=h\to0.$$

For $h<0$,

$$\frac{f(h)-f(0)}h=\frac{ah}h=a.$$

Therefore $f'_+(0)=0$ and $f'_-(0)=a$. Both exist for every $a$, but agree exactly when $\boxed{a=0}$. That is the unique parameter for differentiability at zero.

## 3. Describe the derivative function in the differentiable case

When $a=0$, the whole function is

$$f(x)=\begin{cases}0,&x<0,\\x^2,&x\ge0.\end{cases}$$

Its derivative is $0$ for $x<0$, $2x$ for $x>0$, and $0$ at the join by the one-sided calculation. The derivative itself is continuous there because both side limits are zero.

For any nonzero $a$, the left slope stays at that nonzero number while the right slope approaches zero. Thus no two-sided tangent slope exists at the join, despite the same continuous height on both sides. A finite plot might make a small nonzero $a$ look smooth, but the exact one-sided quotient distinguishes it from the differentiable case without a visual tolerance.

## 4. Verification and geometric explanation

At $a=0$, the negative branch is horizontal and meets the right-hand parabola with the same zero slope. The difference quotient is $0$ from the left and $h\to0$ from the right, confirming the derivative.

At $a=1$, the two branches still meet at the origin, but their slopes are $1$ and $0$. The resulting corner prevents differentiability despite continuity. This example explains concretely why matching function values does not guarantee matching tangent slopes.
