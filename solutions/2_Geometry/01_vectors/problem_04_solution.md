# Exercise 4. Dot Product and Perpendicularity

## The question

For $u=(1,2,-1)$ and $v=(2,-1,3)$ compute $u\cdot v$ and determine whether the vectors are perpendicular. Then find $a$ so that $w=(2,-1,a)$ is perpendicular to $u$, and check the result.

## Before calculating: the perpendicularity test

For nonzero vectors, $u\cdot v=\|u\|\|v\|\cos\theta$. They are perpendicular exactly when their dot product is zero. In coordinates, multiply corresponding components and add.

The coordinate dot product is $u_1v_1+u_2v_2+u_3v_3$. Unlike the cross product, it returns a scalar. Its geometric identity involves both lengths, so the conclusion “zero means a right angle” is applied here to nonzero vectors. A nonzero negative dot product cannot be repaired by taking an absolute value when testing perpendicularity.

## 1. Test the given pair

$$u\cdot v=1\cdot2+2(-1)+(-1)3=2-2-3=\boxed{-3}.$$

It is nonzero, so the vectors are not perpendicular. Its negative sign means the angle between them is obtuse.

## 2. Construct a perpendicular vector

For $w=(2,-1,a)$, the required condition is

$$u\cdot w=1\cdot2+2(-1)+(-1)a=-a=0.$$

Thus $\boxed{a=0}$ and $\boxed{w=(2,-1,0)}$.

The condition determines the third coordinate because the coefficient of $a$ is $-1$, which is nonzero. We are solving a linear condition, not changing the first two prescribed entries.

## 3. Read the perpendicularity condition as a plane

For a variable vector $q=(q_1,q_2,q_3)$,

$$u\cdot q=q_1+2q_2-q_3.$$

Thus all vectors perpendicular to $u$ satisfy one homogeneous linear equation, $q_1+2q_2-q_3=0$. The prescribed first coordinates $q_1=2$, $q_2=-1$ make the first two terms cancel and force $q_3=0$. This explains why there is exactly one allowed $a$.

For the original $v$, the same expression gives $2+2(-1)-3=-3$, matching the direct dot product. The contrast is caused entirely by its third coordinate: the first two contributions already cancel in both cases.

## 4. Interpret the result

The original first two coordinate products already cancel. A nonzero third coordinate of $w$ would introduce an extra term $-a$, so perpendicularity forces it to vanish. All vectors perpendicular to $u$ lie in the plane $x+2y-z=0$ through the origin.

## 5. Verification

$$u\cdot(2,-1,0)=2-2+0=0.$$

Also $w\ne0$, so it has a genuine direction and the zero dot product does describe a right angle. Its coordinates satisfy $2+2(-1)-0=0$, agreeing with the perpendicular plane equation.
