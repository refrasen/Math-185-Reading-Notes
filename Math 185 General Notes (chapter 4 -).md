# Math 185 General Notes (chapter 4 -)

## Chapter 4 Complex Integration and Analyticity

### 1. Complex Line Integrals

For complex analysis define $dz = dx + idy$ 

##### (1.1) $\int_\gamma h(z)dz = \int_\gamma h(z)dx + i\int_\gamma h(z) dy$

$\gamma$ is parameterized by $t \mapsto z(t) = x(t) + iy(t), a \leq t \leq b$ 

The Riemann sum approximating $\int_\gamma h(z)(dx + idy)$ corresponding to the subdivision $a = t_0 < t_1 < \cdots < t_n = b$ 

by $\sum h(z_j)(x_{j+1}-x_j) + i \sum h(z_j)(y_{j+1}-y_j)$ , 

where $z(t_j) = z_j = x_j + i y_j$ 

##### (1.2) $\int_\gamma h(z)dz \approx \sum h(z_j)(z_{j+1}-z_j)$ 

##### Example: $\int_0^{1+i}z^2 dz$ 

parametrize the line segment $z(t) = (1+i)t$ 

do $dz = \frac{dz}{dt}dt$ , $z  = 0$ when $t = 0$ , $z = 1 +i$ when $t = 1$

##### Example $\oint_{|z| = 1}\frac{dz}{z}$ 

$z = e^{i\theta}$ 

$\frac{dz}{d\theta} = ie^{i\theta} = iz$ $\implies$ $\frac{dz}{z} = i d\theta$  

------

$|dz| = ds = \sqrt{(dx)^2+(dy)^2}$ , $ds$ is the infinitesimal arc length

So, if a curve $\gamma$ is parametrized by $z(t) = x(t) + iy(t)$, then

##### (1.3) $\int_\gamma h(z)|dz| = \int_\gamma h(z) ds = \int_a^b h(z(t))\sqrt{(\frac{dx}{dt})^2 + (\frac{dy}{dt})^2}dt$ 

So, the length of $\gamma$ is

$L = \int_\gamma |dz| = \int_a^b \sqrt{(\frac{dx}{dt})^2 + (\frac{dy}{dt})^2}dt$ 

#### Theorem. Triangle inequality for integrals, and $ML-$estimate

Suppose $\gamma$ is a piecewise smooth curve. If $h(z)$ is a continuous function on $\gamma$, then

##### (1.6) $|\int_\gamma h(z)dz| \leq \int_\gamma |h(z)||dz|$ 

Further, if $\gamma$ has length $L$ and $|h(z)| \leq M$ on $\gamma$, then

##### (1.7) $|\int_\gamma h(z)dz| \leq ML$ 

Both of these following from Triangle-inequality for approx. Riemann sums

##### Sharp estimate: when equality holds 

### 2. Fundamental Theorem of Calculus for Analytic Functions

Let $f(z)$ be a continuous function on a domain $D$ 

#### Complex primitive for a continuous function $f(z)$ on a domain $D$: a function $F(z)$ on $D$ that is analytic and $F'(z)= f(z)$ 

#### Theorem (Part I). If $f(z)$ is continuous on a domain $D$, and if $F(z)$ is a primitive for $f(z)$, then

##### $\int_A^B f(z)\, dz = F(B)-F(A)$ 

where the integral can be taken over any path in $D$ from $A$ to $B$ 

​	so any path $\gamma$ s.t. $\gamma(a) = A, \gamma(b) = B$ $\gamma(t) = x(t) +iy(t)$ 

##### Evaluating $\int_A^B f(z)$ is reduced to that of finding an analytic function $F(z)$ whose derivative is $f(z)$ 

#### Theorem (Part II) Let $D$ be a star-shaped domain, and let $f(z)$ be analytic on $D$. Then $f(z)$ has a primitive on $D$, and the primitive is unique up to adding a constant. A primitive for $f(z)$ is given explicitly by 

##### $F(z) = \int_{z_0} ^z f(\zeta)\, d\zeta, \; z \in D$ 

where $z_0$ is any fixed point of $D$, and where the integral can be taken along any path in $D$ from $z_0 $ to $z$ 

#### Note: integrals of analytic functions in star-shaped domains are independent of path. Not true for arbitrary domains.

### 3. Cauchy's Theorem

