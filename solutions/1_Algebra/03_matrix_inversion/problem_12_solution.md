# Exercise 12. Finding Inverses Without Starting from Scratch

## The question

It is known that
$$A^{-1}=\begin{pmatrix}2&-1\\-3&2\end{pmatrix}.$$
Without finding $A$, compute $(3A)^{-1}$, $(A^T)^{-1}$, and $(A^2)^{-1}$. Justify each result using the appropriate property.

## Before calculating: the concepts

Put $C=A^{-1}$. Then $(cA)^{-1}=C/c$ for $c\ne0$, $(A^T)^{-1}=C^T$, and $(A^2)^{-1}=C^2$.

## 1. Use the known inverse as the starting point

Write $C=\begin{pmatrix}2&-1\\-3&2\end{pmatrix}$. All three requested expressions can be computed directly from $C$. For scalar multiplication divide $C$ by $3$; for transpose interchange its rows and columns; for the square multiply $C$ by itself.

## 2. Apply the three inverse identities

Write $C=A^{-1}=\begin{pmatrix}2&-1\\-3&2\end{pmatrix}$.

For scalar multiplication, divide every entry of $C$ by $3$:

$$\boxed{(3A)^{-1}=\frac13C=\begin{pmatrix}2/3&-1/3\\-1&2/3\end{pmatrix}}.$$

For transpose, turn rows of $C$ into columns:

$$\boxed{(A^T)^{-1}=C^T=\begin{pmatrix}2&-3\\-1&2\end{pmatrix}}.$$

For the square, use $(AA)^{-1}=A^{-1}A^{-1}=C^2$:

$$C^2=\begin{pmatrix}2\cdot2+(-1)(-3)&2(-1)+(-1)2\\(-3)2+2(-3)&(-3)(-1)+2\cdot2\end{pmatrix}=\boxed{\begin{pmatrix}7&-4\\-12&7\end{pmatrix}}.$$

No computation of $A$ itself is needed.

## 3. Explain the order in the transpose identity

Since $C=A^{-1}$, we know $AC=CA=I$. Transposing the identity $CA=I$ reverses the factor order:

$$(CA)^T=A^TC^T=I.$$

Similarly, transposing $AC=I$ gives $C^TA^T=I$. Thus $C^T$ is the two-sided inverse of $A^T$, which justifies $(A^T)^{-1}=C^T$.

For the square, the product-inverse rule also reverses order, but both factors are the same matrix: $(AA)^{-1}=A^{-1}A^{-1}=C^2$. No visible rearrangement remains. This explains why the transpose calculation needs an order argument even though squaring the known inverse looks like an ordinary repeated product. The verification below checks all three identities without finding $A$.

## 4. Verification

Each candidate satisfies its inverse identity using only $AC=CA=I$:

$$(3A)(C/3)=AC=I,\qquad (C/3)(3A)=CA=I.$$

For transpose, the order reverses when transposing a product:

$$A^TC^T=(CA)^T=I,\qquad C^TA^T=(AC)^T=I.$$

For the square, associativity and adjacent cancellations give

$$A^2C^2=A(AC)C=I,\qquad C^2A^2=C(CA)A=I.$$

As an arithmetic check, $\det C=4-3=1$ and the computed $C^2$ has determinant $49-48=1=(\det C)^2$.
