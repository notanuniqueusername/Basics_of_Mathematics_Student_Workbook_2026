# Problem 4. A Quotient and Domain Control

## The question

For
$$f(x)=\frac{x^2+1}{x-1}$$
determine the domain, compute the derivative, simplify the result, and explain why the restriction $x\neq1$ remains important.

## Before calculating: quotient rule and excluded points

The domain requires $x-1\ne0$. For $u/v$, the derivative is $(u'v-uv')/v^2$, with that order in the numerator. Squaring the denominator does not restore an excluded point.

The quotient rule follows by differentiating $u(x)v(x)^{-1}$ with the product and chain rules. This explains both the squared denominator and the subtraction order in the numerator. Its use requires $v\ne0$, so a simplified formula must never silently include a point excluded from the original quotient.

## 1. Differentiate and simplify

$$\boxed{D_f=\mathbb R\setminus\{1\}}.$$

Using $u=x^2+1$, $u'=2x$, $v=x-1$, $v'=1$,

$$f'(x)=\frac{2x(x-1)-(x^2+1)}{(x-1)^2}=\boxed{\frac{x^2-2x-1}{(x-1)^2}},\qquad x\ne1.$$

The negative sign must distribute over the entire $x^2+1$.

## 2. Check by polynomial division

$$f(x)=x+1+\frac2{x-1}.$$

Differentiating this equivalent form gives

$$f'(x)=1-\frac2{(x-1)^2}=\frac{(x-1)^2-2}{(x-1)^2},$$

which expands to the same numerator $x^2-2x-1$.

## 3. Show the quotient rule as a product calculation

Rewrite $f=(x^2+1)(x-1)^{-1}$. Then

$$f'=2x(x-1)^{-1}-(x^2+1)(x-1)^{-2}.$$

Giving the two terms a common denominator yields

$$f'=\frac{2x(x-1)-(x^2+1)}{(x-1)^2}.$$

The second term is subtracted because the derivative of $(x-1)^{-1}$ is $-(x-1)^{-2}$. Expanding the numerator gives $2x^2-2x-x^2-1=x^2-2x-1$.

This step-by-step derivation checks the quotient-rule signs independently of memorizing the finished formula. Both the factored-denominator and polynomial-division calculations remain valid on the same domain $x\ne1$.

## 4. Verification and interpretation

At $x=0$, both formulas give $f'(0)=-1$. Near $x=1$ the term $2/(x-1)$ is unbounded; the original function has a genuine vertical asymptote, not a removable hole. Thus neither $f$ nor its derivative has a value there. The alternative calculation checks the derivative independently while keeping the same domain restriction.

**Definition check at an ordinary domain point.** At $x=0$, $f(0)=-1$. For small nonzero $h$,

$$\frac{f(h)-f(0)}h=\frac{(h^2+1)/(h-1)+1}{h}=\frac{h^2+h}{h(h-1)}=\frac{h+1}{h-1}\longrightarrow-1.$$

This agrees with the derivative formula at zero. The check stays away from the excluded point $1$ and does not require any extension there. It tests the numerator subtraction sign directly, which both the quotient-rule and product-rule computations must get right.
