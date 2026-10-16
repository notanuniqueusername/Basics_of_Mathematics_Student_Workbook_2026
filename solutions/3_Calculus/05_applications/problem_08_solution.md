# Problem 8. Number of Requests Handled by a Server

## The question

The rate at which requests arrive at a server during the first 5 minutes is described by the function
$$
r(t)=100+20t\quad [\text{requests/min}],\qquad 0\le t\le5.
$$

1. Compute the total number of requests that arrived during this time.
2. Compute the average rate of incoming requests over this interval.
3. Compare the average rate with the values $r(0)$ and $r(5)$.

## Before calculating: distinguish rate from accumulated count

The rate is measured in requests per minute, with $t$ in minutes. Integrating over five minutes gives a request count; dividing that count by the elapsed time gives the average rate. The problem specifies arrivals, so the calculation counts incoming requests rather than assuming a separate service capacity.

An arrival rate is a flow per unit time, not a running total. Integration accumulates that flow and increases the units from requests per minute to requests. The title's wording about handled requests does not provide a processing-capacity model; the supplied function explicitly describes arrivals, so the defensible total is the number arriving during the interval.

## 1. Compute total arrivals

$$R=\int_0^5(100+20t)\,dt=\left[100t+10t^2\right]_0^5=500+250.$$

Thus $\boxed{R=750\text{ requests}}$ within the continuous-rate model.

## 2. Compute and compare the average rate

$$\boxed{\bar r=\frac{750}{5}=150\text{ requests/min}}.$$

The endpoint rates are $r(0)=100$ and $r(5)=200$ requests/min. Their arithmetic mean is $(100+200)/2=150$, equal to the integral average because the rate is linear in time.

## 3. Build and check the cumulative-arrival function

Define $R(t)=\int_0^tr(u)\,du$. Then

$$R(t)=100t+10t^2,\qquad R(0)=0,\qquad R'(t)=100+20t=r(t).$$

At $t=5$, this gives the total $750$ arrivals. Its slope starts at $100$ and rises to $200$ requests/min, reflecting the increasing input rate rather than a constant accumulation slope.

The average arrival rate $150$ is attained at $t=2.5$, since $100+20(2.5)=150$. This midpoint equality is specific to a linear rate. The total's decomposition into $500$ baseline arrivals and $250$ extra arrivals corresponds exactly to the rectangle-plus-triangle rate-graph areas, giving both an algebraic and geometric check of the accumulation model.

## 4. Verification

The area under the rate graph is a rectangle plus triangle:

$$100\cdot5+\frac12\cdot5\cdot(200-100)=500+250=750.$$

Also $100\le r(t)\le200$, so total arrivals must lie between $500$ and $1000$, and average rate between $100$ and $200$. Both answers satisfy those bounds. The units check is $(\text{requests/min})\cdot\text{min}=\text{requests}$, while dividing the total by $5$ min restores the rate units.
