# Exercise 14. Rotation Matrices

## The question

The matrix of a rotation through an angle $\theta$ is

$$R(\theta)=\begin{pmatrix}\cos\theta&-\sin\theta\\\sin\theta&\cos\theta\end{pmatrix}.$$

Compute $R(\alpha)R(\beta)$, use the angle-sum formulas to show that $R(\alpha)R(\beta)=R(\alpha+\beta)$, and explain the result geometrically.

## Before calculating: what we need

The columns of $R(\theta)$ are the images of the basic vectors (Exercise 5): $e_1=(1,0)$ goes to $(\cos\theta,\sin\theta)$, and $e_2=(0,1)$ goes to $(-\sin\theta,\cos\theta)$. That is exactly a counterclockwise turn by $\theta$. For $\theta=90^\circ$ this gives the matrix $R$ from Exercise 9.

The angle-sum formulas are

$$\cos(\alpha+\beta)=\cos\alpha\cos\beta-\sin\alpha\sin\beta,\qquad \sin(\alpha+\beta)=\sin\alpha\cos\beta+\cos\alpha\sin\beta.$$

## 1. Compute $R(\alpha)R(\beta)$

Rows of $R(\alpha)$ paired with columns of $R(\beta)$:

$$R(\alpha)R(\beta)=\begin{pmatrix}\cos\alpha\cos\beta-\sin\alpha\sin\beta & -\cos\alpha\sin\beta-\sin\alpha\cos\beta\\ \sin\alpha\cos\beta+\cos\alpha\sin\beta & -\sin\alpha\sin\beta+\cos\alpha\cos\beta\end{pmatrix}.$$

## 2. Recognize the angle-sum formulas

Entry by entry:

- $(1,1)$: $\cos\alpha\cos\beta-\sin\alpha\sin\beta=\cos(\alpha+\beta)$.
- $(2,1)$: $\sin\alpha\cos\beta+\cos\alpha\sin\beta=\sin(\alpha+\beta)$.
- $(2,2)$: $\cos\alpha\cos\beta-\sin\alpha\sin\beta=\cos(\alpha+\beta)$.
- $(1,2)$: $-(\cos\alpha\sin\beta+\sin\alpha\cos\beta)=-\sin(\alpha+\beta)$.

Therefore

$$R(\alpha)R(\beta)=\begin{pmatrix}\cos(\alpha+\beta)&-\sin(\alpha+\beta)\\\sin(\alpha+\beta)&\cos(\alpha+\beta)\end{pmatrix}=R(\alpha+\beta).\ \blacksquare$$

## 3. Geometric meaning

A product of matrices is a composition of transformations, read right to left (Exercise 9). So $R(\alpha)R(\beta)$ means "rotate by $\beta$, then rotate by $\alpha$". Turning by $\beta$ and then by $\alpha$ is the same as turning once by $\alpha+\beta$, and the result says exactly that.

This is also the reason the angle-sum formulas exist. Multiplying the two matrices is a way of computing the sine and cosine of a combined angle, and the two formulas appear as the entries of the product.

Two consequences:

- **Rotations commute.** Since $\alpha+\beta=\beta+\alpha$, we get $R(\alpha)R(\beta)=R(\beta)R(\alpha)$. This contrasts with Exercise 9, where $R$ and the nonuniform scaling $S$ did not commute. The difference is that a rotation treats all directions equally, while $S$ favors one.
- **The inverse is the opposite rotation.** $R(\alpha)R(-\alpha)=R(0)=I$, so $R(\theta)^{-1}=R(-\theta)$. Since $\cos(-\theta)=\cos\theta$ and $\sin(-\theta)=-\sin\theta$, this is also $R(\theta)^T$.

## 4. Verification

**Special case: $\alpha=\beta=90^\circ$.** Then $R(90^\circ)=\begin{pmatrix}0&-1\\1&0\end{pmatrix}$ and

$$R(90^\circ)^2=\begin{pmatrix}0&-1\\1&0\end{pmatrix}\begin{pmatrix}0&-1\\1&0\end{pmatrix}=\begin{pmatrix}-1&0\\0&-1\end{pmatrix}=R(180^\circ).\ ✓$$

**Special case: $\alpha=30^\circ$, $\beta=60^\circ$.** Using $\cos30^\circ=\tfrac{\sqrt3}{2}$, $\sin30^\circ=\tfrac12$, $\cos60^\circ=\tfrac12$, $\sin60^\circ=\tfrac{\sqrt3}{2}$:

$$(1,1):\ \tfrac{\sqrt3}{2}\cdot\tfrac12-\tfrac12\cdot\tfrac{\sqrt3}{2}=0,\qquad (2,1):\ \tfrac12\cdot\tfrac12+\tfrac{\sqrt3}{2}\cdot\tfrac{\sqrt3}{2}=\tfrac14+\tfrac34=1.$$

The first column is $(0,1)$, which is the first column of $R(90^\circ)$, as expected since $30^\circ+60^\circ=90^\circ$. ✓

**Determinant check.** $\det R(\theta)=\cos^2\theta+\sin^2\theta=1$, so $\det\big(R(\alpha)R(\beta)\big)=1\cdot1=1$. The product has the form of a rotation matrix, whose determinant is also $1$. ✓

**Length check.** The columns of $R(\theta)$ are $(\cos\theta,\sin\theta)$ and $(-\sin\theta,\cos\theta)$.

- Each has length $\sqrt{\cos^2\theta+\sin^2\theta}=1$.
- They are perpendicular: $\cos\theta\cdot(-\sin\theta)+\sin\theta\cdot\cos\theta=0$.

Unit length alone would not be enough, since two unit columns could still point in non-perpendicular directions. Together, the two facts give $R(\theta)^TR(\theta)=I$. Therefore, for any vector $x$,

$$\|R(\theta)x\|^2=x^TR(\theta)^TR(\theta)x=x^Tx=\|x\|^2.$$

So a rotation preserves lengths, and so does the product $R(\alpha)R(\beta)$, which agrees with $R(\alpha+\beta)$ being a rotation. ✓
