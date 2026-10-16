# Exercise 6. From a Sequence to a Function — Limit at Infinity

## The question

Compute
$$\lim_{x\to\infty}\frac{3x^2-x+1}{5x^2+4x-2}.$$
Compare the method with Exercise 1. Explain what changes when moving from $n$ to a real variable $x$, and what stays the same.

## Before calculating: transfer the sequence method

At positive infinity, divide by the dominant power exactly as for polynomial sequences. The difference is that $x$ can take every sufficiently large real value, rather than only integer values; the algebra and limit laws remain the same.

A real-variable limit at infinity is stronger than observing the same expression at integer values. To prove it, the estimate must work for every sufficiently large real $x$. The normalized quotient supplies that control directly, so no interpolation assumption about behavior between integers is needed.

## 1. Divide by x squared

$$\frac{3x^2-x+1}{5x^2+4x-2}=\frac{3-1/x+1/x^2}{5+4/x-2/x^2}.$$

As $x\to+\infty$, the numerator tends to $3$ and the denominator to $5\ne0$. Therefore

$$\boxed{\lim_{x\to\infty}\frac{3x^2-x+1}{5x^2+4x-2}=\frac35}.$$

Any isolated zeros of the original denominator at finite values do not affect behavior on a sufficiently far right-hand tail.

## 2. Compare with the sequence calculation

Both examples have equal numerator and denominator degrees. Dividing by the common highest power leaves the leading coefficients and terms tending to zero. A sequence samples integer arguments; the function limit controls the expression at all sufficiently large real arguments, including those between consecutive integers.

## 3. Give an explicit real-variable error estimate

For $x\ge1$, the denominator satisfies $5x^2+4x-2\ge5x^2$, and $17x-11\le17x$. Hence

$$\left|f(x)-\frac35\right|=\frac{17x-11}{5(5x^2+4x-2)}\le\frac{17}{25x}.$$

For any $\varepsilon>0$, taking $x>\max(1,17/(25\varepsilon))$ makes the error smaller than $\varepsilon$. This estimate applies to all real inputs on that tail, not just integers.

It also confirms the graph's position relative to its horizontal asymptote: the exact numerator of the signed error is negative for $x\ge1$, so the approach is from below. The size estimate and sign information answer different questions and can be checked separately.

## 4. Verification

Subtract the proposed answer:

$$\frac{3x^2-x+1}{5x^2+4x-2}-\frac35=\frac{-17x+11}{5(5x^2+4x-2)}\longrightarrow0.$$

The error is a quotient with lower numerator degree, confirming the limit independently. It is negative for sufficiently large positive $x$, so the graph approaches the horizontal asymptote $y=3/5$ from below.
