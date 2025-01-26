# Orthogonal polynomials

The Fourier spectral method, which is presented in previous chapters, if applied to a non-periodic problem, induces the so-called Gibbs phenomenon, and reduces the global convergence rate. Therefore, it can be said that Fourier spectral method is appropriate for problems with periodic boundary conditions. So, how to handle the problem with non-periodic boundary conditions? To this end, we should use orthogonal polynomials. In this chapter, we will discuss the classical orthogonal polynomials, such as the Jacobi, Ultraspherical, Legendre, Chebyshev, Hermite and Laguerre polynomials. The aim of this chapter is to present essential properties and computation aspects of these orthogonal polynomials.

## Introduction

Let $\alpha\left(x\right)$ be a distribution, which is non-decreasing function, and not contant in the interval $\left[a,b\right].$ If $a=-\infty$ or $b=+\infty$ then we require $\alpha\left(\pm\infty\right)$ to be finite in the limiting sense. Then, two functions, $f$ and $g$ on $\left[a,b\right]$are said to be orthogonal with respect to the distribution $\alpha(x)$, if

$$\left(f,g\right):=\int_{a}^{b}f(x)g(x)d\alpha(x)=0$$

In this chapter we will use following form of distribution:

$$d\alpha\left(x\right)=w(x)dx$$

where, $w(x)\in L^{1}\left(a,b\right)$ is called the weight funciton, which is strictly positive in the interval.

A polynomial of degree $n$ is given by

$$p_{n}(x)=\sum_{m=0}^{n}k_{m}x^{m}$$

The leading coefficient of $p_{n}$is denoted by $k_{n}\ne0$.

The collection of polynomial of degree upto $n$ will be denoted by $\mathcal{P}^{n}:=\left\{ p_{m}\left(x\right)\right\} _{m=0}^{n}$. Then, $\left\{ p_{m}\left(x\right)\right\} _{m=0}^{n}$ forms a orthogonal set of polynomials on $\left[a,b\right]$with respect to the distribution $\alpha(x)$, if

$$\int_{a}^{b}p_{m}(x)p_{n}(x)d\alpha(x)=h_{n}\delta_{mn}$$

where, $\delta_{mn}$is diract-delta symbol. It can be seen that $p_{m}\in L_{\alpha}^{2}\left(a,b\right),m=0,1,\cdots$, and

$$h_{n}:=\Vert p_{n}\Vert^{2}=\int_{a}^{b}p_{n}(x)p_{n}(x)d\alpha(x)$$

> **Theorem:** A polynomial $q_{n}\in\mathcal{P}^{n}$ can be given by linear combination of orthogonal polynomials $p_{0},\cdots,p_{n}$ as
>
> $$q_{n}(x)=\sum_{m=0}^{n}a_{m}p_{m}(x)$$
>
> **Corollary:** For $q_{n}\in\mathcal{P}^{n}$, we have following results:
>
> $$\left(q_{n},p_{m}\right)=0,\forall m>n$$

## From independent to orthonormal

If $\left\{ f_{m}(x)\right\} _{m=0,\cdots,n}$ are the independent functions defined on $[a,b]$, then we can obtain a unique set of orthonormal polynomials $\left\{ p_{m}\left(x\right)\right\} _{m=1}^{m=n}$ from these independent functions.

## Formal Fourier expansion

A function $f(x)$ can be written as a linear combination of orthonormal polynomials.

$$f(x)=\sum_{m=0}^{\infty}f_{m}p_{m}(x)$$

where,

$$f_{m}:=\frac{\left(f,p_{m}\right)}{h_{m}}=\frac{\int_{a}^{b}f(x)p_{m}(x)d\alpha(x)}{h_{m}}$$

## Notations

From here on, we will use the following conventions to define orthogonal polynomials.

-   $P_{n}$ denotes a orthogonal polynomial of order $n$, with leading coefficient $k_{n}$ and $\Vert P_{n}\Vert^{2}=h_{n}$

