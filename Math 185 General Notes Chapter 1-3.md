# Math 185 General Notes

## Chapter 1

### 1. Complex Numbers

#### Properties

##### Addition, multiplication, modulus/absolute value $|z|$ 

##### Triangle Inequality

$|z+w| \leq |z| + |w|$ 

$|z-w| \geq |z| - |w|$ 

##### Multiplication follows usual laws of algebra

Associative, commutative, distributive 

#### Multiplicative inverse

$\frac{1}{z} = \frac{x-iy}{x^2+y^2}$ 

#### Complex Conjugate Properties

$\overline{\overline {z}} = z$ 

$\overline{z+w} = \overline{z} + \overline{w} $ 

$\overline{zw}  = \overline{z}\overline{w}$ 

$|z| = |\overline{z}|$ 

$|z|^2 = z\overline{z}$ 

$\frac{1}{z} = \frac{\overline{z}}{|z|^2}$ 

#### Recover Real and Imaginary Parts

$Re z = (z+\overline{z})/2$ 

$Im z = (z-\overline{z})/2i$ 

##### $|zw| = |z||w|$ 

$|zw|^2 = (zw)(\overline{zw}) = z\overline{z}w\overline{w} = |z|^2|w|^2$ 

#### Fundamental Theorem of Algebra

### 2. Polar Representation

$r = |z|$, $\theta = \arctan{y/x}$ 

$x = |z|\cos\theta$, $y = |z|\sin\theta$ 

#### Argument of $z$ , angle $\theta$ 

$\arg z$ is *multivalued* function defined for $z \neq 0$ 

##### Principal value of $\arg z$ 

##### the value of $\theta$ s.t. $\theta \in (-\pi, \pi]$ 

##### $z = re^{i\theta}$ is the polar representation

##### also: $e^{i\theta} = \cos\theta + i\sin\theta$ (see power series)[^1]

[^1]: http://www.toomey.org/tutor/harolds_cheat_sheets/Harolds_Taylor_Series_Cheat_Sheet_2016.pdf

#### Common Complex exponentials

$e^{i\pi} = -1$, $e^{i\pi/2} = i$  $e^{i\pi/3} = \frac{1 + \sqrt{3}i}2$, $e^{i\pi/4} = \frac{1+i}{\sqrt{2}}$ 

and $e^{2\pi mi} = 1$ 

#### Useful Identities for exponential functions

##### (2.3) $|e^{i\theta}| = 1$

##### (2.4) $\overline{e^{i\theta}} = e^{-i\theta}$ 

##### (2.4) $1/e^{i\theta} = e^{-i\theta}$ 

##### (2.6) $e^{i(\theta + \phi)} = e^{i\theta}e^{i\phi} $ 

	Proven using trigonometric identities 

##### (2.7) $\cos(\theta + \phi) = cos\theta \cos\phi - sin\theta \sin\phi \\ \sin(\theta  +\phi ) = \sin\theta\cos\phi +\cos\theta \sin\phi$ 

##### 

##### (2.8) $\arg \overline{z} = - \arg z$

##### (2.9) $\arg(1/z) = -\arg z$ 

##### (2.10) $\arg(z_1z_2) = \arg z_1 + \arg z_2$ 

#### de Moivre's formulae (for finding roots, taking the power)

$\cos(n\theta) + i\sin(n\theta) = (\cos\theta + i\sin\theta)^n$ 

$\cos(n\theta) = Re(\cos\theta + i\sin\theta)^n$

$\sin(n\theta) = Im(\cos\theta + i\sin\theta)^n$ 

#### Explicit solutions for nth roots of a complex number

if $w = \rho e^{i\phi}$ 

then its $n$ roots are $re^{i\theta}$ where:

$r = \rho ^{1/n}$

$\theta = \phi/n + 2\pi k/n$ 

#### nth roots of unity: nth roots of 1

$\omega_k = e^{2\pi i k/n}, 0 \leq k \leq n-1$ 

So finding the nth roots:

if one roots is given by $z_0 = \rho^{1/n}e^{i\phi/n}$ 

Then other roots are found by multiplying $z_0$ by the nth roots of unity

### 3. Stereographic Projection

#### The extended complex plane = $\C^* = \C \cup${$\infin$} 

#### Stereographic Projection of $P = (X,Y,Z)$ on the unit sphere toher than the north pole $N = (0, 0, 1)$ 

is the point $z = (x,y,0)$ where the straight line through $N$ and $P$ meets the coordinate plane $Z = 0$ 

##### parametric equation: $(0, 0, 1) + t(X, Y, Z-1) = (x,y,0)$ 

$t = 1/(1-Z)$ 

##### Solve for x,y in terms of $X, Y, Z$ 

$x = tX = X/(1-Z)$

$y = tY = Y/(1-Z)$ 

##### Solve for $X,Y, Z$ in terms of $x,y$ 

$X = 2x/(|z|^2+1)$

$Y = 2y/(|z|^2+1)$

$Z = 1 - 1/t = (|z|^2-1)/(|z|^2+1)$ 

##### one-to-one correspondence between points P of the sphere except at N and points (x,y) of the complex plane

#### Tips

Lines of Latitude correspond to circles centered at 0

