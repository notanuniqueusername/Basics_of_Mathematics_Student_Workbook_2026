# Problem 15. Find the Error in the Monotonicity Analysis

## The question

For the function
$$f(x)=x^3-3x$$
the derivative was correctly computed as
$$f'(x)=3(x-1)(x+1).$$

However, a student wrote the following conclusion:

> The derivative is positive between its zeros and negative outside them. Therefore, the function is decreasing on $(-\infty,-1)\cup(1,\infty)$, increasing on $(-1,1)$, has a local minimum at $x=-1$, and a local maximum at $x=1$.

1. Without differentiating again, explain why merely identifying the zeros of the derivative does not justify the stated sign chart, and find the error in the student's reasoning.
2. Construct the correct sign chart for $f'(x)$.
3. Give the correct intervals of monotonicity and the character of the extrema.
4. In each of the three intervals, choose one simple test point and show that the sign of the derivative confirms your classification.

## Before calculating: zeros do not determine derivative signs alone

The factors and their leading coefficient determine signs between zeros. A statement such as “positive between the roots” is not a general rule. Here the given derivative is already correct, so no redifferentiation is necessary.

A sign chart is justified by continuity and absence of zeros or singularities on each open interval. Within such an interval a continuous derivative cannot switch sign without passing through zero. That is why one correctly chosen test point per interval is enough here, after the derivative's complete zero set has been identified.

## 1. Build the correct factor sign chart

For $f'(x)=3(x-1)(x+1)$:

| Interval | $x-1$ | $x+1$ | Product and $f'$ |
|---|---|---|---|
| $(-\infty,-1)$ | $-$ | $-$ | $+$ |
| $(-1,1)$ | $-$ | $+$ | $-$ |
| $(1,\infty)$ | $+$ | $+$ | $+$ |

The student's signs are reversed: two negative factors multiply to a positive number, while opposite signs give a negative product.

## 2. Correct the monotonicity and extrema

The function increases separately on $(-\infty,-1)$ and $(1,\infty)$, and decreases on $(-1,1)$. At $-1$, $f'$ changes $+\to-$, giving local maximum $\boxed{(-1,2)}$. At $1$, it changes $-\to+$, giving local minimum $\boxed{(1,-2)}$.

The heights follow from $f(-1)=-1+3=2$ and $f(1)=1-3=-2$.

## 3. Explain the student's reversed extrema from the sign error

A local maximum occurs when increasing motion changes to decreasing motion; its derivative signs are $+\to-$. The actual chart has that transition at $-1$, not at $1$. A local minimum has signs $-\to+$, which occur at $1$.

The student's mistaken sign chart reverses both transitions and therefore reverses both extremum labels as a direct consequence. Correct derivative algebra does not protect a conclusion based on an unjustified sign rule.

For an extra consistency check, the function is odd: $f(-x)=-f(x)$. Its two critical heights are $2$ and $-2$, paired symmetrically. The correct left peak and right valley agree with the positive leading cubic term, which makes the graph rise from negative infinity on the far left to positive infinity on the far right.

## 4. Verification with the requested test points

$$f'(-2)=3(-3)(-1)=9>0,$$

$$f'(0)=3(-1)(1)=-3<0,$$

$$f'(2)=3(1)(3)=9>0.$$

Each interval contains one test point, and no derivative zero occurs inside any interval, so the signs cannot change there. This verifies every corrected classification using the supplied derivative alone.
