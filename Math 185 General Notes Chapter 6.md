# Math 185 Chapter 6 General Notes

## Laurent Series and Isolated Singularities

### 1. The Laurent Decomposition

Splits a function analytic in an annulus as the sum of a function analytic inside the annulus and a function analytic outside the annulus.

#### Theorem (Laurent Decomposition)

Suppose $0 \leq \rho < \sigma \leq +\infin$ and suppose $f(z)$ is analytic for $\rho < |z-z_0| < \sigma$ 

Then $f(z)$ can be decomposed as a sum

##### (1.1) $f(z) = f_0(z)+f_1(z)$

where $f_0(z)$ is analytic for $|z-z_0| < \sigma$ 

and $f_1(z)$ is analytic for $|z-z_0| > \rho$  and at $\infin$ 

If we normalize the decomposition so that $f_1(\infin) = 0$, then the decomposition is unique.

---

If $f(z)$ is already analytic for $|z-z_0| < \sigma$, $f_0(z) = f(z), f_1(z) = 0$ 

If $f(z)$ is already analytic for $|z-z_0| > \rho$ and vanishes at $\infin$, $f_0(z) = 0$, $f_1(z) = f_1(z)$ 

**proof of uniqueness**:

let $f(z) = g_0(z) + g_1(z)$ be another

##### (1.2) $g_0(z)-f_0(z) = f_1(z)-g_1(z)$ for $\rho < |z-z_0| < \sigma$

let $h(z) = g_0 - f_0$ for $|z-z_0| < \sigma$ 

let $h(z) = f_1-g_1$ for $|z-z_0| > \rho$ 

these domains overlap in $\rho < |z-z_0| < \sigma$ and the two def. of $h$ agree here

so $h(z)$ is defined for all $\C$ and is entire, so because $h(z) \rightarrow 0$ as $z \rightarrow \infin$ 

it is constant and $h(z) \equiv 0$, so we have $g_0 = f_0$, $g_1 = f_1$ 

---

**To find such a decomposition, we apply Cauchy integral representation theorem on an annulus:**

1. Choose $r$ and $s$ such that $\rho < r < s< \sigma$ 
2. Cauchy Integral formula for an annulus yields
   1. $f(z) = \frac{1}{2\pi i}\oint_{|\zeta - z_0| = s}\frac{f(\zeta)}{\zeta -z}d\zeta - \frac{1}{2\pi i}\oint_{|\zeta - z_0| = r}\frac{f(\zeta)}{\zeta -z}d\zeta$ 
   2. valid for $r < |z-z_0| < s$ 
3. $f_0(z) = \frac{1}{2\pi i}\oint_{|\zeta - z_0| = s}\frac{f(\zeta)}{\zeta - z}d\zeta$, $|z-z_0| < s$ is analytic for $|z-z_0| < s$ 
4. $f_1(z) = - \frac{1}{2\pi i}\oint_{|\zeta - z_0| = r}\frac{f(\zeta)}{\zeta -z}d\zeta$ is analytic for $|z-z_0| > r$, and tends to $0$ as $z \rightarrow \infin$ 

Note: This decomposition technically depends on $r$ and $s$, but the uniqueness assertion already established shows that the decomposition is independent of $r$ and $s$, so $f_0, f_1$ are defined for the annulus and have the properties of the theorem

---

#### Example: $f(z) = 1/(z-1)(z-2)$ 

$f(z)$ is already analytic for $|z| < 1$ and $|z| > 2$ so trivial decompositions here

but for $1 < |z| < 2$, $f(z)$ is not analytic for $|z|  >1$ nor for $|z| < 2$ 

Using partial fraction decomposition:

$A/(z-1) + B/(z-2)$

$Az - 2A + Bz - B = 1$

$-2A - B = 1$

$Az +Bz = 0$

$A = -B$

$-2A + A = 1$, $A = -1$, $B= 1$ 