-   The orthonormal polynomial corresponding to $P_{n}$ will be denoted by $\tilde{P}_{n}$, note that $\Vert\tilde{P}_{n}\Vert=1$

-   The monic orthogonal polynomial corresponding to $P_{n}$ will be denoted by $\pi_{n}$, the leading coefficient is 1.

-   The monic orthonormal polynomial will be denoted by $\tilde{\pi}_{n}$, the leading coefficient is 1 and and $\Vert\tilde{\pi}_{n}\Vert=1$

## Recurrence for $\pi_{n}$

Let $\pi_{n}$ be a monic orthogonal polynomial of order $n$ with respect to the distribution $\alpha(x)$ on $[a,b]$. Then the leading coefficient $k_{n}$ of $\pi_{n}$ is the coefficient of $x^{n}$. For a monic orthogonal polynomial $k_{n}=1$. Then, following three term recurrence relation is satisfied by the monic orthogonal polynomials.

$$\pi_{n+1}=\left(x-\alpha_{n}\right)\pi_{n}-\beta_{n}\pi_{n-1},\quad n=0,1,2$$

$$\pi_{-1}=0,\pi_{0}=1$$

$$\beta_{0}=\left(1,1\right)_{d\lambda}=\int_{a}^{b}d\alpha(x)=\int_{a}^{b}w(x)dx$$

$$\alpha_{n}=\frac{\left(x\pi_{n},\pi_{n}\right)}{\left(\pi_{n},\pi_{n}\right)}$$

$$\beta_{n}=\frac{\left(\pi_{n},\pi_{n}\right)}{\left(\pi_{n-1},\pi_{n-1}\right)}=\frac{\Vert\pi_{n}\Vert^{2}}{\Vert\pi_{n-1}\Vert^{2}}$$

$$\Vert\pi_{n}\Vert^{2}=\Pi_{i=0}^{n}\beta_{i}$$

Following points should be noted

-   $x\pi_{n}$ is also a monic polynomial of order $n+1$, therefore,

$$x\pi_{n}=\sum_{m=0}^{n+1}a_{m}\pi_{m}$$

By comparing the leading coefficient we get $a_{n+1}=1$, therefore, the above relation can be written as

$$x\pi_{n}=\pi_{n+1}+\sum_{m=0}^{n}a_{m}\pi_{m}$$

Therefore,

$$\left(x\pi_{n},\pi_{n+1}\right)=\left(\pi_{n},x\pi_{n+1}\right)=\left(\pi_{n+1},\pi_{n+1}\right)=\Vert\pi_{n+1}\Vert^{2}=h_{n+1}$$

We obtain the above mentioned expression for $\alpha_{n}$ by following process:

$$\left(\pi_{n+1},\pi_{n}\right)=\left(x\pi_{n},\pi_{n}\right)-\alpha_{n}\left(\pi_{n},\pi_{n}\right)-\beta_{n}\left(\pi_{n-1},\pi_{n}\right)$$

$$\alpha_{n}=\frac{\left(x\pi_{n},\pi_{n}\right)}{\left(\pi_{n},\pi_{n}\right)}$$

## Recurrence for $\tilde{\pi}_{n}$

Monic polynomials $\pi_{n}$ are not orthonormal, that is $\Vert\pi_{n}\Vert\ne1$, however, one can obtain the monic orthonormal polynomials, denoted by $\tilde{\pi}_{n}$, as shown below:

$$\pi_{n}=\Vert\pi_{n}\Vert\tilde{\pi}_{n}$$

Consequently, the three term recurrence relation for monic orthonormal polynomial can be obtained.

$$\tilde{\pi}_{n+1}=\frac{\left(x-\alpha_{n}\right)}{\sqrt{\beta_{n+1}}}\tilde{\pi}_{n}-\frac{\beta_{n}}{\sqrt{\beta_{n+1}\beta_{n}}}\tilde{\pi}_{n-1},\quad n=0,1,2$$

with