Begin with smooth complex-valued function $f(z) = u +iv$ 

Express $f(z)dz = (u+iv)(dx + idy) = (u+iv)dx + (-v + iu)dy$ 

$f(z)dz$ is a closed differential if: $\frac{\partial}{\partial y}(u+iv) = \frac{\partial}{\partial x}(-v + iu)$ 

This is equivalent to the CR equations for $u, v$ 

#### Theorem. A continuously differentiable function $f(z)$ on $D$ is analytic if and only if the differential $f(z)dz$ is closed

#### Theorem (Cauchy's Theorem)

Let $D$ be a bounded domain with piecewise smooth boundary. If $f(z)$ is an analytic function on $D$ that extends smoothly to $\partial D$ then $\int_{\partial D} f(z)dz$ = 0

### 4. The Cauchy Integral Formula

#### Cauchy Integral Formula Theorem

Let $D$ be a bounded domain with piecewise smooth boundary. If $f(z)$ is analytic on $D$, and $f(z)$ extends smoothly to the boundary of $D$, then 

##### (4.1) $f(z) = \frac{1}{2\pi i}\int_{\partial D}\frac{f(w)}{w-z}dw, \; z \in D$

#### Theorem. Let $D$ be a bounded domain with piecewise smooth boundary. If $f(z)$ is an analytic function on $D$ that extends smoothly to the boundary of $D$, then $f(z)$ has complex derivatives of all orders on $D$, which are given by 

##### (4.2) $f^{(m)}(z) = \frac{m!}{2\pi i} \int_{\partial D}\frac{f(w)}{(w-z)^{m+1}}dw, z \in D, m\geq 0$

##### Corollary. If $f(z)$  is analytic on a domain $D$, then $f(z)$ is infinitely differentiable, and the successive complex derivatives $f'(z), f''(z), ..., $ are all analytic on $D$

### 5. Liouville's Theorem

Suppose that $f(z)$ is analytic on the closed disk {$|z-z_0| \leq \rho$}, that is, it is analytic on some domain containing the closed disk.

1. Using *Cauchy Integral Formula* for $f^{(m)}(z)$, we obtain

   $f^{(m)}(z_0) = \frac{m!}{2\pi i}\int_{|z-z_0| = \rho}\frac{f(z)}{(z-z_0)^{m+1}}dz$ 

2. Then Parameterize the boundary circle by $z = z_0 +\rho e^{i\theta}$, $dz = i\rho e^{i\theta}d\theta$ and obtain

   1. $\frac{1}{2\pi i} \frac{f(z)}{(z-z_0)^{m+1}}dz = \frac{f(z_0+\rho e^{i\theta})}{\rho^me^{mi\theta}}\frac{d\theta}{2\pi}$ 
3. Plug back into integral:

   1. $f^{(m)}(z_0) = \frac{m!}{\rho^m}\int_{0}^{2\pi} \frac{f(z_0 + \rho e^{i\theta})}{e^{mi\theta}}\frac{d\theta}{2\pi}$ 
4. Using triangle inequality for integrals

   1. $|f^{(m)}(z_0)| \leq \frac{m!}{\rho ^m} \int_{0}^{2\pi}|f(z_0+\rho e^{i\theta})|\frac{d\theta}{2\pi}$ 

This and using ML estimate leads to the following Theorem:

#### Cauchy Estimates

Suppose $f(z)$ is analytic for $|z-z_0| \leq \rho$  $\equiv$ $f(z)$ is analytic on the closed disk with center $z_0$, radius $\rho$ 

If $|f(z)| \leq M$ for $|z-z_0| = \rho$, then:

$|f^{(m)}(z_0)| \leq \frac{m!}{\rho^m}M$, $m \geq 0$ 

##### Remarks

1. This estimate scales correctly with respect to $M$, in that if we multiply $f(z)$ by a positive constant, the estimate is multiplied by that same constant
2. It scales correctly with respect to $\rho$: 
   1. Dilate the disk by a factor fo $c > 0$, then the mth derivative of the dilated function and the factor $1/\rho^m$ are multiplied by $1/c^m$ 
3. Invariant w.r.t. Translations

In special case of analytic functions bounded in modulus by one on the unit disk, all derivatives of the function are bounded in modulus by one at the origin 