$f(z) = \frac{1}{z-2} - \frac{1}{z-1}$ 

####  Example: $f(z) = 1/\sin z$ 

Has one with respect to each annulus $n\pi < |z| < (n+1)\pi$ 

---

Suppose now: $f(z) = f_0(z)+f_1(z)$ is the Laurent decomposition for a function analytic for $\rho < |z-z_0| < \sigma$ 

We can express $f_0(z)$ as a power series in $|z-z_0|$

$f_0(z) = \sum_{k=0}^\infin a_k(z-z_0)^k, |z-z_0| < \sigma$ 

where the series converges absolutely, and for any $s < \sigma$ it converges uniformly for $|z-z_0| \leq s$ (positive distances away from $\sigma$)

We can express $f_1(z)$ as a series of negative powers of $z-z_0$, with zero constant term because $f_1(z) \rightarrow 0$ at $\infin$

$f_1(z) = \sum_{k=-\infin}^{-1}a_k(z-z_0)^k, |z-z_0| > \rho$  

$\equiv$ $f_1(z) = \sum_{k=1}^\infin \frac{a_k}{(z-z_0)^k}$ , $|z-z_0| > \rho$ 

* converges absolutely
* for any $r > \rho$ converges uniformly for $|z-z_0| \geq r$ 

adding the two series:

##### (1.3) Lauren series expansion of $f(z)$ w.r.t. the annulus $\rho < |z-z_0| < \sigma: f(z) = \sum_{k=-\infin}^\infin a_k(z-z_0)^k, \rho <|z-z_0| < \sigma$ 

* converges absolutely
* converges uniformly for $r \leq |z-z_0| \leq s$ 

##### (1.4) $a_n = \frac{1}{2\pi i}\oint_{|z-z_0| =r}\frac{f(z)}{(z-z_0)^{n+1}}dz$ , $-\infin  < n < \infin$ 

---

#### Theorem: Laurent Series Expansion

Suppose $0 \leq \rho  < \sigma \leq \infin$ and suppose $f(z)$ is analytic for $\rho < |z-z_0| < \sigma$ 

Then $f(z)$ has a Laurent expansion $(1.3)$ that converges absolutely at each point of the annulus, and that converges uniformly on each subannulus $r \leq |z-z_0| \leq s$, where $\rho < r <s < \sigma$. The coefficients are uniquely determined by $f(z)$, and they are given by $(1.4)$ for any fixed $r, \rho < r < \sigma$ 

---

The largest open domain on which the full Laurent series $(1.3)$ converges is the largest open annulus set centered at $z_0$ containing the annulus {$\rho < |z-z_0| < \sigma$} to which $f(z)$ extends analytically

* punctured disk, full disk or punctured complex plane, full complex plane

**Exercise**: Consider the Laurent series $f(z) = (z^2 -\pi^2)/\sin z$ that is centered at 0 and that converges for $|z| = 1$. What is the largest open set on which the series converges?

$(z-\pi)(z+\pi)/\sin z$ 

$\sin z$ has a simple zero at $\pi$ 

so $\sin z$ power series centered at $\pi$?

$a_0 = \sin(\pi)$, $a_1 = \cos(\pi)$, $a_2 = 0$, $a_3 = -\cos(\pi)/3!$ 

so $a_{2k + 1} = -\frac{1}{(2k+1)!}$, $a_{2k + 3} = \frac{1}{(2k+3)!}$

either way, $\sin z/(z-\pi)$ has a power series: $-1 + (z-\pi)^2/3! - (z-\pi)^4/(5!)+...$

so $(\sin z)/(z-\pi)$ extends to be analytic and nonzero at $z = \pi$  which means 

because $\sin z/(z-\pi)$ doesn't disappear at $z = \pi$, 

we can say $(z+\pi)/(\sin z/(z-\pi))$ is analytic at $z = \pi$ 

