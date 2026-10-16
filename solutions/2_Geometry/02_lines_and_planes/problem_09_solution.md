# Exercise 9. Distances

## The question

Compute:
1. the distance from $P=(2,3)$ to the line $3x+4y-10=0$,
2. the distance from $Q=(2,-1,3)$ to the plane $2x-2y+z-4=0$.

Compare the two formulas and explain their common connection with the normal direction.

## Before calculating: distance is normal displacement

For a line $ax+by+c=0$, distance is $|ax_0+by_0+c|/\sqrt{a^2+b^2}$. For a plane, add the third coordinate term and normal component. The numerator measures the signed normal residual; division by the normal length converts it to distance.

For an equation $n\cdot X-d=0$, the normalized vector $n/\|n\|$ measures displacement in actual length units along the normal. The residual $n\cdot P-d$ is not itself a geometric distance unless the normal is unit length. This explains the denominator shared by the line and plane formulas.

## 1. Distance to the line

$$\boxed{d(P,L)=\frac{|3\cdot2+4\cdot3-10|}{\sqrt{3^2+4^2}}=\frac85}.$$

## 2. Distance to the plane

The normal is $n=(2,-2,1)$, with length $3$. The residual at $Q$ is $2\cdot2-2(-1)+3-4=5$. Therefore

$$\boxed{d(Q,\Pi)=\frac53}.$$

The absolute value ensures nonnegative distance in both dimensions. Multiplying an equation by a nonzero scalar changes numerator and denominator by the same magnitude, leaving the distance unchanged.

## 3. Derive both formulas from the same projection argument

Let $H=P-\alpha n$ be the perpendicular foot. Requiring $n\cdot H=d$ gives

$$n\cdot P-\alpha\|n\|^2=d\quad\Longrightarrow\quad\alpha=\frac{n\cdot P-d}{\|n\|^2}.$$

Then the segment length is

$$\|P-H\|=|\alpha|\|n\|=\frac{|n\cdot P-d|}{\|n\|}.$$

The reasoning works for two- or three-component vectors without any structural change. It also explains why the projection feet in the verification use squared normal lengths, $25$ and $9$, whereas the distances use normal lengths, $5$ and $3$. Confusing these denominators would give a point on the normal line but usually not on the target line or plane.

## 4. Verification by projection feet

For the line, subtract the residual divided by the normal squared:

$$H=P-\frac8{25}(3,4)=\left(\frac{26}{25},\frac{43}{25}\right).$$

Then $3H_x+4H_y-10=(78+172-250)/25=0$ and $\|P-H\|=(8/25)5=8/5$.

For the plane,

$$K=Q-\frac59(2,-2,1)=\left(\frac89,\frac19,\frac{22}{9}\right).$$

Its plane residual is $(16-2+22)/9-4=0$, and $\|Q-K\|=(5/9)3=5/3$. Both segments point along their respective normals, confirming shortest distances.