so $|f'(z_0)| \leq 1$ $\implies$ $|f''(z_0)| \leq 1$ $\implies$ . . . $|f^{(m)}(z_0)| \leq 1$ 

#### Liouville's Theorem: A bounded entire function is constant

Let $f(z)$ be analytic on the complex plane.

If $f(z)$ is bounded, then $f(z)$ is constant

Proof:

1. Suppose $|f(z)| \leq M$ for all $z \in \C$ 
2. Apply Cauchy Estimate to a disk centered at any $z_0$ of any radius $\rho$
3. $|f'(z_0)| \leq \frac{M}{\rho}$ 
4. letting $\rho$ tend to $\infin$, $f'(z_0) = 0$ 
   1. we are allowed to do this since $f(z)$ is analytic on the complex plane and is bounded
5. this is true for all $z_0$, as $z_0$ was arbitrary.
6. $f(z)$ is constant, since $f'(z) = 0$ 

#### Entire Function Definition

An entire function is a function that is analytic on the entire complex plane.

##### Examples

1. polynomials
2. transcendental functions $e^z, \cos z, \sin z, \cosh z, \sinh z$

##### Properties

1. Preserved under linear combinations
2. products of entire functions are entire

##### Nonexamples

1. 1/z
2. $\log z$
3. $\sqrt{z}$

##### A <u>bounded</u> <u>entire</u> function is <u>constant</u>

###### Can use this to give a proof of the Fundamental theorem of algebra

Tricky part

$1/p(z)$ is a constant $\implies$ $p(z)$ is a constant, but $p(z) \neq 0$, as it doesn't have a zero by supposition

but $1/p(z) \rightarrow 0$, as $z \rightarrow \infin$ 

$\implies$ $1/p(z)$ is a bounded entire function

$\implies1/p(z) = C$ but that would contradict $p(z) \rightarrow \infin$ 

or it would mean $1/p(z) = 0$, but then that means $1 = 0$? 

### 6. Morera's Theorem

differential $f(z)dz$ is closed if and only if $f(z)$ is analytic

#### Morera's Theorem

Let $f(z)$ be a **continuous** function on a domain $D$.

If $\int_{\partial R}f(z)dz = 0$ for every closed rectangle $R$ contained in $D$ with sides parallel to the coordinate axes, 

then $f(z)$ is analytic on $D$ 

What's nice: only continuity is required.

Proof:

1. Assume $D$ is a disk with center $z_0$ 
2. Define: $F(z) = \int_{z_0}^{z}f(\zeta)d\zeta, z \in D$  
   1. path of integration runs along horizontal line and then a vertical line
   2. the path of integration running along the vertical line then the horizontal line would give the same result 
   3. the difference between path 1 and path 2 is a rectangle, and so we can use the hypothesis to show the integral is the same
3. $F(z+\Delta z) - F(z) $ $= \int_{z}^{z+\Delta z}f(\zeta)d\zeta$ 
   1. $\int_{z_0}^{z+\Delta z}f(\zeta)d\zeta +\int_{z}^{z_0}f(\zeta)d\zeta$ 
   2. $\int_{z_0}^{w} +\int_{w}^{z+\Delta z} + \int_z^{z_0} +\int_w^{z} +\int_z^w$
   3. where $w$ is the point where the horizontal line through $z$ meets the vertical line through $z + \Delta z$ 
   4. $z_0 $to $w$, $w$ to $z$ and $z$ to $z_0$ make a rectangle so we're left with
   5. $\int_z^w + \int_w^{z+\Delta z}$, which is a horizontal line from $z$  to $w$  and a vertical line from $w$ to $z+\Delta z$
   6. so we end up with $\int_z^{z+\Delta z}$ as desired
4. Add $f(z)$ and subtract $f(z)$ on the right
   1. $F(z+\Delta z) - F(z) = f(z)\int_{z}^{z + \Delta z}d\zeta + \int_z^{z+\Delta z}(f(\zeta)-f(z))d\zeta$ 
   2. $ = f(z)\Delta z + \int_z^{z+\Delta z}(f(\zeta)-f(z))d\zeta$ 
5. The length of the contour from $z$ to $z+\Delta z$ is at most $2|\Delta z|$ 
   1. since we must go from $z$ to $z+\Delta z$ with horzintal then vertical lines
   2. the horizontal, vertical components of $\Delta z$ are less than $|\Delta z|$
   3. thus adding their lengths are at most $2|\Delta z|$ 