$(z^2 - \pi^2)/\sin z$ extends to be analytic at $z = \pi$ 

similarly for $z \rightarrow - \pi$ 

so $z^2 - \pi^2/\sin z$ extends analytically to $z = \pm \pi$ 

as $z \rightarrow \pm2\pi, 0$, $f(z) \rightarrow \infin$  

so the largest annulus on which the series converges is the punctured disk $0 < |z| < 2\pi$ 

## 2. Isolated Singularities of an Analytic Function

A point $z_0$ is an **isolated singularity** of $f(z)$ if $f(z)$ is analytic in some punctured disk {$0 < |z-z_0| < r$} centered at $z_0$ 

Suppose $f(z)$ has an isolated singularity at $z_0$

Then $f(z)$ has a Laurent series expansion

$(2.1)$ $f(z) = \sum_{k=-\infin}^\infin a_k(z-z_0)^k$, $0<|z-z_0| < r$ 

three types of isolated singularity according to whether no negative powers of $z-z_0$ appears, finitely many, or infinitely many appear 

##### removable singularity (no negative powers of $z-z_0$)

the isolated singularity of $f(z)$ at $z_0$ is removable singularity, if $a_k = 0$ for all $k < 0$ 

"a proof?"

The Laurent series becomes a power series if $a_k = 0$ for $k < 0$ 

$f(z) = \sum_{k=0}^\infin a_k(z-z_0)^k$ , $0 < |z-z_0| < r$ 

**Defining $f(z_0) = a_0$ makes $f(z)$ an analytic function on the entire disk {$|z-z_0| < r$}**

---

**if $f(z)$ has a removable singularity at $z_0$, then $f(z)$ is bounded near $z_0$ ** 

​	is this because $f(z_0) = a_0$?, and $f(z)$ is analytic and therefore continuous near $z_0$?

There is a converse of this statement:

### Riemann's Theorem on Removable Singularities

Let $z_0$ be an isolated singularity of $f(z)$. If $f(z)$ is bounded near $z_0$, then $f(z)$ has a removable singularity at $z_0$ 

Proof:

1. expand $f(z)$ in a Laurent series like in $(2.1)$ 
2. Use formula $(1.4)$ for the coefficients
3. Suppose $|f(z)| \leq M$ for $z$ near $z_0$ and let $r > 0$ be small
4. Use ML-estimate to estimate the integral in $(1.4)$ and get $|a_n| \leq \frac{1}{2\pi}\frac{M}{r^{n+1}}(2\pi r) = \frac{M}{r^n}$ 
5. if $n < 0$, the right hand side tends to $0$ as $r \rightarrow 0$ 
6. conclude $a_n = 0$ for $n < 0$, and consequently the singularity at $z_0$ is removable

---

##### pole (finitely many negative powers of $z-z_0$)

The isolated singularity of $f(z)$ at $z_0$ is defined to be a **pole** if there is $N > 0$ such that $a_{-N} \neq 0$, but $a_k = 0$ for all $k < -N$ 

###### **order of the pole** is the integer $N$ 

The Laurent series for this becomes

$f(z) = \sum_{k = -N}^\infin a_k(z-z_0)^k$ 

##### principal part of $f(z$) at the pole $z_0$:

$P(z) = \sum_{k=-N}^{-1}a_k(z-z_0)^k$

the sum of the negative powers

**The principal part $P(z)$ coincides with the summand $f_1(z)$ in the Laurent decomposition $f(z) = f_0(z) +f_1(z)$ **

"bad behavior of $f(z)$ at $z_0$ is incorporated into $P(z)$ in the sense that $f(z)-P(z)$ is analytic at $z_0$"

##### simple pole: a pole of order one

$a_{-1} \neq 0$

##### double pole: a pole of order two

$a_{-2} \neq 0$ 

---

#### Examples of poles

#####  $1/z$: simple pole at $0$

