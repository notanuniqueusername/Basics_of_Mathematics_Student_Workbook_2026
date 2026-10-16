# Problem 6. A Logarithmic Function

## The question

Analyze the domain, zero, and monotonicity of
$$f(x)=\ln x-x+1.$$
Explain why the analysis must begin with the domain.

## Before calculating: start with the logarithm's domain

The real logarithm requires $\boxed{x>0}$. There is no function value or derivative at nonpositive $x$, so a sign chart over all real numbers would be invalid.

The logarithmic domain is not a detail added after differentiation: it determines which sign intervals and end limits even make sense. The boundary $0$ is approached only from the right. A maximum at a zero value is compatible with the function being strictly negative everywhere else.

## 1. Differentiate and determine monotonicity

$$f'(x)=\frac1x-1=\frac{1-x}{x}.$$

Because $x>0$, the derivative is positive on $(0,1)$ and negative on $(1,\infty)$. It vanishes at $x=1$, where

$$f(1)=0-1+1=0.$$

Thus $\boxed{(1,0)\text{ is the unique global maximum}}$.

## 2. Identify the zero and end behavior

Strict increase up to a maximum of $0$ and strict decrease afterward show that $\boxed{x=1}$ is the only zero and $f(x)<0$ otherwise.

As $x\to0^+$, $\ln x\to-\infty$, so $f\to-\infty$. As $x\to\infty$, $\ln x/x\to0$, so the negative linear term dominates and $f\to-\infty$. The vertical asymptote at the domain boundary is $x=0$.

## 3. Derive the key bound directly from the logarithm

For $x\ge1$,

$$\ln x=\int_1^x\frac1t\,dt\le\int_1^x1\,dt=x-1.$$

For $0<x<1$, write $\ln x=-\int_x^1dt/t$ and use $1/t\ge1$ to obtain the same inequality. It is strict unless $x=1$.

Therefore $\ln x-x+1\le0$, with equality only at $1$, independently verifying both the unique zero and the global maximum. This argument explains the bound geometrically as an integral comparison. The derivative analysis additionally describes how the graph reaches and leaves that maximum, so the two approaches check different aspects of the same result rather than merely repeat the critical equation.

## 4. Verification

$f'(1/2)=1>0$, while $f'(2)=-1/2<0$, checking both derivative intervals. Also $f''(x)=-1/x^2<0$ on the entire domain, so the graph is strictly concave and the critical point is a maximum. Rearranging the global bound $f(x)\le0$ gives the familiar inequality $\ln x\le x-1$, with equality exactly at $1$, consistent with the zero analysis.
