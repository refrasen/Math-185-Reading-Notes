# Math 185 Midterm II Review Sheet

## Preliminaries

##### chain rule in multivariable calculus

have a function $f(x_1(t_1, . . ., t_n), . . ., x_m(t_1, . . ., t_n))$ 

$\frac{\partial f}{\partial t_j} = \frac{\partial f}{\partial x_1}\frac{\partial x_1}{\partial t_j} + . . . +\frac{\partial f}{\partial x_m}\frac{\partial x_n}{\partial t_j}$ 

##### connected set: cannot be partitioned into two nonempty open subsets

##### analytic functions are harmonic

##### a function that has both real and imaginary parts harmonic is harmonic

##### harmonic conjugate $v$ for $u$: $u$ is harmonic, $v$ is harmonic, $u+iv$ is analytic

##### switching order of differentiation, integration: kosher for continuously differentiable functions (smooth)

* for $\frac{\partial^2 h}{\partial x \partial y} = \frac{\partial ^2 h}{\partial y \partial x}$
* requires the above to be continuous
* so for our purposes with the differential $Pdx + Qdy$, we required $P, Q$ to be continuously differentiable

## Chapter 3: Line Integrals and Harmonic Functions

### 1. Line Integrals and Green's Theorem

#### path definition

A path in the plane from A to B is a continuous function $t \mapsto \gamma(t)$ on some parameter interval $a \leq t \leq b$ such that $\gamma(a) = A$ and $\gamma(b) = B$. 

#### simple path definition (no intersections)

The path is simple if $\gamma(s) \neq \gamma(t)$ when $s \neq t$ 

closed path definition

The pat is closed if it starts and ends at the same point, i.e., $\gamma(a) = \gamma(b)$ 

#### simple closed path definition

closed path $\gamma$ s.t. $\gamma(s) \neq \gamma(t)$ for $a\leq s< t < b$ 

#### re-parametrization of $\gamma$ 

If $\phi(s), \alpha \leq s \leq \beta$ is a strictly increasing function satisfying $\phi(\alpha) = a$ and $\phi(\beta) = b$, then the composition $\gamma(\phi(s))$ is also a path from $A$ to $B$ 

#### trace of the path $\gamma$ 

is its image $\gamma([a,b])$ which is a subset of the plane

For now we can denote the trace of a path also by $\gamma$

Soon, we'll need to be careful about this

#### smooth path definition

a path that can be represented in the form $\gamma(t) = (x(t), y(t)), a \leq t\leq b$, where the functions $x(t), y(t)$ are smooth, that is, have as many derivatives as is necessary for whatever is being asserted to be true

#### piecewise smooth path definition

a concatenation of smooth paths

#### curve definition

usually mean a smooth or piecewise smooth path

definition of line integral of $Pdx + Qdy$ 

Let $\gamma$ be a path in the plane from $A$ to $B$, and let $P(x,y)$ and $Q(x,y)$ be continuous complex-valued functions on $\gamma$ 

(1.3) $\int_\gamma Pdx + Qdy = \int_a^b P(x(t), y(t))\frac{dx}{dt}dt + \int_a^b Q(x(t), y(t))\frac{dy}{dt}dt$ 

If we have $\gamma = \gamma_1 + . . . + \gamma_n$

$\int_{\gamma}Pdx + Qdy = \int_{\gamma_1}Pdx + Qdy + . . . + \int_{\gamma_n}Pdx + Qdy$

#### Green's Theorem

$D$: bounded domain

$\partial D$: boundary of $D$ that has finite number of disjoint piecewise smooth closed curves

$P, Q$: continuously differentiable on $D \cup \partial D$ 

$\int_{\partial D} P \, dx \; + \; Q\, dy = \int\int_D(\frac{\partial Q}{\partial x}\; - \; \frac{\partial P}{\partial y})\,dx\,dy$

### 2. Independence of Path

#### Fundamental Theorem of Calculus

1. $F(t)$ is an antiderivative of $f(t)$ $\equiv$ $F'(t) = f(t)$ $\implies$ $\int_{a}^b f(t)dt = F(b) - F(a)$ 
   1. $f$ need not be continuous, just Riemann integrable on $[a,b]$ 
