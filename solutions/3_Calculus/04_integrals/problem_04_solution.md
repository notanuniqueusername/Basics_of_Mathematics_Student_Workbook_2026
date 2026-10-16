# Problem 4. Substitution as Reversing the Chain Rule

## The question

Compute
$$\int 2x(x^2+1)^4\,dx.$$
Before calculating, identify a candidate for the new variable $u$ and show that its derivative appears in the integral. Finally, verify the result by differentiation.

## Before calculating: recognize the derivative of the inside

The integrand is a power of $x^2+1$ multiplied by its derivative $2x$. Substitution reverses the chain rule by replacing the entire inner expression with one variable.

Substitution is justified by the chain rule: if $H'(u)=u^4$, then $(H(g(x)))'=H'(g(x))g'(x)$. The given integrand has exactly that latter form with $g=x^2+1$. The symbol $du=2x\,dx$ records this matching; it should not be interpreted as permission to divide by $x$ and exclude zero unnecessarily.

## 1. Make the substitution

$$u=x^2+1,\qquad du=2x\,dx.$$

Thus

$$\int2x(x^2+1)^4\,dx=\int u^4\,du.$$

No extra factor is required because the differential matches exactly.

## 2. Integrate and return to x

$$\int u^4\,du=\frac{u^5}{5}+C.$$

Substituting back gives

$$\boxed{\frac{(x^2+1)^5}{5}+C}.$$

The integrand and answer are defined on $\mathbb R$. The substitution is recognized by the inner derivative; expanding the fourth power would be possible but would introduce unnecessary terms.

## 3. Check the answer by expanding the polynomial instead

The binomial expansion is

$$(x^2+1)^4=x^8+4x^6+6x^4+4x^2+1.$$

Multiplying by $2x$ and integrating termwise gives

$$\frac{x^{10}}5+x^8+2x^6+2x^4+x^2+C.$$

Expanding the compact answer gives

$$\frac{(x^2+1)^5}{5}=\frac{x^{10}}5+x^8+2x^6+2x^4+x^2+\frac15.$$

The formulas differ only by a constant $1/5$, so they represent the same antiderivative family. This independently checks every coefficient and explains why two apparently different indefinite-integral answers can both be correct. Substitution is the shorter route because it avoids this full expansion, but the expansion makes a useful verification.

## 4. Verification

Use the chain rule:

$$\frac{d}{dx}\left(\frac{(x^2+1)^5}{5}+C\right)=\frac15\cdot5(x^2+1)^4\cdot2x=2x(x^2+1)^4.$$

The factor $1/5$ cancels the outer derivative factor, and the inner derivative restores $2x$. This also confirms the formula at $x=0$; no division by $x$ was needed, so the zero inner derivative there introduces no domain exclusion.

**Check the substitution at negative and zero inputs.** The map $u=x^2+1$ is not one-to-one on the whole real line, but the proposed antiderivative is a composition whose derivative can be verified at every real $x$. On either side of zero, the usual local substitution gives the same formula, and at zero the direct chain-rule calculation gives derivative $0$, equal to the integrand. No global inverse of $x^2+1$ is required for this indefinite-integral answer. This explains why the result is valid on all of $\mathbb R$, not only for $x>0$.