Lines of Longitude correspond to straight lines through 0

#### Theorem: Circles on sphere correspond to circles and straight lines in the plane

locus of points in the plane satisfying a quadratic equation of the form

##### (3.1) $x^2 +y^2 + ax + by +c = 0$ is either a circle, a point, or empty

##### (3.1.1) $(x+a/2)^2 +(y+b/2)^2 = (a^2+b^2)/4 - c$  

###### Circle if right side is positive

###### Point if right side is 0

###### Empty if right side is negative

##### If we start with a circle on the sphere, we express it as the intersection of the sphere and a plane: $AX + BY + CZ = D$ 

Then the projection of the circle satisfies when we replace $X, Y, Z$ in terms of $x, y$ 

so : $A\frac{2x}{|z|^2+1} + B\frac{2y}{|y|^2+1} + C\frac{|z|^2-1}{|z|^2+1} = D$ 

###### (3.2) $(C-D)(x^2+y^2) + 2Ax + 2By - (C+D) = 0$ 

##### If we start with a circle in the plane

$x^2 + y^2 + ax + by + c = 0$ 

We want to find what points $X, Y, Z$ satisfies this equation

We want to find the plane $AX + BY + CZ = D$ satisfying this equation

Using the earlier formulae, such a plane would satisfy

$(C-D) = 1$ 

$a = 2A$ 

$b = 2B$ 

and $-(C+D) = c$ 

##### If we start with a straight line in the plane:

Using same methodology:

$(C-D) = 0, C= D$

$2A = a$

$2B = b$ 

$-(2D) = c$ 

Example?:

$y = x+2$ 

$x - y +2 = 0$ 

$A = 1/2$ 

$B = -1/2$ 

$-(C + D) = 2$ 

$C = D = -1$ 

$\frac{1}{2}X - \frac{1}{2}Y -Z =-1$



##### Since straight lines in the plane correspond to circles on the sphere, it is convenient to regard a straight line in the complex plane as a circle passing through $\infin$ 

### 4. The Square and Square Root Functions

#### Polar Decomposition $w = z^2 = r^2e^{2i\theta}$ 

We have

##### (4.1) $|w| = |z|^2$

##### (4.2) $\arg w = 2 \arg z$ 

So circles of radius $|z|$ get mapped to circles of radius $|z|^2$ 

and as $z = r_0e^{i\theta}$ (fixed $r_0$ ) moves around the circle in the positive direction at constant angular velocity

$w = r^2_0e^{2i\theta}$ moves around the image circle in the same direction but at double the angular velocity

For rays of fixed angle $\theta$

as $z$ traverses the ray from origin to $\infin$ at constant speed

the value of $w$ traverses the image ray from $0$ to $\infin$ starting slowly and

then increasing its speed

##### slit or branch

as rays sweep out the open right half $z$-plane, 

image rays under $w= z^2$ sweep out the entire $w$ plane except for the negative axis

This leads to us drawing a slit/branch cut in the $w$-plane from $-\infin$ to 0

and to define the inverse function on the slit plane 

Each determination of the inverse function is referred to as a *branch* of the inverse

### 5. The Exponential Function

#### Definition of the exponential function over complex numbers z

$e^{z} = e^x\cos y + i e^{x}\sin y $ , $z = x+iy \in \C$ 

$e^{z} = e^{x}e^{iy}$ 

##### (5.1) $|e^{z}| = e^x$ 

##### (5.2) $\arg e^{z} = y$ 

#### The exponential function is periodic with period $2\pi i$ 

##### $e^{z +2\pi i } = e^z$ 

##### (5.3) $e^{z+w} = e^z e^w$ 

$1/e^{z} = e^{-z}$ 

##### Images of horizontal lines: rays issuing out at angle $y$ 

##### Images of vertical lines: circles centered at origin

### 6. The Logarithm Function

For $z \neq 0$ we define $\log z$ to be the multivalued function

	$\log z = \log|z| + i\arg z \\ = \log|z| + iArg\,z + 2\pi i m$ 

The values of $\log z$ are the numbers $w$ s.t. $e^{w} = z$ 

## Chapter 2 Analytic Functions

### 1. Review of Basic Analysis

#### A sequence {$s_n$} converge to $s$ 

##### Informal: The sequence eventually lies in any disk centered at $s$ 

##### Formal: A sequence of complex numbers {$s_n$} converges to $s$  if for any $\epsilon > 0$, there is an integer $N \geq 1$ such that $|s_n -s| < \epsilon$ for all $n \geq N$ 

#### Examples:

##### (1.1) $\lim_{n\rightarrow \infin} \frac{1}{n^p} = 0$         $0 < p < \infin$ 

##### (1.2) $\lim_{n\rightarrow \infin} |z|^n = 0$       $|z| < 1$ 

##### (1.3) $\lim_{n\rightarrow \infin} \sqrt[n]{n} = 1$

#### Bounded sequence

A sequence of complex numbers {$s_n$}  is said to be **bounded** if there is some number $R > 0$ such that $|s_n| \leq R$ for all $n$. In other words, the sequence is bounded if it is contained in some disk.

#### Theorem: A convergent sequence is bounded. Further, if {$s_n$} and {$t_n$} are sequences of complex numbers converging to $s$ and $t$ respectively