2. if $f(t)$ is continuous on $[a,b]$, then $F(t) = \int_a^t f(s)ds$, $a \leq t \leq b$ is an antiderivative for $f(t)$ and if $G(t)$ is another antiderivative for $f(t)$, then $G(t) = F(t) +C$ 

#### Differential $dh$ of a continuously differentiable complex-valued function $h(x,y)$ 

$dh = \frac{\partial h}{\partial x}dx + \frac{\partial h}{\partial y}dy$

#### Exact differential:

The differential $P dx + Qdy $ is exact if $Pdx + Qdy = dh$ for some function $h$ 

#### Analogous FTC for Line Integrals

If

$\gamma$: piecewise smooth curve from $A$ to $B$ 

$h(x,y)$: continuously differentiable on $\gamma$ 

$\implies$ $\int_{\gamma} dh = h(B) - h(A)$ 

#### Independent of Path definition

$P, Q$: continuous complex valued functions on a domain $D$

$\int Pdx + Qdy$ is independent of path in $D$:

for any two points $A$, $B$ of $D$ 

for any $\gamma$ that is a path in $D$ from $A$ to $B$, $\int_{\gamma}Pdx + Qdy$ is the same.

$\equiv$ $\int_{\gamma} Pdx + Qdy = 0$ whenever $\gamma$ is closed in $D$ 

#### Independent of path $\equiv$ exact

Trick: can define any function $h(B) = \int_A^B Pdx + Qdy$, $B \in D$ and $A$ is fixed in $D$ 

#### Closed Differential Definition: $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$ ($P, Q$ are continuously differentiable and complex-valued)

differential is exact $\implies$ differential is closed

$\exists$ a function $h$, s.t. $dh = Pdx + Qdy$ $\implies$ $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$ 

#### on a star-shaped domain: closed $\equiv$ independent of path $\equiv$ exact

#### Continuously deformed only applies to closed differentials

* the two paths $\gamma_0, \gamma_1$ must be both in $D$
  * if not closed paths: must start at same point A and end at same point B
  * paths $\gamma_s(t)$, $a \leq t \leq b$ 
    * go from $A$ to $B$
    * depend continuously on $s$
    * so $\gamma(s,t)$ is continuous in $s$ and $\gamma(0, t) = \gamma_0(t)$, $\gamma(1, t) = \gamma_1(t)$ 
  * if closed: starting/ending point can be moved

### 3. Harmonic Conjugates

#### if $u(x,y)$ is harmonic $\implies$ $-\frac{\partial u}{\partial y} dx \; + \; \frac{\partial u}{\partial x} dy$ is closed

#### on a star-shaped domain $D$ : $-\frac{\partial u}{\partial y} dx \; + \; \frac{\partial u}{\partial x} dy$ is exact, and a harmonic conjugate for $u(x,y)$, $v(x,y)$ exists on $D$ 

#### this harmonic conjugate $v(B) = \int_A^B -\frac{\partial u}{\partial y} dx \; + \; \frac{\partial u}{\partial x} dy$ , is unique up to an additive constant, $A$ is fixed, $B$ is any point in $D$, and this is exact, independent of path, and closed

### 4. The Mean Value Property: only applies to continuous real-valued functions in this section

#### Big Takeaway: harmonic functions have the mean value property which means for any point $z_0$ in $D$, the average value of the function on any small disk centered on $z_0$ is the value of the function at $z_0$ 

##### $\rho > 0$ is the radius of a circle centered on $z_0$ that is contained in $D$, $h(z)$ is a continuous real-valued function on $D$, and so the Average value of $h(z)$ on a circle of radius $r$ centered on $z_0$: $A(r) = \int_0^{2\pi} h(z_0 + re^{i\theta}) d\theta/2\pi$, $r < \rho$ 

##### $u(z)$ is harmonic function on $D$, $|z-z_0| < \rho$ is in $D$ $\implies$ $u(z_0) = \int_0^{2\pi} u(z_0 + re^{i\theta})\frac{d\theta}{2\pi}, 0 < r <\ rho$ 

Note: the proof for this required using

