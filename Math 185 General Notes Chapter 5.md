# Math 185 General Notes Chapter 5

## 1. Infinite Series

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

## 2. Sequences and Series of Functions

#### {$f_j$} a sequence of complex-valued functions defined on a set $E$

##### {$f_j$} converges pointwise on $E$ if for each $x \in E$, {$f_j(x)$} converges

##### the limit $f(x)$ of {$f_j(x)$} is then a complex-valued function on $E$ 

#### {$f_j$} Converges Uniformly to $f$ on $E$ if |$f_j(x) - f(x)$| $\leq \epsilon_j$ for all $x \in E$

##### $\epsilon_j \rightarrow 0$ as $j \rightarrow \infin$, and $\epsilon_j = \sup_{x \in E}|f_j(x) - f(x)|$ 

##### Converge uniformly to $f$ on $E$ $\implies$ converge pointwise to $f$ on $E$ 

#### a uniform limit of continuous functions is continuous

#### an integral of a uniform limit is the limit of the integrals

$\gamma$: piecewise smooth curve in complex plane

{${f_j}$}: a sequence of continuous complex valued functions on $\gamma$  

if {$f_j$} converges uniformly to $f$ on $\gamma$, then 

##### $\int_{\gamma} f_j(z)dz$ converges to $\int_{\gamma}f(z)dz$ 

#### $\sum g_j(x)$ series of complex valued functions defined on set $E$

##### $S_n(x) = \sum_{k=0}^n g_j(x)$ is the partial sum

##### Series converges pointwise on $E$ if the sequence of partial sums converges pointwise on $E$

- and each sequence for a fixed $x \in E$, {$S_n(x)$} is a sequence of complex numbers, so each limit is unique

##### Series converges uniformly on $E$ if the sequence of partial sums converges uniformly on $E$ 

and thus converges pointwise.

#### Weierstrass M-Test

Suppose $M_k \geq 0$ and $\sum M_k$ converges

If $g_k(x)$ are complex valued functions on a set $E$ such that $|g_k(x)| \leq M_k$ for all $x \in E$, then $\sum g_k(x)$ converges uniformly on $E$ 

#### If {$f_k(z)$} is a sequence of analytic functions on a domain $D$ that converges uniformly to $f(z)$ on $D$, then $f(z)$ is analytic

a limit of analytic functions that converges uniformly is analytic.

#### $f_k(z)$ is analytic for $|z-z_0| \leq R$, and suppose that {$f_k(z)$} converges uniformly to $f(z)$ for $|z-z_0| \leq R$. Then for each $r < R$ and for each $m \geq 1$, the sequence of mth derivatives {$f_k^{(m)}(z)$} converges uniformly to $f^{(m)}(z)$ for $|z-z_0| \leq r$ 

#### Converge normally:

A sequence of analytic functions {$f_k(z)$} on domain $D$ converges normally to an analytic function $f(z)$  on $D$ if it converges uniformly to $f(z)$ on each closed disk contained in $D$ $\equiv$ {$f_k(z)$} converges to $f(z)$ uniformly on each bounded subset $E$ of $D$ at a strictly positive distance from the boundary of $D$ 

##### Theorem: {$f_k(z)$} is a sequence of analytic functions on a domain $D$ that converges normally on $D$ to the analytic function $f(z)$. Then for each $m \geq 1$, the sequence of mth derivatives {$f_k^{(m)}(z)$} converges normally to $f^{(m)}(z)$ on $D$ 

## 3. Power Series

#### A power series (centered at $z_0$) is a series of the form $\sum_{k = 0}^\infin a_k(z-z_0)^k$ 

#### $\sum a_k z^k$ a power series, then there is $R$, $0 \leq R \leq +\infin$ such that $\sum a_kz^k$ converges absolutely if $|z| < R$, and $\sum a_k z^k$ does not converge if $|z| > R$. For each fixed $r$ satisfying $r < R$, the series $\sum a_k z^k$ converges uniformly for $|z| \leq r$ 

#### The radius of convergence depends only on the tail of the series. If we alter a finite number of coefficients, the radius of convergence remains the same. 

