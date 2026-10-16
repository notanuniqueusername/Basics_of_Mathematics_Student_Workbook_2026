# Exercise 12. Recognizing a Surface from Cross-Sections

## The question

A certain surface has the following properties:
- the cross-section $z=0$ is a point,
- for $z>0$, the cross-sections $z=\text{const}$ are circles with increasing radius,
- vertical cross-sections through the $Oz$ axis are parabolas.

Propose a simple equation for such a surface and justify your choice.

## Before calculating: construct rather than uniquely identify

The stated cross-sections suggest a rotationally symmetric surface opening upward. The description does not fix a unique scale, so it is enough to propose one simple equation and check every condition.

The phrase “a simple equation” asks for a valid model, not proof of unique identification. The data specify circular horizontal sections and parabolic meridians but do not assign a radius at any positive height. A positive scale factor is therefore free, and the solution should distinguish what the description forces from what is chosen for simplicity.

## 1. Propose an equation

Choose

$$\boxed{z=x^2+y^2}.$$

At $z=0$, the equation $x^2+y^2=0$ forces $x=y=0$, giving just the origin. At $z=c>0$, the section $x^2+y^2=c$ is a circle of radius $\sqrt c$. Its radius increases strictly with $c$.

## 2. Check every vertical plane through the axis

Such a plane can be parametrized horizontally by $x=r\cos\phi$, $y=r\sin\phi$, with fixed angle $\phi$ and signed coordinate $r$. Substitution gives

$$z=r^2\cos^2\phi+r^2\sin^2\phi=r^2.$$

Thus every vertical plane through the $z$-axis cuts out a parabola, not merely the two coordinate planes.

## 3. Compare the chosen proposal with two plausible alternatives

A circular cone $z^2=x^2+y^2$ also has circular horizontal sections with radius increasing for $z>0$, but its vertical axis sections are pairs of straight lines, not parabolas. It therefore fails the last condition.

A cylinder $x^2+y^2=1$ has circular sections, but its section at $z=0$ is a circle rather than a point, and its radius does not grow. It fails two conditions.

The proposed $z=x^2+y^2$ satisfies all three simultaneously. Checking alternatives explains why each part of the description matters: the point section removes the cylinder, and the parabolic meridians distinguish the paraboloid from the cone. The arbitrary positive coefficient changes scale while preserving these qualitative properties.

## 4. Verification and interpretation

At heights $1,4,9$, the circle radii are $1,2,3$, confirming growth. The coordinate-plane sections are $z=x^2$ and $z=y^2$, both upward parabolas. There are no points at negative heights because a sum of squares cannot be negative.

This is a circular elliptic paraboloid. More generally $z=k(x^2+y^2)$ with any $k>0$ has the same qualitative properties, so the proposal is valid without being uniquely forced by the data.