1. harmonic functions are closed
2. green's theorem on the boundary of the circle
3. parameterizing $u$ with $x = x_0 + r\cos \theta$ and y similarly
4. recognizing chain rule
5. switching the order of integration and derivation

### 5. The Maximum Principle

##### Strict maximum principle: if a real valued harmonic function attains its maximum on a domain $D$, then it is constant

##### complex-valued harmonic functions: if they attain their maximum modulus on $D$, then they are constant on $D$ 

##### Maximum Principle: complex-valued harmonic functions on a bounded domain $D$ that extend continuously to the boundary of $D$ must attain their maximum on the boundary. In other words, if the function is bounded in modulus on the boundary, it is bounded by the same upper bound in the region

## Chapter 4 Complex Integration and Analyticity

### 1. Complex Line Integrals

#### $dz = dx + idy$ 

#### $\int_{\gamma} h(z) dz = \int_{\gamma}h(z) dx + i \int_{\gamma}h(z)dy$ 

#### Reminder: parameterize curves $\gamma(t) = z(t) = x(t) + iy(t) \equiv (x(t), y(t))$

##### $\frac{dz}{dt} = x'(t) + iy'(t) \equiv dz = x'(t)dt + iy'(t)dt$

##### or $ \gamma(\theta) = z(\theta) \implies dz = \frac{dz}{d\theta} d\theta$

#### $|dz| = ds = \sqrt{(dx)^2 + (dy)^2}$ 

##### $L$: length of $\gamma$, $L = \int_{\gamma}|dz| = \int_a^b \sqrt{(dx/dt)^2 + (dy/dt)^2}dt$

#### Triangle inequality for integrals, ML-estimate

Suppose $\gamma$ is a piecewise smooth curve. If $h(z)$ is a continuous function on $\gamma$, then

##### (1.6) $|\int_\gamma h(z)dz| \leq \int_\gamma |h(z)||dz|$ 

Further, if $\gamma$ has length $L$ and $|h(z)| \leq M$ on $\gamma$, then

##### (1.7) $|\int_\gamma h(z)dz| \leq ML$ 

##### Sharp estimate: when equality holds 

### 2. Fundamental Theorem of Calculus for Analytic Functions

#### $f(z)$ is continuous on a domain $D$ and has a complex primitive on a domain $D$ if there is a function $F(z)$ on $D$ that is analytic and $F'(z) = f(z)$ 

#### Part 1 of the FTC for Analytic Functions: $f(z)$ is continuous, $F(z)$ is a primitive for $f(z)$ $\implies$ $\int_A^B f(z) dz = F(B) - F(A)$

##### can be taken along any path in $D$ from $A$ to $B$ 

#### Part 2 of the FTC for Analytic Functions: if $D$ is a <u>star-shaped</u> domain and $f(z)$ is analytic on $D$, then $f(z)$ as a primitive on $D$, and the primitive is unique up to adding a constant. The primitive is given by $F(z) = \int_{z_0}^z f(\zeta)d\theta $, $z \in D$ 

##### Integrals of analytic function in star-shaped domains are independent of path: the differential $f(z)dz$ is exact and independent of path, because $\frac{dF}{dz} = f(z)$ for some function $F$ 

### 3. Cauchy's Theorem

#### $f(z)dz$ closed is equivalent to $f(z)$ being analytic

#### $D$ bounded domain with piecewise smooth boundary and $f(z)$ an analytic function on $D$ that extends smoothly to $\partial D$ $\implies$ $\int_{\partial D} f(z)dz = 0$ 

### 4. The Cauchy Integral Formula

#### Cauchy Integral Formula Theorem: $D$ bounded domain with piecewise smooth boundary, $f(z)$ is analytic on $D$, and $f(z)$ extends smoothly to the boundary of $D$ $\implies$ $f(z) = \frac{1}{2\pi i}\int_{\partial D}\frac{f(w)}{w-z}dw, \; z \in D$ 

##### Also, $f(z)$ has complex derivatives of all orders on $D$  $f^{(m)}(z) = \frac{m!}{2\pi i} \int_{\partial D}\frac{f(w)}{(w-z)^{m+1}}dw, z \in D, m\geq 0$