$$\tilde{\pi}_{-1}=0,\tilde{\pi}_{0}=1$$

or

$$\tilde{\pi}_{n+1}=\left(x-\alpha_{n}\right)s_{n}^{a}\tilde{\pi}_{n}-\beta_{n}s_{n}^{b}\tilde{\pi}_{n-1},\quad n=0,1,2$$

where,

$$s_{n}^{a}=\frac{1}{\sqrt{\beta_{n+1}}}$$

$$s_{n}^{b}=s_{n}^{a}s_{n-1}^{a}$$

## Recurrence for $p_{n}$

$p_{n}$ is neither monic nor orthonormal. The leading coefficient of $p_{n}$ is $k_{n}.$ The relationship between $p_{n}$ and $\pi_{n}$is given by:

$$p_{n}=k_{n}\pi_{n}$$

Consequently, following recurrence relation is obtained for $p_{n}$:

$$\frac{p_{n+1}}{k_{n+1}}=\left(x-\alpha_{n}\right)\frac{p_{n}}{k_{n}}-\beta_{n}\frac{p_{n-1}}{k_{n-1}},\quad n=0,1,2$$

with

$$p_{-1}=0,p_{0}=1$$

$$p_{n+1}=\left(x-\alpha_{n}\right)\frac{k_{n+1}}{k_{n}}p_{n}-\beta_{n}\frac{k_{n+1}}{k_{n-1}}p_{n-1},\quad n=0,1,2$$

$$p_{n+1}=\left(x-\alpha_{n}\right)s_{n}^{a}p_{n}-\beta_{n}s_{n}^{b}p_{n-1},\quad n=0,1,2$$

$$s_{n}^{a}=\frac{k_{n+1}}{k_{n}}$$

$$s_{n}^{b}=s_{n}^{a}s_{n-1}^{a}$$

## Recurrence for $\tilde{p}_{n}$

The orthonormal polynomial $\tilde{p}_{n}$ is given by

$$p_{n}=\Vert p_{n}\Vert\tilde{p}_{n}=\sqrt{h_{n}}\tilde{p}_{n}$$

$$\tilde{p}_{n+1}=\left(x-\alpha_{n}\right)s_{n}^{a}p_{n}-\beta_{n}s_{n}^{b}\tilde{p}_{n-1},\quad n=0,1,2$$

with

$$\tilde{p}_{-1}=0,\tilde{p}_{0}=1,$$

$$s_{n}^{a}=\frac{k_{n+1}}{k_{n}}\sqrt{\frac{h_{n}}{h_{n+1}}}$$

$$s_{n}^{b}=s_{n}^{a}s_{n-1}^{a}$$

## Kernel polynomial

Let $p_{0,}\cdots p_{n}$ be the orthogonal polynomials, then the kernel polynomial $K_{n}(x,y)$ is given by

$$K_{n}(x,y):=\sum_{m=0}^{n}\frac{p_{m}(x)p_{m}(y)}{h_{m}}$$

where, $h_{m}=\Vert p_{m}\Vert^{2}.$

Kernel polynomial satisfies has following important properties.

$$K_{n}(x,x)>0$$

If

$$s_{n}(x)=\sum_{m=0}^{n}f_{m}p_{m}(x)=\int_{a}^{b}f(y)K_{n}(x,y)dy$$

> **Theorem:** $\forall q\in\mathcal{P}^{n}$following is true:
>
> $$q(x)=\int_{a}^{b}q(y)K_{n}(x,y)dy$$ 

Moreover, the polynomial sequence $\left\{ K_{n}\left(x,a\right)\right\}$ is orthogonal with respect to the weight function $\left(x-a\right)w(x),$ and the sequence $\left\{ K_{n}\left(x,b\right)\right\}$ is orthogonal with respect to the $\left(x-b\right)w(x),$

## Christoff-Darboux formula

