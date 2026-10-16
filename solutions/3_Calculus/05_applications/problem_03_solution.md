# Problem 3. A Box Made from Cardboard

## The question

From a $30\text{ cm}\times40\text{ cm}$ sheet, squares of side length $x$ are cut from the corners and the edges are folded up to form an open box.

Write the volume as a function of $x$, determine the physically meaningful domain, and find the value of $x$ for which the volume is greatest.

## Before calculating: model all three dimensions

Cutting out squares of side $x$ cm leaves base dimensions $30-2x$ and $40-2x$, and creates height $x$. Each of these must be positive for an actual box.

The two reductions of each base dimension come from cutting a square at both ends of that side. Forgetting one of those cuts changes the model before calculus begins. A root of the volume derivative is only a candidate; it must lie in the geometric domain and be compared with the remaining admissible behavior.

## 1. Build the volume and physical domain

$$\boxed{V(x)=x(30-2x)(40-2x)=1200x-140x^2+4x^3\ \mathrm{cm}^3},$$

$$\boxed{0<x<15\ \mathrm{cm}}.$$

The shorter original side supplies the tighter upper bound. At either boundary the limiting box is degenerate and has zero volume.

## 2. Differentiate and select the admissible root

$$V'(x)=1200-280x+12x^2=4(3x^2-70x+300).$$

Solve the quadratic:

$$x=\frac{70\pm\sqrt{4900-3600}}6=\frac{35\pm5\sqrt{13}}3.$$

The larger root exceeds $15$ and is not physically admissible. The candidate is

$$\boxed{x_* =\frac{35-5\sqrt{13}}3\approx5.6574\ \mathrm{cm}}.$$

The resulting base dimensions are approximately $18.6852$ cm and $28.6852$ cm, with volume approximately $3032.30\ \mathrm{cm}^3$.

## 3. Check the rejected root and the positive dimensions

The second root is $(35+5\sqrt{13})/3\approx17.676$, which exceeds the upper domain bound $15$. It would make $30-2x$ negative, so it cannot describe any folded box. Rejecting it is a modeling decision, not an algebraic error in solving the quadratic.

At the admissible root, $x_*\approx5.6574$ is positive and below $15$. The base sides are both positive, and the volume's units are $\mathrm{cm}\cdot\mathrm{cm}\cdot\mathrm{cm}=\mathrm{cm}^3$.

For a numerical comparison, cuts $x=5$ and $x=6$ give volumes $5\cdot20\cdot30=3000$ and $6\cdot18\cdot28=3024$ cubic centimeters, both below the proved optimum near $3032.30$. These checks support the physical interpretation without replacing the derivative-sign proof of global maximality.

## 4. Verification of global maximality

The upward quadratic $V'$ is positive before its smaller root and negative between its roots. Thus within $(0,15)$ the volume increases up to $x_*$ and decreases afterward. The zero-volume endpoint limits confirm it is the global maximum.

Also $V''(x_*)=-280+24x_*=-40\sqrt{13}<0$, checking the local character. Substituting the proposed dimensions into $x(30-2x)(40-2x)$ gives the stated positive volume. The second algebraic root must be rejected by the geometric domain, even though it solves the derivative equation.
