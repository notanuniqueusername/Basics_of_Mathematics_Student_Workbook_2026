# Problem 12. Symmetry, Sign, and Absolute Value

## The question

Compare
$$\int_{-2}^{2}x\,dx$$
and
$$\int_{-2}^{2}|x|\,dx.$$
Before calculating, predict the results from symmetry and a sketch, then carry out the calculation and explain the difference.

## Before calculating: predict cancellation and area

The function $x$ is odd, so its contributions on a symmetric interval cancel. The function $|x|$ is even and nonnegative, so its two halves add rather than cancel.

Symmetry can determine a definite integral before an antiderivative is found, but only after identifying the correct symmetry. An odd function has canceling signed contributions on a symmetric interval. An even function has equal contributions, which may add positively or negatively according to its sign; evenness alone does not guarantee a positive integral.

## 1. Sketch the distinction

```text
 y=x on [-2,2]           y=|x| on [-2,2]
      y                         y
      |  /                   \  |  /
 -----O---- x                  \ | /
    / |                     ----O---- x
 negative left area          both areas positive
```

The first integral is predicted to be zero; the second is predicted to be positive, equal to two congruent triangles.

## 2. Carry out the calculations

$$\boxed{\int_{-2}^2x\,dx=\left[\frac{x^2}{2}\right]_{-2}^2=2-2=0}.$$

Using $|x|=-x$ on the left and $|x|=x$ on the right,

$$\int_{-2}^2|x|\,dx=\int_{-2}^0(-x)\,dx+\int_0^2x\,dx=2+2=\boxed4.$$

## 3. Derive the cancellation by a change of variable

For the negative half of the odd integrand, set $u=-x$. Then

$$\int_{-2}^0x\,dx=-\int_0^2u\,du.$$

It cancels the positive-half integral exactly, giving zero. For absolute value, the same substitution gives

$$\int_{-2}^0|x|\,dx=\int_0^2u\,du,$$

so the halves are equal and add rather than cancel. This derives the symmetry rules from the actual signs instead of treating them as memorized labels.

The two triangles in the sketch have the same dimensions in both problems. What changes is how their contributions are counted: signed for $x$, nonnegative for $|x|$. That is why replacing a function by its absolute value changes an integral even when the underlying geometric shapes appear closely related.

## 4. Verification

Each triangle has base $2$ and height $2$, hence area $2$. For $x$, one contributes $-2$ and the other $+2$; for $|x|$, both contribute $+2$. This geometric check matches the exact antiderivative evaluations.

The total geometric area under $y=x$ over the interval is also $4$, despite its signed integral being zero. Symmetry predicts the correct behavior only after identifying whether the function is odd or even and whether signed accumulation or unsigned area is required.
