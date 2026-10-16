# Exercise 10. Projection of a Point onto a Plane

## The question

Find the orthogonal projection of $P=(2,1,3)$ onto the plane $x+y+z=3$, and then find the reflection of $P$ across this plane. Check that the midpoint of the segment joining the point and its reflection lies on the plane.

## Before calculating: projection and reflection

For $\Pi:n\cdot X=d$, the projection is $H=P-\alpha n$ where $\alpha=(n\cdot P-d)/\|n\|^2$. Reflection continues the same perpendicular displacement a second time: $R=P-2\alpha n=2H-P$.

An orthogonal projection must satisfy two independent conditions: the foot lies on the plane, and the displacement to it is parallel to the plane normal. A reflection additionally makes that foot the midpoint between the original and reflected points. Midpoint membership alone does not establish perpendicular reflection.

## 1. Find the perpendicular foot

Here $n=(1,1,1)$ and $d=3$. Since $n\cdot P=6$ and $\|n\|^2=3$,

$$\alpha=\frac{6-3}{3}=1,\qquad\boxed{H=(2,1,3)-(1,1,1)=(1,0,2)}.$$

## 2. Reflect the point

$$\boxed{R=2H-P=(2,0,4)-(2,1,3)=(0,-1,1)}.$$

The displacement $P-H=(1,1,1)$ is normal to the plane. The reflected displacement $R-H=(-1,-1,-1)$ is equal in length and opposite in orientation.

## 3. Explain the factor of two in reflection

The first displacement from $P$ to its foot is $H-P=-n$. To continue the same distance through the plane, apply this displacement again:

$$R=H+(H-P)=2H-P=P-2n.$$

Thus projection subtracts one normal correction, while reflection subtracts two. In this example the foot is one normal vector from $P$, but the reflected point is two normal vectors from $P$.

Reflecting twice must restore the original point. The residual at $R$ is $-3$, so its projection correction is $-n$ and its reflection is $R-2(-n)=R+2n=P$. This checks the reflection operation as an inverse of itself, paralleling the self-inverse matrix examples in the reference folder.

## 4. Verification

$H$ lies on the plane because $1+0+2=3$. The midpoint is

$$\frac{P+R}{2}=\frac{(2,1,3)+(0,-1,1)}2=(1,0,2)=H.$$

Its coordinate sum is again $3$. Both endpoint distances from $H$ are $\sqrt3$. The plane residuals of $P$ and $R$ are respectively $6-3=3$ and $0-3=-3$, confirming equal distances on opposite sides. Midpoint membership alone would not prove a reflection without the normal-direction condition.
