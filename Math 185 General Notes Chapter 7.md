# Math 185 General Notes Chapter 7

## The Residue Calculus

### 1. The Residue Theorem

Suppose $z_0$ is an isolated singularity of $f(z)$ and that $f(z)$ has Laurent series:

$f(z) = \sum_{n = -\infin}^\infin a_n(z-z_0)^n, 0  < |z-z_0| < \rho$ 

##### residue of $f(z)$ at $z_0$: 

the coefficient $a_{-1}$ of $1/(z-z_0)$ in the Laurent Expansion of $f(z)$ centered at $z_0$ on the punctured disk of radius $ \rho$

##### (1.1) $\text{Res}[f(z), z_0] = a_{-1} = \frac{1}{2\pi i}\oint_{|z-z_0| = r} f(z)dz$, $0 < r < \rho$ 

##### Examples: Just from Definition Alone

$\text{Res}[\frac{1}{z}, 0] = 1$

$\text{Res}[\frac{1}{(z-z_0)^2}, z_0] = 0$

##### Examples: Using Partial Fractions Decomposition

$\frac{1}{z^2 + 1} = \frac{1}{2i}[\frac{1}{z-i} - \frac{1}{z+i}] = \frac{1}{2i}\frac{1}{z-i} + [\text{analytic at }i]$ 

yields

$\text{Res}[\frac{1}{z^2 + 1}, i] = \frac{1}{2i}$ 

Why:

if a function is analytic, then the line integral around a boundary will be $0$ 

and $\frac{1}{2\pi i}\frac{1}{2i}\oint_{|z-i| = r} \frac{1}{z-i}dz$

$z = i + re^{i\theta}$ so 

$\int_0^{2\pi} \frac{rie^{i\theta}}{re^{i\theta}} d\theta =2\pi i $

so using that, we get $a_{-1} = \frac{1}{2i}$ 

---

#### Theorem (Residue Theorem): important tool for evaluating complex line integrals

* extends Cauchy's theorem by allowing for a finite number of singularities inside the contour of integration
* When there are no singularities, theorem reduces to Cauchy's Theorem

Statement of Theorem:

Let $D$ be a bounded domain in the complex plane with piecewise smooth boundary. Suppose that $f(z)$ is analytic on $D \cup \partial D$, except for a finite number of isolated singularities $z_1, . . ., z_m$ in $D$. Then

##### (1.2) $\int_{\partial D} f(z) dz = 2\pi i \sum_{j =1}^m \text{Res}[f(z), z_j]$ 

#### Four Rules for Calculating Residues

##### Rule 1. $f(z)$ has a simple pole at $z_0$ 

$\text{Res}[f(z), z_0] = \lim_{z\rightarrow z_0}(z-z_0)f(z)$ 

Proof:

The Laurent Series of $f(z)$:

$f(z) = \frac{a_{-1}}{z-z_0} + [\text{analytic at }z_0]$

 NOte: once we obtain an expression for $(z-z_0)f(z)$ as an analytic function, the limit is evaluated by simply plugging $z = z_0$ into the expression

###### Example of Rule 1

$\text{Res}[\frac{1}{z^2 + 1}, i] = \lim_{z\rightarrow i}\frac{z-i}{z^2 + 1} = \lim_{z\rightarrow i}\frac{1}{z+i} = \frac{1}{z+i}|_{z= i} = \frac{1}{2i}$ 

##### Rule 2. $f(z)$ has a double pole at $z_0$ 

$\text{Res}[f(z), z_0] = \lim_{z\rightarrow z_0} \frac{d}{dz}[(z-z_0)^2 f(z)]$ 

Proof:

The Laurent expansion:

$f(z) = \frac{a_{-2}}{(z-z_0)^2} + \frac{a_{-1}}{z-z_0} + a_0 + \cdots $ $\implies$ 

We obtain a power series expansion:

$(z-z_0)^2 f(z) = a_{-2} + a_{-1}(z-z_0) + a_0(z-z_0)^2 + \cdots$

Differentiate this: 

$a_{-1} + 2a_0(z-z_0) + O((z-z_0)^2)$

Plug in $z = z_0$ to get $a_{-1}$ 

---

Note about Rule 2: It can be regarded as the formula for the coefficient of $z-z_0$ in the power series expansion of the analytic function $(z-z_0)^2 f(z)$ 

---

###### Example of Rule 2:

$1/(z^2+1)^2$ has double poles at $\pm i$ 

$\text{Res}[\frac{1}{(z^2+1)^2}, i] = \lim_{z\rightarrow i}\frac{d}{dz}\frac{1}{(z+i)^2} = \frac{-2}{(z+i)^3}|_{z= i} = \frac{-2}{-8i} = \frac{1}{4i}$

##### Rule 3. for $\frac{f(z)}{g(z)}$ if $f, g$ are analytic at $z_0$ and $g(z)$ has a simple zero at $z_0$ 

$\text{Res}[\frac{f(z)}{g(z)}, z_0] = \frac{f(z_0)}{g'(z_0)}$

Proof:

* $f(z)/g(z)$ has at most a simple pole at $z_0$, so use Rule 1
  * $g(z) = h(z)(z-z_0)$
  * $f(z)/g(z) = \frac{f(z)}{h(z)(z-z_0)}$ 
  * $g(z)/f(z) = \frac{h(z)(z-z_0)}{f(z)}$ , a zero of at most order $1$ at $z_0$, since $h(z_0) \neq 0$ and possible that $f(z)$ has a zero at $z_0$ , which means $f(z)/g(z)$ has at most a simple pole at $z_0$ 
* $\lim_{z\rightarrow z_0}(z-z_0)\frac{f(z)}{g(z)} = \lim_{z\rightarrow z_0}\frac{f(z)}{(g(z)-g(z_0))/(z-z_0)}$
  * Why? $g(z_0) = 0$ so $g(z)/(z-z_0)$ $= (g(z) - 0)/(z-z_0)$ $= (g(z)-g(z_0))/(z-z_0)$ 
* Using definition of a derivative this equals $ \frac{f(z_0)}{g'(z_0)}$ 

###### Example of Rule 3

$z^3/(z^2+1)$ Using Partial Fractions Decomposition

$\frac{z^3}{z^2+1} = z - \frac{1}{2}\frac{1}{z-i} - \frac{1}{2}\frac{1}{z+i}$, residues are $- \frac{1}{2}$ for both $\pm i$  

* I'm guessing from integrating?

Using Rule 3:

$f(z) = z^3$, $g(z) = z^2 + 1$, $\frac{f(\pm i)}{g'(\pm i)} = \frac{z^3}{2z}|_{z= \pm i} = \frac{z^2}{2}|_{z= \pm i} = -\frac{1}{2}$

##### Rule 4. for $\frac{1}{g(z)}$, if $g(z)$ is analytic and has a simple zero at $z_0$

$\text{Res}[\frac{1}{g(z)}, z_0] = \frac{1}{g'(z_0)}$ 

###### Example of Rule 4

$1/(z^2 + 1)$, at $i$

$\frac{1}{2z}|_{z= i} =  \frac{1}{2i}$

### 2. Integrals Featuring Rational Functions

##### (2.1) $\int_{-\infin}^\infin \frac{dx}{1+x^2} = \pi$ 

$\frac{d}{dx}[\arctan x] = \frac{1}{1+x^2}$

and $\lim_{x \rightarrow \infin} \arctan x = \pi/2$

$\lim _{x\rightarrow - \infin}\arctan x = -\pi/2$ 

so $\arctan(\infin) - \arctan{-\infin} = \pi $

---

To Evaluate (2.1) using contour integration:

Let $D_R$ be the half-disk in the upper half-plane bounded by the interval $[-R, R]$ on the real axis and the semicircular contour $\Gamma_R$ of radius $R$ in the upper half-plane 

The function $\frac{1}{1+z^2}$ has one pole in $D_R$: a simple pole at $i$ with residue $1/2i$ 

The Residue Theorem yields:

$\int_{\partial D_R} \frac{dz}{1 + z^2} = 2\pi i \text{Res}[\frac{1}{1+z^2}, i] = 2\pi i\cdot \frac{1}{2i} = \pi$

Now:

$\int_{\partial D_R}\frac{dz}{1+z^2} = \int_{-R}^R \frac{dx}{1+x^2} + \int_{\Gamma_R}\frac{dz}{1+z^2}$

On $\Gamma_R$:

$|1/(1+z^2)| \leq 1/(R^2 - 1) \sim 1/R^2$

the length of $\Gamma_R$ is $\pi R$ , so by $ML$-estimate

$|\int_{\Gamma_R}\frac{dz}{1+z^2}| \leq \frac{1}{R^2 -1}\cdot \pi R \sim \frac{1}{R}$ 

which tends to $0$ as $ R\rightarrow \infin$

so $\int_{\partial D_R}\frac{dz}{1+z^2} = \pi = \int_{-R}^R \frac{dx}{1+x^2} + 0$  

so $\lim_{R\rightarrow \infin}\int_{-R}^R \frac{dx}{1+x^2} = \pi $ 

---

##### (2.2) $\int_{-\infin}^\infin \frac{P(x)}{Q(x)}dx$ 

$P(z), Q(z)$ are polynomials

$Q(z)$ has no zeros on the real axis

For convergence, it is required that:

##### (2.3) $\deg Q(z) \geq \deg P(z) + 2$

The integral is evaluated by integrating $P(z)/Q(z)$ around the boundary of a half-disk in the upper-half-plane and letting the radius tend to $\infin$ 

##### (2.4) $\int_{-\infin}^\infin \frac{P(x)}{Q(x)} dx = 2\pi i \sum \text{Res}[\frac{P(z)}{Q(z)}, z_j]$ 

summed over the poles $z_j$ of $P(z)/Q(z)$ in the upper half-plane

---

The same contour can be used to evaluate the integrals of rational functions times trigonometric functions

$\int_{-\infin}^\infin \frac{P(x)}{Q(x)}\cos(\alpha x)dx$ 

$P(z), Q(z)$ have real coefficients and satisfy $(2.3)$ 

The cosine function is essentially a hyperbolic cosine on the imaginary axis which grows exponentially fast, so $\cos(\alpha z)$ behaves too badly in the upper half plane

Trick: substitute $e^{iz}$ for the cosine function in the contour integr

and to recover the cosine integral at the end, take real parts

$e^{i(x+iy)} = e^{-y}$ $\implies$ $e^{iz}$ is bounded by $1$ in the upper half-plane

so $|e^{iz}| \leq 1$, $\Im (z) \geq 0$

##### Example: Contour integration of $\frac{\cos(a x)}{1 + x^2}dx$ , $a > 0$

##### (2.5) $\frac{\cos(a x)}{1 + x^2}dx = \pi e^{-a}$, $a  > 0$ 

Let $D_R$ be the half-disk in the upper half-plane bounded by $[-R, R]$ on the real axis and the semicircular contour $\Gamma_R$ of radius $R$ in the upper half-plane

We integrate $e^{iaz}/(1+z^2)$ over the boundary of $D_R$ 

function only has one pole in the upper half-plane, a simple pole $i$ 

With residue calculated by Rule 3:

$\text{Res}[\frac{e^{iaz}}{1+z^2}, i] = \frac{e^{iaz}}{2z}|_{z = i} = \frac{e^{-a}}{2i}$ 

So 

$\int_{\partial D_R}\frac{e^{iaz}}{1+z^2}dz = 2\pi i \cdot \frac{e^{-a}}{2i } = \pi e^{-a}$

since $|e^{iaz} \leq 1|$ in the upper half-plane, ML-estimate yields

$|\int_{\Gamma_R}\frac{e^{iaz}}{1+z^2}dz| \leq \frac{1}{R^2-1}\cdot \pi R \sim \frac{1}{R}$ 

so $\int_{\partial D_R} \frac{e^{iaz}}{1+z^2}dz = \int_{-R}^R \frac{e^{iax}}{1+x^2}dx + \int_{\Gamma_R}\frac{e^{iaz}}{1+z^2}dz$ 

so passing to the limit as $R \rightarrow \infin$ we have

$\int_{-R}^R \frac{e^{iax}}{1+x^2}dx = \pi e^{-a}, a > 0$  

and $e^{iax} = \cos(ax) + i \sin(ax)$ 

so taking the real part, we have $(2.5)$ 

### 3. Integrals of Trigonometric Functions

Some definite integrals can be evaluated through converting to complex contour integrals and using the residue theorem

##### (3.1) $\int_0^{2\pi}\frac{d\theta}{a + \cos \theta}, a > 1$ 

Idea: convert to a complex contour integral around the unit circle

$z = e^{i\theta}$ 

$dz = ie^{i\theta}d\theta = iz d\theta$ 

we have $d\theta = \frac{dz}{iz}$ 

$\cos \theta = \frac{e^{i\theta}+e^{-i\theta}}{2} = \frac{z + 1/z}{2}$

$\sin \theta  = \frac{e^{i\theta}-e^{-i\theta}}{2}= \frac{z - 1/z}{2i}$

so substituting:

$\int_0^{2\pi} \frac{d\theta}{a + \cos \theta}= \oint_{|z| = 1}\frac{1}{a + \frac{1}{2}(z+1/z)}\frac{dz}{iz}$$=$$\frac{2}{i}\oint_{|z| = 1}\frac{dz}{z^2 + 2az  + 1}$

the poles of the integrand:

$\frac{-2a \pm \sqrt{4a^2-4 }}{2} = -a \pm \sqrt{a^2 -1}$

only one of these roots is inisde the unit circle, $-a + \sqrt{a^2 -1}$ 

And using rule 3, with $z_0 = -a + \sqrt{a^2-1}$ 

$\text{Res}[\frac{1}{z^2 + 2az+1}, z_0] = \frac{1}{2z + 2a}|_{z= z_0} = \frac{1}{2\sqrt{a^2 -1}}$

so

##### (3.2) $\int_0^{2\pi}\frac{d\theta}{a+\cos \theta}= \frac{2}{i}\cdot 2\pi i \cdot \frac{1}{2\sqrt{a^2-1}}$ $=$$\frac{2\pi}{\sqrt{a^2-1}}$ 

---

Consider $(3.1)$ but instead of positive real $a$, we replace it with a complex parameter $w$ 

##### (3.3) $\int_0^{2\pi}\frac{d\theta}{w + \cos \theta} = \frac{2\pi}{\sqrt{w^2-1}}$ , $w \in \C\setminus[-1, 1]$ 

the right hand side of the identity corresponds to the branch of $\sqrt{w^2-1}$ that is positive on the real interval $(1, +\infin$)

Proof:

The functions appearing on each side of the identity $(3.3)$ are analytic for $w$ in the slit plane $\C \setminus [-1, 1]$ 

The identity, $(3.2)$ shows that these two analytic functions coincide for $w \in (1, +\infin)$ 

By the uniqueness principle, these two analytic functions coincide for all $w \in \C \setminus [-1, 1]$ 

### 4. Integrands with Branch Points

Integrals featuring $x^a$ and $\log x$ can sometimes be evaluated using contour integration

**It is important to specify carefully the branch of the function $z^a$ or $\log z$ used in the complex integral** 

Illustration:

##### (4.1) $\int_0^\infin \frac{x^a}{(1+x^2)}dx = \frac{\pi a}{\sin(\pi a)}$ , $-1 < a < 1$ 

easily seen to be $1$ if $a = 0$ 

so suppose $a \neq 0$ 

consider t

the branch of the function $z^a/(1+z^2)$ defined on the slit plane $\C\setminus [0, +\infin]$ 

##### (4.2) $f(z) = \frac{r^a e^{ia\theta}}{(1+z)^2}$ , $z = re^{i\theta}, 0  < \theta < 2\pi$ 

regard the slit $[0, +\infin)$ as having a top edge and a bottom edge and extend the function by continuity to each edge of the slit, so it is defined by $(4.2)$ with $\theta = 0$ on the top edge and by $(4.2)$ with $\theta = 2\pi$ on the bottom edge

The values on the bottom edge are obtained from those on the top edge by multiplying by the phase factor $e^{2i\pi a}$ 

For $\epsilon > 0$ small and $R > 0$ large, we consider the keyhole domain $D$ consisting of $z$ in the slit plane $\C \setminus[0, \infin]$ satisfying $\epsilon < |z| < R$ 

The function $f(z)$ has one pole in $D$, a double pole at $z = -1$  

Rule 2 gives the residue:

$\text{Res}[\frac{z^a}{(z+1)^2}, -1] = \frac{d}{dz}z^a|_{z= -1} = a\frac{z^a}{z}|_{z=-1} = -ae^{i\pi a} $

The residue theorem yields:

##### (4.3) $\int_{\partial D}f(z)dz = -2\pi ia e^{\pi i a}$ 

The integral around $\partial D$ breaks into the sum of four integrals

1. from $\epsilon$ to  $R$ along the top edge of the slit
2. The circular contour $\Gamma_R$ of radius $R$ in the counter clockwise direction
3. from $R$ back to $\epsilon$ along the bottom edge of the slit
4. around the circular contour $\gamma_\epsilon$  of radius $\epsilon$  in the clockwise direction

$\int_\epsilon^R \frac{x^a}{(1+x)^2}dx + \int_{\Gamma_R}f(z)dz + \int_R^\epsilon \frac{e^{2\pi i a}}{(1+x)^2}dx + \int_{\gamma \epsilon }f(z)dz$

For the integrals over $\Gamma_R$ and $\gamma_\epsilon$ 

$|\int_{\Gamma_R}\frac{z^a}{(1+z)^2}dz| \leq \frac{R^a}{(R-1)^2}\cdot 2 \pi R \sim R^{a-1}$ 

$|\int_{\gamma_\epsilon}\frac{z^a}{(1+z)^2}dz| \leq \frac{\epsilon^a}{(1-\epsilon)^2}\cdot 2\pi \epsilon \sim \epsilon ^{a+1}$

and since $-1 < a < 1$ both these integrals tend to $0$ as $R \rightarrow \infin$  and $\epsilon \rightarrow 0$ 

then reversing the direction of the third integral from $R$ to $\epsilon$ and using $(4.3)$ 

$-2\pi i a e^{\pi i a} = (1- e^{2\pi i a})\int_0^\infin \frac{x^a}{(1+x)^2}dx$ 

and so we obtain the required identity:

$\int_0^\infin \frac{x^a}{(1+x)^2}dx = \frac{-2\pi i a e^{\pi i a}}{1 - e^{2\pi ia}}$

$ = \frac{2\pi i a}{e^{\pi i a}-e^{-\pi i a}} = \frac{\pi a}{\sin (\pi a)}$

This identity can be extended to complex values of the parameter $a$ 

the function 

$g(w)= \int_0^\infin \frac{x^w}{(1+x^2)}dx$ is analytic on the strip {$-1 < \Re(w)<1$} as is the function $\pi w/\sin (\pi w)$ 

We have already shown these two functions coincide on the interval (-1, 1), so by uniqueness principle, they coincide in the entire strip