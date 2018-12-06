# Math 185 General Notes Chapter 8

# The Logarithmic Integral

* derive argument principle from the residue theorem

## Chapter 8 Sections 1-4

### 1. The Argument Principle

Suppose $f(z)$ is analytic on a domain $D$ 

For a curve $\gamma$ in $D$ such that $f(z) \neq 0$ on $\gamma$ 

#### Logarithmic Integral of $f(z)$ along $\gamma$ 

##### (1.1) $\frac{1}{2\pi i}\int_{\gamma}\frac{f'(z)}{f(z)}dz = \frac{1}{2\pi i}\int_{\gamma}d \log f(z)$ 

- measures the change of $\log f(z)$ along the curve $\gamma$ 
- used to count zeros and poles of meromorphic functions

#### Theorem: Way to Evaluate (1.1)

Let $D$ be a bounded domain with piecewise smooth boundary $\partial D$, and let $f(z)$ be a meromorphic function on $D$ that extends to be analytic on $\partial D$, such that $f(z) \neq 0$ on $\partial D$. Then

##### (1.2) $\frac{1}{2\pi i}\int_{\partial D}\frac{f'(z)}{f(z)}dz = N_0 - N_{\infin}$

###### $N_0$ is the number of zeros of $f(z)$ in $D$ and $N_{\infin}$ is the number of poles of $f(z)$ in $D$, counting multiplicities 

Proof?:

1. Let $z_0$ be a zero or a pole of $f(z)$ with order $N$ 
   1. $N$ is the order of the zero if $z_0$ is a zero
   2. $N$ is minus the order of the pole if $z_0$ is a pole
2. $f(z) = (z-z_0)^Ng(z)$
   1. $g(z)$ is analytic at $z_0$ and $g(z_0) \neq 0$ 
3. $\frac{f'(z)}{f(z)} = \frac{N(z-z_0)^{N-1}g(z)}{(z-z_0)^Ng(z)} + \frac{(z-z_0)^Ng'(z)}{(z-z_0)^Ng(z)} = \frac{N}{z-z_0} + [\text{analytic}]$ 
4. So, because $a_1 = N$, and from Residue Theorem, we add up all residues to get the integral
5. positive $N_0's$ , negative $N_{\infin}'s$ 

---

Focus attention on $(1.1)$ 

$\frac{1}{2\pi i}\int_{\gamma}d \log f(z) = \frac{1}{2\pi i}\int_{\gamma}d \log |f(z)| + \frac{1}{2\pi}\int_{\gamma}d \arg (f(z))$ 

* I suppose since $\log f(z) = \log |f(z)| + i \arg ( f(z))$ 

The differential $d \log |f(z)|$ is exact and we may parameterize$\gamma(t) = x(t) + iy(t)$, $a \leq t \leq b$ $\implies$ 

$\int_{\gamma}d\log |f(z)| = \log|f(\gamma(b))| - \log|f(\gamma(a))|$

* In particular, $\int_{\gamma}d\log |f(z)| = 0$ if $\gamma$ is a closed curve

The differential $d \arg f(z)$ is closed, but **not exact** 

