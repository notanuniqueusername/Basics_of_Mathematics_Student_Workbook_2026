# Exercise 11. Two Similar Surfaces

## The question

Compare
$$x^2+y^2-z^2=1$$
and
$$x^2+y^2-z^2=-1.$$
For several values $z=c$, check whether the cross-section exists and what its radius is. Based on this, describe qualitatively the difference between the surfaces and make sketches.

## Before calculating: inspect the radius squared

Rearrange each equation at height $z=c$ into $x^2+y^2=R^2$. A positive $R^2$ gives a circle, zero gives a point, and a negative value gives an empty section.

The sign of the constant changes which variable can be isolated with a positive remainder. Although both surfaces have the same quadratic coefficients, that constant determines whether the horizontal radius ever vanishes and whether there is a forbidden band of heights. This is why memorizing only the coefficient-sign pattern is insufficient here.

## 1. Compute sample sections

For $S_1:x^2+y^2-z^2=1$, the radius is $R_1=\sqrt{1+c^2}$ at every real height. For $S_2:x^2+y^2-z^2=-1$, it is $R_2=\sqrt{c^2-1}$ only when $|c|\ge1$.

| Height $c$ | $S_1$ section | $S_2$ section |
|---|---|---|
| $0$ | Circle of radius $1$ | Empty |
| $\pm1$ | Circle of radius $\sqrt2$ | One point |
| $\pm2$ | Circle of radius $\sqrt5$ | Circle of radius $\sqrt3$ |

## 2. Infer the shapes and sketch their meridians

$S_1$ is a one-sheet hyperboloid: every height has a nonempty circle, with a narrow waist at $z=0$. $S_2$ is a two-sheet hyperboloid: separate upper and lower pieces begin at $z=1$ and $z=-1$, with an empty gap between them.

```text
Meridian y=0; rotate each about z
 one sheet              two sheets
     z                       z
  )  |  (                 \  |  /
   ) | (                   \_*/   tip z=1
 ---)O(--- x             ----O---- x
   ) | (                    /*\   tip z=-1
  )  |  (                  / | \
```

## 3. Explain the connection or separation of the surface pieces

For the first surface, the parametrization

$$(x,y,z)=(\sqrt{1+c^2}\cos t,\sqrt{1+c^2}\sin t,c)$$

exists at every real $c$ and varies continuously through the central circle. There is no missing band between negative and positive heights, so the surface has one connected sheet.

For the second, a real circle requires $c\le-1$ or $c\ge1$. The upper and lower pieces cannot connect through any intermediate height because no points exist for $-1<c<1$. At $c=\pm1$, the radii become zero and each piece ends at a tip. These statements follow from the section equations, rather than from assigning the names one-sheet and two-sheet in advance.

## 4. Verification

The waist point $(1,0,0)$ satisfies $S_1$ but cannot satisfy $S_2$. The tip $(0,0,1)$ satisfies $S_2$ because $0+0-1=-1$. These checks show why changing only the constant changes connectivity, even though the quadratic signs are identical.
