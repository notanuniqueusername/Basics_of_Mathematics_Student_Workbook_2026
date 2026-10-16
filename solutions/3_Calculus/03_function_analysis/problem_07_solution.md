# Problem 7. A Trigonometric Function

## The question

On $[0,2\pi]$, find the intervals of monotonicity and the extrema of
$$f(x)=\sin x+\cos x.$$
Include the endpoints of the interval and compare the function values at the critical points and at the endpoints.

## Before calculating: include endpoints on a closed interval

Interior extrema may occur at zeros of the derivative. Absolute extrema on $[0,2\pi]$ require comparing those values with both endpoints. Use radians throughout.

On a closed bounded interval, extrema may occur at endpoints even when the derivative does not vanish there. Interior and endpoint candidates must therefore be listed together before an absolute maximum or minimum is chosen. One-sided endpoint extrema are relative to the restricted domain and should not be confused with interior turning points.

## 1. Find critical points and derivative signs

$$f'(x)=\cos x-\sin x=\sqrt2\cos(x+\pi/4).$$

Its zeros in the interval are $x=\pi/4$ and $x=5\pi/4$.

| Interval | $(0,\pi/4)$ | $(\pi/4,5\pi/4)$ | $(5\pi/4,2\pi)$ |
|---|---|---|---|
| $f'$ | $+$ | $-$ | $+$ |
| $f$ | Increasing | Decreasing | Increasing |

## 2. Compare all candidates

$$f(0)=1,\quad f(\pi/4)=\sqrt2,\quad f(5\pi/4)=-\sqrt2,\quad f(2\pi)=1.$$

Thus the absolute maximum is $\boxed{\sqrt2\text{ at }x=\pi/4}$ and the absolute minimum is $\boxed{-\sqrt2\text{ at }x=5\pi/4}$; these are also the interior local extrema.

Relative to the restricted interval, $0$ is a one-sided local minimum and $2\pi$ a one-sided local maximum, since the nearby graph rises at each end. They are not absolute extrema.

## 3. Explain the critical values through a phase shift

The identity

$$\sin x+\cos x=\sqrt2\sin(x+\pi/4)$$

shows that the graph is a sine wave of amplitude $\sqrt2$ shifted left by $\pi/4$. Its peak occurs when $x+\pi/4=\pi/2$, giving $x=\pi/4$; its trough occurs when $x+\pi/4=3\pi/2$, giving $x=5\pi/4$.

This checks the derivative-root calculation and the exact heights without a decimal approximation. At the endpoints the phase differs by a full period, so the heights both equal $1$. The signs of the derivative between the critical points then establish the traversal order: rise to the peak, fall to the trough, rise to the final endpoint. That order is the essential information for a correct interval sketch.

## 4. Verification

Test $x=0,\pi,3\pi/2$: $f'$ is $1,-1,1$, confirming all three signs. The identity $f(x)=\sqrt2\sin(x+\pi/4)$ guarantees $-\sqrt2\le f(x)\le\sqrt2$, verifying the absolute bounds independently. The listed critical arguments attain both bounds, while the endpoints have the same value because of period $2\pi$.
