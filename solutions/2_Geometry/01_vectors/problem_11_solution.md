# Exercise 11. Decomposition into Parallel and Perpendicular Components

## The question

Decompose $u=(3,4)$ into components parallel and perpendicular to $v=(1,2)$. Check
$$u=u_{\parallel}+u_{\perp},\qquad u_{\perp}\cdot v=0.$$
Explain why these are two independent checks of correctness.

## Before calculating: parallel and perpendicular parts

For $v\ne0$, set $u_{\parallel}=\frac{u\cdot v}{v\cdot v}v$ and $u_{\perp}=u-u_{\parallel}$. This produces a decomposition with the first part in the line spanned by $v$ and the second perpendicular to it.

The decomposition has three conditions: the parts sum to $u$, the parallel part belongs to the span of $v$, and the perpendicular part has zero dot product with $v$. Any arbitrary split satisfies the first condition, so the geometric constraints must be verified separately. They also force a unique decomposition for every nonzero target direction.

## 1. Find the parallel part

$$u\cdot v=3+8=11,\qquad v\cdot v=1+4=5.$$

Therefore

$$\boxed{u_{\parallel}=\frac{11}{5}(1,2)=\left(\frac{11}{5},\frac{22}{5}\right)}.$$

## 2. Subtract to obtain the perpendicular part

$$\boxed{u_{\perp}=(3,4)-\left(\frac{11}{5},\frac{22}{5}\right)=\left(\frac45,-\frac25\right)}.$$

The parallel component is visibly a scalar multiple of $v$. The residual points along $(2,-1)$, a direction perpendicular to $(1,2)$.

## 3. Derive the coefficient and prove uniqueness

Write the parallel part as $cv$. Orthogonality of the residual requires

$$(u-cv)\cdot v=u\cdot v-c(v\cdot v)=11-5c=0,$$

hence $c=11/5$. Because $v\cdot v=5\ne0$, there is exactly one solution for $c$. This establishes that the projection formula is forced by the requirements, not just one convenient split.

A useful length check is

$$\|u_{\parallel}\|^2=\frac{121+484}{25}=\frac{121}{5},\qquad\|u_{\perp}\|^2=\frac{16+4}{25}=\frac45.$$

Their sum is $25=3^2+4^2$. The orthogonality makes these squared lengths additive; ordinary lengths would not add to $\|u\|$ in this decomposition.

## 4. Verification and independence of the checks

Check reconstruction:

$$u_{\parallel}+u_{\perp}=\left(\frac{11+4}{5},\frac{22-2}{5}\right)=(3,4)=u.$$

Check orthogonality:

$$u_{\perp}\cdot v=\frac45\cdot1-\frac25\cdot2=0.$$

Reconstruction alone would also hold for the incorrect choice $u_{\parallel}=0$, $u_{\perp}=u$, so it does not prove perpendicularity. Conversely, taking both parts zero would make the purported residual perpendicular but fail reconstruction. Both conditions, together with parallelism of $u_{\parallel}$, are needed. Finally $121/5+4/5=25=\|u\|^2$ checks the orthogonal lengths.

**Check uniqueness geometrically.** If there were two valid parallel components, their difference would be parallel to $v$. Since each corresponding residual is perpendicular to $v$, subtracting those residuals shows that this same difference is perpendicular to $v$ as well. A vector both parallel and perpendicular to a nonzero vector must be zero: if it is $cv$, its dot product with $v$ is $c\|v\|^2$, forcing $c=0$. Therefore both parallel components coincide, and their residuals coincide too. The decomposition is uniquely determined by the stated geometric requirements.