##### (a) $s_n + t_n \rightarrow s+t$ 

##### (b) $s_nt_n \rightarrow st$ 

##### (c) $s_n/t_n \rightarrow s/t$ , provided $t\neq 0$ 

#### In-Between Theorem: If $r_n\leq s_n\leq t_n$, and if $r_n \rightarrow L$ and $t_n \rightarrow L$ then $s_n \rightarrow L$ 

#### monotone increasing: $s_{n+1} \geq s_n$ for all $n$ 

#### monotone decreasing: $s_{n+1} \leq s_n$ for all $n$ 

#### A bounded monotone sequence of real numbers converges

#### "upper limit" to {$s_n$} denoted $\lim \sup s_n$ 

the largest possible limit of a subsequence of {$s_n$}, $S$ (unique extended real number)

if $t >S$ then $s_n \geq t$ for only finitely many indices $n$

	there's only so many elements in the sequence that are larger than $S$  

if $t < S$, then $s_n <t$ for infinitely many indices $n$ 

	there's infinitely many elements in the sequence that are smaller than $S$  

#### A "lower limit" of {$s_n$} denoted $\lim\inf s_n$ 

the smallest limit of a subsequence of {$s_n$}, $L$ (unique?)

if $t < S$ then $s_n \leq t$ for only finitely many indices $n$ 

if $t > S$ then $s_n > t$ for infinitely many indices $n$ 

It satisfies:

##### $\lim\inf s_n = -\lim \sup (-s_n)$ 

#### The sequence converges iff its $\lim \sup$ and $\lim \inf$ are FINITE and EQUAL

#### A sequence of complex numbers converges if and only if the corresponding sequences of real and imaginary parts of the $s_ks converge

#### Cauchy sequence: $s_n - s_m$ tend to 0 as $n, m$ tend to $\infin$ 

##### For any $\epsilon > 0$, $\exists N \geq 1$ s.t. $|s_n - s_m| < \epsilon$ for all $n, m \geq N$ 

DO NOT CONFUSE WITH $|s_n+1 - s_n|< \epsilon$ It must be that ALL elements after a certain point are all really close to each other.

#### A sequence of complex numbers converges if and only if it is a Cauchy sequence.

#### The Limit of a function at $z_0$ 

for any $\epsilon > 0$, there exists $\delta > 0$ such that

for any $z \in D$ with $|z-z_0| < \delta$  $|f(z)-L| < \epsilon$ 

So we say: $\lim_{z\rightarrow z_0} f(z) = L$ etc.

#### The complex-valued function $f(z)$ has lmit $L$ as $z \rightarrow z_0$ if and only if $f(z_n) \rightarrow L$ for any sequence {$z_n$} in the domain of $f(z)$ such that $z_n \neq z_0$ and $z_n \rightarrow z_0$ 

#### Theorem: algebra of limits for functions

#### Continuous definition

#### Examples of continuous functions

##### $f(z) =c, c \in \C$ 

##### $f(z) = z$ 

##### polynomial

##### rational functions are continuous wherever the denominator is not zero

	both numerator and denominators are polynomials

##### $Re(z)$ 

##### $Im(z)$ 

##### $|z|$ 

#### Definition of open: for any point in the set there exists a disk centered at that point fully contained in the set

#### If $h(x,y)$ is a continuously differentiable function on a domain $D$ such that $\nabla h = 0$ on $D$, then $h$ is constant

##### Directional Derivative in direction of $u: \nabla_uh(x,y) = \lim_{t\rightarrow 0}\frac{h(x + tu_1, y + tu_2) - h(x,y)}{t} = u/|u| \times \nabla h$ 

##### last equality is valid because $h$ is continuously differentiable

##### and $\nabla h = (\frac{\partial h}{\partial x}, \frac{\partial h}{\partial y})$ 

so with $\nabla h = 0$ we have $h(x + tu_1, y+tu_2)  = h(x,y)$ 

for any point $x,y$ in the domain, we can connect it to other points in the domain via line segment, so roughly we have $v_1, v_2, . . ., v_n$ representing the vectors of the broken line segments joining one point to $z = (x,y)$  

$h(z + v_1+ . . . v_n) = h(z + v_1 + v_2 + v_{n-1}) = . . . = h(z + v_1) = h(x,y)$ 

#### Also: Definitions of domain, star-shaped, convex

#### Closed set : contains every limit of every convergent sequence of elements in the set

#### Boundary of a set: points such that every disk centered at $z$ contains both points in the set and points not in the set

accumulation points?

#### Compact: closed and bounded in the complex plane

#### A continuous real-valued function on a compact set attains its maximum

### 2. Analytic Functions

#### Def. of differentiable

#### Examples:

##### constant functions have derivative of 0

##### power function has derivative $mz^{m-1}$ 

##### $f(z) =$ the conjugate of z is not differentiable at all

	see $(\overline{z+\Delta z} -z)/\Delta z = \overline{\Delta z}/\Delta z$ 
	
	if real, 1, if imaginary, -1

#### Differentiable at $z_0$ means continuous at $z_0$ 

#### Algebra of derivatives, product rule, quotient rule

