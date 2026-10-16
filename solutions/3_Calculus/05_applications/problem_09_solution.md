# Problem 9. Minimizing the Material Used for a Can

## The question

A closed cylinder has fixed volume $V$.

1. Write the volume constraint.
2. Eliminate one of the variables.
3. Express the surface area as a function of the radius $r$.
4. Find the relation between the height $h$ and the radius $r$ for which the material usage is minimal.

Interpret the obtained relation geometrically.

## Before calculating: include both end disks

Assume fixed volume $V>0$. Let radius $r>0$ and height $h>0$ be measured in consistent length units. A closed cylinder has surface area $S=2\pi r^2+2\pi rh$, including the top and bottom, unlike an open container.

The objective is surface area because uniform material thickness and cost per unit area make material usage proportional to it. The volume is fixed, so changing radius forces a compensating height change. Both variables must stay positive, and the closed-can condition requires two circular disks in addition to the curved side area.

## 1. Eliminate the height

The volume constraint is $\boxed{\pi r^2h=V}$, hence $h=V/(\pi r^2)$. Substitution gives

$$\boxed{S(r)=2\pi r^2+\frac{2V}{r},\quad r>0}.$$

## 2. Find the minimizing dimensions

$$S'(r)=4\pi r-\frac{2V}{r^2}=0\Longrightarrow4\pi r^3=2V.$$

Thus

$$r_* =\left(\frac{V}{2\pi}\right)^{1/3},\qquad h_* =\frac{V}{\pi r_*^2}=2r_*.$$

The requested relation is $\boxed{h=2r}$: the height equals the base diameter.

## 3. Explain the balance at the minimizing dimensions

The area derivative has two competing terms: $4\pi r$ is the increasing disk-area contribution, while $-2V/r^2$ is the decreasing lateral-area contribution after height has been eliminated. At the optimum their magnitudes balance.

Using $V=\pi r^2h$ in the critical equation $4\pi r=2V/r^2$ gives

$$4\pi r=2\pi h\quad\Longrightarrow\quad h=2r.$$

This derives the height-to-diameter relation directly without first computing the radius. It also gives an area check: when $h=2r$, the curved side area is $4\pi r^2$, twice the combined disk area $2\pi r^2$.

The relation is independent of the fixed volume, while the actual scale $r=(V/(2\pi))^{1/3}$ changes with it. Doubling every length multiplies volume by eight, consistently with that cube-root dependence.

## 4. Verify the minimum globally

$$S''(r)=4\pi+\frac{4V}{r^3}>0\qquad(r>0).$$

The objective is strictly convex, so the critical point is its unique minimum. Also $S\to\infty$ as $r\to0^+$ and as $r\to\infty$, ruling out an unexamined boundary improvement.

At the proposed dimensions, the volume is $\pi r_*^2(2r_*)=2\pi r_*^3=V$, checking the constraint. The resulting minimum area is $6\pi r_*^2$, with the correct squared-length units. The relation depends on the cylinder being closed; excluding a disk would change the objective and optimum.