##### Note: Green's theorem says that $P, Q$ are continuously differentiable on $D$ AND $\partial D$ 

##### So $f(z)$ analytic on $D$ is infinitely differentiable with each complex derivative being analytic on $D$ 

### 5. Liouville's Theorem

#### Cauchy Estimates

Suppose $f(z)$ is analytic for $|z-z_0| \leq \rho$  $\equiv$ $f(z)$ is analytic on the closed disk with center $z_0$, radius $\rho$ 

If $|f(z)| \leq M$ for $|z-z_0| = \rho$, then:

$|f^{(m)}(z_0)| \leq \frac{m!}{\rho^m}M$, $m \geq 0$ 

Note:

* this is derived using the Cauchy Integral Formula, parameterizing the boundary circle, and using the triangle inequality

* invariant with translations, scales as expected with $M$ and $1/\rho^m$ 

#### entire function: a function that is analytic on the entire complex plane

#### Liouville's Theorem: A bounded entire function is constant

if $f(z)$ is entire and bounded, then $f(z)$ is constant 

because $|f'(z_0)| \leq M/\rho$, and as $\rho \rightarrow \infin$, since $f(z)$ is analytic on any disk, $|f'(z_0)| \rightarrow 0$, so $f'(z_0) = 0$, 

### 6. Morera's Theorem

#### if $f(z)$ is continuous on a domain $D$ and $\int_{\partial R} f(z)dz$ $= 0$ for every closed rectangle $R \sub D$ with sides parallel to the coordinate axes, then $f(z)$ is analytic on $D$ 

* Related to Cauchy's Theorem:
* $f(z)dz $ closed $\equiv$ $f(z)$ analytic $\implies$ $\int_{\partial D}f(z) = 0$ 

#### If the integrand depends analytically on a parameter, then the integral depends analytically on the parameter:

##### $h(t,z)$ is a continuous, complex-valued function for $t \in [a,b], z \in D$ 

##### if for each fixed $t$, $h(t,z)$ is an analytic function of $z \in D$ 

then $H(z) = \int_a^b h(t,z)dt, z \in D$ is analytic on $D$ 

#### Theorem: if $f(z)$ is continuous on $D$ and analytic on $D\setminus \R$, then $f(z)$ is analytic on $D$ 

## Chapter 5: Power Series

### 1. Infinite Series

#### A series $\sum_{k=0}^\infin a_k$ of complex numbers converges to $S$ if the sequence of partial sums {$S_k$} converges to $S$

##### $S_k = \sum_{j=0}^k a_j$ 

##### $S = \sum_{k=0}^\infin = \sum a_k$ 

#### Any statement concerning series can be reinterpreted as a statement about sequences  in terms of the sequence of partial sums of the series

##### $\sum a_k = A, \sum b_k = B \implies \sum(a_k + b_k) = A+B$

$c\sum a_k = cA$ 

#### Comparison Test: If $0 \leq a_k \leq r_k$ and if $\sum r_k$ converges, then $\sum a_k $ converges and $\sum a_k \leq \sum r_k$ 

#### $a_k = S_k - S_{k-1}$

#### If $\sum a_k $ converges, then $a_k \rightarrow 0$ as $k \rightarrow \infin$ 

##### $\equiv$ if $a_k$ does not converge to $0$, then $\sum a_k$ diverges

#### Geometric series: $\sum_{k=0}^\infin z^k$

##### $S_k = 1 + z + . . . + z^k = \frac{1 - z^{k+1}}{1-z}$, $z \neq 1$ 

##### $\sum_{k=0}^\infin z^k = \frac{1}{1-z}, |z| < 1$ 

##### if $|z| \geq 1$, then $z^k$ does not converge to $0$, so series doesn't converge

#### Converge absolutely: $\sum|a_k|$ converges $\implies$ $\sum a_k$ converges

##### $|\sum_{k=0}^\infin a_k| \leq \sum_{k=0}^\infin |a_k|$ 

#### Geometric series: $|\frac{1}{1-z} - \sum_{k=0}^n z^k| \leq \frac{|z|^{n+1}}{1 - |z|}$ , $|z| < 1$ 