* Its integral is computed by choosing a continuous **single-valued determination** of $\arg f(\gamma(t))$ for $a \leq t \leq b$ 
* single-valued probably means one-to-one or many to one
* A single-valued complex function of a [complex variable](http://mathworld.wolfram.com/ComplexVariable.html) is a [complex function](http://mathworld.wolfram.com/ComplexFunction.html) ![f:C->C](http://mathworld.wolfram.com/images/equations/Single-ValuedFunction/Inline1.gif) that has
  the same value at every point ![z_0](http://mathworld.wolfram.com/images/equations/Single-ValuedFunction/Inline2.gif) independent
  of the path along which it is reached by [analytic  continuation](http://mathworld.wolfram.com/AnalyticContinuation.html) (Knopp 1996).

##### (1.3) $\int_{\gamma}d\arg (f(z))  = \arg f(\gamma(b)) - \arg f(\gamma(a))$ 

* This is the **increase in the argument of $f(z)$ along $\gamma$** 
* It is defined for any (continuous) path $\gamma$ in $D$ 
* Any two continuous determinations of $\arg f(\gamma(t))$ differ by a constant, so the increase in the argument given by $(1.3)$ is independent of the continuous determination
  * cause $\arg f(\gamma(b)) + C - (\arg f(\gamma(a))+C)$

---

* If $\gamma$ is a concatenation of curve segments, the increase in the argument of $f(z)$ along $\gamma$ is obtained by adding the increases along the various curve segments

* If the direction of the curve $\gamma$ is reversed, the increase in the argument is replaced by its negative 
* If $\gamma$ is a closed curve, i.e., $\gamma(a) = \gamma(b)$, the determination of $\arg f(\gamma(a))$ and $\arg f(\gamma(b))$ differ by an integral multiple of $2\pi$, so that the increase in the argument of $f(z)$ around $\gamma$ is an itnegral multiple of $2\pi$  

#### Example (Increase in the argument of $(z-z_0)^n$ counterclockwise around the circle $|z-z_0|  = \rho$) 

1. parameterize the circle by $\gamma(t) = z_0 + \rho e^{it}$, $0 \leq t \leq 2\pi$ 
2. $f(\gamma(t)) = \rho^n e^{int}$
3. a continuous determination for argument of $f(\gamma(t))$: $\arg f(\gamma(t)) = nt, 0 \leq t \leq 2\pi$ 

So the increase in argument of $f(z)$ around $\gamma$:

$\int_{\gamma}d\arg(f(z)) = nt |_{t=0}^{t = 2\pi} = 2\pi n$ 

---

#### The increase in the argument of $f(z)$ around the boundary of $D$ 

the sum of its increases around the closed curves in $\partial D$ 

#### Theorem $(\int_{\partial D} \arg (f(z)))$ evaluation when $f(z)$ satisfies some requirements

$D$ must:

1. be bounded
2. have a piecewise smooth boundary

$f(z)$ must:

1. be meromorphic on $D$  
2. extend to be analytic on $\partial D$
3. $\neq 0$ on $\partial D$ 

Then:

1. The increase in the argument of $f(z)$ around the boundary of $D$ is $2\pi$ times the number of zeros minus the number of poles of $f(z)$ in $D$ 

##### (1.4) $\int_{\partial D}d \arg (f(z)) = 2\pi (N_0 - N_\infin)$ 

---

Remarks:

* It is easy to track the argument of $f(z)$ along a segment of a curve in a domain where a single-valued determination of the argument function is available
* Suppose, the values of $f(\gamma(t))$ start from the positive real axis at $t = a$, lie in the upper half-plane for $a < t < b$ then hit the negative real axis at $t = b$
  * the increase in the argument of $f(\gamma(t))$ for $a \leq t \leq b$ is $\pi$
* Similarly, $f(\gamma(t))$ starts at positive real axis at $t =a$, lies in the lower half-plane for $a < t< b$, then terminates at the negative real axis at $t = b$
  * the increase in the argument of $f(\gamma(t))$ for $a \leq t \leq b$ is $-\pi$ 

---

#### Example: Using the argument principle to find the number of zeros of the polynomial $p(z) = z^6 + 9z^4 + z^3 + 2z + 4$ 

note: $p(x) > 0$ for $- \infin < x< \infin$

$4 + x^3 + 2x > 0$ for $-1 \leq x \leq 0$ and $9x^4 + x^3 + 2x > 0$ for $ x\leq 1$

There are no real zeros for $p(z)$

the coefficients of $p(z)$ are real, so the zeros come in complex conjugate pairs

 There are three zeros in the upper half-plane

to Determine the number of zeros in the first quadrant, we estimate the increase of $\arg p(z)$ around the boundary of the quarter disk $D_R$ of a large radius $R$, consisting of points $z$ in the first quadrant satisfying $|z| <R$ 

The increase in the arg of $p(z)$ around $\partial D_R$ is $2\pi$ times the number of zeros in $D_R$ 

"any reasonable approximation will yield the exact value"

* break $\partial D_R$ into three paths

  * along the real axis from $0$ to $R$, $p(x) > 0$, so the argument is constant and the increase is 0
  * along the quarter-circle $\Gamma_R$ defined by $|z| = R$ and $0 \leq \arg z \leq \pi/2$, the term $z^6$ dominates, and $\arg p(z) \approx 6 \arg z$ $\implies$ $6 \times \pi/2 = 3\pi$ 
  * along the imaginary axis from $iR$ to $0$: substitute $z = iy$ and follow the values of
    * $p(iy) = -y^6 + 9y^4 + 4 + i(-y^3 + 2y)$ as $y$ decreases from $R$ to $0$ 
    * initial point of this segment: $\Re p(iR) \approx -R^6$, $\Im p(iR) \approx -R^3$ $\implies$ $p(iR)$ lies in the third quadrant and has argument approximately $-\pi$
    * terminal point: $p(0) = 4$
    * To see how $\arg p(iy)$ behaves, we determine when the curve $p(iy)$ crosses the $x$-axis
    * crosses the real axis for values $y$ satisfying $-y^3 + 2y = 0$ 
      * solutions: $y = 0, \pm \sqrt{2}$ 
    * only one crossing point corresponding to $y > 0$: $y = \sqrt{2}$ 
    * the crossing point is $p(i\sqrt{2})$ $= 32$ 
    * so $p(iy)$ remains in the lower half plane as the parameter $y$ decreases from $y = R$ to $y = \sqrt{2}$ and it hits the positive real axis at $y = \sqrt{2}$ 
    * the increase in argument from $p(iy)$ from $R$, where $\arg p(iR) \approx -\pi$ to $\sqrt{2}$ where $\arg p(i\sqrt{2}) = 0$ is $\pi$   (since we are in the lower half plane, so we are going from $-\pi$ to $0$)
    * $p(iy)$ is in the upper half-plane for $y$ between $\sqrt{2}$ and $0$, and since the starting and ending points for this segment of the curve are on the positive real axis, the increase in the argument of $p(iy)$ as $y$ decreases from $\sqrt{2}$ to $0$ is zero
    * so the total change here is $\pi$ 

* Thus, the total increase of $\arg p(z)$ around $\partial D_R$ is approximately $3\pi + \pi = 4\pi$ 

  * so since we are dealing with $2\pi$ times an integer, it is exactly $4\pi$ 

* By the argument principle, $p(z)$ has two zeros in the first quadrant (it has no poles :P)

* there are no zeros on the imaginary axis, so the remaining zero of $p(z)$ is in the second quadrant


### 2. Rouche's Theorem

general principle: the number of zeros of an analytic function on a domain does not change if we make a small change in the function

#### Theorem (Rouche's Theorem)

Let $D$ be a bounded domain with piecewise smooth boundary $\partial D$ 

Let $f(z)$ and $h(z)$ be analytic $D \cup \partial D$ 

If $|h(z)| < |f(z)|$ for $z \in \partial D$, then $f(z)$ and $f(z)+h(z)$ have the same number of zeros in $D$, counting multiplicities 

---

The hypothesis implies that $f(z) \neq 0$ on $\partial D$, and that $f(z) + h(z) \neq 0$ on $\partial D$ 

From $f(z) + h(z) = f(z)[1 + h(z)/f(z)]$ we obtain:

##### (2.1) $\arg( f(z) + h(z)) = \arg(f(z)) + \arg ( 1 + \frac{h(z)}{f(z)})$ 

since $|h(z)/f(z)| < 1$, the values of $1 + h(z)/f(z)$ lie in the right half plane

and the increase of $\arg(1 + h(z)/f(z))$ around a closed boundary curve is $0$ 

* because remember, it has to be some multiple of $2\pi$, but we never actually get a full rotation about $0$ as we stay in the right plane the whole time

$\arg f(z)$ and $arg( f(z) + h(z))$ have the same increase around $\partial D$ 

By the argument principle, the functions have the same number of zeros in $D$ 

* we have that $N_{\infin} = 0$ as $f(z), h(z)$ are analytic on $D \cup \partial D$ 

#### Examples

##### number of zeros of $p(z) = z^6 + 9 z^4 + z^3 + 2z + 4$ that lie inside the unit circle

we seek to express $p(z)$ in the form:

$p(z) = \text{BIG }+ \text{ little}$ 

where

1. "BIG" dominates "little" on the unit circle
2. it is apparent how many zeros "BIG" has inside the unit circle

Our choice for BIG is $f(z) = 9z^4$, which has four zeros inside the unit circle, all at the origin

little is $h(z) = z^6 + z^3 + 2z + 4$, which satisfies $|h(z)| < |f(z)|$ for $|z| = 1$ 

By Rouche's Theorem, $p(z) = f(z) + h(z)$ also has four zeros inside the unit circle

##### Find all solutions of the equation $e^z = 1 + 2z$ that satisfy $|z| = 1$ 

One obvious solution: $z = 0$ 

To determine whether there are other solutions:

Apply Rouche's theorem to count the number of zeros of $e^z - 1 - 2z$ in the unit disk

the term $f(z) = -2z$ is the dominant term on the unit circle

$h(z) = e^z - 1$, and estimate:

$|h(z)| = |e^z - 1| = |z + \frac{z^2}{2!} + \frac{z^3}{3!}+ . . . | \leq |z| + \frac{|z|^2}{2!}+ \frac{|z|^3}{3!}+ ...$ 

If $|z| = 1$, the right hand side is $e - 1 \approx 1.7 < 2$ 

so $|h(z)| < |f(z)|$ for $|z| = 1$

since $f(z)$ has only one zero in the unit disk, $f(z) + h(z)$ also has only one zero, and the equation has no solutions in the unit disk other than $z = 0$ 

---

#### Proof of Fundamental Theorem of Algebra (Rouche's Theorem)

$p(z) = z^m + a_{m-1}z^{m-1}+ \cdots + a_0$ 

be a monic polynomial of degree $m \geq 1$ 

for $|z|$ large, the term $z^m$ dominates

$f(z) = z^m$, $h(z)= a_{m-1}z^{m-1} + \cdots + a_0$ 

If $R$ is large, we have $|h(z)| < |f(z)|$ for $|z| = R$

Consequently, $p(z) = f(z)+h(z)$ has the same number of zeros in the disk $|z| < R$ as $f(z) = z^m$, which is $m$ 

### 3. Hurwitz's Theorem

The argument principle (logarithmic integral) provides a tool for studying the behavior of the zeros of a convergent sequence of analytic functions.

#### Theorem (Hurwitz's Theorem):

Suppose {$f_k(z)$} is a sequence of analytic functions on a domain $D$ that converges normally on $D$ to $f(z)$, and suppose that $f(z)$ has a zero of order $N$ at $z_0$. 

Then there exists $\rho > 0$ such that for $k$ large, $f_k(z)$ has exactly $N$ zeros in the disk {$|z-z_0| < \rho$} counting multiplicity, and these zeros converge to $z_0$ as $k \rightarrow \infin$ 

Proof:

let $\rho > 0$ be sufficiently small so that the closed disk {$|z-z_0| \leq \rho$} is contained in $D$ 

and so that $f(z) \neq 0$ for $0 < |z-z_0| \leq \rho$ (since $z_0$ is an isolated zero?)

Choose $\delta > 0$ such that $|f(z)| \geq \delta$ on the circle $|z-z_0| = \rho$

Since $f_k(z)$ converges uniformly to $f(z)$ for $|z-z_0| \leq \rho$, for $k$ large we have $|f_k(z)| > \delta/2$ for $|z-z_0| = \rho$, and further, $f_k'(z)/f_k(z)$ converges uniformly to $f'(z)/f(z)$ for $|z-z_0| = \rho$ 

Hence the integrals converge:

$\frac{1}{2\pi i}\int_{|z-z_0| = \rho}\frac{f_k'(z)}{f_k(z)}dz \rightarrow \frac{1}{2\pi i}\int_{|z-z_0| = \rho}\frac{f'(z)}{f(z)}dz$ 

The integral on the left is the number $N_k$ of zeros of $f_k(z)$ in the disk {$|z-z_0| < \rho$}

the integral on the right is the number $N$ of zeros of $f(z)$ in the disk

(WHY?: first, since the earlier parts helped us establish $f_k$ and $f(z)$ don't equal zero in the circle and we used the argument principle)

Since $N_k \rightarrow N$, $N_k = N$ for k large: $f_k(z)$ has $N$ zeros satisfying $|z-z_0| < \rho$ 

The Same argument works for smaller $\rho > 0$, so the zeros of $f_k(z)$ must accumulate at $z_0$ 

##### univalent function on a domain $D$: analytic and one-to-one on $D$ 

univalent functions on $D$ are the conformal maps of $D$ to other domains

Applying the preceding theorem to univalent functions, where $N = 1$, we obtain the following:

#### Theorem: (another Hurwitz's theorem?)

Suppose {$f_k(z)$} is a sequence of univalent functions on domain $D$ that converges normally on $D$ to a function $f(z)$. Then either $f(z)$ is univalent or $f(z)$ is constant

Proof:

Suppose the limit function $f(z)$ is not constant:

Suppose $z_0$ and $\zeta_0$ satisfy $f(z_0) = f(\zeta_0) = w_0$ (so not one-to-one)

Then $z_0$ and $\zeta_0$ are zeros of finite order for $f(z) -w_0$ 

By the preceding theorem, there are sequences $z_k \rightarrow z_0$ and $\zeta_k \rightarrow \zeta_0$ such that $f_k(z_k) - w_0 = 0$, and $f_k(\zeta_k) - w_0 = 0$. Since $f_k(z)$ is univalent, we have $z_k = \zeta_k$ and in the limit $z_0 = \zeta_0$ 

Thus $f(z)$ is univalent

#### Example: when the limit of univalent functions isn't univalent, but constant:

$f_k(z) = z/k$ is univalent for $k \geq 1$ on the complex plane

The sequence {$f_k(z)$} converges normally to the constant $f(z) = 0$ 

Thus a normal limit of a sequence of univalent functions need not be univalent, and both alternatives of the theorem occur 

### 4. Open Mapping and Inverse Function Theorems

Let $f(z)$ be a meromorphic function on a domain $D$ 

##### $f(z)$ attains the value $w_0$ $m$ times at $z_0$:

if $f(z) -w_0$ has a zero of order $m$ at $z_0$ 

We make the usual modifications to cover the cases $z_0 = \infin$ and $w_0 = \infin$, so that 

* $f(z)$ attains a finite value $w_0$ $m$ times at $z_0 = \infin$ if $f(1/z) -w_0$ has a zero of order $M$ at $z = 0$ 

* $f(z)$ attains the value $\infin$ $m$ times at $z_0$ if $z_0$ is a pole of $f(z)$ of order $m$ 

The number of times that $f(z)$ attains a value $w_0$ on $D$ is obtained by adding the number of times it attains the value $w_0$ at the various points of $D$ 

#### Examples

##### $z^m + 1$ 

attains the value $w = 1$ $m$ times at $z = 0$ 

attains the value $w = \infin$ $m$ times at $z = \infin$ 

##### polynomial $f(z)$ of degree $m \geq 1$ 

* attains each value $w \in C^*$ $m$ times on $\C^*$, always counting multiplicity
* For fixed finite $w$, $f(z) - w$ is a polynomial of degree $m$ which has $m$ zeros counting multiplicity
* Since $f(z)$ has a pole of order $m$ at $\infin$, it attains the value $w = \infin$ $m$ times at $z = \infin$ 

---

#### Dependence on $w$ of the number of times that an analytic or meromorphic function attains the value $w$ 

Instead of a sequence of functions, we treat functions that depend continuously on a parameter 

1. Let $f(z)$ be a nonconstant analytic function on a domain $D$ 
2. Let $z_0$ $\in$ $D$
3. $w_0 = f(z_0)$ 
4. Assume $f(z)-w_0$ has a zero of order $m$ at $z_0$ 
5. since the zeros of $f(z)-w_0$ are isolated (?), we can choose $\rho > 0$ so that $f(z)-w_0 \neq 0$ for $0 < |z-z_0| \leq \rho$ 
6. Let $\delta > 0$ satisfy $|f(z)-w_0| \geq \delta$ for $|z-z_0| = \rho$ 

##### (4.1) $N(w) = \frac{1}{2\pi i}\int_{|z-z_0| = \rho}\frac{f'(z)}{f(z)-w}dz, |w-w_0| < \delta$ 

(4.1) depends analytically on $w$ 

(No singularities? since $f(z)$ is analytic on $D$)

Since $N(w)$ is the number of zeros of $f(z)-w$ in the disk {$|z-z_0| < \rho$}

The analytic function $N(w)$ is integer-valued, hence constant

* so refer to page 231
* $f(z) -w$ is going to be very close to $f(z)-w_0$ for $\delta$ small
* So the integrals are going to be very close
* and since the values of the integrals are integers, they must be the same

$N(w_0) = m$, so $N(w) = m$ for $|w- w_0| < \delta$ 

Thus each value $w$ satisfying $|w-w_0| < \delta$ is assumed exactly $m$ times, counting multiplicity, by $f(z)$ in the disk {$|z-z_0| < \rho$}

---

Nonconstant analytic functions are "open mappings"

#### Open Mapping Theorem for Analytic Functions

If $f(z)$ is analytic on a domain $D$

and $f(z)$ is nonconstant

$\implies$

$f(z)$ maps open sets to open sets

$\equiv$

$f(U)$ is open for each open subset $U \sub D$

Proof:

let $w_0 \in f(U)$, say $w_0 = f(z_0)$ 

Apply the above to $f(z)$: we obtain a disk centered at $z_0$ of radius $\rho$ that is contained in $U$ such that the values of $f(z)$ on this disk include the disk centered at $w_0$ of radius $\delta$ 

This implies that $f(U)$ is open.

---

Now consider the case where $f(z) -w_0$ has a simple zero at $z_0$ 

$N(w_0) = N_0 = 1$, and we conclude that $N(w) = 1$ for $|w-w_0| < \delta$ 

Thus, every value of $w$ satisfying $|w-w_0| < \delta$ is taken on exactly once by $f(z)$ in the disk {$|z-z_0| < \rho$}

#### Theorem (Inverse Function Theorem)

Suppose

$f(z)$

1. is analytic for $|z-z_0| \leq \rho$ 
2. satisfies $f(z_0) = w_0$ 
3. satisfies $f'(z_0) \neq 0$ 
4. satisfies $f(z) \neq w_0$ for $0 < |z-z_0| \leq \rho$

Let $\delta > 0$ be chosen such that $|f(z) - w_0| \geq \delta$ for $|z-z_0| = \rho$ 

Then for each $w$ such that $|w-w_0| < \delta$

there is a unique $z$ satisfying $|z-z_0| < \rho$ and $f(z) = w$ 

Writing $z = f^{-1}(w)$, we have

##### (4.2) $f^{-1}(w) = \frac{1}{2\pi i}\int_{|\zeta - z_0| = \rho}\frac{\zeta f'(\zeta)}{f(\zeta) - w}d\zeta, |w-w_0| <\delta$  

Proof:

Already established everything but $(4.2)$

Fix $w$ such that $|w-w_0| <\delta$ and set $z = f^{-1}(w)$ so that $f(z) = w$ 

The function 

$\zeta f'(\zeta)/[f(\zeta)-w]$ is an analytic function of $\zeta$ for $|\zeta - z_0| \leq \rho$ 

except for a simple pole at $\zeta = z$ with residue

$\text{Res }[\frac{\zeta f'(\zeta)}{f(\zeta)-w}, z] = \lim_{\zeta \rightarrow z}\frac{(\zeta -z)\zeta f'(z)}{f(\zeta)-w} = z$ 

Residue Theorem yields (4.2) immediately

---

We remark that this gives an alternative proof of the existence of a locally defined inverse for $f(z)$ when $f'(z) \neq 0$ which depends on the residue theorem rather than on the inverse function theorem.

This procedure also gives an explicit disk on which the inverse function is defined

The explicit formula (4.2) shows that the inverse function is analytic (how? analytic w.r.t to $w$....)

