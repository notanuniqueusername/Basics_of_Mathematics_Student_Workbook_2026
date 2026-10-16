# Problem 10. A Cable Through Water and Land

## The question

Point $A$ lies on one bank of a river of width $100$ m, and point $B$ lies on the other bank, $500$ m along the bank from the point directly opposite $A$.

The cost per meter of cable underwater is twice the cost per meter of cable on land.

Build a cost function depending on the point where the cable comes out of the water, determine the domain, and find the solution that minimizes the cost.

## Before calculating: choose a landing coordinate and cost unit

Place $A=(0,0)$, the opposite bank at vertical coordinate $100$, and $B=(500,100)$ in meters. Let $X=(x,100)$ be where the underwater segment ends. Assume a straight underwater segment followed by travel along the bank. Let land cost be $c>0$ per meter, so underwater cost is $2c$ per meter.

Cost is a weighted sum of lengths, not the total path length alone. The underwater segment must be computed by the Pythagorean theorem because its horizontal displacement varies with the landing point. Its cost multiplier is twice the land multiplier, which changes the optimum away from a pure shortest-route construction.

## 1. Build the objective and domain

For $0\le x\le500$, underwater length is $\sqrt{100^2+x^2}$ and land length is $500-x$:

$$\boxed{C(x)=c\left(2\sqrt{10000+x^2}+500-x\right)}.$$

Landing outside this interval cannot improve the cost: $x<0$ lengthens both water and land compared with $x=0$, while $x>500$ lengthens both compared with $x=500$. Thus the stated domain loses no optimal route in this model.

## 2. Optimize

$$\frac{C'(x)}c=\frac{2x}{\sqrt{10000+x^2}}-1.$$

Setting it to zero gives $2x=\sqrt{10000+x^2}$ and, since $x\ge0$,

$$4x^2=10000+x^2\Longrightarrow\boxed{x_* =\frac{100}{\sqrt3}\approx57.735\ \mathrm m}.$$

The water length is $200/\sqrt3\approx115.470$ m; the land length is $500-100/\sqrt3\approx442.265$ m. Minimum cost is $\boxed{c(500+100\sqrt3)}$.

## 3. Interpret the critical equation as a marginal-cost balance

Increasing the landing coordinate by a small amount shortens the land route at rate $1$ meter per meter. It lengthens the underwater route at rate $x/\sqrt{10000+x^2}$, and that increase costs twice as much per meter. The derivative equation

$$2\frac{x}{\sqrt{10000+x^2}}=1$$

balances the added underwater cost against the saved land cost.

At the optimum the horizontal displacement is half the underwater segment length. If $\theta$ is the underwater segment's angle from the bank normal, then $\sin\theta=x/\sqrt{10000+x^2}=1/2$, so $\theta=30^\circ$. This angle gives a geometric interpretation of the weight ratio. The numerical landing distance then follows from the fixed river width, rather than from a guessed fraction of the $500$-meter bank distance.

## 4. Verification

$$\frac{C''(x)}c=\frac{20000}{(10000+x^2)^{3/2}}>0,$$

so the critical point is the unique global minimum. Its cost is approximately $673.205c$, below $C(0)=700c$ and $C(500)=200\sqrt{26}\,c\approx1019.804c$. Substituting $x_*$ into $2x/\sqrt{10000+x^2}$ gives exactly $1$, checking the unsquared derivative equation and excluding any spurious root from squaring.