### 2. Sequences and Series of Functions

#### {$f_j$} a sequence of complex-valued functions defined on a set $E$

##### {$f_j$} converges pointwise on $E$ if for each $x \in E$, {$f_j(x)$} converges

fix $x \in E$, {$f_j(x)$} is a sequence of complex numbers that has a unique limit

##### the limit $f(x)$ of {$f_j(x)$} is then a complex-valued function on $E$ 

#### Note: Most things require uniform convergence and lead to uniform convergence

#### {$f_j$} Converges Uniformly to $f$ on $E$ if |$f_j(x) - f(x)$| $\leq \epsilon_j$ for all $x \in E$

##### $\epsilon_j \rightarrow 0$ as $j \rightarrow \infin$, and $\epsilon_j = \sup_{x \in E}|f_j(x) - f(x)|$ 

##### Converge uniformly to $f$ on $E$ $\implies$ converge pointwise to $f$ on $E$ 

#### a uniform limit of continuous functions is continuous

#### an integral of a uniform limit is the limit of the integrals

$\gamma$: piecewise smooth curve in complex plane

{${f_j}$}: a sequence of continuous complex valued functions on $\gamma$  

if {$f_j$} converges uniformly to $f$ on $\gamma$, then 

##### $\int_{\gamma} f_j(z)dz$ converges to $\int_{\gamma}f(z)dz$ 

Note: each term in the sequence of integrals is a complex number, so we use the term converge, not converge uniformly/pointwise

#### $\sum g_j(x)$ series of complex valued functions defined on set $E$

##### $S_n(x) = \sum_{k=0}^n g_j(x)$ is the partial sum

##### Series converges pointwise on $E$ if the sequence of partial sums converges pointwise on $E$

* and each sequence for a fixed $x \in E$, {$S_n(x)$} is a sequence of complex numbers, so each limit is unique

##### Series converges uniformly on $E$ if the sequence of partial sums converges uniformly on $E$ 

and thus converges pointwise.

#### Weierstrass M-Test

Suppose $M_k \geq 0$ and $\sum M_k$ converges

If $g_k(x)$ are complex valued functions on a set $E$ such that $|g_k(x)| \leq M_k$ for all $x \in E$, then $\sum g_k(x)$ converges uniformly on $E$ 

#### A uniform limit  of analytic functions is analytic

If {$f_k(z)$} is a sequence of analytic functions on a domain $D$ that converges uniformly to $f(z)$ on $D$, then $f(z)$ is analytic

a limit of analytic functions that converges uniformly is analytic.

#### $f_k(z)$ is analytic for $|z-z_0| \leq R$, and suppose that {$f_k(z)$} converges uniformly to $f(z)$ for $|z-z_0| \leq R$. Then for each $r < R$ and for each $m \geq 1$, the sequence of mth derivatives {$f_k^{(m)}(z)$} converges uniformly to $f^{(m)}(z)$ for $|z-z_0| \leq r$ 

##### if a sequence of analytic functions on a closed disk converges uniformly on that closed disk $D$ to $f(z)$, then for each closed disk strictly smaller than $D$, the sequence of mth derivatives converges uniformly to $f^{(m)}(z)$ 

#### Converge normally (applies only to analytic functions on $D$)

##### it is a type of uniform convergence

A sequence of analytic functions {$f_k(z)$} on domain $D$ **converges normally** to an analytic function $f(z)$  on $D$ if it converges uniformly to $f(z)$ on each closed disk contained in $D$ $\equiv$ {$f_k(z)$} converges to $f(z)$ uniformly on each bounded subset $E$ of $D$ at a strictly positive distance from the boundary of $D$ 

##### Theorem: {$f_k(z)$} is a sequence of analytic functions on a domain $D$ that converges normally on $D$ to the analytic function $f(z)$. Then for each $m \geq 1$, the sequence of mth derivatives {$f_k^{(m)}(z)$} converges normally to $f^{(m)}(z)$ on $D$ 

### 3. Power Series

#### A power series (centered at $z_0$) is a series of the form $\sum_{k = 0}^\infin a_k(z-z_0)^k$ 

