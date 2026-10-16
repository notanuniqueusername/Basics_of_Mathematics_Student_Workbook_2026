# Exercise 15. Complete Classification of a Line Relative to a Plane

## The question

Let
$$L:p+tv,\qquad \Pi:n\cdot x=d.$$
State the conditions distinguishing the three cases: one intersection point, parallel with no common points, and the line contained in the plane. Then illustrate each case with your own simple numerical example.

## Before calculating: assumptions and substitution

Assume $v\ne0$ and $n\ne0$, so $L$ is a genuine line and $\Pi$ a genuine plane. A common point requires

$$n\cdot(p+tv)=d\quad\Longleftrightarrow\quad t(n\cdot v)=d-n\cdot p.$$

This one linear equation supplies the complete classification.

These conditions are exhaustive because the line-plane substitution is a single linear equation in $t$. It cannot have exactly two or finitely many more than one solutions: a nonzero slope gives one parameter, and zero slope gives either a contradiction or an identity. The assumptions $n\ne0$ and $v\ne0$ exclude degenerate objects before this argument is used.

## 1. State the three cases

| Conditions | Common set |
|---|---|
| $n\cdot v\ne0$ | One point, at $t=(d-n\cdot p)/(n\cdot v)$ |
| $n\cdot v=0$ and $n\cdot p\ne d$ | No common points; parallel and disjoint |
| $n\cdot v=0$ and $n\cdot p=d$ | Every line point; $L\subset\Pi$ |

## 2. Give examples using the same plane

Take $\Pi:z=0$, with $n=(0,0,1)$ and $d=0$.

**Crossing:** $L_1=(0,0,1)+t(0,0,-1)$. Here $n\cdot v=-1$, so $t=1$ and the intersection is $(0,0,0)$.

**Disjoint parallel:** $L_2=(0,0,1)+t(1,0,0)$. Here $n\cdot v=0$ but $n\cdot p=1\ne0$.

**Contained:** $L_3=(0,0,0)+t(1,0,0)$. Both dot products are zero.

## 3. Explain which information controls each decision

The scalar $n\cdot v$ depends only on the line direction and plane orientation, so it determines whether a crossing is possible. When it is nonzero, the location information $d-n\cdot p$ selects the crossing parameter. When it is zero, that same location information separates a line lying in the plane from a parallel line outside it.

Rescaling $n$ and $d$ together leaves all conditions unchanged, and rescaling $v$ changes the crossing parameter but not its point. These invariances are important consistency checks: the classification must describe geometric objects, not depend on which equivalent equation or direction vector was chosen to represent them.

## 4. Verification

The three height coordinates are, respectively, $1-t$, $1$, and $0$. The first vanishes once, the second never, and the third always. This explicitly verifies the three predicted intersection types. There is no fourth possibility because the parameter equation is linear: a nonzero coefficient gives one solution, while a zero coefficient gives either none or all.
