# Exercise 14. Closest Point on a Line

## The question

Given a point $P=(4,1)$ and a line through the origin with direction $v=(1,2)$. Using projection, find the closest point on the line, the distance from $P$ to the line, and verify that the appropriate vector is perpendicular to the direction of the line.

## Before calculating: closest point by projection

The line is $L=\{tv:t\in\mathbb R\}$. The closest point $Q$ is the projection of $P$ onto that line, characterized by $(P-Q)\cdot v=0$. The distance is the length of this perpendicular residual.

Projection onto a line through the origin treats a point's coordinates as its position vector. For a line with a different anchor $A$, one would instead project $P-A$ and then add $A$ back. Here the anchor is zero, so no translation is needed; the closest point itself is a scalar multiple of $v$.

## 1. Find the projection coefficient

$$P\cdot v=4+2=6,\qquad v\cdot v=1+4=5.$$

Thus

$$\boxed{Q=\frac65(1,2)=\left(\frac65,\frac{12}{5}\right)}.$$

## 2. Compute the distance

$$P-Q=\left(4-\frac65,1-\frac{12}{5}\right)=\left(\frac{14}{5},-\frac75\right).$$

$$\boxed{d(P,L)=\sqrt{\frac{196+49}{25}}=\frac{7\sqrt5}{5}=\frac7{\sqrt5}}.$$

## 3. Verify the minimum without assuming the projection formula

A general line point is $Q(t)=(t,2t)$. Its squared distance from $P$ is

$$D(t)=(4-t)^2+(1-2t)^2=5t^2-12t+17.$$

Completing the square gives

$$D(t)=5\left(t-\frac65\right)^2+\frac{49}{5}.$$

The first term is nonnegative and vanishes only at $t=6/5$. Thus the nearest point is exactly $(6/5,12/5)$, and the distance is $\sqrt{49/5}=7/\sqrt5$.

This supplies an independent algebraic minimum proof, checking both the projection location and the distance. Minimizing squared distance is legitimate because the square-root function is strictly increasing on nonnegative values.

## 4. Verification and minimality

$Q$ lies on the line because it is $\frac65v$. Perpendicularity gives

$$(P-Q)\cdot v=\frac{14}{5}-\frac{14}{5}=0.$$

For any other point $tv$,

$$\|P-tv\|^2=\|P-Q\|^2+\|Q-tv\|^2\ge\|P-Q\|^2.$$

The equality uses perpendicularity of $P-Q$ and $Q-tv$. Equality occurs only at $tv=Q$, proving the projection is the unique closest point, not simply a stationary candidate. The line equation $2x-y=0$ also gives distance $|8-1|/\sqrt5=7/\sqrt5$.

**Clarify the perpendicular segment's orientation.** The residual from the foot to the point is $P-Q=(14/5,-7/5)$, while the displacement from the point to the foot is its negative. Both are perpendicular to $v$ and have the same length, so either orientation gives the same distance. The line's normal vector $(2,-1)$ is proportional to the residual, $P-Q=(7/5)(2,-1)$, confirming that the segment follows the normal. The coefficient $7/5$ is not itself the distance because this normal has length $\sqrt5$, not $1$.
