# Exercise 13. Closest Point on a Plane

## The question

Find the point on the plane $x+2y+2z=4$ closest to $P=(3,0,0)$. Give the distance and check that the segment joining the two points is perpendicular to the plane.

## Before calculating: shortest segment follows the normal

For a point outside a plane, the closest point is the perpendicular projection. A plane $n\cdot X=d$ has normal $n$; seek the foot as $H=P+\lambda n$ and choose $\lambda$ so that $H$ satisfies the equation.

The plane's normal has length $\sqrt{1^2+2^2+2^2}=3$, but the coefficient used to reach the plane divides by its squared length $9$. These are different quantities: the coefficient determines how much of the nonunit normal to travel, and multiplying that coefficient by the normal length gives the actual distance.

## 1. Locate the foot

Here $n=(1,2,2)$, $d=4$, and $n\cdot P=3$. Thus

$$n\cdot(P+\lambda n)=3+9\lambda=4,$$

so $\lambda=1/9$. Therefore

$$\boxed{H=(3,0,0)+\frac19(1,2,2)=\left(\frac{28}{9},\frac29,\frac29\right)}.$$

## 2. Compute the distance

$$\boxed{d(P,\Pi)=\|H-P\|=\frac19\sqrt{1+4+4}=\frac13}.$$

The equivalent residual formula gives $|3-4|/3=1/3$.

## 3. Explain the sign and size of the correction

At $P$, the plane expression $x+2y+2z$ equals $3$, one below the required value $4$. Moving by $\lambda n$ increases this expression by $\lambda(n\cdot n)=9\lambda$. Therefore the required positive correction is $\lambda=1/9$, not $1$ or $1/3$.

The foot's first coordinate $28/9$ is greater than $3$, while the other two become positive, consistently with movement in the positive normal direction $(1,2,2)$. A displacement by $-n/9$ would instead reduce the expression to $2$ and move away from the plane. This residual check detects a sign error before computing a distance, which would erase the sign through a norm.

## 4. Verification and minimality

The plane check is

$$\frac{28}{9}+2\frac29+2\frac29=\frac{36}{9}=4.$$

The segment $H-P=\frac19n$ is normal to the plane, hence perpendicular to every in-plane direction. For any other plane point $Q$, $H-Q$ lies in the plane, so

$$\|P-Q\|^2=\|P-H\|^2+\|H-Q\|^2\ge\|P-H\|^2.$$

Equality occurs only for $Q=H$, proving that the point found is uniquely closest.
