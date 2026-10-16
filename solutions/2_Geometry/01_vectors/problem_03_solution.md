# Exercise 3. Vector Normalization

## The question

For $v=(3,4)$ find a unit vector $e$ with the same direction and orientation. Check that $\|e\|=1$, reconstruct $v$ in the form $v=\|v\|e$, and explain what changes during normalization and what remains unchanged.

## Before calculating: normalization

For any nonzero vector $v$, the unit vector in the same direction and orientation is $e=v/\|v\|$. Division uses a positive scalar, so orientation is preserved. The zero vector cannot be normalized because it has no direction and its length is zero.

The norm has the homogeneity property $\|cv\|=|c|\|v\|$. Dividing a nonzero vector by its positive norm therefore gives norm $1$. The absolute value matters when a scalar is negative, because length is always nonnegative even when orientation is reversed. Normalization uses the positive factor $1/\|v\|$ specifically to retain orientation.

## 1. Find the original length

$$\|v\|=\sqrt{3^2+4^2}=\sqrt{25}=5.$$

## 2. Divide every coordinate by the length

$$\boxed{e=\frac15(3,4)=\left(\frac35,\frac45\right)}.$$

The original vector has been shortened by the factor $1/5$. Its coordinate ratio remains $3:4$, so it lies on the same ray from the origin.

## 3. Relate the answer to direction and uniqueness

Any vector with the same direction and orientation as $v$ has the form $cv$ with $c>0$. If it is also a unit vector, then

$$1=\|cv\|=c\|v\|=5c,$$

so $c=1/5$. This proves the chosen unit vector is the only one on the same ray. The opposite unit vector $(-3/5,-4/5)$ has the same length but fails the orientation requirement.

The coordinates of $e$ can also be read as $\cos\theta=3/5$ and $\sin\theta=4/5$ for its direction angle. Their squared sum is $1$, expressing the same normalization condition geometrically.

## 4. Separate length from direction

The representation $v=\|v\|e$ separates a positive scalar length from a unit direction vector. Here $\|v\|=5$ records the size and $e=(3/5,4/5)$ records the direction. Using $-e$ would give the opposite orientation and would not answer the question.

## 5. Verification

Check the defining unit-length condition:

$$\|e\|=\sqrt{\left(\frac35\right)^2+\left(\frac45\right)^2}=\sqrt{\frac9{25}+\frac{16}{25}}=1.$$

Reconstruct the original vector:

$$\|v\|e=5\left(\frac35,\frac45\right)=(3,4)=v.$$

The first check verifies the new length; the second verifies that the direction and scale combine to recover the given vector.
