# Problem 12. A Function with an Absolute Value

## The question

Analyze
$$f(x)=|x^2-4|.$$
First sketch $x^2-4$, then explain the effect of the absolute value. Indicate the points where the derivative does not exist and justify the reason geometrically.

## Before calculating: reflect the negative part of the graph

The base parabola $q(x)=x^2-4$ has vertex $(0,-4)$ and zeros $\pm2$. Taking an absolute value leaves its nonnegative parts unchanged and reflects its negative part above the axis.

Absolute value is applied to function values, so it reflects only the graph portions below the horizontal axis. It does not replace $x$ by $|x|$, although this particular function is even already. The joins where a reflected and unreflected piece meet must be tested for one-sided slopes, because differentiability of the underlying polynomial does not automatically survive absolute value.

## 1. Sketch the original parabola and write the reflected formula

First draw $q(x)=x^2-4$, before applying the absolute value. It opens upward, crosses the axis at $(-2,0)$ and $(2,0)$, and has vertex $(0,-4)$:

```text
 q(x)                   y
                        ^
          \             |             /
           \            |            /
 0 ---------*-----------+-----------*--------> x
          (-2,0)        |         (2,0)
              \        |        /
                \      |      /
                  \    |    /
-4                  \__*__/
                     (0,-4)
```

The central arc on $-2<x<2$ is below the axis. Reflect that arc upward, leaving both outer arms unchanged. Algebraically this gives

$$f(x)=\begin{cases}x^2-4,&|x|\ge2,\\4-x^2,&|x|<2.\end{cases}$$

Away from $\pm2$,

$$f'(x)=\begin{cases}2x,&|x|>2,\\-2x,&|x|<2.\end{cases}$$

It decreases on $(-\infty,-2)$, increases on $(-2,0)$, decreases on $(0,2)$, and increases on $(2,\infty)$. Thus $(\pm2,0)$ are global minima and $(0,4)$ is a local maximum.

## 2. Identify the corners and sketch

At $-2$, the one-sided derivatives are $-4$ and $4$; at $2$, they are $-4$ and $4$. They disagree, so the derivative does not exist at either join, even though the function is continuous there.

```text
After reflection: f(x)=|x²-4|
 y
4            * (0,4)
 | \       /   \       /
 |  \    /       \    /
0+---*-------------*--------- x
   (-2,0)        (2,0)
```

## 3. Compute the one-sided slopes at both corners

At $x=-2$, the outer formula gives derivative $2(-2)=-4$ from the left, while the inner reflected formula gives $-2(-2)=4$ from the right. At $x=2$, the inner formula gives $-4$ from the left and the outer gives $4$ from the right.

Each join therefore has the slope pattern negative-to-positive, consistent with its sharp minimum, but no single derivative value. At zero the reflected formula is a smooth downward parabola with derivative zero and value $4$.

Continuity holds everywhere because absolute value is continuous and the original polynomial is continuous. This example separates three properties: continuous joins at $\pm2$, failure of derivatives there, and a differentiable local maximum at zero. The sketch must show corners only at the two zeros, not at the central peak.

## 4. Verification

$f(0)=4$, $f(\pm2)=0$, and $f(\pm3)=5$, agreeing with the reflected shape and even symmetry. Since absolute value is nonnegative, the zeros are necessarily global minima. At $x=0$, $f''=-2<0$, confirming the local maximum; the unequal one-sided slopes at the zeros explain the sharp corners geometrically.
