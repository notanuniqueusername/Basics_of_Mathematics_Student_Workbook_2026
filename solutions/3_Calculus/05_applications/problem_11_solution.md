# Problem 11. Volume of a Solid of Revolution

## The question

The region under the graph
$$
y=\sqrt{x},\qquad x\in[0,4],
$$
is rotated about the $x$-axis.

1. Construct the integral describing the volume using the disk method.
2. Compute the volume.
3. Explain where the factor $\pi y^2$ in the integral comes from.

## Before calculating: construct the cross-sectional area

Rotating the vertical segment from $y=0$ to $y=\sqrt x$ about the $x$-axis creates a solid disk of radius $\sqrt x$. There is no inner hole, so the cross-section is a disk rather than a washer.

A solid of revolution is built from two-dimensional cross-sectional areas multiplied by thin axial widths. Squaring the radius changes the length unit to area, and multiplying by $dx$ gives volume. Keeping this dimensional sequence explicit prevents using circumference or the original curve height in place of the disk area.

## 1. Set up the disk integral

At coordinate $x$, disk area is

$$A(x)=\pi(\text{radius})^2=\pi(\sqrt x)^2=\pi x.$$

A thin slice of thickness $dx$ therefore has volume approximately $\pi x\,dx$. Summing the slices gives

$$\boxed{V=\int_0^4\pi x\,dx}.$$

## 2. Evaluate

$$V=\pi\left[\frac{x^2}{2}\right]_0^4=\pi\frac{16}{2}=\boxed{8\pi\text{ cubic units}}.$$

The factor $\pi y^2$ is the actual disk area, not the circumference $2\pi y$; circumference would have the wrong dimensions for a volume slice.

## 3. Explain how the region determines the disks

For each $x\in[0,4]$, the original planar region contains every height $0\le y\le\sqrt x$. Rotating that whole vertical segment sweeps every radius from zero to $\sqrt x$, filling a disk. Rotating only its top endpoint would trace a circle rather than fill the solid cross-section.

The radius varies as $\sqrt x$, but its squared value is $x$, making the cross-sectional area linear: $A(x)=\pi x$. This is why the exact volume equals interval length $4$ times average disk area $2\pi$.

The construction also explains the shell check's width: at fixed height $y$, the region runs from the inverse curve $x=y^2$ to the right boundary $x=4$. The two integration directions describe the same solid, providing a meaningful geometric cross-check rather than just a second antiderivative evaluation.

## 4. Verification

The final disk radius is $\sqrt4=2$, giving area $4\pi$. Since disk area grows linearly from $0$ to $4\pi$ over length $4$, its average is $2\pi$, so volume is $2\pi\cdot4=8\pi$.

An independent shell calculation uses horizontal strips: at height $y\in[0,2]$, the region runs from $x=y^2$ to $x=4$. Thus

$$V=2\pi\int_0^2y(4-y^2)\,dy=2\pi[2y^2-y^4/4]_0^2=8\pi,$$

agreeing with the disk construction.
