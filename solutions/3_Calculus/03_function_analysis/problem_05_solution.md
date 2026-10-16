# Problem 5. An Exponential Function with a Maximum

## The question

Analyze the monotonicity and extrema of
$$f(x)=xe^{-x}.$$
Also examine the behavior as $x\to\infty$ and explain how the limit affects the shape of the graph on the right-hand side.

## Before calculating: a positive exponential preserves signs

The domain is $\mathbb R$, and $e^{-x}>0$ everywhere. After using the product and chain rules, this positive factor can be ignored for sign analysis, but not for the derivative value itself.

A positive exponential factor can be removed when deciding a derivative's sign, but it cannot be discarded when evaluating the derivative numerically. A global extremum requires comparison over the whole domain; the all-domain increase-then-decrease pattern here establishes that no point elsewhere exceeds the critical value.

## 1. Find monotonicity and the extremum

$$f'(x)=e^{-x}-xe^{-x}=e^{-x}(1-x).$$

Thus $f'>0$ for $x<1$, $f'=0$ at $1$, and $f'<0$ for $x>1$. The function increases on $(-\infty,1)$ and decreases on $(1,\infty)$.

$$\boxed{\text{Global maximum at }(1,1/e)}.$$

The derivative sign on the entire domain proves the global classification.

## 2. Examine the ends

As $x\to+\infty$, $xe^{-x}=x/e^x\to0^+$ because exponential growth dominates linear growth. For instance $e^x\ge x^2/2$ for $x>0$, giving $0\le x/e^x\le2/x\to0$.

As $x\to-\infty$, writing $x=-t$ gives $-te^t\to-\infty$. The graph crosses the origin, reaches its positive peak, then descends toward horizontal asymptote $y=0$ on the right without crossing it.

## 3. Explain the right tail without using an indeterminate quotient

The statement $x/e^x\to0$ follows from an explicit bound. For positive $x$, the exponential series gives $e^x\ge x^2/2$, so

$$0\le xe^{-x}\le\frac2x\longrightarrow0.$$

Thus the positive branch decreases after its maximum but never reaches or crosses the horizontal asymptote. On the left, $x=-t$ makes $f=-te^t$; this tends to $-\infty$ rather than zero because both $t$ and $e^t$ grow.

The contrast explains why $y=0$ is only a right-hand horizontal asymptote. One cannot infer both end limits from the exponential symbol alone; the sign of its exponent changes its behavior at the two ends.

## 4. Verification

$f'(0)=1>0$ and $f'(2)=-e^{-2}<0$ confirm the change. The second derivative is $f''(x)=e^{-x}(x-2)$, so $f''(1)=-1/e<0$, independently confirming the local maximum. Finally $f(0)=0$ and the sign of $f(x)$ is the sign of $x$, agreeing with the stated graph behavior.