#### $\sum a_k z^k$ a power series with radius of convergence of $R > 0$, then the function $f(z) = \sum_{k=0}^\infin a_k z^k, |z| <R$ is analytic. 

##### derivatives: $f'(z) = \sum_{k=1}^\infin ka_kz^{k-1}$, $f''(z) = \sum_{k=2}^\infin k(k-1)a_kz^{k-2}$ , $|z| < R$ 

##### $a_k = \frac{1}{k!}f^{(k)}(0), k \geq 0$ 

#### Due to uniform convergence of power series on subdisks of radius strictly smaller than $R$, a power series can be integrated term by term: $\int_0^z \sum(a_k\zeta^k)d\zeta = \sum a_k \int_0^z \zeta ^k d\zeta = \sum a_k \frac{z^{k+1}}{k+1}, |z| <R$

#### Finding $R$:

$|a_k/a_{k+1}| \rightarrow R$ as $k \rightarrow \infin$ 

##### $\sqrt[k]{|a_k|} \rightarrow \frac{1}{R}$ as $k \rightarrow \infin$ 

##### or $R = \frac{1}{\lim \sup \sqrt[k]{|a_k|}}$ 

## 4. Power Series Expansion of an Analytic Function

Note: power series expansions $\sum a_k (z-z_0)^k$ are analytic inside the disk of convergence {$|z-z_0| < R$}

### Any function analytic on a disk can be expanded in a power series that converges on the disk

#### Theorem:

1. Suppose that $f(z)$ is analytic for $|z-z_0| < \rho$. 

Then

1. $f(z)$ is represented by the power series

##### (4.1) $f(z) = \sum_{k = 0}^\infin a_k(z-z_0)^k, |z-z_0| < \rho$ 

where

##### (4.2) $a_k = \frac{f^{(k)}(z_0)}{k!}, k \geq 0$

and where the power series has radius of convergence $R \geq \rho$ 

2. For any fixed $r, 0 < r < \rho$ we have

##### (4.3) $a_k = \frac{1}{2\pi i}\oint _{|\zeta - z_0| = r}\frac{f(\zeta)}{(\zeta - z_0)^{k+1}}d\zeta$, $k \geq 0$ 

Further, if $|f(z)| \leq M$ for $|z-z_0| = r$, then

##### (4.4) $|a_k| \leq \frac{M}{r^k}, k \geq 0$ 

#### Examples: $e^z, \sin z, \cos z$ power series expansions

#### Corollary. an analytic function on a disk is completely determined by its value and the values of its derivatives at the center of the disk

Suppose that $f(z)$ and $g(z)$ are analytic for $|z-z_0| < r$. If $f^{(k)}(z_0) = g^{(k)}(z_0)$ for $k \geq 0$, then $f(z) = g(z)$ for $|z-z_0| < r$ 

#### Corollary. method for determining the radius of convergence of a power series

Suppose that $f(z)$ is analytic at $z_0$, with power series expansion $f(z) = \sum a_k(z-z_0)^k$ centered at $z_0$. Then the radius of convergence of the power series is the largest number $R$ such that $f(z)$ extends to be analytic on the disk {$|z-z_0| < R$}. 

##### Examples:

###### $1/(1+z^2)$ has radius of convergence $R = 1$ 

###### $f(z) = (z^3 -1)/(z^2 -1)$ about $z = 2$ has radius of convergence $R = 3$ , Removable Singularity at $z = 1$ 

1. $f(z) = \sum a_k (z-2)^k$ 
2. $f(z)$ is analytic in the entire complex plane except at $z = \pm 1$,
3. This is illusory: eliminate common factor $z-1$ from numerator and denominator
4. $f(z) = (z^2 + z + 1)/(z+1)$ 
5. The singularity at $z = -1$ is unavoidable so
6. $|2 - (-1)| = 3$ is the radius of convergence

###### $\sum a_k(z-5)^k$ of the function $(\text{Log }z)/(z-1)$ about $z = 5$: $R = 5$ 

What to do with the singularity at $z = 1$?

Take the power series representation of $\text{Log }z$ about $z = 1$ and divide by $(z-1)$ 

