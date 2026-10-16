# Exercise 4. Parabola

## The question

For
$$y^2=12x,$$
identify the vertex, axis of symmetry, and opening direction. Find points on the parabola for $x=3$ and use them to make a sketch.

## Before calculating: the squared coordinate determines the axis

In $y^2=4px$, the vertex is the origin and the axis is horizontal. A positive $p$ gives opening toward positive $x$, while symmetry under $y\mapsto-y$ gives upper and lower branches.

A parabola is not described by an enclosed center and radius. Its vertex is the endpoint of its symmetry axis on the curve, and its arms extend without bound. In the form $y^2=4px$, the parameter $p$ measures the vertex-to-focus distance, while the sign of $p$ fixes whether the opening is rightward or leftward.

## 1. Identify the geometry

Comparing $y^2=12x$ with $y^2=4px$ gives $p=3$. Thus the vertex is $\boxed{(0,0)}$, the symmetry axis is $\boxed{y=0}$, and the parabola opens $\boxed{\text{to the right}}$. The focus is $(3,0)$ and directrix is $x=-3$.

The condition $y^2\ge0$ forces $x\ge0$, so there are no points to the left of the vertex.

## 2. Find the requested points and sketch

At $x=3$, $y^2=36$, hence $\boxed{(3,6),(3,-6)}$.

```text
          y
          |       * (3,6)
          |    .'
          | .'
 ---------V-----------> x
          | '.
          |    '.
          |       * (3,-6)
       V=(0,0)
```

The two points have equal height magnitudes and the same $x$ coordinate, showing the symmetry.

## 3. Recover the equation from the focus and directrix

With focus $(3,0)$ and directrix $x=-3$, a point $(x,y)$ on the parabola has equal distances to those objects:

$$\sqrt{(x-3)^2+y^2}=|x+3|.$$

Squaring gives $(x-3)^2+y^2=(x+3)^2$, hence $y^2=12x$. The stated focus-directrix data therefore reproduce the original equation, rather than being unrelated extra labels.

For sketching, the two points at $x=3$ are six units above and below the axis. At $x=0$ both arms meet at the vertex; at $x=12$, the heights are $\pm12$. These landmarks establish the rightward growth and show why the diagram's horizontal and vertical scales must be read from the labels.

## 4. Verification

Both satisfy $y^2=36=12\cdot3$. Their distance to the focus $(3,0)$ is $6$, and their distance to the directrix $x=-3$ is $|3+3|=6$, providing a geometric check. At the vertex, both distances equal $3$. The sketch therefore agrees with both the equation and the focus-directrix description.
