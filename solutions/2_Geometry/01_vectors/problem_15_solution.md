# Exercise 15. Comparing Directions Using the Cosine of the Angle

## The question

Given
$$a=(1,2,1),\qquad b=(2,4,2),\qquad c=(2,0,3).$$
For each pair, compute
$$\frac{u\cdot v}{\|u\|\,\|v\|}.$$
Order the pairs by increasing angle between the vectors. Explain why for $a$ and $b$ the value is $1$ even though the vectors have different lengths.

## Before calculating: compare cosines instead of inverse cosines

For nonzero vectors, $\cos\theta=(u\cdot v)/(\|u\|\|v\|)$. On $[0,\pi]$, cosine is decreasing, so a larger cosine means a smaller angle. Positive rescaling of a vector leaves this ratio unchanged.

The normalized dot product is unchanged by multiplying either vector by a positive scalar. Multiplying by a negative scalar would instead reverse its orientation and generally replace the angle by its supplement. Therefore “parallel” alone does not guarantee cosine $1$; parallel vectors pointing in opposite directions have cosine $-1$.

## 1. Compute lengths and dot products

$$\|a\|=\sqrt6,\qquad \|b\|=\sqrt{24}=2\sqrt6,\qquad \|c\|=\sqrt{13}.$$

$$a\cdot b=2+8+2=12,\qquad a\cdot c=2+0+3=5,\qquad b\cdot c=4+0+6=10.$$

## 2. Compute the three ratios

$$\boxed{\cos\theta_{ab}=\frac{12}{\sqrt6\,2\sqrt6}=1},$$

$$\boxed{\cos\theta_{ac}=\frac5{\sqrt{78}}},\qquad \boxed{\cos\theta_{bc}=\frac{10}{2\sqrt{78}}=\frac5{\sqrt{78}}}.$$

Consequently the increasing-angle order is

$$\boxed{\theta_{ab}=0<\theta_{ac}=\theta_{bc}=\arccos\left(\frac5{\sqrt{78}}\right)}.$$

## 3. Explain the tie and the ordering without decimal angles

The identity $b=2a$ implies

$$\frac{b\cdot c}{\|b\|\|c\|}=\frac{2(a\cdot c)}{2\|a\|\|c\|}=\frac{a\cdot c}{\|a\|\|c\|}.$$

Thus the equal angles with $c$ are forced by the shared direction of $a$ and $b$, not by accidental cancellation in the numerical answers. To compare with the $ab$ angle, observe that $25<78$, so $5/\sqrt{78}<1$. Since inverse cosine decreases on $[-1,1]$, its angle is strictly larger than $\arccos1=0$.

No rounding is needed to establish the strict inequality or the tie. Decimal angles merely illustrate the exact ordering already proved.

## 4. Explain the equality and verify

Since $b=2a$, $a$ and $b$ point along the same ray even though their lengths differ. Their length factor $2$ cancels between numerator and denominator. The same cancellation explains the equal angles with $c$.

Numerically $5/\sqrt{78}\approx0.5661$, so both remaining angles are about $55.5^\circ$, consistent with positive dot products. Finally $0<25<78$ guarantees the common cosine lies strictly between $0$ and $1$, confirming these angles are acute and nonzero.
