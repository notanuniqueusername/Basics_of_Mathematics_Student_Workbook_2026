# Exercise 6. Projection and Perpendicular Component

## The question

Find the projection of $u=(4,2)$ onto the direction $v=(1,1)$. Then compute
$$r=u-\operatorname{proj}_v u$$
and verify that $r\cdot v=0$. Explain this result geometrically.

## Before calculating: orthogonal projection

For $v\ne0$, $\operatorname{proj}_v u=\frac{u\cdot v}{v\cdot v}v$. The result is parallel to $v$; subtracting it from $u$ leaves the perpendicular component. The denominator is the squared norm, not the norm.

A projection is a vector along the target direction, not the scalar coefficient multiplying that direction. Here the coefficient is $3$ while the projection vector is $(3,3)$. The scalar projection onto the unit vector $v/\|v\|$ is a third quantity, $(u\cdot v)/\|v\|=3\sqrt2$, equal to the signed length along that unit direction.

## 1. Compute the parallel component

$$u\cdot v=4+2=6,\qquad v\cdot v=1+1=2.$$

Thus

$$\boxed{p=\operatorname{proj}_v u=\frac62(1,1)=(3,3)}.$$

## 2. Find the residual

$$\boxed{r=u-p=(4,2)-(3,3)=(1,-1)}.$$

This decomposes $u$ as a component along the line $y=x$ and a component perpendicular to that line.

## 3. Explain why the perpendicular residual gives the closest point

A general point of the projection line is $(t,t)$. Its squared distance from $u=(4,2)$ is

$$(4-t)^2+(2-t)^2=2t^2-12t+20=2(t-3)^2+2.$$

This expression is smallest exactly when $t=3$, giving the point $(3,3)$ found by projection. The minimum squared distance is $2$, equal to $\|r\|^2=1^2+(-1)^2$.

This calculation connects the orthogonal decomposition with a minimum-distance statement. It also checks the projection coefficient independently: using $6/\sqrt2$ as the coefficient of the nonunit vector $v$ would not minimize this distance, illustrating why the formula divides by $v\cdot v$.

## 4. Explain perpendicularity

A point $tv$ lies on the projection line. Requiring $u-tv$ to be perpendicular to $v$ gives $(u-tv)\cdot v=0$, hence $t=(u\cdot v)/(v\cdot v)=3$. This derives the projection coefficient rather than merely quoting it.

## 5. Verification

Check reconstruction and orthogonality separately:

$$p+r=(3,3)+(1,-1)=(4,2)=u,$$

$$r\cdot v=1\cdot1+(-1)1=0.$$

Also $\|u\|^2=20$, $\|p\|^2=18$, and $\|r\|^2=2$, so the orthogonal decomposition obeys $20=18+2$, as the Pythagorean theorem requires.

**Verify independence of the direction vector's scale.** The same line can be represented by $v'=2v=(2,2)$. Its projection coefficient is $(u\cdot v')/(v'\cdot v')=12/8=3/2$, so the projection is $(3/2)(2,2)=(3,3)$, unchanged. This checks that the formula depends on a line direction rather than an arbitrary choice of vector length. The coefficient changes inversely with the scale of the direction vector, while their product remains the same geometric component. The perpendicular residual therefore remains $(1,-1)$ as well.