$a_n = \frac{1}{2\pi}\oint_{|z| = r}\frac{1/z}{(z)^{n+1}}$ 

$z = re^{i\theta}$

$a_n = \frac{1}{2\pi}\int_0^{2\pi}\frac{1}{re^{i\theta}r^{n+1}e^{i(n+1)\theta}}rie^{i\theta}d\theta$

$a_n = \frac{i}{2\pi}\int_0^{2\pi}\frac{1}{r^{n+1}e^{i(n+1)}\theta}d\theta$

so if $ n < -1$, $a_n = 0$ 

so $1/z$ has a simple pole

##### $1/(z-i)^2$ double pole at $i$

$a_n = \frac{1}{2\pi}\oint_{|z-i| = r}\frac{1/(z-i)^2}{(z-i)^{n+1}}dz$

$z = i + re^{i\theta}$

$a_n = \frac{i}{2\pi}\int_0^{2\pi}\frac{1}{r^{n+2}{e^{i(n+2)\theta}}}d\theta$ 

so like earlier, if $n < -2$, $a_n = 0$

---

### Theorem

Let $z_0$ be an isolated singularity of $f(z)$. Then $z_0$ is a pole of $f(z)$ of order $N$ if and only if $f(z) = g(z)/(z-z_0)^N$, where $g(z)$ is analytic at $z_0$ and $g(z_0) \neq 0$ 

Proof:

if $f(z)$ has a pole of order $N$ at $z_0$, then $f(z)$ has the laurent series as above that is valid for $0 < |z-z_0| < r$ 

* the series converges for the punctured disk of radius $r$ to $f(z)$ 
* convergence of a power series largely depends on $a_k$, so the coefficients which means that multiplying this series by $(z-z_0)^N$ doesn't change its convergence

the power series, $f(z)(z-z_0)^{N}$ 

$a_{-N} + a_{-N+1}(z-z_0) + a_{-N+2}(z-z_0)^2 + . . . $ converges to a function $g(z)$ that is analytic at $z_0$ 

Converse:

If $g(z)$ is analytic at $z_0$ and satisfies $g(z_0) \neq 0$, then $f(z) = g(z)/(z-z)^N$ has Laurent series with leading term $g(z_0)/(z-z_0)^N$, so that $f(z)$ has a pole of order $N$ at $z_0$ 

---

### Theorem 

Let $z_0$ be an isolated singularity of $f(z)$. Then $z_0$ is a pole of $f(z)$ of order $N$ if and only if $1/f(z)$ is analytic at $z_0$ and has a zero of order $N$ 

Proof:

$f(z)$ has a pole of order $N$ at $z_0$ 

Let $g(z) = (z-z_0)^Nf(z)$ be as above

$g(z_0) \neq 0$ so the function $h(z) = 1/g(z)$ is analytic at $z_0$ with $h(z_0) \neq 0$ 

so $1/f(z) = (z-z_0)^N h(z)$ has a zero of order $N$ at $z_0$ 

Converse:

$1/f(z)$ is analytic at $z_0$ and has a zero of order $N$

which means $1/f(z) = (z-z_0)^Nh(z)$ for some function $h(z)$ that satisfies $h(z_0) \neq 0$ 

and $h(z)$ is analytic near $z_0$

and since $h(z_0) \neq 0$, $1/h(z) = g(z)$ is analytic near $z_0$ and doesn't equal $0$ at $z_0$ 

and we have  $f(z) = g(z)/(z-z_0)^N$ has a pole of order $N$ at $z_0$ 

---

##### Notes from exercise