$\frac{1}{g}'(z) = \lim_{\Delta z \rightarrow 0} \frac{1/g(z+\Delta z) - 1/g(z))}{\Delta z}$

$= \frac{g(z) - g(z+\Delta z)}{\Delta z g(z + \Delta Z)g(z)} \rightarrow -g'(z)/g(z)^2 $

#### Examples

##### Polynomials are differentiable, rational functions are differentiable except at finitely many points: the zeros of $q(z)$ 

#### Chain Rule: $(f\circ g)'(z_0) = f'(g(z_0))g'(z_0)$ 

#### Analytic functions on an open set $U$ are differentiable at each point of $U$ and the derivative is continuous on $U$ 

##### Sums and products of analytic functions are analytic

##### Quotients are analytic where denominator does not vanish

##### analytic just means differentiable for now?

### 3. Cauchy Riemann Equations

##### Notation: $f = u+iv$ on domain D

#### Suppose $f = u+iv$ is analytic

##### (3.1) $f'(z) = \frac{\partial u}{\partial x}(x,y) +i\frac{\partial v}{\partial x}(x,y)$ 

obtained by taking the derivative with respect to only $\Delta x$ keeping $y$ constant

##### (3.2) $f'(z) = \frac{\partial v}{\partial y}(x,y) - i\frac{\partial u}{\partial y}(x,y)$  

obtained by taking the derivative with respect to only $i\Delta y$  keeping $x$ constant

#### Cauchy Riemann equations: $\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y}$ , $\frac{\partial u}{\partial y} = -\frac{\partial v}{\partial x}$ 

#### $f = u+iv$ defined on domain D is analytic if and only if $u(x,y), v(x,y)$ have continuous first-order partial derivatives that satisfy the CR equations

Proof in backwards direction requires using taylor's theorem[^taylor's]

