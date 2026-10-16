# Exercise 10. Triangle Area from Vectors

## The question

The points $A=(0,0,0)$, $B=(2,1,0)$, and $C=(1,3,2)$ form a triangle. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$, compute the area of the parallelogram using the cross product, and then find the area of the triangle. Explain the factor $\frac12$.

## Before calculating: cross product as area

Two side vectors from the same vertex span a parallelogram of area $\|a\times b\|$. A triangle with those sides occupies half that parallelogram, so its area is $\frac12\|a\times b\|$.

The area formula uses two side displacements, not the absolute coordinates of three points independently. Translating the whole triangle does not change those displacements. The cross product may change sign if the sides are reordered, but its norm, and hence either area, remains unchanged. This is the spatial extension of absolute determinants for planar area.

## 1. Construct the sides

$$a=\overrightarrow{AB}=B-A=(2,1,0),\qquad b=\overrightarrow{AC}=C-A=(1,3,2).$$

Using a common starting vertex is essential: these vectors represent the two sides enclosing the triangle's angle at $A$.

## 2. Calculate the areas

$$a\times b=(1\cdot2-0\cdot3,0\cdot1-2\cdot2,2\cdot3-1\cdot1)=(2,-4,5).$$

Thus

$$\boxed{A_{\rm parallelogram}=\sqrt{2^2+(-4)^2+5^2}=\sqrt{45}=3\sqrt5},$$

$$\boxed{A_{\rm triangle}=\frac{3\sqrt5}{2}}.$$

The parallelogram diagonal splits it into two congruent triangles, explaining the factor $1/2$ independently of the calculation.

## 3. Check the area using a different triangle vertex

From $B$, the two sides are $A-B=(-2,-1,0)$ and $C-B=(-1,2,2)$. Their cross product is

$$(-2,-1,0)\times(-1,2,2)=(-2,4,-5)=-(2,-4,5).$$

Its norm is again $\sqrt{45}=3\sqrt5$, so the triangle area is still $3\sqrt5/2$. The sign change records a different ordering of the directed sides, not a negative geometric area.

This checks that using a different common vertex has not changed the geometric quantity. It also guards against mixing a side from $A$ with a side from $B$ without explaining the relationship: a consistent common-vertex construction makes the area mechanism transparent.

## 4. Verification

The cross product is perpendicular to both sides:

$$(2,-4,5)\cdot(2,1,0)=4-4=0,\qquad (2,-4,5)\cdot(1,3,2)=2-12+10=0.$$

Also $\|a\|^2=5$, $\|b\|^2=14$, and $a\cdot b=5$, so the area squared is $5\cdot14-5^2=45$, matching the norm squared above. The positive area confirms the three points are not collinear.
