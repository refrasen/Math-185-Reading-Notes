# Math 185 Notes: Ch. 9.1-2, Ch. 10.1-2

# Chapter 9 

page 140

## 1. The Schwarz Lemma

#### Theorem (Schwarz Lemma)

Let $f(z)$ be analytic for $|z| < 1$. Suppose $|f(z)| \leq 1$ for all $|z| < 1$, and $f(0) = 0$. Then

##### (1.1) $|f(z)| \leq |z|, |z| < 1$ 

Further, if $|f(z_0)| = |z_0|$ at some point $z_0 \neq 0$, $|z_0| < 1$, then $f(z) = \lambda z$ for some constant $\lambda$, s.t. $|\lambda| = 1$ 

---

Proof:

1. factor $f(z) = zg(z)$, where $g(z)$ is analytic
   1. Question, is this because $f(0) = 0$? I believe yes: see page 87/154 V.7 The Zeros of an Analytic function
2. Apply maximum principle to $g(z)$ see page 53/87, III.5 The Maximum Principle
   1. If $|z| = r < 1$, then $|g(z)| = |f(z)|/r \leq 1/r$ 
   2. Maximum principle $\implies$ for all $|z| \leq r$, $|g(z)| \leq 1/r$
   3. if we let $r \rightarrow 1$, we obtain $|g(z)| \leq 1$ for all $|z| < 1$ 
      1. Trick: we have $|z-z_0| < M$, and want to show another inequality involving that, so we let $|z-z_0| = m < M$, then let $m \rightarrow M$ 
3. If we have $|f(z_0)| = |z_0|$ as stated above, we obtain $|g(z_0)| = 1$, and the strict maximum principle implies that since $|g(z)| \leq 1$ for all $|z| <1$, we have $g(z)$ constant $= \lambda$ $\implies$ $f(z) = \lambda z$ 

---

#### Schwarz Lemma holds for any disk

If $f(z)$ is analytic for $|z-z_0| < R$, $|f(z)| \leq M$, and $f(z_0) = 0$, then

##### (1.2) $|f(z)| \leq \frac{M}{R}|z-z_0|, |z-z_0| < R$ 

equality holding only when $f(z)$ is a multiple of $z-z_0$

---

Proof: Multiples ways:

1. Directly, using $f(z)= (z-z_0)g(z)$ 
   1. Apply maximum principle, $|z-z_0| = r < R$, $|g(z)| = |f(z)|/r \leq M/r$, let $r \rightarrow R$, get $|g(z)| \leq M/R$ for all $|z-z_0| < R$
   2. Strict max: if $w$ exists such that $|f(w)| = C|w|$, $C$ is a multiple, and obtain $|g(w)| = C =? \frac{M}{R}$ 
2. from $(1.1)$, scaling in both $z$ and $w$ variable, $w = f(z)$ and translating the center of disk to $z_0$: $\zeta \rightarrow R\zeta + z_0$ maps the unit disk onto the disk centered at $z_0$ with radius $R$
   1. $h(\zeta) = f(R\zeta + z_0)/M$, then $h(\zeta)$ is analytic on the open unit disk, satisfies $|h(\zeta)| \leq 1$, and $h(0) = 0$. 

---

#### Theorem (infinitesimal Schwarz Lemma)

Let $f(z)$ be analytic for $|z| < 1$. If $|f(z)| \leq 1$ for $|z| < 1$, and $f(0) = 0$, then

##### (1.3) $|f'(0)| \leq 1$ 

with equality if and only if $f(z) = \lambda z$ for some constant $\lambda$ with $|\lambda| = 1$ 

---

Proof $|f'(0)| = |\lim_{z\rightarrow 0}\frac{f(z) - f(0)}{z-0}|$ $ = |\lim_{z\rightarrow 0} \frac{f(z)}{z}|$ $ \lim_{z\rightarrow 0}|\frac{f(z)}{z}|$ 

and for all $|z| < 1$, $\frac{f(z)}{z} \leq 1$ from the schwarz lemma, so $|f'(0)| \leq 1$ 

and since $g(z) = \frac{f(z)}{z}$, then we obtain $\lim_{z \rightarrow 0} g(z)$ = $f'(0)$ 

so since $g$ is analytic, $g(0) = f'(0)​$ 

if $|f'(0)| = 1$, we then have $|g(0)| = 1$, and by the strict maximum principle, $g(z)$ is constant, hence $f(z) = \lambda z$ 

##### Note: (1.3) is the same as the Cauchy estimate for $f'(0)$ derived in IV.4 without the hypothesis that $f(0) = 0$ 