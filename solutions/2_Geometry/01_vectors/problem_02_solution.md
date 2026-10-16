# Exercise 2. Distance as the Length of a Vector

## The question

The points are $A=(1,2,3)$ and $B=(4,-2,6)$.

1. Construct $\overrightarrow{AB}$.
2. Compute its length.
3. Compute the distance between the points using the coordinate formula.
4. Explain why both calculations give the same result.

## Before calculating: displacement and length

The displacement from $A$ to $B$ is the endpoint minus the starting point. The Euclidean norm is $\|(x,y,z)\|=\sqrt{x^2+y^2+z^2}$, obtained by the Pythagorean theorem in three perpendicular coordinate directions.

A point records a location, whereas a displacement records how one location changes to another. That distinction fixes the subtraction order: $B-A$ points from $A$ to $B$. Reversing the subtraction changes the orientation but leaves the geometric distance unchanged. All squared coordinate differences in the length formula have the same squared-length units.

## 1. Construct the displacement

$$\overrightarrow{AB}=B-A=(4-1,-2-2,6-3)=\boxed{(3,-4,3)}.$$

The negative second coordinate means a displacement of $4$ units in the negative $y$ direction.

## 2. Compute its length and the distance

$$\|\overrightarrow{AB}\|=\sqrt{3^2+(-4)^2+3^2}=\sqrt{9+16+9}=\boxed{\sqrt{34}}.$$

The coordinate distance formula gives

$$d(A,B)=\sqrt{(4-1)^2+(-2-2)^2+(6-3)^2}=\sqrt{34}.$$

These are the same calculation: distance is precisely the length of the displacement joining the points. The formula is not a separate geometric principle.

## 3. Explain the three-dimensional Pythagorean calculation

The horizontal change $(3,-4,0)$ has length $\sqrt{3^2+(-4)^2}=5$. The remaining change $(0,0,3)$ is perpendicular to it, so a second application of the Pythagorean theorem gives

$$d^2=5^2+3^2=34.$$

Thus the three-dimensional distance formula is the two-dimensional theorem applied twice. Its numerical value is $\sqrt{34}\approx5.831$ length units, which is larger than either perpendicular component, $5$ and $3$, and smaller than their sum, $8$. Those inequalities provide a useful size check: adding the coordinate magnitudes would give the length of a broken coordinate path, not the straight segment joining the points.

## 4. Explain the effect of reversing direction

$\overrightarrow{BA}=(-3,4,-3)=-\overrightarrow{AB}$. Reversing a vector changes its orientation but not its length, since all coordinates are squared in the norm.

## 5. Verification

Reconstruct the endpoint:

$$A+\overrightarrow{AB}=(1,2,3)+(3,-4,3)=(4,-2,6)=B.$$

Also $\|\overrightarrow{BA}\|=\sqrt{9+16+9}=\sqrt{34}$, so $d(B,A)=d(A,B)$ as required of a distance.