$$K_{n}(x,y):=\sum_{m=0}^{n}\frac{p_{m}(x)p_{m}(y)}{h_{m}}=\frac{k_{n}}{k_{n+1}}\frac{p_{n+1}(x)p_{n}(y)-p_{n}(x)p_{n+1}(y)}{\left(x-y\right)h_{n}}$$

or

$$\frac{p_{n+1}(x)p_{n}(y)-p_{n}(x)p_{n+1}(y)}{\left(x-y\right)}=\frac{k_{n+1}h_{n}}{k_{n}}\sum_{m=0}^{n}\frac{p_{m}(x)p_{m}(y)}{h_{m}}$$

$$\frac{p_{n+1}(x)p_{n}(y)-p_{n}(x)p_{n+1}(y)}{\left(x-y\right)}=\frac{k_{n+1}h_{n}}{k_{n}}K_{n}(x,y)$$

or

$$K_{n}(x,y)=\frac{k_{n}}{k_{n+1}h_{n}}\frac{p_{n+1}(x)p_{n}(y)-p_{n}(x)p_{n+1}(y)}{\left(x-y\right)}$$

$$K_{n}(x,x)=\frac{k_{n}}{k_{n+1}h_{n}}\left(\frac{dp_{n+1}}{dx}p_{n}(x)-\frac{dp_{n}(x)}{dx}p_{n+1}(x)\right)$$

## Zeros of orthogonal polynomials

Zeros of orthogonal polynomials are chosen as the nodes of Gauss-type quadratures. These zeros are also used to generate computational grids for spectral methods. Let $\left\{ p_{n}\right\}$ be a sequence of polynomials orthogonal with respect to the weight function $w(x)$ in $[a,b]$.

> **Theorem:** Zeros of $p_{n+1}$are all real, unique, and distributed between $\left[a,b\right].$
>
> **Theorem:** Let zeros of $p_{n}$ be denoted by $x_{1}<x_{2}<\cdots<x_{n},$let $x_{0}=a$ and $x_{n+1}=b$, let $I_{m}=\left(x_{m},x_{m+1}\right)$, for $m=0,1,\cdots n$ be n interval, then each $I_{m}$ contains exactly one zero of $p_{n+1}$.
>
> **Theorem** Let $\left\{ p_{n}\right\}$be a sequence of orthogonal polynomials, then the zeros of $\frac{dp_{n}}{dx}$ are real, and there exists exactly one zeros of $\frac{dp_{n}}{dx}$ between two consecutives zeros of $p_{n}.$

The zeros $\left\{ x_{j}\right\} _{j=0}^{n}$ of orthogonal polynomial $p_{n+1}$, which satisfies the following recurrence relation

$$p_{n+1}=\left(x-\alpha_{n}\right)s_{n}^{a}p_{n}-\beta_{n}s_{n}^{b}p_{n-1},\quad n=0,1,2$$

with $p_{-1}=0,p_{0}=1$, and $s_{n}^{b}=s_{n}^{a}s_{n-1}^{a}$

are eigenvalues of the following symmetric tridiagonal matrix (Jacobi matrix):

$${\bf J}_{n+1}=\left[\begin{array}{ccccc}
\alpha_{0} & \sqrt{\beta_{1}}\\
\sqrt{\beta_{1}} & \alpha_{1} & \sqrt{\beta_{2}}\\
 & \sqrt{\beta_{2}} & \ddots & \ddots\\
 &  & \ddots & \alpha_{n-1} & \sqrt{\beta_{n}}\\
 &  &  & \sqrt{\beta_{n}} & \alpha_{n}
\end{array}\right]$$

## Gauss-Quadrature

Let $d\alpha$ be a measure with bounded or unbounded support $[a,b]$. An n-point quadrature rule for the measure $d\alpha$ is given by

$$\int_{a}^{b}f(x)d\alpha(x)=\sum_{m=1}^{n}f(x_{j})w_{j}+R_{n}(f)$$

