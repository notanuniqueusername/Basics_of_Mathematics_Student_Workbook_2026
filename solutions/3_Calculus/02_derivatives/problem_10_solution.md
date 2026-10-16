# Problem 10. The Tangent Line as an Application of the Derivative

## The question

For
$$f(x)=x^2-3x+1$$
find the equation of the tangent line at the point with $x=2$. Give the point of tangency, the value $f'(2)$, the equation of the line, and verify that the point lies on the obtained tangent line.

## Before calculating: tangent needs a point and slope

At $x=x_0$, the tangent line is $y-f(x_0)=f'(x_0)(x-x_0)$. The derivative supplies the slope; the function value supplies the height. They are different quantities.

Two conditions determine a nonvertical line uniquely: a point it passes through and a slope. Tangency adds that the slope must equal the graph's derivative at the same horizontal coordinate. Using $f'(2)$ as the point's height or using $f(2)$ as the slope would mix these separate roles and generally produce the wrong line.

## 1. Find the point of tangency

$$f(2)=2^2-3\cdot2+1=4-6+1=-1.$$

Thus the point is $\boxed{(2,-1)}$.

## 2. Find the slope and line

$$f'(x)=2x-3,\qquad\boxed{f'(2)=1}.$$

Therefore

$$y+1=x-2\quad\Longrightarrow\quad\boxed{y=x-3}.$$

The positive slope means the tangent rises from left to right.

## 3. Derive the line from a local horizontal increment

Write $x=2+h$. Direct expansion gives

$$f(2+h)=(2+h)^2-3(2+h)+1=-1+h+h^2.$$

The constant $-1$ is the contact height, the coefficient of $h$ is the slope $1$, and $h^2$ is the nonlinear remainder. Keeping only the first-order terms gives $y=-1+h$. Since $h=x-2$, this becomes $y=x-3$, agreeing with point-slope form.

This also clarifies the meaning of tangency: the graph-minus-line error is $h^2$, so relative to a horizontal change $h$ it tends to zero. Merely passing through $(2,-1)$ would not be enough; infinitely many lines pass through that point with the wrong first-order behavior.

## 4. Verification

At $x=2$, the line gives $y=2-3=-1$, so it contains the correct point.

More strongly, compare the function with the line:

$$f(x)-(x-3)=x^2-4x+4=(x-2)^2.$$

At $x=2+h$ the gap is $h^2$, and the gap divided by $h$ tends to zero. Thus the line has first-order contact with the graph, not merely an intersection. The nonnegative square also shows the parabola stays above its tangent everywhere.
