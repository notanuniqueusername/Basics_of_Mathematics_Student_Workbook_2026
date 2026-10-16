# Exercise 1. Recognizing Curves from Canonical Form

## The question

Recognize the curves
$$x^2+y^2=9,$$
$$\frac{x^2}{16}+\frac{y^2}{9}=1,$$
$$y^2=8x,$$
$$\frac{x^2}{9}-\frac{y^2}{4}=1.$$
For each one, identify the most important features and make a sketch. Explain which parts of the equation let you recognize the type of curve.

## Before calculating: recognize the signs and squared terms

Equal positive squared-coordinate coefficients describe a circle. Unequal positive coefficients give an ellipse. One squared coordinate gives a parabola. Opposite signs of two squared coordinates give a hyperbola. The positive right-hand sides here ensure nondegenerate real curves.

Canonical equations should be read as coordinate constraints, not just recognized by a name. Setting one coordinate to zero finds axis intercepts, changing a coordinate's sign tests symmetry, and requiring a squared quantity to be nonnegative identifies which parts of the plane can contain points. These checks determine the main shape and prevent a misleading sketch.

## 1. Read the four canonical forms

| Equation | Type | Main features |
|---|---|---|
| $x^2+y^2=9$ | Circle | Center $(0,0)$, radius $3$, intercepts $(\pm3,0),(0,\pm3)$ |
| $x^2/16+y^2/9=1$ | Ellipse | Center $(0,0)$, horizontal semiaxis $4$, vertical semiaxis $3$ |
| $y^2=8x$ | Parabola | Vertex $(0,0)$, axis $y=0$, opens right |
| $x^2/9-y^2/4=1$ | Hyperbola | Center $(0,0)$, vertices $(\pm3,0)$, asymptotes $y=\pm(2/3)x$ |

For the parabola, $y^2=4px$ gives $p=2$, so its focus is $(2,0)$ and its directrix is $x=-2$. Its nonnegative left side forces $x\ge0$.

## 2. Qualitative sketches

The sketches are schematic; the table supplies the exact scales.

```text
Circle                 Ellipse
       y                       y
     .-+-.                   .--+--.
   /   |   \               /   |   \
 --+---O---+-- x        ---+----O----+--- x
   \   |   /               \   |   /
     '-+-'                   '--+--'

Right-opening parabola      Horizontal hyperbola
       y                         y
       |  /                \   ) | (   /
       | /                  \ )  |  ( /
 ------V------ x          ----V---O---V---- x
       | \                  / )  |  ( \
       |  \                /   ) | (   \
```

The sloping lines in the hyperbola panel indicate asymptote directions, not curve intersections.

## 3. Build the sketches from exact coordinate tests

For the circle, $y=\pm\sqrt{9-x^2}$ requires $|x|\le3$. For the ellipse, $y=\pm3\sqrt{1-x^2/16}$ requires $|x|\le4$; the different horizontal and vertical endpoint scales explain its wider appearance.

For the parabola, $x=y^2/8$ permits all real $y$ but only $x\ge0$, producing upper and lower arms around its horizontal axis. For the hyperbola, $y=\pm\frac23\sqrt{x^2-9}$ requires $|x|\ge3$, leaving a gap between the two branches. These exact coordinate restrictions distinguish bounded closed curves from unbounded ones. The schematic sketches below should be read with the endpoint labels and these allowed-coordinate ranges, not as scale drawings.

## 4. Verification

The points $(3,0)$, $(4,0)$, $(2,4)$, and $(3,0)$ satisfy the four respective equations: $9=9$, $16/16=1$, $16=8\cdot2$, and $9/9=1$. The circle and ellipse are bounded; the parabola and hyperbola extend indefinitely. These facts agree with the coefficient patterns and sketches.
