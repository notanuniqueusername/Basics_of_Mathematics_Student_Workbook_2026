# Exercise 5. Angle Between Vectors

## The question

Given $u=(1,1,0)$ and $v=(1,0,1)$:

1. Use the sign of $u\cdot v$ to predict the type of angle.
2. Compute the angle.
3. Compare the result with the prediction.

## Before calculating: angle from a dot product

For nonzero vectors, $\cos\theta=(u\cdot v)/(\|u\|\|v\|)$ with $0\le\theta\le\pi$. A positive dot product implies $0\le\theta<\pi/2$, allowing a zero angle when the vectors point along the same ray. To conclude that the angle is strictly acute, also rule out that same-ray case.

The angle is defined between vectors translated to a common starting point, not between their endpoints as points. Its standard range $[0,\pi]$ ensures a unique inverse-cosine value. Dividing the dot product by both lengths removes the effect of scale, leaving only the directional information needed for the angle.

## 1. Predict the angle type

$$u\cdot v=1\cdot1+1\cdot0+0\cdot1=1>0.$$

The vectors are not parallel: if $v=cu$, their first coordinates would force $c=1$, but their second coordinates would then require $0=1$. Thus they do not point along the same ray. Combining this with the positive dot product gives $0<\theta<\pi/2$, so the angle is strictly acute.

## 2. Compute the cosine and angle

$$\|u\|=\sqrt{1+1}=\sqrt2,\qquad \|v\|=\sqrt{1+1}=\sqrt2.$$

Hence

$$\cos\theta=\frac1{\sqrt2\sqrt2}=\frac12,\qquad \boxed{\theta=\frac\pi3=60^\circ}.$$

The angle belongs to $[0,\pi]$, so the value $\pi/3$ is unambiguous. A second angle with the same cosine outside this interval is not relevant to the standard angle between vectors.

## 3. Give a second geometric description of the angle

The three points $O=(0,0,0)$, $U=u$, and $V=v$ form a triangle. Its side lengths are

$$OU=OV=\sqrt2,\qquad UV=\|u-v\|=\sqrt{0^2+1^2+(-1)^2}=\sqrt2.$$

All three sides are equal, so the triangle is equilateral and its angle at the origin is $60^\circ$. This identifies the same angle without evaluating an inverse cosine. The original vectors have positive dot product, and the equilateral interpretation therefore agrees with the earlier acute-angle prediction. Equal lengths alone would not have implied equal angles; the third equal side is the additional fact that makes this check conclusive.

## 4. Compare with the prediction

Since $60^\circ<90^\circ$, the exact answer agrees with the positive-dot-product prediction. The two vectors are neither parallel nor perpendicular.

## 5. Verification

Use the distance between their endpoints: $u-v=(0,1,-1)$ has squared length $2$. The cosine law requires

$$\|u-v\|^2=\|u\|^2+\|v\|^2-2\|u\|\|v\|\cos\theta=2+2-2\cdot2\cdot\frac12=2.$$

This matches the direct squared length and checks the angle independently.