where the sum on the right provides an approximation to the integral on the left and $R_{n}$is the error of such numerical integration. The set $\left\{ x_{j}\right\} _{j=1}^{n}$ contains n distinct points in $[a,b]$ and called the quadrature points, and $\left\{ w_{j}\right\} _{j=1}^{n}$contains n positive numbers, which are called weight of the quadrature points.

The above quadrature rule is said to have degree of exactness (DOE) $d$ if $R_{n}(p)=0$ for $p\in\mathcal{P}^{d}$. It is said to have precise DOE d if it has DOE $d$ but not $d+1$. A quadrature rule with DOE $d=n-1$ is called interpolatory. Usually, $n$ points have DOE of $d=n-1$. But we want to find $n$ points such that we can achieve maximum valuea of DOE. Such points corresponds to the Gauss-Quadrature.

> **Theorem (Gauss-Quadrature)**: Let $\left\{ x_{m}\right\} _{m=1}^{n}$ be the set if zeros of the orthogonal polynomial $p_{n}$. Then there exists a unique set of quadrature weights $\left\{ w_{m}\right\} _{m=1}^{n}$ such that $$\int_{a}^{b}p(x)w(x)dx=\sum_{m=1}^{n}p(x_{m})w_{m},\forall p\in P_{2n-1}$$ $N$ point Gauss-Quadrature rule has DOE $d=2N-1$

> **Theorem** **(Gauss-Left-Radau)**: Let $x_{1}=a$, and $\left\{ x_{m}\right\} _{m=2}^{n}$ be the $n-1$ zeros of the orthogonal polynomial $q_{n-1}\in\mathcal{P}^{n-1}$ given by $$q_{n-1}=\frac{p_{n}+\alpha_{n-1}p_{n-1}}{x-a}$$ with $\alpha_{n-1}=-\frac{p_{n}(a)}{p_{n-1}(a)}$, then there exists a unique set of quadrature weights $\left\{ w_{m}\right\} _{m=1}^{n}$ such that $$\int_{a}^{b}p(x)w(x)dx=\sum_{m=1}^{n}p(x_{m})w_{m},\forall p\in P_{2n-2}$$ $N$ point Gauss-Radau rule has DOE $d=2N-2$

> **Theorem** (Gauss-Right-Radau): Let $x_{n}=b$, and $\left\{ x_{m}\right\} _{m=1}^{n-1}$ be the zeros of the orthogonal polynomial $q_{n-1}\in\mathcal{P}^{n-1}$ given by $$q_{n-1}=\frac{p_{n}+\alpha_{n-1}p_{n-1}}{x-b}$$ with $\alpha_{n-1}=-\frac{p_{n}(b)}{p_{n-1}(b)}$, then there exists a unique set of quadrature weights $\left\{ w_{m}\right\} _{m=1}^{n}$ such that $$\int_{a}^{b}p(x)w(x)dx=\sum_{m=1}^{n}p(x_{m})w_{m},\forall p\in P_{2n-2}$$ $N$ point Gauss-Radau rule has DOE $d=2N-2$

> **Theorem** (**Gauss-Lobatto**): Let $x_{1}=a,x_{n}=b$, and $\left\{ x_{m}\right\} _{m=2}^{n-1}$ be the $n-2$ zeros of the orthogonal polynomial $z_{n-2}\in\mathcal{P}^{n-2}$ given by $$z_{n-2}=\frac{p_{n}+\alpha_{n-1}p_{n-1}+\beta_{n-1}p_{n-2}}{\left(x-a\right)\left(b-x\right)}$$ with $\alpha_{n-1},\beta_{n-1}$, such $p_{n}+\alpha_{n-1}p_{n-1}+\beta_{n-1}p_{n-2}=0$ at $x=a,b$, then there exists a unique set of quadrature weights $\left\{ w_{m}\right\} _{m=1}^{n}$ such that $$\int_{a}^{b}p(x)w(x)dx=\sum_{m=1}^{n}p(x_{m})w_{m},\forall p\in P_{2n-3}$$ $N$ point Gauss-Lobatto rule has DOE $d=2N-3$
