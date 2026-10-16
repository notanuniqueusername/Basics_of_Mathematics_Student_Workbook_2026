# Exercise 13. Do Four Points Lie in One Plane?

## The question

Given
$$A=(0,0,0),\qquad B=(1,2,0),\qquad C=(0,1,1),\qquad D=(2,5,1).$$

1. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$.
2. Find $n=\overrightarrow{AB}\times\overrightarrow{AC}$.
3. Construct $\overrightarrow{AD}$ and check whether $\overrightarrow{AD}\cdot n=0$.
4. Based on this, decide whether $D$ lies in the plane determined by $A,B,C$, and justify the criterion.

## Before calculating: a coplanarity criterion

If $a,b$ are independent directions in a plane and $n=a\times b\ne0$, a vector $q$ lies parallel to that plane exactly when $q\cdot n=0$. A point $D$ lies in the plane through $A$ when $q=D-A$ satisfies this condition.

The dot-product criterion assumes the first three points determine a plane. That must be checked by verifying the cross product is nonzero. Without it, a zero cross product would make every fourth-point test equal zero, even though the initial three collinear points would not specify a unique plane.

## 1. Construct the directions and normal

$$a=B-A=(1,2,0),\qquad b=C-A=(0,1,1).$$

$$n=a\times b=(2\cdot1-0\cdot1,0\cdot0-1\cdot1,1\cdot1-2\cdot0)=\boxed{(2,-1,1)}.$$

Since $n\ne0$, $A,B,C$ determine a unique plane.

## 2. Test the fourth point

$$D-A=(2,5,1),\qquad (D-A)\cdot n=2\cdot2+5(-1)+1\cdot1=4-5+1=0.$$

Hence $\boxed{D\text{ lies in the plane through }A,B,C}$, so all four points are coplanar. The plane equation is $2x-y+z=0$ because it passes through the origin $A$.

## 3. Explain necessity and sufficiency of the criterion

Every displacement in the plane has form $sa+tb$. Since $n$ is perpendicular to both $a$ and $b$,

$$n\cdot(sa+tb)=s(n\cdot a)+t(n\cdot b)=0.$$

This proves the condition is necessary. It is also sufficient here: the independent vectors $a,b$ span a two-dimensional plane, and all vectors perpendicular to the nonzero $n$ form that same two-dimensional plane.

For the actual data, $D-A=2a+b$ supplies an explicit sufficient representation. The coefficients can be recovered from coordinates: the first coordinate forces $s=2$, the third forces $t=1$, and the second then gives $2s+t=5$. All three coordinates agree.

## 4. Verification

Reconstruct the displacement using the two plane directions:

$$2a+b=2(1,2,0)+(0,1,1)=(2,5,1)=D-A.$$

Thus $D=A+2a+b$ directly expresses membership in the plane. Also $n\cdot a=2-2=0$ and $n\cdot b=-1+1=0$, checking that the normal used in the test is correct.
