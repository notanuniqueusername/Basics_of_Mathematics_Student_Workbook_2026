# Problem 1. Antiderivative and Verification

## The question

For
$$f(x)=3x^2-4x+5$$
find one antiderivative $F(x)$. Write the entire family of antiderivatives, verify the result by differentiation, and explain the meaning of the constant $C$.

## Before calculating: an integral is a family

An antiderivative $F$ satisfies $F'=f$. For powers, reverse differentiation: $\int x^p\,dx=x^{p+1}/(p+1)+C$ for $p\ne-1$. On an interval, any two antiderivatives differ by a constant.

An indefinite integral is not a single numerical value and is not an area with unspecified bounds. It represents all functions having the given derivative on the stated interval. The power integration rule follows by reversing $(x^{p+1})'=(p+1)x^p$, so division by $p+1$ is what cancels the factor introduced by differentiation.

## 1. Integrate term by term

$$\int(3x^2-4x+5)\,dx=3\frac{x^3}{3}-4\frac{x^2}{2}+5x+C.$$

Thus one antiderivative is

$$\boxed{F_0(x)=x^3-2x^2+5x},$$

and the entire family is

$$\boxed{F(x)=x^3-2x^2+5x+C,\quad C\in\mathbb R}.$$

All expressions are defined on $\mathbb R$.

## 2. Explain the constant

Differentiation sends every constant to zero, so $f$ cannot determine the vertical position of its antiderivative. Changing $C$ shifts the graph vertically without changing any slope. A condition such as $F(0)=7$ would select $C=7$; without such a condition there is no distinguished constant.

## 3. Explain why a single constant represents the entire freedom

Integrating the three terms separately might introduce constants $C_1,C_2,C_3$, but their sum is simply another arbitrary real number $C$. Keeping all three would not describe more functions.

The antiderivative's slopes are fixed, but its height at a point is not. Here $F(0)=C$, so the constant directly records the graph's vertical placement. Choosing $C=0$ supplies the requested one antiderivative, while allowing every real $C$ supplies the full family.

The completeness argument uses the connected domain: if two functions have the same derivative on $\mathbb R$, their difference has zero derivative throughout an interval and is constant there. This is why the verification must specify a domain as well as differentiate the displayed formula.

## 4. Verification

Differentiate the whole family:

$$F'(x)=3x^2-4x+5+0=f(x).$$

For example, both $F_0$ and $F_0+10$ have this derivative. Conversely, if $G'=f$ on $\mathbb R$, then $(G-F_0)'=0$, so the mean value theorem forces $G-F_0$ to be constant. This establishes that the family is complete, rather than merely a collection of examples.