1. recall that largest open set on which Laurent series converges is (sometimes?) the largest open annular set such that $1/\sin z$ extends analytically and containing the circle of interest....(?) 
2. remember to use the fact that the principal part of $f(z)$ at the pole coincides with $f_1(z)$  but not exactly...
3. expanded $\sin z = (z-z_0) + \mathcal{O}((z-z_0)^3)$ where $z_0$ are the singularities of $1/\sin z$ to find that $1/\sin z = \frac{\cos(z_0)}{z-z_0} + analytic$ 
4. so $1/\sin z - \cos(z_0)/(z-z_0)$ is analytic
5. and we have $f_1(z) = $ the sum of all such $-\cos(z_0)/(z-z_0)$ so that $f_0(z) = 1/\sin z - f_1(z)$ is analytic for $|z| < 2\pi$ 
6. and we have $f_0 + f_1$ is the Laurent decomposition for $1/\sin z$  

---

##### A meromorphic function $f(z)$ on a domain $D$ 

is a function $f(z)$ that is analytic on $D$ except possibly at isolated singularities, each of which is a pole

###### sums and products of meromorphic functions are meromorphic

###### quotients of meromorphic functions are meromorphic if the denominator is not IDENTICALLY zero

###### What if there are infinitely many pole of $f(z)$ in $D$

arrange them in a sequence that accumulates only at the boundary of $D$ 

Else there would be a point of accumulation IN $D$ of the poles of $f(z)$, and this point would not be an isolated singularity, since for this point, let's call it $z_0$, there are infinitely many singularities in any disk centered on $z_0$, which contradicts the definition of an isolated singularity

##### Examples of meromorphic functions

$1/\sin z$ is meromorphic on the entire complex plane

$R(z)$, a rational function can be expressed as $R(z)  = c\frac{(z-\zeta_1)^{m_1}\cdots (z-\zeta_k)^{m_k}}{(z-z_1)^{n_1}\cdots (z-z_l)^{n_l}}$

where the $\zeta_j's, z_j's$ are all distinct

$R(z)$ has a zero of order $m_j$ at each $\zeta _j$ and a pole of order $n_j$ at each $z_j$ 

so $R(z)$ is meromorphic on the entire complex plane

### Theorem

Let $z_0$ be an isolated singularity of $f(z)$. Then $z_0$ is a pole if and only if $|f(z)| \rightarrow \infin$ as $z\rightarrow z_0$ 

Proof:

If $f(z)$ has a pole of order $N$ at $z_0$, then $g(z) = (z-z_0)^Nf(z)$is analytic and nonzero at $z_0$, so

$|f(z)| = |z-z_0|^{-N}|g(z)| \rightarrow \infin$ as $z \rightarrow z_0$ 

Converse: use Riemann's theorem on removable singularities 

Suppose $|f(z)| \rightarrow \infin$ as $z\rightarrow z_0$

Then $f(z) \neq 0$ for $z$ near $z_0$ 

so $h(z) = 1/f(z)$ is analytic in some punctured neighborhood of $z_0$ 

$h(z) \rightarrow 0$ as $z\rightarrow z_0$

Riemann's theorem: $h(z)$ extends to be analytic at $z_0$ since $h(z)$ is bounded near $z_0$ 

moreover $h(z_0) = 0$

If $N$ is the order of the zero of $h(z)$ at $z_0$, then $f(z)  = 1/h(z)$ has a pole of order $N$ at $z_0$ 

---

##### essential singularity (has infinitely many powers of $(z-z_0)^k$)

isolated singularity of $f(z)$ at $z_0$ is an essential singularity if $a_k \neq 0$ for infinitely many $k < 0$

so an isolated singularity that is neither removable nor a pole is essential

###### example: $e^{1/z}$ has essential singularity at $z = 0$ 

**At an essential singularity, the values of $f(z)$ cluster towards the entire complex plane**

### Casorati-Weierstrass Theorem

Suppose $z_0$ is an essential singularity of $f(z)$, then for every complex number $w_0$ there is a sequence $z_n \rightarrow z_0$ such that $f(z_n) \rightarrow w_0$ 

Proof by contraposition:

suppose there is a $w_0$ such that there is not a limit of values of $f(z)$ as above