[^taylor's]: page 48

Then the CR equations to show $f'(z$) exists

#### Examples

$f(x,y) = x+iy$

##### $e^{z}$ 

##### $e^{az}$

##### Linear combinations of complex exponential functions are analytic

##### $(\sinh z)' = \cosh z$ and vice versa 

#### If $f(z)$ is analytic on domain D and if $f'(z) = 0$ on D, then $f(z)$ is constant

#### If $f(z)$ is analytic and real-valued on $D$ then $f(z)$ is constant

### 4. Inverse Mappings and the Jacobian

#### $f= u+iv$ is analytic on $D$ . then we may regard $D$ as a domain in the Euclidean plane and $f$ as a map from $D$ to the plane with components $(u(x,y), v(x,y))$ 

##### The Jacobian Matrix of this map is $J_f = \begin{pmatrix} \frac{\partial u}{\partial x} & \frac{\partial u}{\partial y} \\ \frac{\partial v}{\partial x} & \frac{\partial v}{\partial y} \end{pmatrix}$  

First column: with respect to x, second column: with respect to y

first row: u, second row: v

#### If $f(z)$ is analytic, then its Jacobian matrix $J_f$ has $\det J_f(z) = |f'(z)|^2$ 

##### Inverse Function Theorem: Multivariable Calculus

if the function is continuously differentiable (analytic, so check)

from $\R^n$ into  $\R^n$  we have $n =2$ 

The Jacobian determinant at $z_0$ is nonzero ($f'(z_0) \neq 0$) 

Then the function is invertible near $z_0$ 

##### Jacobian is change of variables for multiple integrals...

#### Suppose $f(z)$ is analytic on a domain $D$, $z_0 \in D$ and $f'(z_0) \neq 0$ then

##### There is a small disk $U$ $\sub D$ containing $z_0$ such that $f(z)$ is one-to-one on $U$ 

##### the image $V = f(U)$ of $U$ is open

##### the inverse function $f^{-1}: V \rightarrow U$ is analytic and satisfies

###### (4.1) $(f^{-1})'(f(z)) = 1/f'(z)$     $z \in U$ 

#### Examples

$w = Log z$ ... $e^w$ is analytic and $e^w \neq 0$ so $Log z$ is analytic

##### Any continuous branch of $\sqrt{z}$ is analytic

so we are working with $w = \sqrt{z}$ 

we know the inverse, $w^2 = z$ is analytic

##### Mnemonic: $\frac{dz}{dw} = \frac{1}{\frac{dw}{dz}}$ 

since $f^{-1}$ maps $w = f(z)$ to $z$ and such

### 5. Harmonic Functions

#### Laplace's equation: sum of second order partial derivatives = 0

##### Laplacian operator

#### Harmonic functions: $u(x,y)$ is harmonic if all of its first- and second-order partial derivatives exists and are continuous and satisfy Laplace's equation

#### If $f = u+iv$ is analytic, and functions $u$ and $v$ have continuous second-order partial derivatives, then $u$ and $v$ are harmonic

##### second hypothesis of the theorem is redundant, analytic functions have continuous partial derivatives of all orders

#### Harmonic conjugate:

##### $u$ is harmonic, $v$ is harmonic, and $u+iv$ is analytic: $v$ is harmonic conjugate to $u$ 

###### unique up to adding a constant

#### A harmonic conjugate $v$ for $u$ is given explicitly by:

##### (5.3) $v(x,y) = \int_{y_0}^y \frac{\partial u}{\partial x}(x,t) dt - \int_{x_0}^x \frac{\partial u}{\partial y}(s, y_0)ds + C$

#### Let $D$ be an open disk, or an open rectangle with sides parallel to the axes, and let $u$ be a harmonic function on $D$ Then:

##### there is a harmonic function $v$ on $D$ such that $u+iv$ is analytic on $D$ 

##### The harmonic conjugate $v$ is unique up to adding a constant

### 6. Conformal Mappings

#### Notation

##### Let $\gamma(t) = x(t)+iy(t)$ , $0 \leq t \leq 1$ be a smooth parameterized curve terminating at $z_0 = \gamma(0)$ 

###### $\gamma'(0) = \lim_{t \rightarrow 0}\frac{\gamma(t)- \gamma(0)}t = x'(0) +iy'(0)$ is the tangent vector to the curve $\gamma$ at $z_0$ 

#### If $\gamma(t), 0\leq t \leq 1$ is a smooth parameterized curve terminating at $z_0 = \gamma(0)$ and $f(z)$ is analytic at $z_0$ then the tangent to the curve $f(\gamma(t))$ terminating at $f(z_0)$ is

##### $(f\circ\gamma)'(0) = f'(z_0)\gamma'(0)$ 

proof is close to the chain rule proof

#### Ways to think of this

##### 1. the tangent vector is the vector in the plane with tail at $z_0$ and composing a parameterized curve with $f(z)$ has the effect of multiplying (complex) the tangent vector by $f'(z_0)$ and moving the tail to $w_0 = f(z_0)$ 

##### 2. If the tangent vector is represented by $z-z_0$ then the tangent to the image curve is represented by $f'(z_0)(z-z_0)$ 

##### 3. The effect of composing the tangent vector with $f(z)$ is the same as composing with the function $f(z_0) + f'(z_0)(z-z_0)$ 

f maps the tangent vector to $f(z_0) + f'(z_0)(z-z_0)$ ? or

$f(z_0) + f'(z_0)(z-z_0)$ 

#### Conformal: preserves angles

##### Conformal @ $z_0$  means that whenever $\gamma_1, \gamma_2$ are two curves terminating at $z_0$ with nonzero tangents, then the image of their curves have nonzero tangents and the angle between the image curves is the same as the angle between the curves.

Angle between curves determined by the tangent vectors

##### Conformal mapping of one domain $D$ onto another $V$ is a continuously differentiable function that is conformal at each point of $D$ AND is one-to-one and onto

#### If $f(z)$ is analytic at $z_0$ and $f'(z_0) \neq 0$ then $f(z)$ is conformal at $z_0$ 

#### Examples

Just because a function is conformal at every point, does not make it a conformal mapping

Think about periodicity, continuity, etc.

We can find domains for functions such that it is a conformal mapping from that domain

#### Level curves: two families: $u,v$ s.t. each curve in the family is when the function is held constant 

$f$ maps each level curve for $u$ to a vertical line

and each level curve of $v$ to a horizontal line

If $f$ is analytic, it is conformal and preserves angles

so since we have $f$ mapping level curve intersections to intersections of perpendicular lines, level curve intersections are orthogonal

##### I think if $f'(z_0) = 0$, $f$ is not conformal at $z_0$ since cures with nonzero angles vanish

###  7. Fractional Linear Transformations

Questions:

How do we know when/if FLT are conformal?

Well: they map the extended complex plane onto itself one-to-one

are they analytic? yes, they have derivatives... the only issue is where does $f'(z) = 0$ 

from the formula, we actually have that $f'(z) = \frac{ad - bc}{(cz +d)^2}$ so this is never equal to 0 as by definition, FLT satisfies ad-bc not equal to 0

Fractional Linear Tranformations aren't constant

and they may not always have a derivative equal to 0

## Chapter 3

### 1. Line Integrals and Green's Theorem

##### path definition

A path in the plane from A to B is a continuous function $t \mapsto \gamma(t)$ on some parameter interval $a \leq t \leq b$ such that $\gamma(a) = A$ and $\gamma(b) = B$. 

##### simple path definition (no intersections122)

The path is simple if $\gamma(s) \neq \gamma(t)$ when $s \neq t$ 

##### closed path definition

The pat is closed if it starts and ends at the same point, i.e., $\gamma(a) = \gamma(b)$ 

##### simple closed path definition

closed path $\gamma$ s.t. $\gamma(s) \neq \gamma(t)$ for $a\leq s< t < b$ 

##### reparemtrization of $\gamma$ 

If $\phi(s), \alpha \leq s \leq \beta$ is a strictly increasing function satisfying $\phi(\alpha) = a$ and $\phi(\beta) = b$, then the composition $\gamma(\phi(s))$ is also a path from $A$ to $B$ 

##### trace of the path $\gamma$ 

is its image $\gamma([a,b])$ which is a subset of the plane

For now we can denote the trace of a path also by $\gamma$

Soon, we'll need to be careful about this

##### smooth path definition

a path that can be represented in the form $\gamma(t) = (x(t), y(t)), a \leq t\leq b$, where the functions $x(t), y(t)$ are smooth, that is, have as many derivatives as is necessary for whatever is being asserted to be true

##### piecewise smooth path definition

a concatenation of smooth paths

##### curve definition

usually mean a smooth or piecewise smooth path

#### definition of line integral of $Pdx + Qdy$ 

Let $\gamma$ be a path in the plane from $A$ to $B$, and let $P(x,y)$ and $Q(x,y)$ be continuous complex-valued functions on $\gamma$ 

We consider successive points on the path: $A = (x_0, y_0), (x_1, y_1), . . ., B = (x_n, y_n)$ 

the sum:

##### (1.1) $\sum P(x_j, y_j)(x_{j+1}-x_j) + \sum Q(x_j, y_j)(y_{j+1}-y_j)$

If these sums have a limit as distances between the successive points on $\gamma$ tend to 0...

##### (1.2)$\int_\gamma Pdx + Qdy$ 

#### to evaluate a line integral over a smooth curve

##### (1.3) $\int_\gamma Pdx + Qdy = \int_a^b P(x(t), y(t))\frac{dx}{dt}dt + \int_a^b Q(x(t), y(t))\frac{dy}{dt}dt$ 

#### To evaluate a line integral over a piecewise smooth path:

Parametrize each smooth subpath, calculate the corresponding integrals, and add them

###### Different parameterizations give the same integral

#### Green's Theorem 

Let $D$ be a bounded domain in the plane whose boundary $\partial D$ consists of a finite number of disjoint piecewise smooth closed curves. Let P and Q be continuously differentiable functions on $D \cup\partial D$ 

Then

##### (1.4) $\int_{\partial D} P \, dx \; + \; Q\, dy = \int\int_D(\frac{\partial Q}{\partial x}\; - \; \frac{\partial P}{\partial y})\,dx\,dy$ 

### 2. Independence of Path

#### Fundamental Theorem of Calculus

##### Part I. If $F(t)$ is an antiderivative for the continuous function $f(t)$, then 

$\int_a^b f(t) dt = F(b) - F(a)$ 

##### Part II. If $f(t)$ is a continuous function on $[a,b]$, then 

the indefinite integral $F(t) = \int_a^t f(s)ds$ $a \leq t \leq b$ is an antiderivative for $f(t)$ 

Each antiderivative for $f(t)$ differs from $F(t)$ by a constant

#### Differential $dh$ of a continuously differentiable complex-valued function $h(x,y)$ 

$dh = \frac{\partial h}{\partial x}dx + \frac{\partial h}{\partial y}dy$ 

##### Definition of an exact differential

$P dx + Qdy $ is exact if $Pdx + Qdy = dh$ for some function $h$ 

#### Theorem (Part I)

If $\gamma$ is a piecewise smooth curve from $A$ to $B$ and if $h(x,y)$ is continuously differentiable on $\gamma$ then

##### (2.1) $\int_\gamma dh = h(B) - h(A)$ 

#### Not every differential is exact

#### Independent of Path definition

Let $P$ and $Q$ be continuous complex-valued functions on a domain $D$. We say that the line integral $\int Pdx + Qdy$ is independent of path in $D$ if for any two points $A$ and $B$ of $D$ the integrals $\int_\gamma Pdx + Qdy$ are the same for any path in $\gamma$ in $D$ from $A$ to $B$ 

$\equiv$ $\int\gamma Pdx + Qdy = 0$ whenever $\gamma$ is closed path in $D$ 

#### Lemma. 

Let $P$ and $Q$ be continuous complex-valued functions on a domain $D$. Then $\int P dx + Qdy$ is independent of path in $D$ if and only if $Pdx + Qdy$ is exact, that is, there is a continuously diff. function $h(x,y)$ s.t. $dh = Pdx + Qdy$. This function h is unique up to adding a constant.

#### Closed differential definition

##### (2.2) $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$ 

#### If a differential is exact, then it is closed

##### Not every closed differential is exact

#### Theorem (Part II)

Let $P$ and $Q$ be continuously differentiable complex-valued functions on a domain $D$. Suppose

(i) $D$ is a star-shaped domain 

and

(ii) the differential $Pdx + Qdy$ is closed on $D$

then $Pdx + Qdy$ is exact on $D$ 

#### Deformed Paths and Closed Differentials

##### Intro:

$Pdx + Qdy$ is closed on a domain $D$ 

If two paths $\gamma_0$ and $\gamma$ from $A$ to $B$ are sufficiently near to each other, then $\int_{\gamma_0}Pdx + Qdy = \int_{\gamma}Pdx + Qdy$ 

Sufficiently near meaning: There are successive points $A = A_0, A_1, A_2, . . ., A_n = B$ on $\gamma_0$ and $A = C_0, C_1, C_2, . . . , C_n = B$ on $\gamma$ such that intervals on $\gamma_0$ from $A_{k-1}$ to $A_k$ and on $\gamma$ from $C_{k-1}$ to $C_k$ lie in the same disk $\Delta_k$ which is contained in $D$ 

Consider $\gamma_k$ from $C_0 $to $ C_K$ then goes along a straight line segment in $\Delta_k$ to $A_k$ then following $\gamma_0$ from $A_k$ to $B$ 

We get $\gamma_k$ from $\gamma_{k-1}$ by changing only the subpath in $\Delta_k$ from $C_{k-1}$ to $A_k$ 

so that instead of following $C_{k-1}$ to $A_{k-1}$ along a straight line then from $A_{k-1}$ to $A_k$ along $\gamma_0$

we follow $C_{k-1}$ to $C_k$ along $\gamma$ then following the straight line from $C_k$ to $A_k$ 

Since $Pdx + Qdy$ is independent of path in the disk $\Delta_k$ 

$\int_{\gamma_{k-1}} = \int_{\gamma_k}$ for $1 \leq k \leq n$ 

and $\gamma_n = \gamma$ , so we eventually get the integral of $Pdx + Qdy$ along $\gamma_0$ = the integral along $\gamma$ 

##### Theorem

Let $D$ be a domain, and let $\gamma_0(t)$ and $\gamma_1(t)$ , $a \leq t \leq b$ be two paths in $D$ from $A$ to $B$. Suppose that $\gamma_0$ can be continuously deformed to $\gamma_1$, in the sense that for $0 \leq s \leq 1$ there are paths $\gamma_s(t)$ , $a \leq t\leq b$ from $A$ to $B$ such that $\gamma_s(t)$ depends continuously on $s$ and $t$ for $0 \leq s \leq 1$ and $a \leq t \leq b$ 

Then

###### (2.3) $\int_{\gamma_0}Pdx + Qdy = \int_{\gamma_1} Pdx + Qdy$ 

for any closed differential on $D$ 

#### Summary:

independent of path $\equiv$ exact $\implies$ closed 

And in starshaped domains

independent of path $\equiv$ exact $\equiv$ closed

### 3. Harmonic Conjugates

#### Lemma. If $u(x,y)$ is harmonic, then the differential 

##### (3.1) $-\frac{\partial u}{\partial y} dx \; + \; \frac{\partial u}{\partial x} dy$ is closed

Setting $P = -\partial u/\partial y$ and $Q = \partial u/ \partial x$ 

$\partial P/\partial y = -\partial^2 u/\partial y^2$

$\partial Q/\partial x = \partial^2 u/\partial x^2$ 

and since $u(x,y)$ is harmonic: $\partial Q/\partial x - \partial P/\partial y = 0$ 

so $\partial Q/\partial x = \partial P/\partial y$ 

##### Now suppose $u(x,y)$ is harmonic on a star-shaped domain $D$

This means that the differential is also exact, so there exists some $v(x,y)$ such that 

##### (3.2 )$dv = -\frac{\partial u}{\partial y} dx \; + \; \frac{\partial u}{\partial x} dy$ 

and this is equivalent to the CR equations

###### so with a star-shaped domain D and harmonic u, and v with (3.2), u + iv is analytic

#### Theorem. Any harmonic function $u(x,y)$ on a star-shaped domain $D$ (as a disk or rectangle) has a harmonic conjugate function $v(x,y)$ on $D$ 

##### (3.3) $v(B) = \int_A^B -\frac{\partial u}{\partial y} dx \; + \; \frac{\partial u}{\partial x} dy$ 

1. Up to an additive constant

2. A is fixed

3. Integral is independent of path $\equiv$ exact

### 4. The Mean Value Property

$h(z)$: continuous, real-valued function on a domain $D$ 

Let $z_0 \in D$ 

Suppose $D$ contains the disk {$|z-z_0| < \rho$}

#### Average value of $h(z)$ on the circle {$|z-z_0| = r$} 

$A(r) = \int_0^{2\pi} h(z_0 + re^{i\theta})\frac{d\theta}{2\pi}, \; \; 0 < r <\rho$ 

**$A(r)$ varies continuously with the radius $r$**

​	because $h(z)$ is continuous 

Values of $h(z)$ are all near $h(z_0)$ when $z$ near $z_0$ $\implies$ Averages $A(r)$ near $h(z_0)$ when $r$ is small

$\implies $ $A(r) \rightarrow h(z_0)$ as $r \rightarrow 0^+$ 

Proof: page 85

#### Theorem. If $u(z)$ is a harmonic function on a domain $D$, and if the disk {$|z-z_0| < \rho$} is contained in $D$, then

##### (4.1) $u(z_0) = \int_0^{2\pi} u(z_0 + re^{i\theta})\frac{d\theta}{2\pi}$ ,    $0 < r < \rho$ 

The average value of a harmonic function on the boundary circle of any disk contained in $D$ = its value at the center of the disk

Proof:

The line integral of a boundary

Green's Theorem

and that differentials involving harmonic function partial derivatives are closed

so $0 = \oint_{|z-z_0| = r} -\frac{\partial u}{\partial y}dx + \frac{\partial u}{\partial x}dy$ 

parameterize $x(\theta) = x_0 + r\cos\theta$, $y(\theta) = y_0 + r\sin \theta$ 

so $\partial x/\partial \theta = -r\sin\theta$, $\partial y/\partial \theta = r\cos\theta$ 

and using $\partial x/\partial \theta \times \partial \theta = dx$

##### (4.2) $0 = r\int_0^{2\pi} (\frac{\partial u}{\partial x}\cos \theta + \frac{\partial u}{\partial y}\sin \theta)d\theta = r\int_0^{2\pi}\frac{\partial u}{\partial r}(z_0 + re^{i\theta})$

because $\frac{\partial u}{\partial r} = \frac{\partial u}{\partial x}\frac{\partial x}{\partial r} + \frac{\partial u}{\partial y}\frac{\partial y}{\partial r} = \frac{\partial u}{\partial x}\cos\theta + \frac{\partial u}{\partial y}\sin\theta$ 

and $z = z_0 + re^{i\theta}$ and $u(z) = u(z_0 + re^{i\theta})$ 

... switch order of integration and derivation, divide by $2\pi r$ 

we see the integral is constant for $r \in (0, \rho)$ 

as in no matter what $r$ is, the integral $\int_0^{2\pi} u(z_0 + re^{i\theta})\frac{d\theta}{2\pi}$ is the same value

and letting $r \rightarrow 0$, we see this value is $u(z_0)$ 

#### Mean value property for continuous function $h(z)$ on a domain $D$ 

if for each point $z_0 \in D$ , $h(z_0)$ is the average of its value over any small circle centered at $z_0$ 

So for each point in the domain, $z_0$ 

​	there exists an $\epsilon > 0$ s.t.

​		for any $r \in (0, \epsilon)$ 

​			$A(r)$ $=h(z_0)$  

#### Harmonic functions have the mean value property

### 5. The Maximum Principle

#### The strict maximum principles asserts that if a real-valued harmonic function attains its maximum on a domain $D$, then it is constant.

#### Strict Maximum Principle (Real Version)

Let $u(z)$ be a real-valued harmonic function on a domain $D$ 

such that $u(z) \leq M$ for all $z \in D$ 

If $u(z_0) = M$ for some $z_0 \in D$ , then $u(z) = M$ for all $z \in D$ 

---

Idea of the proof is to use the mean value property

assume $u(z_1) = M$ 

since we have

$u(z_1) = \int_0^{2\pi} u(z_1 + re^{i\theta}) \frac{d\theta}{2\pi}$ , 

$\int_0^{2\pi}u(z_1)\frac{d\theta}{2\pi} = u(z_1)$ 

(5.1)  $\int_0^{2\pi}[u(z_1) - u(z_1 +re^{i\theta})]\frac{d\theta}{2\pi} = 0$ for $ 0 < r < \rho$ 

the integrand is nonnegative since $u(z_1)$ is the max value

and it is continuous, since... $u(z_1) - u(z_1 +re^{i\theta})$ is continuous

so the integral (5.1) can be zero only if $u(z_1) - u(z_1 +re^{i\theta})$ is zero

so we have that for each point $z_1$ s.t. $u(z_1) = M$, there exists a small disk centered on it such that all points in this didk, $z$, satisfy $u(z) = M$, so the set {${u(z) = M}$} is open

and the set {$u(z)< M$} is open, since

$u$ is continuous $\equiv$ for all $z_0$, $\forall \, \epsilon > 0, \exists \, \delta > 0$ such that for all $z$ s.t. $|z-z_0| < \delta$ , $u(z) \in (u(z_0) - \delta, u(z_0) + \delta)$ 

so there's a small disk around each point $z_0$ s.t. $u(z_0) < M$ s.t. for all points $z$ in this disk

$u(z) < u(z_0) + \epsilon$ and we set $\epsilon = M - u(z_0)$ so $u(z) < M$ 

Suppose the sets {u(z) = M} and {u(z)< M} are both nonempty

AH, hm. at the boundary of {u(z) = M}, it must either be a point in {u(z) = M} or $u(z) < M$ 

it means that either {u(z) = M} or {u(z)< M} contains its boundary points

but we must still have that a disk centered on these points is fully contained in its respective set, 

so all points must be from one set or the other

otherwise, we get a contradiction from the definition of a boundary point.

​	that boundary points aren't really boundary points.

OR

$D$ is a domain, which means that points from {u(z) = M} and {u(z)< M} are connected by broken line segments

I mean, at the boundary points, we're going to get noncontinuity 

since approaching from the side of {u(z) = M} we get M

and approaching from the other side, {u(z)<M} we get some value < M

#### Recall: a complex-valued function is harmonic if its real and imaginary parts are harmonic

##### Any analytic function is harmonic

#### Strict Maximum Principle (Complex Version)

Let $h$ be a bounded complex-valued harmonic function on a domain $D$ 

if $|h(z)| \leq M$ for all $z \in D$ and $|h(z_0)| = M$ for some $z_0 \in D$ , then $h(z)$ is constant on $D$ 

#### Maximum Principle

Let $h(z)$ be a complex-valued harmonic function on a bounded domain $D$ such that $h(z)$ extends continuously to the boundary $\partial D$ of $D$. If $|h(z)| \leq M$ for all $z \in \partial D$ , then $|h(z)| \leq M$ for all $ z \in D$ 

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

paramterize the line segment $z(t) = (1+i)t$ 

do $dz = \frac{dz}{dt}dt$ , $z  = 0$ when $t = 0$ , $z = 1 +i$ when $t = 1$

##### Example $\oint_{|z| = 1}\frac{dz}{z}$ 

$z = ie^{i\theta}$ 

$\frac{dz}{d\theta} = -e^{i\theta}$ 

-- -

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

### 



