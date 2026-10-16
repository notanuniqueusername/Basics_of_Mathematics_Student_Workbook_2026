# Exercise 9. One-Sided Limits and an Asymptote

## The question

Analyze the left-hand and right-hand limits of
$$f(x)=\frac1{x-2}$$
as $x\to2$. Does the two-sided limit exist? Interpret the result on a sketch of the graph and identify the vertical asymptote.

## Before calculating: the sign of a small denominator matters

A reciprocal becomes unbounded as its denominator tends to zero, but its sign depends on the side. A two-sided limit requires agreement of both one-sided limits, including when infinite limits are considered.

An infinite one-sided limit means values eventually exceed every positive threshold in magnitude with a specified sign. It does not mean the function attains an “infinite value” at the excluded point. The graph has two disconnected branches because $x=2$ is outside the domain; a sketch must not connect them across the asymptote.

## 1. Compute the one-sided limits

For $x<2$, $x-2<0$ and tends to zero from below:

$$\boxed{\lim_{x\to2^-}\frac1{x-2}=-\infty}.$$

For $x>2$, the denominator tends to zero from above:

$$\boxed{\lim_{x\to2^+}\frac1{x-2}=+\infty}.$$

They disagree, so the two-sided limit does not exist, even as a single extended-real infinite limit. The vertical asymptote is $\boxed{x=2}$.

## 2. Sketch the behavior

```text
      y              x=2
      ^               : *
      |               : *
      |               :  *
      |               :   *
      |               :     *
      |               :        *   *    *      *
 0 ---+---------------:----------------------------> x
      | *  *   *      :
      |          *    :
      |            *  :
      |             * :
      |             * :
      |             * :
```

The stars mark schematic branch locations, with spacing chosen for clarity rather than a uniform numerical scale. Every right-branch point is strictly above the horizontal axis, and every left-branch point is strictly below it: $1/(x-2)>0$ when $x>2$ and $1/(x-2)<0$ when $x<2$. Neither branch touches or crosses $y=0$.

The left branch descends without bound as $x\to2^-$; the right branch rises without bound as $x\to2^+$. Far from the vertical asymptote, the branches approach $y=0$ from below and above, respectively.

## 3. Distinguish nonexistence from an unsigned blowup statement

The magnitude satisfies $|f(x)|=1/|x-2|\to+\infty$ as $x\to2$, but the signed function has no single two-sided limit. These statements are compatible: the distance from zero grows on both sides while the signs disagree.

For example, the two sequences $x_n=2-1/n$ and $y_n=2+1/n$ both approach $2$, but $f(x_n)=-n$ and $f(y_n)=n$. A single two-sided extended-real limit would have to agree along both, which is impossible.

The vertical line $x=2$ records where this behavior occurs. The horizontal asymptote $y=0$ concerns a different limit, at large $|x|$, and should not be confused with the finite-point analysis.

## 4. Verification

For $h>0$, $f(2-h)=-1/h$ and $f(2+h)=1/h$. At $h=0.1,0.01,0.001$, these values are $-10,-100,-1000$ and $10,100,1000$. More generally, choosing $0<h<1/M$ makes the magnitudes exceed any prescribed $M>0$, verifying unboundedness on each side.