#### $\sum a_k z^k$ a power series, then there is $R$, $0 \leq R \leq +\infin$ such that $\sum a_kz^k$ converges absolutely if $|z| < R$, and $\sum a_k z^k$ does not converge if $|z| > R$. For each fixed $r$ satisfying $r < R$, the series $\sum a_k z^k$ converges uniformly for $|z| \leq r$ 

##### The radius of convergence depends only on the tail of the series. If we alter a finite number of coefficients, the radius of convergence remains the same. 

#### $\sum a_k z^k$ a power series with radius of convergence of $R > 0$, then the function $f(z) = \sum_{k=0}^\infin a_k z^k, |z| <R$ is analytic. 

##### derivatives: $f'(z) = \sum_{k=1}^\infin ka_kz^{k-1}$, $f''(z) = \sum_{k=2}^\infin k(k-1)a_kz^{k-2}$ , $|z| < R$ 

##### $a_k = \frac{1}{k!}f^{(k)}(0), k \geq 0$ 

#### Due to uniform convergence of power series on subdisks of radius strictly smaller than $R$, a power series can be integrated term by term: $\int_0^z \sum(a_k\zeta^k)d\zeta = \sum a_k \int_0^z \zeta ^k d\zeta = \sum a_k \frac{z^{k+1}}{k+1}, |z| <R$

#### Finding $R$:

$|a_k/a_{k+1}| \rightarrow R$ as $k \rightarrow \infin$ 

##### $\sqrt[k]{|a_k|} \rightarrow \frac{1}{R}$ as $k \rightarrow \infin$ 

##### or $R = \frac{1}{\lim \sup \sqrt[k]{|a_k|}}$ 

### 4. Power Series Expansion of an Analytic Function

#### Any function analytic on a disk can be expanded in a power series that converges on the disk

#### Theorem:

1. Suppose that $f(z)$ is analytic for $|z-z_0| < \rho$. 

Then

1. $f(z)$ is represented by the power series

##### (4.1) $f(z) = \sum_{k = 0}^\infin a_k(z-z_0)^k, |z-z_0| < \rho$ 

where

##### (4.2) $a_k = \frac{f^{(k)}(z_0)}{k!}, k \geq 0$

and where the power series has radius of convergence $R \geq \rho$ 

1. For any fixed $r, 0 < r < \rho$ we have

##### (4.3) $a_k = \frac{1}{2\pi i}\oint _{|\zeta - z_0| = r}\frac{f(\zeta)}{(\zeta - z_0)^{k+1}}d\zeta$, $k \geq 0$ (Cauchy Integral)

$f^{(k)}(z_0) = \frac{k!}{2\pi i} \oint_{|w - z_0| = r} \frac{f(w)}{(w - z_0)^{k+1}}dw$ 

Further, if $|f(z)| \leq M$ for $|z-z_0| = r$, then

##### (4.4) $|a_k| \leq \frac{M}{r^k}, k \geq 0$ (Cauchy Estimates)

$|f^{(k)}| \leq \frac{k!}{\rho^k}M$ 

#### Corollary. an analytic function on a disk is completely determined by its value and the values of its derivatives at the center of the disk

Suppose that $f(z)$ and $g(z)$ are analytic for $|z-z_0| < r$. If $f^{(k)}(z_0) = g^{(k)}(z_0)$ for $k \geq 0$, then $f(z) = g(z)$ for $|z-z_0| < r$ 

#### Corollary. method for determining the radius of convergence of a power series

Suppose that $f(z)$ is analytic at $z_0$, with power series expansion $f(z) = \sum a_k(z-z_0)^k$ centered at $z_0$. Then the radius of convergence of the power series is the largest number $R$ such that $f(z)$ extends to be analytic on the disk {$|z-z_0| < R$}. 

### 5. Power Series Expansion at Infinity

#### $f(z)$ is analytic at $z = \infin$ if the function $g(w) = f(1/w)$ is analytic at $w = 0$ 

We study the behavior of $f(z)$ at $z = \infin$ by studying the behavior of $g(w)$ at $w = 0$ 