$a_0 = \text{Log }(1) = 0$, $a_1 = \frac{1}{1} = 1$, $a_2 = -\frac{1}{1}\frac{1}{2!}$ 

$\text{Log } z  = \log |z| + \text{Arg }z$ $e^{\log|z| + \text{Arg }z} = |z|e^{\text{Arg }z}$ 

## 5. Power Series Expansion at Infinity

### $f(z)$ is analytic at $z = \infin$ if the function $g(w) = f(1/w)$ is analytic at $w = 0$ 

We study the behavior of $f(z)$ at $z = \infin$ by studying the behavior of $g(w)$ at $w = 0$ 

### If $f(z)$ is analytic at $\infin$, then $g(w) = f(1/w)$ has a power series expansion centered at $w = 0$

$g(w) = \sum_{k=0}^\infin b_kw^k$, $|w| < \rho$ 

#### (5.1) $f(z) = \sum_{k=0}^\infin \frac{b_k}{z^k}$, $|z| > \frac{1}{\rho}$ 

This series converges absolutely for $|z| > 1/\rho$, and for any $r > 1/\rho$, it converges uniformly for $|z| \geq r$  

![1540192021872](C:\Users\Renee\AppData\Roaming\Typora\typora-user-images\1540192021872.png)

#### Examples

##### If $n\geq 0$, $f(z) = 1/z^n$ is analytic at $\infin$, since $g(w) = f(1/w) = w^n$ is analytic at $w = 0$ 

##### $f(z) = 1/(z^2+1)$, $g(w) = f(1/w) = \frac{1}{(1/w)^2 + 1} = \frac{w^2}{1 + w^2}$ is analytic at $w = 0$ 

$g(w) = w^2 \frac{1}{1 + w^2} = w^2 \frac{1}{1 - (-w^2)} = w^2 \sum_{k=0}^\infin (-w^2)^k = w^2\sum_{k=0}^\infin (-1)^kw^{2k}$

$= w^2 - w^4 + w^6 -w^8 + . . . , $ $|w| < 1$ 

So:

$f(z) = \sum_{k=1}^\infin \frac{(-1)^{k+1}}{z^2k}$

## 6. Manipulation of Power Series

### For all practical purposes, power series can be treated like polynomials

#### differentiate term by term, integrated term by term

#### added and multiplied like polynomials

Let $f(z), g(z)$ be analytic functions at $0$ with power series representations $f(z) = \sum_{k=0}^\infin a_k z^k$, $g(z) = \sum_{k=0}^\infin b_k z^k$ 

Then:

##### the power series of $f(z) + g(z)$ is $\sum_{k=0}^\infin (a_k + b_k)z^k$ , where $f(z), g(z)$ are analytic at $0$ 

##### for any $c \in \C$, $cf(z) = \sum_{k=0}^\infin ca_kz^k$, $f(z)$ analytic at $0$ 

##### $f(z)g(z) = \sum_{k=0}^\infin c_k z^k$, where $c_k = \sum_{j= 0}^k a_{k-j}b_j$, $f(z), g(z)$ analytic at $0$ 

##### $g(z)$ analytic at $z = 0$, assume $g(0) = 1$, then $1/g(z) = 1 - (\sum_{k=1}^\infin b_kz^k)+ (\sum_{k=1}^\infin b_kz^k)^2 - (\sum_{k=1}^\infin b_kz^k)^3 + . . .$

Terms involving $z^m$ occur only in the first $m+1$ summands

since $(\sum_{k=1}^\infin b_kz^k)^{m} = c_{m} z^m + c_{m+1} z^{m+1} + . . . $ 

The procedure is justified by the uniform convergence of the geometric series for $z$ near $0$ 

#### Example: coefficients of $z^m$ for $m \leq 5$ for power series $\tan z = \sin z / \cos z$ about $z = 0$  

## 7. The Zeros of an Analytic Function

#### Let $f(z)$ be analytic at $z_0$, and suppose $f(z_0) = 0$, but $f(z)$ is not identically zero. We say that $f(z)$ has a zero of order $N$ at $z_0$ if $f(z_0) = f'(z_0) = . . . = f^{(N-1)}(z_0) = 0$

