# Exercise 2. Different Growth Rates

## The question

Compute
$$\lim_{n\to\infty}\frac{3n+1}{n^2+4},\qquad \lim_{n\to\infty}\frac{2n^3-n}{5n^2+1}.$$
Compare the two cases and formulate a general observation about the degrees of the polynomials in the numerator and denominator.

## Before calculating: compare polynomial degrees

For a rational expression at positive infinity, lower numerator degree gives zero, equal degrees give the leading-coefficient ratio, and higher numerator degree gives unbounded magnitude whose sign depends on the leading coefficients. These statements require a nonzero denominator for sufficiently large inputs.

The degree rule describes magnitude first; the leading coefficients determine eventual sign. Here all relevant leading coefficients are positive and the variable tends to positive infinity. At negative infinity, an odd degree difference could reverse the sign, so one should not memorize “higher numerator degree means positive infinity” without the stated sign conditions.

## 1. Lower numerator degree

$$\frac{3n+1}{n^2+4}=\frac{3/n+1/n^2}{1+4/n^2}\longrightarrow\boxed{0}.$$

The denominator grows quadratically while the numerator grows linearly, so the quotient vanishes.

## 2. Higher numerator degree

$$\frac{2n^3-n}{5n^2+1}=n\frac{2-1/n^2}{5+1/n^2}.$$

The second factor approaches $2/5>0$, while $n\to+\infty$. Hence

$$\boxed{\lim_{n\to\infty}\frac{2n^3-n}{5n^2+1}=+\infty}.$$

This is divergence to positive infinity, not convergence to a finite number.

## 3. Connect both answers with leading-order comparisons

For the first expression,

$$\frac{(3n+1)/(n^2+4)}{3/n}=\frac{1+1/(3n)}{1+4/n^2}\longrightarrow1.$$

Thus its size is asymptotically $3/n$, which decays to zero. For the second,

$$\frac{(2n^3-n)/(5n^2+1)}{(2/5)n}=\frac{1-1/(2n^2)}{1+1/(5n^2)}\longrightarrow1.$$

Its size is asymptotically $(2/5)n$, which grows without bound. These ratios explain the degree comparison more precisely: after factoring the leading powers, the remaining correction factors approach $1$. They also show that replacing a whole polynomial by its leading term is a limiting comparison, not an exact algebraic equality for finite $n$.

## 4. Verification by bounds

For $n\ge1$, the first quotient is nonnegative and at most $(3n+1)/n^2\le4/n\to0$, confirming its limit by squeezing.

For the second, $2n^3-n\ge n^3$ and $5n^2+1\le6n^2$. Therefore the quotient is at least $n/6\to+\infty$. This proves the unbounded positive behavior rather than relying only on the informal phrase “higher degree wins.”

**State the general rule with the necessary sign qualification.** If nonzero polynomials have degrees $p,q$ and leading coefficients $a,b$, their quotient at positive infinity has size $(a/b)n^{p-q}$. For $p<q$ it tends to zero; for $p=q$ it tends to $a/b$; for $p>q$ its magnitude diverges, with eventual sign determined by $a/b$. The two exercises use positive leading ratios, so the divergent case is positive infinity. This formulation explains both examples while avoiding a false universal claim that every higher-degree numerator produces the same signed divergence.
