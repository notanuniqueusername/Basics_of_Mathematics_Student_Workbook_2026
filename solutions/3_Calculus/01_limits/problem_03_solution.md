# Exercise 3. A Square Root and Removing an Indeterminate Form

## The question

Compute
$$\lim_{n\to\infty}\left(\sqrt{n^2+5n}-n\right).$$
Use the conjugate expression and explain why this transformation removes the difficulty.

## Before calculating: remove cancellation between large terms

The expression has the indeterminate form $\infty-\infty$. Multiply by its conjugate and use $(a-b)(a+b)=a^2-b^2$. This is an exact algebraic transformation, not an approximation.

The notation $\infty-\infty$ names an indeterminate pattern, not a value. Differences of two growing quantities can approach zero, a finite nonzero number, or infinity. Rationalization exposes the difference of their squares and permits an actual limit calculation. The equality $\sqrt{n^2}=n$ uses positivity of the index, and would require an absolute value for a general real variable.

## 1. Rationalize

$$\sqrt{n^2+5n}-n=\frac{(n^2+5n)-n^2}{\sqrt{n^2+5n}+n}=\frac{5n}{\sqrt{n^2+5n}+n}.$$

For positive $n$, divide the numerator and denominator by $n$. Since $\sqrt{n^2}=|n|=n$ here,

$$\frac{5n}{\sqrt{n^2+5n}+n}=\frac5{\sqrt{1+5/n}+1}.$$

## 2. Take the limit

Continuity of the square root gives $\sqrt{1+5/n}\to1$. The denominator approaches $2$, so

$$\boxed{\lim_{n\to\infty}(\sqrt{n^2+5n}-n)=\frac52}.$$

Rationalization has replaced subtraction of two unbounded quantities with a quotient whose denominator has a nonzero finite limit.

## 3. Bound how far the sequence lies below the answer

Let $s_n=\sqrt{1+5/n}$. The exact difference from $5/2$ is

$$\frac52-\frac5{s_n+1}=\frac{5(s_n-1)}{2(s_n+1)}.$$

Rationalizing $s_n-1$ gives $s_n-1=(5/n)/(s_n+1)$, so

$$0<\frac52-\left(\sqrt{n^2+5n}-n\right)=\frac{25}{2n(s_n+1)^2}\le\frac{25}{8n}.$$

The upper bound tends to zero, proving convergence with a concrete error estimate and confirming approach from below. This check also explains why subtracting the two large original terms numerically is less stable than evaluating the equivalent normalized quotient.

## 4. Verification

The normalized denominator is greater than $2$, so every term is positive and smaller than $5/2$, consistent with approach from below. Let $d_n=\sqrt{1+5/n}-1\to0$. The error from the answer is

$$\frac5{2+d_n}-\frac52=-\frac{5d_n}{2(2+d_n)}\to0.$$

This confirms both the proposed limit and the direction of approach.

**Check that the conjugate does not alter the domain.** For positive $n$, both $n^2+5n$ and the conjugate denominator $\sqrt{n^2+5n}+n$ are strictly positive. Multiplication by the conjugate ratio therefore divides by no zero quantity. After normalization the denominator is also positive and tends to $2$, so the final quotient limit law is legitimate. These checks distinguish an exact equivalent expression from a formal manipulation of an indeterminate symbol. The result $5/2$ is a finite limit of the difference, even though each of its original terms grows without bound.