then there is some small $\epsilon > 0$ such that $|f(z) -w_0| > \epsilon$ for all $z$ near $z_0$ 

so $h(z) = 1/(f(z)-w_0)$ is bounded near $z_0$ 

so $h(z)$ has a removable singularity at $z_0$ 

so $h(z) = (z-z_0)^Ng(z)$ for some $N \geq 0$ and some analytic function $g(z)$ with $g(z_0) \neq 0$ 

**this is due to the whole power series may be written as above

so $f(z) - w_0 = 1/h(z) = (z-z_0)^{-N}/g(z)$, where $1/g(z)$ is analytic at $z_0$ 

if $N = 0$, f(z) extends to be analytic at $z_0$ 

if $N > 0$, $f(z)$ has a pole of order $N$ at $z_0$ 

because $f(z) = (z-z_0)^{-N}/g(z) + w_0$, which has $f(z) \rightarrow \infin$ as $z \rightarrow z_0$

## 3. Isolated Singularity at Infinity

$f(z)$ has isolated singularity at $\infin$ if $f(z)$ is analytic outside some bounded set

* so $\exists R > 0$ s.t. $f(z)$ analytic for $|z|  > R$ 

$f(z)$  has an isolated singularity at $\infin$  if and only if $g(w) = f(1/w)$ has an isolated singularity at $w = 0$ 

Suppose $f(z)$ has Laurent series expansion 

$f(z) = \sum_{k=-\infin}^\infin b_k z^k, |z| >R$ 

**removable**, $b_k = 0, \forall k > 0$ , so $f(z)$ is analytic at $\infin$ 

**essential**, $b_k \neq 0$ for infinitely many $k > 0$ 

**pole of order N**, if $b_N \neq 0$, while $b_k =0 $ for all $k > N$ 

$P(z) = b_N z^N + . . . + b_0$ (principal part of $f(z)$ at $\infin$ ) 

Examples:

polnomial degree $N \geq 1$: pole of order $N$ at infinity, principal part is itself

$e^z$ has essential singularity at $\infin$ 

## 4. Partial Fractiosn Decomposition

##### meromorphic function $f(z)$  on domain $D$ in the extend complex plane $\C^*$ 

$f(z)$ is analytic on $D$ except possibly at isolated singularities, each of which is a pole

* closed under sums and products
* quotients are meromorphic provided denominator is not identically zero

**Any rational function is meromorphic on the extended complex plane $\C^*$ including at $\infin$ **

Want to establish converse:

### Theorem: A meromorphic function on the extended complx plane $\C^*$ is rational

* must have finite number of poles
* $P_{\infin}$ is a polynomial, either equal to $f(\infin)$ (is analytic) or the principal part of $f(z)$ at $\infin$ (is a pole)
* $f(z) - P_{\infin}(z) \rightarrow 0$ as $z \rightarrow \infin$ 
* $z_1, . . ., z_m$  are the poles of $f(z)$ in the finite complex plane $\C$ 
* $P_k(z)$ is the principal part of $f(z)$  at $z_k$ 
* $P_k(z)  = \frac{\alpha_1}{z-z_k}  + \frac{\alpha_2}{(z-z_k)^2}+. . . + \frac{\alpha_n}{(z-z_k)^n}$ 
  * analytic at $\infin$, and vanishes there
* let $g(z) = f(z) - P_{\infin}(z) - \sum_{j=1}^m P_j(z)$ 
  * $g(z)$ is analytic at each $z_k$ so it is entire
  * and $g(z) \rightarrow 0$ as $z \rightarrow \infin$ 
* so by Liouville's theorem, $g(z) = 0$ 

##### (4.1) partial fractions decomposition of rational $f(z)$: $f(z) = P_{\infin}(z) + \sum_{j=1}^m P_j(z)$ 

### Theorem:

Every rational function has a partial fractions decomposition expressing it as the sum of a polynomial in $z$ and its principal parts at each of its poles in the finite complex plane