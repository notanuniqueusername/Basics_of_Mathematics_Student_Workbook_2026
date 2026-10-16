# Problem 5. Distance from Velocity

## The question

The velocity of a car during the first five seconds is described by the function
$$
v(t)=4t+2\quad [\mathrm{m/s}].
$$

Compute the distance traveled and explain why the integral of velocity gives the change in position.

Then answer what would have to be changed in the reasoning if the velocity also took negative values.

## Before calculating: integrate a rate over time

Velocity is position change per unit time. Summing small contributions $v(t)\,dt$ gives displacement. Actual distance integrates speed $|v|$, so sign must be checked before equating the two quantities.

A velocity integral returns displacement whether or not the velocity changes sign. It equals distance only after checking that velocity is nonnegative throughout the interval. The variable's time unit must also match the rate unit: integrating a meters-per-second rate over minutes without conversion would give an incorrect numerical result even with correct calculus.

## 1. Check the velocity sign

For $0\le t\le5$, $v(t)=4t+2\ge2>0$. There is no reversal of direction, and speed equals velocity throughout the interval.

## 2. Compute the distance

$$D=\int_0^5(4t+2)\,dt=\left[2t^2+2t\right]_0^5=50+10=\boxed{60\ \mathrm m}.$$

The units are $(\mathrm{m/s})\cdot\mathrm s=\mathrm m$. The same integral is the displacement because the car never travels backward.

## 3. Connect the accumulation to a position function

An antiderivative of velocity is $s(t)=2t^2+2t+C$. The unknown constant represents the car's initial position, which is not supplied and is unnecessary for traveled distance here.

The displacement is

$$s(5)-s(0)=(50+10+C)-C=60,$$

so the initial position cancels. This explains why a rate history determines position change without determining absolute location.

The endpoint-speed average is $12$ m/s, and multiplying by $5$ seconds gives $60$ m. That arithmetic average is exact because velocity is linear; it would not generally replace integration for a nonlinear rate. If the velocity changed sign, the same antiderivative difference would still be displacement, while distance would require the absolute-value construction described in the solution.

## 4. Explain the negative-velocity case

If velocity took negative values, $\int v$ would still give signed displacement. To find total distance one would locate the sign-changing times, split the interval, and integrate $|v|$, negating the negative-velocity pieces. Opposite-direction travel cancels in displacement but adds in distance.

## 5. Verification

The graph of $v$ is a straight line with endpoint values $v(0)=2$ and $v(5)=22$. Its area is the trapezoid

$$\frac{2+22}{2}\cdot5=12\cdot5=60\ \mathrm m.$$

Differentiating the accumulated-position expression $2t^2+2t$ gives $4t+2$, checking the antiderivative independently.
