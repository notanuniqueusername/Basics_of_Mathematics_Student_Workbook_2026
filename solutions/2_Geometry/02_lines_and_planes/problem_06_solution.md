# Exercise 6. Angle Between Planes

## The question

Given
$$\Pi_1:x+y+z=1,\qquad \Pi_2:x-y=2.$$
First use the normal vectors to decide whether the planes are parallel. If not, compute the angle between them and explain why the normal vectors alone are enough for this calculation.

## Before calculating: use normals for plane angles

Plane orientation is determined by its normal. The usual angle between two planes is the acute or right angle with cosine $|n_1\cdot n_2|/(\|n_1\|\|n_2\|)$; the absolute value makes the answer independent of the chosen normal orientations.

Plane equations may be multiplied by any nonzero scalar without changing their point sets. Accordingly, an angle formula must be independent of scaling or reversing either normal. The product of normal lengths cancels scalar magnitudes, and the absolute value in the numerator removes any change caused by reversing a normal's orientation.

## 1. Read and compare the normals

$$n_1=(1,1,1),\qquad n_2=(1,-1,0).$$

They are not proportional, so the planes are not parallel. Their different constants do not affect their orientations.

## 2. Compute the angle

$$n_1\cdot n_2=1-1+0=0,\quad\|n_1\|=\sqrt3,\quad\|n_2\|=\sqrt2.$$

Therefore

$$\cos\theta=\frac0{\sqrt6}=0,\qquad\boxed{\theta=\frac\pi2=90^\circ}.$$

The planes are perpendicular.

## 3. Explain why normals determine the angle

A plane's normal fixes its orientation: all in-plane displacements are perpendicular to it. Translating the plane changes only its constant, leaving those directions and every angle unchanged. This is why the constants $1$ and $2$ do not enter the angle calculation.

Here $n_2$ is itself parallel to the first plane, since $n_1\cdot n_2=0$, while it is normal to the second. Thus the second plane has a normal lying parallel to the first, exactly the geometry of perpendicular planes. One common point is $(3/2,-1/2,0)$, which satisfies both equations, so this orientation comparison concerns two actually intersecting planes rather than parallel displaced copies.

## 4. Verification and interpretation

Their normal cross product is $(1,1,-2)$, which is nonzero and perpendicular to both normals: $1+1-2=0$ and $1-1=0$. Thus an intersection direction exists, consistently with nonparallel planes. The normal angle already determines the dihedral angle; locating the intersection line is unnecessary. Replacing either normal by its negative leaves the zero dot product, and hence the right angle, unchanged.
