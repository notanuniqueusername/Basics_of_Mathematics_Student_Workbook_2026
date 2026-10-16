# Exercise 2. A Line in Space

## The question

Given
$$L:(x,y,z)=(2,-1,3)+t(1,2,-2).$$
State a point on the line and its direction vector, check whether $P=(4,3,-1)$ lies on $L$, and find the point corresponding to $t=-1$.

## Before calculating: one parameter controls all coordinates

A spatial line $p+tv$ has a fixed point $p$ and direction $v$. A test point belongs to it only if a single value of $t$ works in all three coordinates.

A spatial parameter value specifies a point, not three independently adjustable coordinate values. Membership therefore requires compatibility of all three coordinate equations. A point satisfying only the $x$ equation gives a candidate parameter, which must still be substituted into $y$ and $z$ before a conclusion is valid.

## 1. Read the geometric data

$$\boxed{p=(2,-1,3),\qquad v=(1,2,-2)}.$$

The coordinate equations are $x=2+t$, $y=-1+2t$, $z=3-2t$. The direction is nonzero, so these describe a line rather than one fixed point.

## 2. Test membership of $P$

From the $x$ coordinate, $4=2+t$, hence $t=2$. Check the other coordinates using that same value:

$$-1+2\cdot2=3,\qquad 3-2\cdot2=-1.$$

Both match, so $\boxed{P\in L}$.

## 3. Derive a parameter-free membership test

Since all direction components here are nonzero, eliminate the parameter:

$$\frac{x-2}{1}=\frac{y+1}{2}=\frac{z-3}{-2}.$$

For $P=(4,3,-1)$ these ratios are $2$, $4/2=2$, and $(-4)/(-2)=2$. Their agreement is the same compatibility test as the parametric calculation. For the point $(1,-3,5)$, the ratios are all $-1$.

The line's direction length is $\sqrt{1+4+4}=3$. Thus moving the parameter by $1$ changes position by a distance $3$, while changing it by $-1$ moves the same distance in the opposite direction. This explains why the parameter is not automatically physical distance.

## 4. Evaluate the negative parameter

For $t=-1$,

$$\boxed{p-v=(2-1,-1-2,3+2)=(1,-3,5)}.$$

A negative parameter moves opposite to $v$; it does not leave the line.

## 5. Verification

$P-p=(2,4,-4)=2v$, directly confirming membership. For the point at $t=-1$, $(1,-3,5)-p=(-1,-2,2)=-v$, confirming all coordinate signs. The line's displacement from the anchor must be parallel to $v$ in either case.