####  In view of formula (4.2) for power series coefficients, this occurs if and only if the power series expansion of $f(z)$ has the form $a_N(z-z_0)^N + a_{N+1}(z-z_0)^{N+1} + . . .$ where $a_N \neq 0$ 

##### (7.1) $f(z) = (z-z_0)^Nh(z)$, where $h(z)$ is analytic at $z_0$ and $h(z_0) = a_N \neq 0$ 

#### If $f(z) = (z-z_0)^Nh(z)$, where $h(z)$ is analytic at $z_0$ and $h(z_0) \neq 0$, then $f(z)$ has a zero of order $N$ at $z_0$ and the power series for $f(z)$ has the leading term $h(z_0)(z-z_0)^N$ 

### simple zero: zero of order one

### double zero: zero of order 2

### Examples:

#### zeros of $\sin z$ are point $n\pi$, and $\cos z = \pm 1$ at these points, so all zeros of $\sin z$ are simple zeros

#### $(z-z_0)^n$ has a zero of order $n$ at $z_0$ and no other zeros

#### $\sin z + z - \pi$ has a triple zero at $z = \pi$

$\sin z = -(z-\pi) + \frac{1}{3!}(z-\pi)^3 - \frac{1}{5!}(z-\pi)^5 + . . . , $

the function $\frac{\sin z}{z - \pi} + 1$, defined to be $0$ at $z = \pi$ has a double zero at $z = \pi$, since the leading term of its power series is $ (z-\pi)^2/3!$ 

### The order of a zero of $f(z)g(z)$ $=$ (order of zero for $f(z)$) + (order of zero for $g(z)$)

### $f(z)$ has zero at $z = \infin$ of order $N$ if $g(w)= f(1/w)$ has a zero at $w = 0$ of order $N$ 

This means:

$g(w) = b_Nw^N + . . . $

and $f(z) = b_N/z^N + . . . $ $|z| > R$, where $b_N \neq 0$ 

#### Examples

##### $\frac{1}{1+z^2}$ has a double zero at $\infin$, since the leading term of its power series is $1/z^2$

$\frac{1}{1 - (-1/w^2)} =  \frac{w^2}{1 + w^2}= w^2\sum (w^2)^k $

##### $1/(z-z_0)^n$ has a zero of order $n$ at $\infin$ 

### $z_0 \in E$ is an isolated point of the set $E$ if there is $\rho > 0$ such that $|z-z_0| \geq \rho$ for all points $z \in E$ other than $z_0$

$z_0$ is an isolated point of $E$ if $z_0$ is at a positive distance from $E\setminus$ {$z_0$}

#### If each point of $E$ is an isolated point of $E$, then we say "points of $E$ are isolated"

#### Examples

##### $E = [-1, 0]\cup ${$1/n: n \geq 1$}, then each of the points $1/n$ is an isolated point of $E$, while no point of the interval $[-1, 0]$ is an isolated point of $E$ 

### Theorem: If $D$ is a domain, and $f(z)$ is an analytic function on $D$ that is not identically zero, then the zeros of $f(z)$ are isolated

#### Each zero of $f(z)$ is of finite order

### Theorem (Uniqueness Principle)

If $f(z)$ and $g(z)$ are analytic on a domain $D$, and if $f(z) = g(z)$ for $z$ belonging to a set that has a nonisolated point, then $f(z) = g(z)$ for all $z \in D$ 

#### Example: since we know $\sin^2 x + \cos^2 x = 1$ for all $x \in \R$, $\R$ has nonisolated points, so $\sin^2 z + \cos^2 z = 1$ for all $z \in \C$ 

### Principle of permanence of functional equations

#### Theorem

Let $D$ be a domain

Let $E$ be a subset of $D$ that has a nonisolated point

Let $F(z,w)$ be a function defined for $z, w$ $\in D$ such that $F(z,w)$ is analytic in $z$ for each fixed $w \in D$ and analytic in $w$ for each fixed $z \in D$. 

If $F(z,w)  = 0$ whenever $z$ and $w$ both belong to $E$, then $F(z,w) = 0$ for all $z, w \in D$ 