6. $|\frac{F(z+\Delta z) - F(z)}{\Delta z} - f(z)| \leq 2 M_\epsilon, |\Delta z| < \epsilon$ , obtained using ML estimate, and dividing both sides by $|\Delta z|$
   1. $M_\epsilon$ is the max of $|f(\zeta)-f(z)|$ over all $\zeta $ satisfying $|\zeta - z|\leq \epsilon$
   2. The rectangle is a compact set, $f(\zeta) -f(z)$ is continuous 
   3. and $M_\epsilon$ depends on $\epsilon$ since $f(\zeta) - f(z)$ varies with $\epsilon$ 
7. since $f$ is continuous, as $\epsilon \rightarrow 0$, $M_{\epsilon} \rightarrow 0$ 
8. So $f(z)$ is the continuous derivative of $F(z)$ , making $F(z)$ analytic
9. and $f(z)$ is therefore analytic as well
   1. somewhere we proved that the derivatives of analytic functions are analytic

#### If the integrand depends analytically on a parameter, then the integral depends analytically on the parameter 

##### Theorem. Suppose that $h(t,z)$ is continuous complex-valued function defined for $a \leq t \leq b$ and $z \in D$ 

###### If for each fixed $t$, $h(t,z)$ is an analytic function of $z \in D$ 

Then:

###### $H(z) = \int_a^b h(t,z)dt, z \in D$ is analytic on $D$ 

Proof:

