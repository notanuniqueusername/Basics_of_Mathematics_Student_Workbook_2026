# Problem 1. Motion — from Position to Velocity

## The question

The position of a point is described by
$$
s(t)=t^3-6t^2+9t+2,\qquad t\ge0.
$$

1. Determine the velocity and acceleration.
2. Find the times at which the point stops.
3. Determine on which intervals the point moves in the positive direction of the axis and on which intervals it moves in the negative direction.

## Before calculating: position, velocity, and acceleration

Velocity is the rate of change of position, $v=s'$, and acceleration is $a=v'=s''$. Stopping means zero velocity; the sign of velocity determines direction, not the sign of position or acceleration. The physical domain is $t\ge0$.

The physical domain starts at zero, so negative algebraic roots would have to be rejected if they appeared. A stop is an instant of zero velocity; a reversal requires an additional sign change across that instant. Acceleration describes how velocity changes and should not be used alone as a test of which direction the point is currently traveling.

## 1. Differentiate twice

$$\boxed{v(t)=3t^2-12t+9=3(t-1)(t-3)},$$

$$\boxed{a(t)=6t-12}.$$

If position is measured in length units and time in time units, velocity and acceleration have units length/time and length/time squared.

## 2. Find stopping times and directions

The equation $v=0$ gives $\boxed{t=1,3}$, both in the domain.

| Time interval | Sign of $(t-1)(t-3)$ | Motion |
|---|---|---|
| $0\le t<1$ | $+$ | Positive direction |
| $1<t<3$ | $-$ | Negative direction |
| $t>3$ | $+$ | Positive direction |

At the stopping instants there is no instantaneous direction of motion; the sign changes show reversal at both times.

## 3. Distinguish position extrema from total distance

The velocity sign changes show that $s$ reaches a local maximum at $t=1$ and a local minimum at $t=3$. Between those instants, the displacement is $s(3)-s(1)=2-6=-4$, while the traveled distance is $4$ length units because velocity is negative throughout that interval.

From $t=0$ to $t=3$, the starting position is $s(0)=2$. The displacement over that full interval is zero, but the point travels from $2$ to $6$ and back to $2$, giving distance $4+4=8$. This concrete comparison illustrates why the derivative's sign matters physically: the point can return to its starting position after substantial motion, and a zero net displacement does not mean it remained stationary.

## 4. Verification

Test $t=0,2,4$: velocities are $9,-3,9$, confirming all signs. The positions at the stops are $s(1)=1-6+9+2=6$ and $s(3)=27-54+27+2=2$, so the point moves backward between them, agreeing with negative velocity. Also $a(1)=-6$ and $a(3)=6$, consistent with the velocity crossing zero downward and upward, respectively.
