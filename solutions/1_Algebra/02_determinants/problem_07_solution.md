# Exercise 7. Using Properties Instead of Recomputing

## The question

Suppose that for a $3\times3$ matrix, $\det A=-4$. Compute
$$\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).$$
Justify each answer using the appropriate property.

## Before calculating: the concepts

For an $n\times n$ matrix, $\det(cA)=c^n\det A$, $\det(A^T)=\det A$, and $\det(AB)=\det A\det B$.

## 1. Distinguish the four operations

The matrix size matters when scaling: multiplying a $3\times3$ matrix by $2$ scales each of its three rows, so it contributes $2^3$, not merely $2$. Transposing and multiplying matrices use different determinant rules.

## 2. Apply the appropriate property to each expression

**Scaling by $2$.** A $3\times3$ matrix has three rows, each scaled by $2$:

$$\det(2A)=2\cdot2\cdot2\det A=8(-4)=\boxed{-32}.$$

**Transpose.** Transposing preserves the determinant:

$$\det(A^T)=\det A=\boxed{-4}.$$

**Square.** Apply the product rule to $A^2=AA$:

$$\det(A^2)=\det A\det A=(-4)(-4)=\boxed{16}.$$

**Negation.** Each of the three rows is scaled by $-1$:

$$\det(-A)=(-1)^3\det A=(-1)(-4)=\boxed{4}.$$

Scaling all entries by a number and multiplying matrices are different operations, so their determinant formulas must not be interchanged.

## 3. Separate scaling from taking a power

The expressions $2A$ and $A^2$ mean different things. In $2A$, entries are scaled and the exponent comes from the size of the matrix. In $A^2=AA$, the product rule gives two factors of $\det A$. Negating a matrix is scaling by $-1$ and therefore also depends on the size.

## 4. Verification

Check the results using identities that undo or combine the operations.

Since $-(-A)=A$, the scaling rule gives $\det(-(-A))=(-1)^3(4)=-4$, recovering the supplied determinant.

Also $(2A)^2=4A^2$. The product rule gives $\det((2A)^2)=(-32)^2=1024$. Independently, the scaling rule gives $\det(4A^2)=4^3\cdot16=64\cdot16=1024$. The agreement checks both the scaling exponent and the square calculation.