1. $H(z)$ is continuous on D (we do this to use (Morera's theorem))
   1. if $z_n \rightarrow z$, then $h(t,z_n) \rightarrow h(t,z)$ uniformly for $a \leq t \leq b$, since $h$ is continuous
   2. Then, $H(z_n) \rightarrow H(z)$ 
2. Let $R$ be a closed rectangle in $D$, we can use Cauchy's Theorem since $h(t,z)$ is analytic on $z$ in $D$ 
   1. $\int_{\partial R} h(t,z)dz = 0$
3. Consequently
   1. $\int_a^b\int_{\partial R}h(t,z)dz dt = 0$ 
   2. since the integral of 0 is 0
4. Parameterization of the sides of $\partial R$ converts the inside integral to a sum of four garden-variety integrals of a continuous function, so we can interchange order of integration
5. $0 = \int_{\partial R}\int_a^bh(t,z)dtdz = \int_{\partial R}H(z)dz$ 
   1. since $H(z)$ is continuous
   2. $R$ was any rectangle in $D$ 
6. So by Morera's theorem, $H(z)$ is analytic in $D$ 

#### Theorem. Suppose that $f(z)$ is a continuous function on a domain $D$ that is analytic on $D\setminus \R$, that is on the part of $D$ not lying on the real axis. Then $f(z)$ is analytic on $D$ 

---

## NOT ON MIDTERM:

### 7. Goursat's Theorem

#### Goursat's Theorem

If $f(z)$ is a complex-valued function on a domain $D$ such that $f'(z_0) =$$\lim_{z\rightarrow z_0}\frac{f(z)-f(z_0)}{z-z_0}$ exists at each point $z_0$ of $D$, then $f(z)$ is analytic on $D$ 

"...as useless as it is aesthetically pleasing"

Proof: Based on Morera's theorem

1. Let $R$ be a closed rectangle in $D$. 

2. Subdivide $R$ into four equal subrectangles

3. Let $R_1$ be the rectangle s.t. $|\int_{\partial R_1}f(z)dz| \geq \frac{1}{4}|\int_{\partial R}f(z)dz|$ 

   1. This is possible since the integral of the boundary of $R$ is the sum of the four subrectangles
   2. in general $a + b + c + d = n$, 
      1. $(a+b+c+d)/4 = n/4$ 
      2. If all $a, b, c, d < n/4$, we'd have a contradiction

4. Subdivide $R_1$ into four equal subrectangles, and repeat

5. So we end up with rectangles $R_i$, where $|\int_{\partial R_i}f(z)dz|\geq \frac{1}{4}|\int_{\partial R_{i-1}}f(z)dz|$ 

   1. Nested sequence of {${R_n}$}  rectangles such that
      1. $|\int_{\partial R_n}f(z)dz| \geq \cdots \geq \frac{1}{4^n}|\int_{\partial R}f(z)dz|$ 

6. $R_n$'s are decreasing and have diameters tending to $0$, the $R_n's$ converge to some point $z_0$ in $D$ 

7. $f(z)$ is differentiable at $z_0$, we have $|\frac{f(z)-f(z_0)}{z-z_0} - f'(z_0)| \leq \epsilon_n, z \in R_n$ 

   1. $\epsilon_n \rightarrow 0, n \rightarrow \infin$ since as $n \rightarrow \infin$, $R_n$ converges to $z_0$ , so $ z\rightarrow z_0$ and f is diff. at $z_0$ and the definition of the limit is used blah blah

8. Let $L$ be the length of $\partial R$. Then the length of $\partial R_n$ is $L/2^n$ 

   1. The length of the sides of each subrectangle is half the corresponding length of the original rectangle, so the perimeter is cut in half

9. So $|f(z)-f(z_0)-f'(z_0)(z-z_0)| \leq \epsilon_n|z-z_0| \leq 2\epsilon_n L/2^n$ 

   1. somehow $|z-z_0| \leq L/2^{n-1}$ 
   2. I think this is just a really safe estimate

10. Using the $ML$-estimate and Cauchy's theorem:

    1. $|\int_{\partial R_n}f(z)dz| = |\int_{\partial R_n} [f(z)-f(z_0)-f'(z_0)(z-z_0)]dz|$
       1. $f(z_0), f'(z_0)$ are constants and therefore analytic, and $z-z_0$ is analytic:
       2. $\int_{\partial R_n}-f(z_0)-f'(z_0)(z-z_0)dz$= 0 by Cauchy's Theorem
    2. Using results from 8. and 9. we obtain
    3. $|\int_{\partial R_n}f(z)dz| \leq (2\epsilon_n L/2^n)(l/2^n) = 2L^2\epsilon_n/4^n$ 

11. so using step 5.1

    1. $|\int_{\partial R}f(z)dz| \leq 4^n|\int_{\partial R^n}f(z)dz| \leq 2L^2\epsilon_n$ 

12. and since $\epsilon_n \rightarrow 0$ as $n \rightarrow \infin$:

    1. $|\int_{\partial R}f(z)dz| = 0$ 

13. By Morera's theorem, $f(z)$ is analytic


###  8. Complex Notation and Pompeiu's Formula

Many results in complex analysis can be expressed very simply in terms of first-order differential operators

$\frac{\partial}{\partial z} = \frac{1}{2}[\frac{\partial}{\partial x}-i\frac{\partial}{\partial y}]$, $\frac{\partial}{\partial \overline{z}} = \frac{1}{2}[\frac{\partial}{\partial x}+i\frac{\partial}{\partial y}]$ 

We may think of $\frac{\partial f}{\partial x}$ as an average of the derivatives of $f(z)$ in the x and iy directions

$\frac{\partial f}{\partial z} = \frac{1}{2}[\frac{\partial f}{\partial x}+ \frac{\partial f}{\partial(iy)}]$ 

When we derived the CR equations in chapter 2 we found

$f'(z) = \frac{\partial f}{\partial x}$ and $f'(z) = -i\frac{\partial f}{\partial y} = \frac{\partial f}{\partial(iy)}$ 

Taking the average of these two we get

#### (8.1) $f'(z) = \frac{\partial f}{\partial z}$ 

This is all provided that $f$ is analytic

To understand the operator $\frac{\partial }{\partial \overline{z}}$, we write $f = u+iv$ and compute

$\frac{\partial f}{\partial \overline{z}} = $$\frac{1}{2}[\frac{\partial u}{\partial x} - \frac{\partial v}{\partial y}] + \frac{i}{2}[\frac{\partial u}{\partial y} + \frac{\partial v}{\partial x}]$ 

Equating real and imaginary parts of the right-hand side to 0 we obtain the $CR$ equations for $u$ and $v$ 

#### Complex Form of the Cauchy Riemann equations

##### (8.2) $\frac{\partial f}{\partial \overline{z}} = 0$ $\equiv$ the Cauchy Riemann equations for $u, v$ 

##### Theorem

Let $f(z)$ be a continuously differentiable function on a domain $D$. Then $f(z)$ is analytic if and only if $f(z)$ satisfies the complex form (8.2) of the Cauchy-Riemann equations. If $f(z)$ is analytic, then the derivative of $f(z)$ is given by (8.1)

#### Rules for operating with $\frac{\partial}{\partial z}$ and $\frac{\partial}{\partial \overline{z}}$ 

1. Linear:

   1. $\frac{\partial}{\partial z}(af + bg) = a\frac{\partial f}{\partial z} + b \frac{\partial g}{\partial z}$ 
      1. same for $\frac{\partial}{\partial \overline{z}}$ 

2. Satisfy Leibniz Rule (product rule)

   1. $\frac{\partial}{\partial z}(fg) = f\frac{\partial g}{\partial z} + g\frac{\partial f}{\partial z}$ 
      1. same for $\frac{\partial }{\partial \overline{z}}$ 

3. The $z$-derivative and the $\overline{z}$-derivative are related to each other by

   $\frac{\partial f}{\partial \overline{z}} = \overline{\frac{\partial \overline{f}}{\partial z}}$

   $\frac{\partial \overline{f}}{\partial \overline{z}}= \overline{\frac{\partial f}{\partial z} }$

   This can be verified by writing $f = u+iv$ and $\overline{f} = u-iv$ and carrying out the calculations

The taylor series expansion of a smooth function $f(z)$ at $z_0$ through only the linear terms, is given by $f(z) = f(z_0) + \frac{\partial f}{\partial z}(z_0)(z-z_0) + \frac{\partial f}{\partial \overline{z}}(z_0)\overline{(z-z_0)} + \mathcal{O}(|z-z_0|^2)$ 

where the "big oh" term is a remainder term bounded by $C|z-z_0|^2$ 

Derive the complex form of the formula for the tangent vector to a curve using Taylor's formula

1. Let $f(z)$ be a smooth function and let $\gamma(t)$ be a smooth curve terminating at $\gamma(0) = z_0$ 

2. $f(\gamma(t)) - f(\gamma(0)) = \frac{\partial f}{\partial z}(z_0)(\gamma(t)-z_0) + \frac{\partial f}{\partial \overline{z}}(z_0)\overline{(\gamma(t)-z_0)}+\mathcal{O}(|\gamma(t)-z_0|^2)$ 

3. Dividing by $t$ and taking limit as $t\rightarrow 0$, we obtain

   1. ##### (8.3)$(f\circ\gamma)'(0) = \frac{\partial f}{\partial z}(z_0)\gamma'(0) + \frac{\partial f}{\partial \overline{z}}(z_0)\overline{\gamma'(0)}$ 

#### Theorem: conformal maps are analytic

Let $f(z)$ be a continuously differentiable function on a domain $D$. Suppose that the gradient of $f(z)$ does not vanish at any point of $D$, and that $f(z)$ is conformal. Then $f(z)$ is analytic on $D$, and $f'(z)\neq 0$ on $D$ 

Proof:

1. Fix a point $z_0 \in D$ 
2. Consider the straight line $\gamma(t) = z_0 + te^{i\theta}$, $0 \leq t \leq \epsilon$ 
   1. Terminates at $z_0$ with tangent $\gamma'(t) = e^{i\theta}$ 
3. By $(8.3)$ the image curve $f\circ \gamma$ has tangent at $f(z_0)$ given by
   1. $(f\circ \gamma)'(0) = \frac{\partial f}{\partial z}(z_0)e^{i\theta} + \frac{\partial f}{\partial \overline{z}}(z_0)e^{-i\theta}$ 
4. since the gradient of $f(z)$ doesn't vanish at any point of $D$, the above is not identically zero
5. For $f(z)$ to preserve angles at $z_0$, the difference in the args of $(f\circ \gamma)'(0)$ and $\gamma'(0)$ must be constant, independent of $\theta$ 
6. So the argument of $\frac{(f\circ\gamma)'(0)}{\gamma'(0)} = \frac{\partial f}{\partial z}(z_0) + \frac{\partial f}{\partial \overline{z}}(z_0)e^{-2i\theta}$ must be independent of $\theta$ 
7. Independence only occurs when we have $\frac{\partial f}{\partial \overline{z}}(z_0) = 0$ , which would mean $f(z)$ is analytic on $D$ 

Confusion:

I'm not so sure about step 5. and 6. This may stem from my inability to understand fully conformal mappings

The gradient condition implies that $f'(z) = \frac{\partial f}{\partial z} \neq 0$ 

gradient of $f$ = $(\frac{\partial u}{\partial z}, \frac{\partial v}{\partial z})$ $= (1/2)(\frac{\partial u}{\partial x}-i\frac{\partial u}{\partial y}, \frac{\partial v}{\partial x}-i\frac{\partial v}{\partial y})$ 

$\frac{\partial f}{\partial z}$ equals adding the $u$ component of the gradient to $i$ times the $v$ component

#### Theorem (Extension of Cauchy's theorem to arbitrary smooth functions)

If $D$ is a bounded domain in the complex plane with piecewise smooth boundary, and if $g(z)$ is a smooth function on $D\cup\partial D$, then 

##### (8.4) $\int_{\partial D}g(z)dz = 2i \int\int_{D}\frac{\partial g}{\partial \overline{z}} dxdy$ 

Proof:

1. replace dz by dx + idy and apply Green"s formula
2. ![1539142430230](C:\Users\Renee\AppData\Roaming\Typora\typora-user-images\1539142430230.png)

If $g(z)$ is analytic on $D$, then $\frac{\partial g}{\partial \overline{z}} = 0$ on$D$, so the integral over $D$ vanishes, and we obtain Cauchy's theorem

#### Pompeius' Formula

Suppose $D$ is a bounded domain with piecewise smooth boundary. If $g(z)$ is a smooth complex-valued function on $D\cup\partial D$, then

Cauchy-Green Formula:

##### (8.5) $g(w) = \frac{1}{2\pi i}\int_{\partial D}\frac{g(z)}{z-w}dz - \frac{1}{\pi}\int\int{D}\frac{\partial g}{\partial \overline{z}}\frac{1}{z-w}dxdy$, $w\in D$ 

Proof: same argument as in section 4, but the correction term appears in the calculation

1. Let $D_\epsilon$ be the domain obtained from $D$ by punching out a disk centered at $w$ of radius $\epsilon$ 

2. Apply complex version (8.4) of Green's theorem to the function $g(z)/(z-w)$ 

   1. Note: $\frac{\partial }{\partial \overline{z}}(\frac{g(z)}{z-w}) = $$\frac{\partial g}{\partial \overline{z}}\frac{1}{z-w} + g\frac{\partial }{\partial \overline{z}}(\frac{1}{z-w}) = \frac{\partial g}{\partial \overline{z}}\frac{1}{z-w}$ 

      1. since $1/(z-w)$ is analytic, $\frac{\partial }{\partial \overline{z}}(\frac{1}{z-w}) = 0$ 

   2. ##### (8.6) $\int_{\partial D_\epsilon}\frac{g(z)}{z-w}dz = 2i\int\int_{D_\epsilon}\frac{\partial g}{\partial \overline{z}}\frac{1}{z-w}dxdy$ 

3. The singularity of $1/(z-w)$ at $z = w$ is absolutely integrable...

   1. $\int\int_{|z-w| \leq 1}\frac{1}{|z-w|}dxdy = \int_0^{2\pi}\int_0^1 (1/r)*r dr d\theta = 2\pi$

4. The area integral in (8.6) over $D_\epsilon$ tends to the improper area integral over $D$ as $\epsilon \rightarrow 0$ 

   1. so the right side has $2i \int \int_D \frac{\partial g}{\partial \overline{z}}\frac{1}{z-w}dxdy$ , 

5. The boundary integral in (8.6) has the form

   1. $\int_{\partial D_\epsilon} = \int_{\partial D} - \int_{|z-w| = \epsilon}$ 

6. Parameterizing the circle $|z-w| = \epsilon$ we obtain the integral 

   1. $\int_{|z-w| = \epsilon}\frac{g(z)}{z-w}dz = i\int_0^{2\pi}g(w+\epsilon e^{i\theta})d\theta$
      1. comes from $\frac{dz}{d\theta} = i\epsilon e^{i\theta}$ and $z-w = \epsilon e^{i\theta}$ 
   2. This tends to $2\pi i g(w)$ as $\epsilon \rightarrow 0$ since $g$ is continuous at $w$ 

7. Thus letting $\epsilon \rightarrow 0$ in $(8.6)$ we obtain $(8.5)​$