#### If $f(z)$ is analytic at $\infin$, then $g(w) = f(1/w)$ has a power series expansion centered at $w = 0$

$g(w) = \sum_{k=0}^\infin b_kw^k$, $|w| < \rho$ 

##### (5.1) $f(z) = \sum_{k=0}^\infin \frac{b_k}{z^k}$, $|z| > \frac{1}{\rho}$ 

### 6. Manipulation of Power Series

#### Power series can be treated like polynomials

* differentiate and integrate term by term
* add and multiply like polynomials

##### the power series of $f(z) + g(z)$ is $\sum_{k=0}^\infin (a_k + b_k)z^k$ , where $f(z), g(z)$ are analytic at $0$ 

##### for any $c \in \C$, $cf(z) = \sum_{k=0}^\infin ca_kz^k$, $f(z)$ analytic at $0$ 

##### $f(z)g(z) = \sum_{k=0}^\infin c_k z^k$, where $c_k = \sum_{j= 0}^k a_{k-j}b_j$, $f(z), g(z)$ analytic at $0$ 

##### $g(z)$ analytic at $z = 0$, assume $g(0) = 1$, then $1/g(z) = 1 - (\sum_{k=1}^\infin b_kz^k)+ (\sum_{k=1}^\infin b_kz^k)^2 - (\sum_{k=1}^\infin b_kz^k)^3 + . . .$

Terms involving $z^m$ occur only in the first $m+1$ summands

### 7. The Zeros of an Analytic Function

#### Let $f(z)$ be analytic at $z_0$, and suppose $f(z_0) = 0$, but $f(z)$ is not identically zero. We say that $f(z)$ has a zero of order $N$ at $z_0$ if $f(z_0) = f'(z_0) = . . . = f^{(N-1)}(z_0) = 0$

####  In view of formula (4.2) for power series coefficients, this occurs if and only if the power series expansion of $f(z)$ has the form $a_N(z-z_0)^N + a_{N+1}(z-z_0)^{N+1} + . . .$ where $a_N \neq 0$ 

##### (7.1) $f(z) = (z-z_0)^Nh(z)$, where $h(z)$ is analytic at $z_0$ and $h(z_0) = a_N \neq 0$ 

#### If $f(z) = (z-z_0)^Nh(z)$, where $h(z)$ is analytic at $z_0$ and $h(z_0) \neq 0$, then $f(z)$ has a zero of order $N$ at $z_0$ and the power series for $f(z)$ has the leading term $h(z_0)(z-z_0)^N$ 

#### The order of a zero of $f(z)g(z)$ $=$ (order of zero for $f(z)$) + (order of zero for $g(z)$)

#### $f(z)$ has zero at $z = \infin$ of order $N$ if $g(w)= f(1/w)$ has a zero at $w = 0$ of order $N$ 

This means:

$g(w) = b_Nw^N + . . . $

and $f(z) = b_N/z^N + . . . $ $|z| > R$, where $b_N \neq 0$ 

####  Theorem: If $D$ is a domain, and $f(z)$ is an analytic function on $D$ that is not identically zero, then the zeros of $f(z)$ are isolated

##### Each zero of $f(z)$ is of finite order

#### Theorem (Uniqueness Principle)

If $f(z)$ and $g(z)$ are analytic on a domain $D$, and if $f(z) = g(z)$ for $z$ belonging to a set that has a nonisolated point, then $f(z) = g(z)$ for all $z \in D$ 

##### Example: since we know $\sin^2 x + \cos^2 x = 1$ for all $x \in \R$, $\R$ has nonisolated points, so $\sin^2 z + \cos^2 z = 1$ for all $z \in \C$ 

#### Principle of permanence of functional equations

##### Theorem

Let $D$ be a domain

Let $E​$ be a subset of $D​$ that has a nonisolated point

Let $F(z,w)$ be a function defined for $z, w$ $\in D$ such that $F(z,w)$ is analytic in $z$ for each fixed $w \in D$ and analytic in $w$ for each fixed $z \in D$. 

If $F(z,w)  = 0$ whenever $z$ and $w$ both belong to $E$, then $F(z,w) = 0$ for all $z, w \in D$ 